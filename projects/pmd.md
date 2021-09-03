---
layout: project
type: project
image: images/pmd-square.png
title: Persistent Motion Detector
permalink: projects/pmd
# All dates must be YYYY-MM-DD format!
date: 2021-08-20
labels:
  - Python
  - C++
  - Computer Vision
summary: Asynchronous computer vision motion detector for event cameras built in Python and C++.
---

[Event cameras](https://en.wikipedia.org/wiki/Event_camera) are cameras that only capture changes in intensity rather than periodically capturing an entire frame. This gives them the advantage of extremely low latency and extremely high power efficiency over conventional cameras. The difficulty is that due to the event-based data they output, conventional computer vision approaches cannot be directly applied when working with event cameras.

![events](/images/frame_177_events.jpg)  
Events representing changes in brightness as boats moving through a harbor. Note the high density of events produced by waves, which we are not interested in tracking.

![events+frames](/images/frame_177_events+frames+annot.jpg)  
Events on top of conventional frames captured, with annotations highlighting objects of interest.

![events+frames](/images/frame_177_pmd.jpg)  
Resulting output from the Persistent Motion Detector, with estimated velocities and confidence based on motion analysis of tracked clusters.

The Persistent Motion Detector is written in C++ and loaded as a Python extension using [Cython](https://cython.org) to provide an easy-to-use frontend for development and interfacing with other Python libraries for event-based data processing.

## Overview of the Persistent Motion Detector algorithm
<img src="../images/pmd.png" width="700" alt="PMD Block Diagram">  

Events are input from the event camera sequentially, then passed to the Partitioning module, where they are sorted by location and assigned to an Event Handling instance. Each Event Handling instance interfaces with the Event Buffer and Cluster Buffer to perform concurrent noise filtering and clustering. The Buffer Flushing module periodically clears expired events from the Event Buffer and updates the Cluster Buffer accordingly. The Cluster Sorting module prioritizes each cluster and assigns the highest priority clusters to be tracked by Cluster Tracking instances. Finally, each Cluster Tracking instance tracks and analyzes the movement characteristics of its assigned cluster and outputs a Detection with a corresponding location, bounding box, and confidence value. The Partitioning and Event Handling modules operate on a per-event basis as each input event is read. The Event Buffer and Cluster Buffer are memory modules that can be written to and read from by other modules. The Buffer Flushing, Cluster Sorting, and Cluster Tracking modules operate periodically.

Cluster analysis (in the Cluster Tracking module) leads to greater confidence in clusters that move consistently at the same velocity over time, resulting in positive detections for objects such as boats, and not for objects such as waves.

![confidence over time](/images/confovertime.png)  
Shown here are the confidence values over time for all clusters in a scene. The red and blue clusters represent boats, while the others represent waves and other background objects. The boats reach a high confidence value within dozens of frames, while the other objects can easily be discriminated as they cannot reach or maintain as high of a confidence score.

Source code is available [here](https://github.com/believeinlain/asynch-cv).

## Acknowledgements

Submitted to [AIPR Workshop](https://www.aipr-workshop.org) 2021 with the title *Real-Time Event-Based Tracking and Detection for Maritime Environments*. Images and captions adapted from working manuscript.  

Developed with financial support from University of California San Marcos and Naval Information Warfare Center Pacific.  

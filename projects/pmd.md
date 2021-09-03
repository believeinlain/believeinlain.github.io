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
summary: Asynchronous computer vision motion detector for event cameras build in Python and C++.
---

[Event cameras](https://en.wikipedia.org/wiki/Event_camera) are cameras that only capture changes in intensity rather than periodically capturing an entire frame. This gives them the advantage of extremely low latency and extremely high power efficiency over conventional cameras. The difficulty is that due to the event-based data they output, conventional computer vision approaches cannot be directly applied when working with event cameras.

![events](/images/frame_177_events.jpg)  
Events representing changes in brightness as boats moving through a harbor. Note the high density of events produced by waves, which we are not interested in tracking.

![events+frames](/images/frame_177_events+frames+annot.jpg)  
Events on top of conventional frames captured, will annotations illustrating objects of interest.

![events+frames](/images/frame_177_pmd.jpg)  
Resulting output from the, with estimated velocities and confidence based on motion analysis of tracked clusters.

Source code is available [here](https://github.com/believeinlain/asynch-cv).

## Acknowledgements

Submitted to [AIPR Workshop](https://www.aipr-workshop.org) 2021.  

Developed with financial support from University of California San Marcos and Naval Information Warfare Center Pacific.  

---
layout: project
type: project
image: images/cu-square.png
title: Connective Unconscious
permalink: projects/connectiveunconscious
# All dates must be YYYY-MM-DD format!
date: 2021-09-02
labels:
  - JavaScript
  - Jade
  - Express
  - Node.js
summary: My personal website built in Node.js using Jade and Express to deliver photos, poetry, and applets.
---

<img src="../images/cu-page.png" width="700">

The [Connective Unconscious](http://connectiveunconscious.com/) is my personal website that I host on an Ubuntu Server so that I have full control over the design and execution of everything hosted on it. So far I've only seen fit to host photos, poetry, and an unfinished applet that I wrote about [here](/projects/planetgen).

The website is built as a server-side Node.js app with Jade as a templating engine. I pursued this particular path because the npm package manager allowed me to add only the features that I wanted, making it a perfect fit for a simple personal site, especially compared to feature-packed servers like apache.

All css is custom made, and the photos are loaded dynamically using a json file as a rudimentary database. A custom route is generated for each photo, and in the 日本の夢 album, the poetry is stored in the same json file as the photo filenames.

## Function used to generate routes for each photo in a given album
```js
function serve_photo_album(album_name, display_name) {
  // read the list of captions
  var captions = JSON.parse(fs.readFileSync(`./public/${album_name}/captions.json`, 'utf-8'));
  var photo_array = Object.getOwnPropertyNames(captions);

  router.get(`/${album_name}/`, function(req, res, next) {
    var image = req.query['image'];
    if (!image) {
      res.redirect(`/${album_name}/?image=0`);
      return;
    }
    var photo_id = 0;
    if ((image >= 0) && (image < photo_array.length)) {
      photo_id = Number(image);
    }
    var last_id = (photo_id-1)>=0 ? photo_id-1 : photo_array.length-1;
    var next_id = (photo_id+1)==photo_array.length ? 0 : photo_id+1; 
    var photo_name = photo_array[photo_id].trim();
    // draw the image page
    res.render('photo_album', { 
      album: album_name,
      title: display_name,
      photo: photo_name,
      caption: captions[photo_name],
      no_caption: captions[photo_name]=='' ? ', no_caption' : '',
      photo_id: photo_id,
      last_id: last_id,
      next_id: next_id});
  });
};
```

The result is a persistent hyperlink for each image, such as "[https://connectiveunconscious.com/nihonnoyume/?image=3](https://connectiveunconscious.com/nihonnoyume/?image=3)". The links for "next" and "previous" are also generated and passed to the template engine. **This allows for dynamic content loading with no client-side JavaScript for the photo albums.**

Source code is available [here](https://github.com/believeinlain/connectiveunconscious).

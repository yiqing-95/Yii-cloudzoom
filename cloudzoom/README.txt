Good to know when using in one or lightboxes (non-iframe) and the JavaScript file is being loaded once by the main page:

Initiliase the zoom once the lightbox content has loaded othrwise you mostly see nothing happening:

$(document).ready(function() {
  $('.cloud-zoom, .cloud-zoom-gallery').CloudZoom();
});




For those running jQuery 1.5.*-, this bad boy will work straight out of the gate. Running jQuery 1.6.*+, you'll have issues.

To fix and get back in action, run a find/replace for ".attr(" and replace with ".prop(", you should be good to go (shouldn't be more than 6 or 8 if I remember correctly).
Between versions 1.5.4 and 1.6, jQ updated the way it handled those two classes which breaks the script as it's written here.

# CROPDemoController
Using a webapp to control the CROP Unity 3D model of the underground farm.

Based on work done by Tomaz Geddes de Almeida in https://github.com/tomazgda/web-trex.

The aim is to have a simple webpage, which can be used on a phone, that has twin virtual joysticks and an "interact" button, and this moves the viewpoint around the 3D model of the farm (on a separate screen, running as a WebGL app) and lets the user "click" on e.g. shelves, sensors.
Communication between the controller and the WebGL Unity model is done via WebSockets.

There are three components to this:
1) The Unity model, which is in the `BigScreen` branch of https://github.com/alan-turing-institute/CROPDemoUnity
2) A websocket server, running on a VM in the cloud.
3) The 'controller' webapp, which could be run on that same VM, or as a separate webapp.

The `controller` directory contains the necessary code (just one javascript file and an `index.html`) for 3).   This can be run by changing to that directory and serving via e.g.
`python -m http.server 8000`.

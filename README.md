# Smartshop-journey

Application to experiment with web ar functionality based on opensource libraries.

## Usage

1. Open camera app on your mobile phone
2. Point to QR code
    <br>
    <img src="assets/qr-code.png" width="400" height="400">
3. Allow browser to use camera on web page

    On user first visit, browser asks for permission to use camera. Accept it.

    Recently, manufacturers of operating systems and browsers are moving towards increasing the level of privacy and security of users. Therefore, there may be an issue depending on previous user choices. 
    - On Android system user prohibited usage of camera by application (like Chrome browser)

        Steps to fix that:
        tap Settings > Apps > tap App you want to change (Chrome) > tap Permissions > tap Camera and choose Allow only when using the app or Ask every time

    - Upon first visit on the page, user disallowed usage of camera

        Steps to fix that on Chrome:
        launch Chrome > tap Three-dot menu > Settings > scroll down to section Advanced and tap Site settings > Camera > toggle the switch to allow websites to use camera 

4. Point camera into Markers to see 3d models in AR.
    <p float="left">
    <img src="assets/marker-hiro.png" width="256" height="256" alt="Hiro marker">
    <img src="assets/marker-kanji.png" width="256" height="256" alt="Kanji marker">
    <br>
    <img src="assets/marker-letterA.png" width="256" height="256" alt="LetterA marker">
    <img src="assets/marker-letterB.png" width="256" height="256" alt="LetterB marker">
    <br>
    <img src="assets/barcode-00.png" width="256" height="256" alt="Nb00 barcode">
    <img src="assets/barcode-01.png" width="256" height="256" alt="Nb01 barcode">
    <br>
    <img src="assets/barcode-05.png" width="256" height="256" alt="Nb 5 marker">
    <img src="assets/pattern-index.png" width="256" height="256" alt="Orange small logo marker">
    </p>



## Technical information

### AR.js

AR.js library is used for Augmented Reality on the Web
https://ar-js-org.github.io/AR.js-Docs/
Library is built upon A-Frame and three.js Javascript libraries.

AR.js features the following types of Augmented Reality, on the Web:
<ul>
    <li>
        Image Tracking, when a 2D images is found by the camera, it's possible to show some kind of content on top of it, or near it. The content can be a 2D image, a GIF, a 3D model (also animated) and a 2D video too. Cases of use: Augmented Art, learning (Augmented books), Augmented flyers, advertising, etc.
    </li>
    <li>
        Location Based AR, this kind of AR uses real-world places in order to show Augmented Reality content, on the user device. The experiences that can be built with this library are those that use a user's position in the real world. The user can move (ideally outdoor) and through their smartphones they can see AR content where places are in the real world. Moving around and rotating the phone will make the AR content change according to users position and rotation (so places are 'anchored' in their real position, and appear bigger/smaller according to their distance from the user). With this solution it’s possible to build experiences like interactive support for tourist guides, assistance when exploring a new city, find places of interest like buildings, museums, restaurants, hotels and so on. It’s also possible to build learning experiences like treasure hunts, and biology or history learning games, or use this technology for situated art (visual art experiences bound to specific real world coordinates).
    </li>
    <li>
        Marker Tracking, When a marker is found by the camera, it's possible to show some content (same as Image Tracking). Markers are very stable but limited in shape, color and size. It is suggested for those experiences where are required a lot of different markers with different content. Examples of use: (Augmented books), Augmented flyers, advertising.
    </li>
</ul>

AR.js uses jsartoolkit5 for tracking, but can display augmented content with either three.js or A-Frame.

AR.js uses WebGL technology to present graphics and WebRTC to manage camera.

Marker based tracking is very lightweight, while Image Tracking is more CPU consuming.

### WebXR

The WebXR Device API provides access to input (pose information from headset and controllers) and output (hardware display) capabilities commonly associated with Virtual Reality (VR) and Augmented Reality (AR) devices. It allows you develop and host VR and AR experiences on the web.

It is promissing API for accessing VR & AR, but currently not supported by all significant browsers. https://caniuse.com/webxr



## Examples

Check on top nav bar <div align="right">[:arrow_up:](#smartshop-journey)</div>

About **Marker** subpage

Current experiment uses two out of all markers. Under the first one (also available when user scan QR code with pattern inside) there is two 3d models next to each other:
- a knot (A-Frame primitive) - it have 2 animations attached with different duration and axis
- mobile phone (from free to use GLTF model) - one animation which rotates around y axis

Second marker (Hiro) leads to retro phone model (GLTF). It has Java Script event attached to actively scale and rotate model. To do that firstly marker must be recoginzed (button on the bottom of screen shows up). If user click on button, then model will change accordingly.

About **Stemkoski.github.io (ext)** subpage

It is a collection of basic examples that presents various features in AR.js library (version 2).
Viewing the AR examples will require a device with a camera and various marker images to be detected, which are available in the markers directory in this repository. Requires the kanji marker unless otherwise specified.
Source code hosted at https://github.com/stemkoski/AR.js-examples

## Links

[WebAR vs Native AR: What Are The Key Differences](https://www.softwaretestinghelp.com/webar-vs-native-ar/)
[AR.js library](https://ar-js-org.github.io/AR.js-Docs/)
[WebXR explainer](https://github.com/immersive-web/webxr/blob/master/explainer.md)
[WebXR Device API](https://www.w3.org/TR/webxr/)

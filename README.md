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
    <br>
    <img src="assets/pattern-index.png" width="256" height="256">
    <img src="assets/hiro.png" width="256" height="256">
    



## Technical information

AR.js library is used for Augmented Reality on the Web
https://ar-js-org.github.io/AR.js-Docs/

### AR types

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





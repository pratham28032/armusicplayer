song
- guitar
- drums
- piano
- violin
- male voice
- female voice

Versions
- rock - more focus drums, electronic guitar
- acoustic - guitar is there, drums are not there
- instrumental - only instruments

Dynamic music player
- control which instruments to play
- hence, create your own versions of a song
- control all this using AR markers

Event detection
- whenever the drums marker is on the screen (in view of the camera)
    - detect markerFound event for drums marker
    - start playing the drums
- whenever the guitar marker is on the screen (in view of the camera)
    - detect markerFound event for guitar marker
    - start playing the guitar
- whenever the drums/guitar marker is NOT on the screen (NOT in view of the camera)
    - detect markerLost event for drums/guitar marker
    - lost, gone from the screen
    - stop playing the drums/guitar

Events
- onclick
- onkeypress
- onmouseover
- onmouseout

- markerFound
    - a particular marker is available on the screen, or available in view of the camera
    - it was not visible earlier
    - as soon as it is visible, markerFound event is triggered
- markerLost
    - a particular marker is NOT available on the screen, or NOT available in view of the camera
    - it was visible earlier
    - as soon as it is lost or not visible, markerLost event is triggered

Steps
- want to detect markerFound and markerLost for all markers
- eventListener - MARKER.addEventListener(type, function)

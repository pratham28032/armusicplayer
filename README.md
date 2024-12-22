*Introduction:*
AR Music is an innovative project that merges the realms of music and augmented reality (AR) technology. This unique application was developed using a combination of HTML, CSS, and JavaScript, with the integration of AR.js and AFrame.js for augmented reality functionalities.

*Core Features:*

1. *Real-Time Music Mixing:* The central feature of AR Music allows users to dynamically change the instruments within a song in real-time through AR interactions. By using AR markers, users can seamlessly switch between different versions of a song, each emphasizing a specific instrument like guitar, drums, vocals, and more. This dynamic audio manipulation empowers users to craft their own personalized musical experiences.

2. *Audio Playback Management:* To ensure a seamless audio experience, the project incorporated the Howler.js library. This library managed audio playback with precision, guaranteeing that the different instrument tracks synchronized seamlessly. The result is an immersive and captivating musical journey that keeps users engaged.

3. *Modular Coding and Clean Structure:* The project was built with a focus on maintainability and scalability. Modular coding practices were employed, which facilitated easier debugging, maintenance, and future enhancements of the AR music application. This approach allowed for smooth updates and feature additions.

4. *Error Handling:* Robust error handling mechanisms were implemented to provide informative messages to users in case of marker detection failures or audio playback issues. This proactiveness significantly improved the overall user experience, ensuring a smooth and glitch-free AR music experience.

*User-Centric Approach:*
Throughout the development process, extensive usability testing was conducted, actively seeking feedback from music enthusiasts. This user feedback was invaluable and was incorporated into the application's functionality and user interface. The goal was to create an intuitive and user-friendly AR music player that catered to the preferences and expectations of its users.

*Conclusion:*
AR Music is a testament to the successful fusion of technology and creativity. By pushing the boundaries of AR technology and leveraging the power of interactive audio experiences, this project provides a novel way for users to interact with and enjoy music. It showcases not only technical expertise but also a deep passion for creating innovative applications that redefine the user experience, especially in the field of music. AR Music opens up new possibilities for personalized and interactive music enjoyment through the lens of augmented reality.
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

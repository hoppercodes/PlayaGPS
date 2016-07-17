# PlayaGPS
GPS Application for Burning Man written in Processing 3.0 and utilizing the Ketai library.
The app does a few things better than PlayaCompass:

1) you can read the screen in Noonday Tucson Sunlight;
2) the Mark Location function now writes the location to storage, so it persists as the app moves to the background or is restarted;
3) the navigation function is now designed to give a compass heading rather than some little arrow on the display that you cannot see or sight along,  allowing one to follow a more general compass direction, or if you know the mountains surrounding you, navigate on that basis.  A driver can use a compass on the windscreen to follow a bearing.

The top part (black letters on white) - the Current Position area, show:

1) In Old Italian the name of the wind in your face (people in Da Vinci's day navigated by the wind as well as by less common compasses) (Maestro-Ponente)
2) The compass heading (NNW) - with some hysteresis so it does not bounce wildly at transitions;
3) Clock Angle to Man (5:45)
4) Distance to Man in Feet (3664)
5) The Name of the Street (Donatello), or if between streets, the blocks, for area within city
6) teeny little letters saying to "Tap Gray Box to Mark Location" - if you look under it, there is a hotspot that if tapped, logs the location into the Navigation area

The bottom part (white letters on black background) - the Navigation Area - shows:
1) Bearing: Compass heading and Distance in feet to marked location.  Navigate using this heading, watch as it changes to change direction of travel as you work your way around obstacles (NW 55 ft)
2) Location that is marked and being navigated to in Man Clock Angle and Man distance Feet (5:46 and 3657).
3) Month, Day, and time that location was marked (7/17 8:24)
4) Latitude and Longitude of marked location.

That is it - there is no long list of marked locations that you can scroll through and select, there is no keyboard to enter a location description.  

The app is open source and written in Processing 3.0 using the Ketai library.  It is not completely stable; there is a frequent burp at start up that causes failed starts.  If this happens, just hit the icon again.  Eventually (sometimes 2 or 3 taps) are necessary.  It seems that it is related to the location manager trying to decide if only GPS is good enough for our purpose - the bug seems to be buried in the library and I am not going to chase it down.  PlayaGPS buffers the location through restarts; this was surprisingly difficult to do in a general way that did not require writing to the user's SD card.  The only permission is FINE LOCATION - ie, to use the GPS.  

The app was written mostly to try out the math and the user interface.  I am CERTAIN that I can read it in bright sunlight while riding a bike!  I am ALMOST CERTAIN that the math is good to go - it works in Tucson, when the Man is at a local major intersection.  

In order to conserve battery life on playa, the GPS receiver is only active when the app is active.  The receiver does not run in the background, consequently it takes a few seconds to a minute to lock in (longer delays associated with initial startups and long delays between use).  Its a trade-off, but seems to me a good trade-off.

Please give it a try, and if you like share it with other bay area folks to try out.  If they our you like it, you will need to download it from the google store to get one that is configured for the Playa and this year's man location..  I am in the process of posting the app on Google Play for download, but would appreciate it if you all tried it and pass it around to SF folks to see if it behaves.  

To install the app, read this email on your android device and tap on the attachment (ending in apk).  It will automagically install from that point.

Regards,  Joe

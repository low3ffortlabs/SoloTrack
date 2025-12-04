# SoloTrack
SoloTrack enables any Android 9+ smartphone with GPS functionality to be used as a dedicated GPS dongle for Windows or Linux PCs. For those who do not have the money or time to obtain a USB GPS receiver for their PC application, SoloTrack utilizes the Android device's built in GPS module and outputs the GPS data stream to any PC via USB.   ​

SoloTrack also displays the Android device's current location (decimal), GPS speed (mph), GPS time zone, and GPS time, all on the app's screen easily visible to the user.

SoloTrack works by reading the raw GPS NMEA-0183 from the Android's chipset and does a couple things. First SoloTrack pipes the raw NMEA data straight to the PC via a TCP server, that is then transmitted to a receiving PC via USB COM port. Secondly, SoloTrack converts the raw NMEA data stream into readable decimal degree coordinates that are visible to the user via the app's display. 

It is important to note that although SoloTrack does stream NMEA data to a PC via USB, it is required that the PC has a method of creating virtual COM ports, since Android does not natively present itself as a USB device to any PC (unless rooted and used in gadget mode). 

In Solotrack's development, Franson GpsGate 2.6 was used as the virtual COM port generator. SoloTrack creates a TCP server on the Android side of things and requires that the PC listens on that server, this is why a virtual COM port is required to be set up specifically with TCP/IP.

It is also important to note that most GPS maps application do not accept NMEA formatted GPS data. Apps such as Google Maps, Apple Maps, Waze, and OnX Maps utilize proprietary GPS data formats and do not generally accept the NMEA standard.

Below is a list of GPS Maps applications for Windows machines that do accept NMEA data streams via TCP/IP. SoloTrack has only been verified to work with GPXSee.​​

GPXSee​               OpenCPN​               Viking GPS​               The Capn​               OziExplorer

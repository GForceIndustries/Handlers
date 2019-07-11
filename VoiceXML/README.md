# VoiceXML
Handlers to initiate a VoiceXML session. The URL to the VoiceXML application is retrieved from an IP table, matching against the ANI and/or DNIS of the call.

With the customisation added to both CustomIncomingCall and CustomInitiateCallRequest, this captures calls to and/or from the specified numbers, both incoming from the PSTN and as dialed by internal users.

VoiceXML documents are recommended to be hosted on a web server and retrieved via HTTP/S. This solution can operate with static VoiceXML scripts, dynamic VoiceXML IVR applications and Genesys Intelligent Automation.

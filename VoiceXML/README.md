# VoiceXML
Handlers to initiate a VoiceXML session. The URL to the VoiceXML application is retrieved from an IP table, matching against the ANI and/or DNIS of the call.

With the customisation added to both CustomIncomingCall and CustomInitiateCallRequest, this captures calls to and/or from the specified numbers, both incoming from the PSTN and as dialed by internal users.

VoiceXML documents are recommended to be hosted on a web server and retrieved via HTTP/S. This solution can operate with static VoiceXML scripts, dynamic VoiceXML IVR applications and Genesys Intelligent Automation. The required InteractionID, ANI and DNIS attributes are retrieved from the interaction and passed via the VoiceXML Initiate toolstep to support integration with Genesys Intelligent Automation.

Calls that match a VoiceXML application are routed to the VoiceXML application instead of being placed externally (outbound calls) and instead of routing to a configured DNIS, Interaction Conference room or Attendant proile (inbound calls).

## Instructions
Import the VoiceXMLRouter IP table via Interaction Administrator. This table should be used to match calls to VoiceXML applications by matching the ANI and/or DNIS of the call. One sample entry is created for you, albeit disabled.

A * wildcard can be entered in the ANI and/or DNIS column, or a specific number for an exact match. Enter the URL or path to the VoiceXML script or application in the URI column and set the Active column to Yes to enable that entry. This column allows individual entries to be disabled if necessary, instead of needing to delete them from the table. The Application and Notes columns allow for basic documentation.

Calls will be evaluated for a match in the following order:

1. Matching ANI and DNIS
2. Matching ANI to any DNIS (\*)
3. Matching any ANI (\*) to DNIS
4. Matching any ANI (\*) to any DNIS (\*)

Publish the Sub_VoiceXML handler. You may need to update the reference to the VoiceXMLRouter IP table for the four Table Lookup toolsteps.

Publish the provided customisation points (CustomIncomingCall and CustomInitiateCallRequest), or manually add the Sub_VoiceXMLRouter subroutine to these customisation points if you have pre-existing modifications in place.

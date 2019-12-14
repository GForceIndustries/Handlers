# TTS
Utility handlers for Text to Speech.

## Notification_AddMrcpTtsLanguage
PureConnect supports the majority of languages resold by Nuance for their Text to Speech products. Some voices for Nuance Vocalizer or for other third-party TTS engines require a language code that is not supported by Interaction Administrator. This handler allows for the required language code to be added to an MRCP TTS server's configuration in Interaction Administrator.

Usage: SendCustomNotification TTS Language <server> <voice> <language>

This requires that you have already added the MRCP TTS server and voice in Interaction Administrator.

## Notification_SetDefaultTtsEngine
Changes the system default TTS provider to the engine specified.

Usage: SendCustomNotification TTS Default <sapi|mrcp|itts>

## Notification_SetMrcpTtsServerStatus
Sets the specified MRCP TTS server as active or inactive. This is useful for testing purposes on a system with multiple MRCP TTS servers configured.

Usage: SendCustomNotification TTS MRCP <enable|disable> <server>
  
This requires that you have already added the MRCP TTS server in Interaction Administrator.

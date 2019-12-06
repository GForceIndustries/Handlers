#ASR
Various utility handlers for Automatic Speech Recognition.

##Notification_SetRecoEIMStatus
This can be used to quickly enable or disable the EIM for an ASR engine via custom notification, to save the need to load Interaction Administrator. This is useful for testing purposes on a system with multiple engine types enabled.

Usage: SendCustomNotification ASR EIM <enable|disable> <loquendo|isr|mrcp|nr9>

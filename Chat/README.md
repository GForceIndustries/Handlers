# Chat
Utility handlers for web and SMS chat.

## Notification_ResetIWebStrings
This can be used to reset the IWeb strings and options for web and SMS chats back to their defaults after they have been changed as part of testing. This will only affect the global settings under Settings: Chat and Settings: SMS and will not remove any workgroup-level or user-level strings or options that have been defined. Running this handler will delete the Settings: Chat and Settings: SMS entries under Web Services Parameters and will recreate them with all options and strings set back to defaults.

Usage: SendCustomNotification Reset IWeb Strings

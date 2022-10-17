# Contract Backward Compatibility
A simple library to decide if you break the backward compatibility for events

## Goal
You have a multiple services that consume and produce number of messages. Each service has it's own repository. You would like to share the event's structure between them to make sure a change in event won't destroy your system and to not duplicate that much code around you codebase.

1. Each change in event is linted.

Adding new field won't be a issue, but it most definitely change the event version.
Changing field type will trigger compatibility issue.
Removing field will trigger compatibility issue.
Changing field name will trigger compatibility issue.

# MLSP protobuf specification
Model Language Server Protocol (MLSP) is a protocol specification for writing gRPC based Model-based Language Servers.

## Feedback Stream Interfaces
Language servers can provide feedback through a variety of methods.
 - Diagnostics
 - Notifications
 - Progress

## Model Resource Interface
Editors can open, close, create and delete models
 - Project Opened - A new project has been opened and the server should clear all cache and load the new project
 - File Created - A new model was created
 - File Deleted - A model was deleted
 - Handle Diff - A change has happened in a model

## Future Work
This specification repository is mostly here until the [buffrs](https://github.com/helsing-ai/buffrs) central repository has been created, or until a different solution is available.

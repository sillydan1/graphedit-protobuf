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

## Languages
### C/C++
This project can be built using CMake.
This means you can depend on this project using [CPM](https://github.com/cpm-cmake/CPM.cmake), or any other CMake-oriented dependency management technique.
```sh
cmake -S . -B Release -DCMAKE_BUILD_TYPE=Release
cmake --build Release
```

### Java
This project can be built using gradle.
This means you can depend on this project by simply adding a dependency to your `build.gradle` (remember to use the latest version):
```gradle
dependencies {
    implementation group: 'dk.gtz.graphedit', name: 'graphedit-protobuf', version: '1.0.0';
    implementation group: 'io.grpc', name: 'grpc-stub', version: '1.60.0';
}
```

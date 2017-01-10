<!---
# license: Licensed to the Apache Software Foundation (ASF) under one
#         or more contributor license agreements.  See the NOTICE file
#         distributed with this work for additional information
#         regarding copyright ownership.  The ASF licenses this file
#         to you under the Apache License, Version 2.0 (the
#         "License"); you may not use this file except in compliance
#         with the License.  You may obtain a copy of the License at
#
#           http://www.apache.org/licenses/LICENSE-2.0
#
#         Unless required by applicable law or agreed to in writing,
#         software distributed under the License is distributed on an
#         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
#         KIND, either express or implied.  See the License for the
#         specific language governing permissions and limitations
#         under the License.
-->

# okstate-plugin-camera-overlay
_works much like the original [cordova-plugin-camera](https://github.com/apache/cordova-plugin-camera) with the simple addition of transparent image overlay_

This plugin defines a global `navigator.camera` object, which provides an API for taking pictures and for choosing images from
the system's image library.

Although the object is attached to the global scoped `navigator`, it is not available until after the `deviceready` event.

```
    document.addEventListener("deviceready", onDeviceReady, false);
    function onDeviceReady() {
        console.log(navigator.camera);
    }
```

## Installation

cordova plugin add cordova-plugin-camera


or


```
    <plugin name="okstate-plugin-camera-overlay" spec="https://github.com/Wambosa/okstate-plugin-camera-overlay#1441e80" source="git">
        <variable name="PHOTOLIBRARY_USAGE_DESCRIPTION" value="App would like to access your camera to take a picture" />
    </plugin>
```

where **1441e80** is the version of the plugin

### todo
- add a working exmaple
- try to speed up compile time
- allow for more control over overlay, such as helptext that is rendered in addition with the location of that text
- refactor the url to be localfile name obvious
- allow for either url or localfile from the js
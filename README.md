# Docker container for Wercker CI to build android application

## Usage

Just specify the box in your `wercker.yml` and run whatever tasks you like with Gradle.

```yaml

box: keithyokoma/wercker-container-android

build:
  steps:
    - script:
        name: run gradle assembleDebug
        code: |
          ./gradlew --project-cache-dir=$WERCKER_CACHE_DIR assemble testDebugUnitTest -PdisablePreDex

```

## License

Apache License v2

```
Copyright (C) 2016 KeithYokoma, Inc. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use
this file except in compliance with the License. You may obtain a copy of the
License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed
under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR
CONDITIONS OF ANY KIND, either express or implied. See the License for the
specific language governing permissions and limitations under the License.
```

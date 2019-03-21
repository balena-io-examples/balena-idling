# Balena-idling

This is most likely the simplest + smallest base image you can use
with a resin.io device, basically just pulling in a base image,
then idling, while periodically printing to the logs that "Idling...".

There's one adjustable parameter: the period of how often "Idling..." is
recorded in the logs. By default it's 600s = 10min, you can change that by
setting an environmental variable called `INTERVAL` to an integer value of your
choosing.

You can use this project to:

* test deploying to your resin.io device the quickest way, or
* get your base image onto your device and develop your project by `resin ssh` into the container.

To use the smallest size, the [Alpine Linux](https://www.alpinelinux.org/) base
image was used, switch that `FROM` line in the `Dockerfile.template` to another
base if you'd like test (Debian, Fedora, or other base images that might be
available for your platform).

## License

Copyright 2017 Resinio Ltd.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

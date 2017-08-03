# Rancher UI for VScale Docker-Machine Driver
This is a Rancher UI for the VScale docker-machine driver. This is unofficial and by no means implies any affiliation with VScale, I just wanted my Rancher UI to be a little prettier.

![Rancher VScale Add Host UI](scaleway-ui.png "Rancher VScale Add Host UI")

## Setup, Development, Build
Follow the guide in the Rancher repository [ui-driver-skel](https://github.com/rancher/ui-driver-skel) to prepare a build environment.

The package.json has been customised with the following additional script functions:

* `deploy`: Pushes a release from the dist subdirectory.

In practice after making changes the following steps will generate a release:

1. `npm run build`
2. `npm run deploy`

## Usage
A release is published to the [GitHub Project Page](https://c58.github.io/ui-driver-vscale/) for this repository:

1. Add a Machine Driver in Rancher (Admin tab -> Settings -> Machine Drivers)
  * Download URL: The URL for the `ubuntu.16.04.x64` driver binary from [https://github.com/vahaah/docker-machine-driver-vscale/releases](https://github.com/vahaah/docker-machine-driver-vscale/releases)
  * Custom UI URL: [https://c58.github.io/ui-driver-vscale/dist/component.js](https://c58.github.io/ui-driver-vscale/dist/component.js)
2. Wait for the driver to become "Active"
3. In Rancher go to (Infrastructure -> Hosts -> Add Host) and the VScale driver and custom UI should show up.

## Alternative UI URLs
These are just for reference as an alternative if there is a problem with GH Pages. Rancher seems to require a correct Content-Type for the .svg logo so directly accessing the raw files on github will not work as intended.

* [https://cdn.rawgit.com/c58/ui-driver-vscale/master/dist/component.js](https://cdn.rawgit.com/c58/ui-driver-vscale/master/dist/component.js)

## Credits
* [vahaah/docker-machine-driver-vscale](https://github.com/vahaah/docker-machine-driver-vscale)
* [rancher/ui-driver-skel](https://github.com/rancher/ui-driver-skel)

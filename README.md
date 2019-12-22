node-red-headstart
# Node-RED - Headstart

Based on "Node-RED Hello, world! Example" at http://developer.opto22.com/nodered/general/getting-started/node-red-hello-world/

## About

### Overview

[Node-RED](http://nodered.org/) is a visual tool for wiring the Internet of Things, by wiring together hardware devices, APIs and online services in new and interesting ways.

![Node-RED](http://developer.opto22.com/images/node-red-pac/node-red-pac-hardware.jpg)

For more information, please see the following information:

- [Getting Started with Node-RED](http://developer.opto22.com/nodered/general/getting-started)
- [PAC Control nodes](http://developer.opto22.com/nodered/pac)
- [groov View nodes](http://developer.opto22.com/nodered/groov)
- groov EPIC processor
  - [GRV-EPIC-PR1 product page](https://www.opto22.com/products/product-container/grv-epic-pr1)
- groov Edge Appliance
  - [GROOV-AR1 product page](https://www.opto22.com/products/groov-ar1-base)
  - [Node-RED announcement](http://blog.opto22.com/optoblog/optonews-iiot-tool-node-red-included-in-new-groov-admin-release)
  - [Digitally Wiring the IIoT with Node-RED](http://blog.opto22.com/optoblog/digitally-wiring-the-iiot-with-node-red)
  - [groov.com](https://groov.com/?__hstc=256016212.dfb3efe4cbcc920bfe85d2853b6262cb.1577022410153.1577022410153.1577022410153.1&__hssc=256016212.2.1577022410154&__hsfp=3201587947)
- [Resources](http://developer.opto22.com/nodered/resources)

## Getting Started with Node-RED

### Introduction

This Getting Started guide covers getting Node-RED running (either on a groov EPIC processor, groov Edge Appliance, or a computer), and provides a few examples of how to use Node-RED.

Node-RED comes pre-installed on groov EPIC processors and the groov Edge Appliance.

If you want to run Node-RED on your own computer, continue to installing Node-RED.

If using a groov EPIC processor or groov Edge Appliance, continue to the Hello, world! example.

#### Node-RED Installation

**Overview**

Node-RED runs on the Node.js platform, a cross-platform JavaScript engine. For more information on Node.js, see [nodejs.org](https://nodejs.org/).

Node-RED is pre-installed on groov EPIC processors and the groov Edge Appliance.

To install Node.js and Node-RED on your own computer, see the following instructions.

**NOTE**: For demo purposes, we have created a server (Server-Node-RED) on Linux Academy Cloud Playground (https://app.linuxacademy.com/dashboard) on which below software has been installed. See https://linuxize.com/post/how-to-install-node-js-on-centos-7/

**Install Node.js**

The recommended installer is on the Node.js [homepage](https://nodejs.org/), and other downloads are available on their [download page](https://nodejs.org/en/download/).

Our SNAP PAC nodes require Node.js version 4.4.5 or newer, so get the current stable version.

For Windows, it’s a typical installer that you download and run.

For Linux, Node.js is available via many [package managers](https://nodejs.org/en/download/package-manager/). For instance, instructions for Debian-based systems like Ubuntu and the Raspberry Pi’s Raspbian are [here](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions). There are also various [binary downloads](https://nodejs.org/en/download/) available.

Once Node.js is installed, you should verify that the version is 4.4.5 or newer. Open a command prompt or terminal window, and enter:

```javascript
node -v
```

You should get a response like:

![Command Prompt](http://developer.opto22.com/nodered/general/getting-started/images/nodejs-install-version.png)

**Install Node-RED**

Like Node-RED, Node.js packages are installed with the npm command-line tool. npm is the Node Package Manager, and is typically used to download and install packages from the central Node registry at [npmjs.com](https://npmjs.com/).

The full Node-RED installation instructions are [on their site](http://nodered.org/docs/getting-started/installation).

On Windows, from a command-prompt, type:
```javascript
npm install -g node-red
```

On Linux, from a terminal window, type:
```javascript
sudo npm install -g --unsafe-perm node-red
```

It can take a few moments before much happens. The npm tool will begin to install Node-RED and all of its dependencies.

Along the way, you’ll probably see some errors like this:

![Command Prompt](http://developer.opto22.com/nodered/general/getting-started/images/nodered-install-win.png)

Those errors can be safely ignored. The [Node-RED website](http://nodered.org/docs/getting-started/installation#install-node-red) says that those are optional dependencies, and that “Node-RED will work without these optional dependencies”.

**Run Node-RED**



#### Node-RED Hello, world! - Part 1

#### Node-RED Hello, world! - Part 2

### Troubleshooting

... more

### Resources

... more

### Code Samples

... more


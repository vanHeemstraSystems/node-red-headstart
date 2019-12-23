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

**NOTE**: For demo purposes, we have created a server (Server-Node-RED) on Linux Academy Cloud Playground (https://app.linuxacademy.com/dashboard) on which below software has been installed. See https://linuxize.com/post/how-to-install-node-js-on-centos-7/ and https://www.cyberciti.biz/faq/howto-install-google-chrome-on-redhat-rhel-fedora-centos-linux/

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

Now run Node-RED with:

```javascript
node-red -v
```

The output will look like:

```javascript
Welcome to Node-RED
===================

16 May 15:10:26 - [info] Node-RED version: v0.13.4
16 May 15:10:26 - [info] Node.js  version: v4.2.5
16 May 15:10:26 - [info] Windows_NT 10.0.10586 x64 LE
16 May 15:10:26 - [info] Loading palette nodes
16 May 15:10:27 - [warn] ------------------------------------------
16 May 15:10:27 - [warn] [rpi-gpio] Info : Ignoring Raspberry Pi specific node
16 May 15:10:27 - [warn] [tail] Not currently supported on Windows.
16 May 15:10:27 - [warn] ------------------------------------------
16 May 15:10:27 - [info] Settings file  : C:\Users\sabrina\AppData\Roaming\npm\n
16 May 15:10:27 - [info] User directory : \Users\sabrina\.node-red
16 May 15:10:27 - [info] Flows file : \Users\sabrina\.node-red\flows_sabrina-W
16 May 15:10:27 - [info] Creating new flow file
16 May 15:10:27 - [info] Starting flows
16 May 15:10:27 - [info] Started flows
16 May 15:10:27 - [info] Server now running at http://127.0.0.1:1880/
```

Open your web browser to the address shown (for example, http://127.0.0.1:1880) and you should see the default Node-RED screen:

**NOTE**: On Linux Academy Cloud Playground server you will have to open the Graphical Shell from the Actions menu of Server-Node-RED to open a browser.

![Server-Node-Red Terminal Node RED](https://github.com/vanHeemstraSystems/node-red-headstart/blob/master/Graphical_Shell_Linux_Academy_Server_Node_RED_Terminal_Node_RED.PNG) 
Start Node-RED from a Terminal window

![Server-Node-Red Terminal List_Settings](https://github.com/vanHeemstraSystems/node-red-headstart/blob/master/Graphical_Shell_Linux_Academy_Server_Node_RED_Terminal_List_Settings.PNG)
Find settings.js file

![Server-Node-Red Terminal Set_Settings](https://github.com/vanHeemstraSystems/node-red-headstart/blob/master/Graphical_Shell_Linux_Academy_Server_Node_RED_Terminal_Set_Settings.PNG)
Set credentialSecret (here: made unreadable : ) in settings.js file and save

![Server-Node-Red Terminal Node RED](https://github.com/vanHeemstraSystems/node-red-headstart/blob/master/Graphical_Shell_Linux_Academy_Server_Node_RED_Terminal_Node_RED_Restart.PNG) 
Restart Node-RED from a Terminal window

![Server-Node-Red Terminal Google Chrome](https://github.com/vanHeemstraSystems/node-red-headstart/blob/master/Graphical_Shell_Linux_Academy_Server_Node_RED_Terminal_Google_Chrome.PNG)
Start Google Chrome from a separate Terminal window

![Server-Node-Red Browser](https://github.com/vanHeemstraSystems/node-red-headstart/blob/master/Graphical_Shell_Linux_Academy_Server_Node_RED_Browser.PNG)
Open the URL for Node-RED, hence http://127.0.0.1:1880, in Google Chrome.

#### Node-RED Hello, world! - Part 1

**Overview**

While this tutorial covers a very basic example, there are a few key concepts that should be discussed first:

- Messages are objects containing data, and they flow from node to node. They are the basic mechanism by which Node-RED operates.
- Nodes either generate a new message or process an incoming message.
- Messages have properties, which are values attached to the message. Properties are basically a variable and can be numbers, strings, booleans, arrays, or objects.
- A very common message property is called the payload. Many nodes will use the payload property by default.
- Inside of a node, the message object is called simply “msg”.
- Flows are a collection of connected nodes that messages pass through.

**Step 1 - Add an Inject node**

First, we need a way to start the flow. That’s one of the main purposes of the Inject node—to inject a message into the flow.

1. If it’s not open already, open Node-RED in your browser.
- If using a groov EPIC processor, then open https://[groov-epic-hostname]/node-red
- If using a groov Edge Appliance, then open https://[groov-box-hostname]:1880.
- If using Node-RED running on your computer, you can use http://127.0.0.1:1880 or whichever address or hostname you’re using.
2. If you haven’t used Node-RED before, there should be one empty flow named “Flow 1”.
3. From the node palette on the left side of the Node-RED editor, select an Inject node and drag it onto the flow.
4. Double-click the node to open the “Edit inject node” view.
5. For the Payload field, select string and enter Hello, world! in the text field.
6. Click Done.

Later, with its msg.payload property set to “Hello, world!” this node is going to inject a message into the flow.

![Text](http://developer.opto22.com/nodered/general/getting-started/images/nodered-helloworld-1.png)

... more

#### Node-RED Hello, world! - Part 2

### Troubleshooting

... more

### Resources

... more

### Code Samples

... more


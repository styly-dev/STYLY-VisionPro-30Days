# Day004 - Display server images

By [from2001](https://github.com/from2001)

## Introduction

Let's display images on the Internet. UnityWebRequest using Unity official Visual Scripting node is tricky and not easy to handle. STYLY provides easy-to-handle Visual Scripting nodes for server resources. I am going to show you how to use [Visual Scripting Nodes for WebRequest](https://github.com/styly-dev/WebRequest_VisualScriptingNodes)


## Add Visual Scripting Nodes for WebRequest

Prerequisites : [Node.js 14.18 or above](https://nodejs.org/en/download/)  
STYLY visionOS Plugin and other supported packages can be installed via [OpenUPM](https://openupm.com/packages/com.styly.styly-vision-os-plugin/). 
```shell
# Install openupm-cli
npm install -g openupm-cli

# Go to your unity project directory
cd YOUR_UNITY_PROJECT_DIR

# Install STYLY visionOS Plugin for Unity
openupm add com.styly.styly-vision-os-plugin
# Install glTFast Visual Scripting Nodes
openupm add com.styly.webrequest-visualscripting-nodes
```

## How to use

### Load an image with URL

Let's start with the simplest one. Add `Get Texture` node to your script graph and set an image URL which you want to display on a Gameobject. 

Use this URL for example.  
https://raw.githubusercontent.com/styly-dev/STYLY-VisionPro-30Days/main/_FIles/Whales001.jpeg

Image will be displayed. The Visual Scripting Nodes for WebRequest has some features which is not implemented in the original UnityWebRequest. One of the feature is caching. The images you used with the Visual Scripting node are stored in the storage and will be used next time.

<img width="1572" alt="Load Image" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/02535efb-ef39-4b83-9bd0-3a0174d30dfa">

### Load random images

[Lorem Picsum](https://picsum.photos/ ) is a great website which provide beautiful random images. For example, each time you access to 
https://picsum.photos/1200, you'll get a different image each each time. However, explained in the previous section, images used with the Visual Scripting node are all cached and reused. So if you want to get random images with the same URL, you need to add random string to the end of the URL.

The string after `?` will be ignored by the photo service, but the WebRequest Visual Scripting node treats them as different URLs.  
https://picsum.photos/200?0.3937196  
https://picsum.photos/200?0.1937254  

<img width="1915" alt="Load Random Images" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/73c223c0-57c6-483a-b99d-15aeb4d731b5">


### Handle download progress

Download progress can be handled with the Visual Scripting node. It is kind that you display download status with text or meter gauge. The status of the download can be obtained like this. The value of the progress is 0 to 1 float number.

<img width="1280" alt="Download Progress" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/01b76fec-c624-44ff-8370-9d7e3d8be52e">

### Upload to STYLY

Drag the Gameobject to PRoject window to make it prefab, and right click on it to build for STYLY. 

<img width="1552" alt="STYLY" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/dbbdd894-5741-4857-ba1a-d6ff56c5843a">

　 
　   
　  

Open the content URL with Safari in Vision Pro to experience the sample with STYLY.

https://spatial-layer.styly.cc/content/2ebc3973-f1a0-4597-86a2-02f87141354e

<img width="884" alt="Random images" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/9318b63c-5754-46d7-b4d0-2ff44114217a">




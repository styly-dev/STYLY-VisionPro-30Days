# Day006 - Play musics on the server

By [from2001](https://github.com/from2001)

## Let's make a music player for Vision Pro

I'm gonna explain about how to make a music player for Vision Pro using STYLY in the coming few articles. Let's start with a very simple Visual Scripting Node to just play a mp3 on the server.

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

## Create Visual Scripting Graph

Just add `Get AudioClip` node to your scripting graph. The node will download a music file from the server, and the output can be used as an Audio Clip. Connect the output to a `audio source - set clip` node. 

<img width="1913" alt="PlayMusicOnServer" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/fd82c411-40d2-4c55-8a33-63fe21114ea0">

`This` on the audio source node means that the audio clip will be set to the audio source on a Gameobject where the scripting graph is located. If you want to specify the Gameobject for the audio source, you can set a Gameobject via Object Variables.

<img width="2012" alt="Specify Audio Source" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/558e55ee-f27c-40d4-b905-28f1b6144e4b">


## Upload to STYLY

Right click on the cube prefab which you want to build and upload. Then select `STYLY` - `Build prefab`

Check the [Day001](https://github.com/styly-dev/STYLY-VisionPro-30Days/tree/main/Day001%20-%20Hello%20Cube) article for the detail

<img width="973" alt="BuildPrefab" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/92ae70a7-01c8-4153-bcdf-933011fa9545">



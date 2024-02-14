# Day001 - Hello Cube

By [from2001](https://github.com/from2001)

First things first. Let's make a cube for Vision Pro!!

![Day001](https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/0a3be490-bed4-4880-b522-f3be851630b7)


## How to setup a project from scratch

You can use the this Day001 directory as an Unity project template which includes required settings, but you can also prepare a project from scratch.

Check the [STYLY visionOS Plugin for Unity](https://github.com/styly-dev/STYLY-VisionOS-Plugin/) repository for the latest information.

### Create new project

- Unity 2022.3.18f1
- 3D (URP)

<img width="1268" alt="New Project" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/96ee575e-6cce-46ae-8263-8348ecaf6470">

### Switch platform to visionOS 
<img width="752" alt="BuildSettings" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/6db1df47-9f71-4fe3-bd23-19709441e408">

### Add STYLY visionOS Plugin to the project

Prerequisites : [Node.js 14.18 or above](https://nodejs.org/en/download/)  
STYLY visionOS Plugin can be installed via [OpenUPM](https://openupm.com/packages/com.styly.styly-vision-os-plugin/). 
```shell
# Install openupm-cli
npm install -g openupm-cli

# Go to your unity project directory
cd YOUR_UNITY_PROJECT_DIR

# Install package
openupm add com.styly.styly-vision-os-plugin
```

### Others
Click `Remove Readme Assets` on Readme to remove tutorial files.

<img width="1229" alt="Remove Tutorial" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/db06f8bd-57a1-4cef-b12a-0953f73b2a42">


## How to create a cube

Right click in the Hierarchy window and select `Cube` to create new 3D object.

<img width="965" alt="Create Cube" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/570b9e5b-21d3-46a6-8e46-e453c14a45e1">

　  
　  
Change the size and rotation of the cube and drag it to the Assets window. The cube now can be handled as a prefab. Prefabs can be uploaded to STYLY using the plugin.

<img width="1093" alt="Cube" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/8bec9f0e-1d03-4ac4-87fd-ca4b270363de">

## Build and upload Prefab

Prefab can only be built and uploaded to STYLY for now. If you want to upload multiple GameObjects, you can do so by making them into a single Prefab.  

Right click on the cube prefab which you want to build and upload. Then select `STYLY` - `Build prefab`

<img width="973" alt="BuildPrefab" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/92ae70a7-01c8-4153-bcdf-933011fa9545">

After several minutes building process, STYLY asset file will be created in          `_Output` directory in your project. The name of the asset file will be something like `xxxxxxxxxxxxxx.styly`.

<img width="1126" alt="Finder" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/a6bdd09e-a828-46f4-b53d-2f51a302bb71">

STYLY webpage will also be opened with a web browser automatically. Login with your STYLY account. If you don't have one, please make it on https://gallery.styly.cc/signup

Note that STYLY contents for mobile AR or VR devices listed on https://gallery.styly.cc/ is not compatible with STYLY for Vision Pro.

<img width="1032" alt="UploadFile" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/4d21a4d7-4cde-4481-837b-33b9e93f8e9e">

Visit [Upload content page](https://spatial-layer.styly.cc) after login with your account. Fill out Title and Description of your content, and select the STYLY asset file to upload.

Display type determines how the content will be displayed.
- Bounded: Your contents will be displayed in 1m x 1m x 1m size. Contents can be displayed with other apps.
- Unbounded: Your contents will be displayed exclusively in a space.

You will get URL of your STYLY content like 
`https://spatial-layer.styly.cc/content/bb325046-61fd-4bb2-a80b-c5ea285ce8e6`

Open the URL on Safari in your Vision Pro device or the simulator. Click `Play on Apple Vision Pro` to launch your content.  

Read the [instruction](https://github.com/styly-dev/STYLY-visionOS-Plugin/blob/develop/README.md#install-styly-for-vision-pro-into-the-visionos-simulator) if you want to install STYLY on Vision Pro simulator. 

<img width="895" alt="Safari on Vision Pro" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/c8e615d6-42f7-4399-ac95-c7f1c79e7715">





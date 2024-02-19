# Day003 - Load glTF/glb 3D models
By [from2001](https://github.com/from2001)

## Introduction

![Cartoon Prototype Car](https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/e853a162-ead6-40a6-b8b8-abfddb1f78e3)

STYLY for Vision Pro supports some Unity packages registered on OpenUPM. One of the package is [glTFast Visual Scripting Nodes](https://github.com/from2001/glTFast_VisualScriptingNodes/) which is a Visual Scripting Node bridge of Unity official [glTFast package](https://docs.unity3d.com/Packages/com.unity.cloud.gltfast@6.2/). 

Using the package, glTF/glb 3D models can be handled with Unity Visual Scripting and distributed to Vision Pro via STYLY without difficulties.

Note that your custom C# scripts cannot be included into STYLY contents, but Visual Scripting graphs can be used.

glTF is a widely used standard file format for three-dimensional scenes and models, which can be exported from major 3D modeling software.

The GLB file format is a binary file format of glTF format. 3D model in glTF format consists of multiple files, and glb format is the easy-to-handle single packed version of the glTF 3D model.   

## Add glTFast Visual Scripting Nodes

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
openupm add com.from2001.gltfast-visualscripting-nodes
```

## gtTF/glb 3D model samples

Find sample 3D models in [KhronosGroup/glTF-Sample-Assets](https://github.com/KhronosGroup/glTF-Sample-Assets/) repository

## Load glTF/glb 3D models into your Unity contents
There are two options to handle glTF/glb 3D models with the package.

### Option A: Load 3D models into Unity Editor

Just drag and drop glTF/glb 3D model files into the project window. The model will be automatically converted to Unity compatible data. Drag it to the hierarchy window to display in your scene. 

<img width="1073" alt="glb1" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/3e52522e-548a-4028-ae51-fa9d02ac044e">

Only prefab can be uploaded to STYLY with the Unity plugin. So drag the 3D model in the hierarchy window to the project window to make it to the prefab.

<img width="1073" alt="glb2" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/9a4afb81-bff3-453c-b22f-cdd26bfe212c">



### Option B: Load 3D models at runtime from a server

3D models can also be loaded at runtime with Unity Visual Scripting. The sample of the Visual Scripting graph is provided in the package.  

<img width="912" alt="Samples" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/d35cf822-4021-4946-84c2-570b02d5e8ef">

#### Simplest usage
Let's load a glb file from a server with the glTFast Visual Scripting Node. Jst add the node to your script graph and set a glb URL to the node. Then make it work on start connecting its input trigger and On Start event node.
That's it. 

<img width="1395" alt="Simple" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/dfcdf5ca-ebdd-41f0-8182-25671c5116cb">

#### Advanced usage

##### Transform the loaded 3d Models

Loaded 3D models can be controlled with Visual Scripting. Once the model is loaded, you can handle the gameobject with the output.

<img width="1915" alt="glb3" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/0147961e-2f41-4a95-a4d0-e2bc0c1a0763">

##### Set the location to spawn the 3D model 

You can also specify the location to load your 3D model. Using the Target Game Object, your 3D model will be transformed with values of the target game object. So, the position, rotation and size can be set to the 3D model.  

<img width="1915" alt="glb4" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/6f4a20e8-517a-4b83-ac07-0f07bcd23bfe">

#### Sketchfab 3D model

Sketchfab is a platform that allows users to publish, share, and discover 3D, VR, and AR content online. 3D models on Sketchfab are converted to glTF and glb in the backend. 3D models of Blender, fbx or other 3D format can be downloaded as glTF/glb format.  

Even just viewing 3D models with STYLY for Vision Pro is a great experience for lots of people including myself since environment lights are affected to the model and make it beautiful. So, please find your favorite models and import them to STYLY.

One of my favorite is [Cartoon Prototype Car](https://sketchfab.com/3d-models/cartoon-prototype-car-88b89d3074cb4946a353ab990d1ff6a2).

<img width="884" alt="Car" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/fda5e9db-15df-4d87-80f2-5afbf2089388">

## Miscellaneous

### Shaders for visionOS
Since shaders in glTFast package in not compatible with visionOS, so compatible shaders from [prefrontalcortex/UnityGLTF](https://github.com/prefrontalcortex/UnityGLTF) will be applied at runtime on visionOS environment or when you import 3D models into Unity Editor. 

STYLY uses assetbundle architecture to distribute your contents. Assetbundle for visionOS cannot include shaders in the file (at least for now), which causes material display problem on STYLY app even though the 3D model is displayed correctly on Unity Editor. Shaders of prefrontalcortex/UnityGLTF are included and compiled into STYLY for Vision Pro app, but not all shader variants are included. If you encounter shader problem, please feedback us in Issues on this repository. 

## 3D models

[Cartoon Prototype Car](https://sketchfab.com/3d-models/cartoon-prototype-car-88b89d3074cb4946a353ab990d1ff6a2)


[Duck](https://github.com/KhronosGroup/glTF-Sample-Assets/blob/main/Models/Duck/README.md)  

&copy; 2006, Sony. [SCEA Shared Source License, Version 1.0](https://spdx.org/licenses/SCEA.html) Sony for Everything

[Damaged Helmet](https://github.com/KhronosGroup/glTF-Sample-Assets/blob/main/Models/DamagedHelmet/README.md)  

&copy; 2018, ctxwing. [CC BY 4.0 International](https://creativecommons.org/licenses/by/4.0/legalcode)
ctxwing for Rebuild and conversion to glTF  

&copy; 2016, theblueturtle_. [CC BY-NC 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/legalcode) theblueturtle_ for Earlier version of model



# Day003 - Load glTF/glb 3D models
By [from2001](https://github.com/from2001)

## Introduction

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

## Load glTF/glb 3D models into your Unity contents
There are two options to handle glTF/glb 3D models with the package.

### Option A: Load 3D models into Unity Editor



### Option B: Load 3D models at runtime from a server



## Miscellaneous

### Shaders for visionOS
Since shaders in glTFast package in not compatible with visionOS, so compatible shaders from [prefrontalcortex/UnityGLTF](https://github.com/prefrontalcortex/UnityGLTF) will be applied at runtime on visionOS environment or when you import files on Unity editor. 

STYLY uses assetbundle architecture to distribute your contents. Assetbundle for visionOS cannot include shaders in the file (at least for now), which causes material display problem. Shaders of prefrontalcortex/UnityGLTF are included and compiled into STYLY for Vision Pro app, but not all shader variants are included. If you encounter shader problem, please feedback us in Issues on this repository. 





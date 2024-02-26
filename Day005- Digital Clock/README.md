# Day005 - Digital Clock

By [from2001](https://github.com/from2001)

## Introduction
When you need to implement logics, your original C# script cannot be included in your STYLY contents. However, Visual Scripting Graph can be used to make programs.  

Today, I am gonna explain how to make a digital clock with Visual Scripting. I implemented the logic of the clock as a subgraph, so you can just use it to make your original clock.  

![Clock2](https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/ffad392e-c2bf-494b-bf06-28ae0bb2daa8)


## Visual Scripting Subgraph

A "subgraph" within the context of Unity's visual scripting is a node or a collection of nodes that encapsulate a specific functionality or logic. Essentially, it's a way to create custom nodes that contain an internal network of pre-existing nodes. Subgraphs can be used to organize complex logic into manageable, reusable components. This helps in keeping the visual script clean and understandable, especially as projects grow in complexity.

### How to use subgraph

Incorporate the subgraph into your visual scripts by dragging it from your project assets into the visual scripting editor, connecting it to other nodes as needed to utilize its functionality. `Clock Subgraph` is included in this project.

You can set prefabs as each digit as well as target locations. 

<img width="1671" alt="ClockSubgraph" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/db5c1d36-600f-41b5-9f05-3cc02baeaeb2">

An animation is attached to each digit prefab to make it look good. Animation is triggered when attached prefab is spawned. If you want to change the design of the clock, you can just change the prefab to set to its variables.

<img width="1671" alt="Animation" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/379cefdf-735c-4538-a4f1-117122574a12">

### The inside of the subgraph

A subgraph is a collection of Visual Scripting node. The clock subgraph is made with a bunch of simple nodes. Let's take a look.

<img width="887" alt="InsideOfSubgraph" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/0c1cbbe4-2f74-491a-af37-3187ca61b171">


### Upload to STYLY

As always, just right click on the clock prefab and build. A new browser will open. Upload the build file to STYLY via the opened webpage as bounded contents.

### Use it in Vision Pro

Open the created content URL with Safari in your Vision Pro. Click `Play on Apple Vision Pro` to launch the content. The URL of the uploaded sample clock is https://spatial-layer.styly.cc/content/18b8ac56-397c-484e-a29a-789615c22d1c  


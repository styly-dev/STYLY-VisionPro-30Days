# Day002 - Hello rotating cube
By [from2001](https://github.com/from2001)

## VIsual Scripting Support for STYLY

With STYLY plugin, Unity prefab will be built as an asset bundle. Because of the limitation of the architecture, your C# script cannot be included and distributed to STYLY.

However, you can use Unity Visual Scripting to make a logic instead. 

### Set up Visual Scripting

Click `Edit` - `Project Settings` - `Visual Scripting` - `Initialize Visual Scripting` to get ready for the node based visual programming environment.

<img width="871" alt="InitializeVisualScripting" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/b181ff57-bb51-4c19-b29b-4e95e5066c8b">

You will see settings like this. Leave all the settings at their default.

<img width="871" alt="InitializeVisualScripting2" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/7b8cc0cf-7314-4888-9b8a-2ef96b31076c">

1. Create a Cube and attach a Script Machine component.
2. Click `New` to create a script graph. Let's name it `Rotate`.
3. Click `Edit Graph`
<img width="1046" alt="ScriptMachine" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/35c137d1-2a47-4d4a-972b-c914eed3a6f8">

Find and add `Transform: Rotate (Eulers, Relative To)` node to the script graph.

<img width="1091" alt="Add Node" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/8be77f72-a663-42ee-bfa8-4be4af477197">


Connect output trigger of `On Update Event` node and input trigger of `Transform: Rotate (Eulers, Relative To)` node. Set the parameters and hit `Play` on the editor.

Cube will rotate!!

![RotatingCube](https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/dee905f4-7bfa-4163-a539-047ed45c7a6c)

Make the cube prefab and build it with STYLY plugin.

<img width="769" alt="Build" src="https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/34ac7d57-bdd0-47a9-804a-32e75a312eab">

Upload the built .styly file, and view it with STYLY for Vision Pro.

![simulator](https://github.com/styly-dev/STYLY-VisionPro-30Days/assets/387880/dbfccbf2-d642-402f-b76e-7ac264370bc3)
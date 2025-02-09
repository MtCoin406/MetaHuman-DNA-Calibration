# DNAViewer
The [`dna_viewer`](/dna_viewer) contains all the needed classes for reading and creating a functional rig in Maya from the DNA file.
It is organized in a way that allows every option to be configurable, so you can easily get the exact result you want.

## Examples
- [Generates rig](/examples/dna_viewer_build_rig.py)
- [Export FBX per LOD](/examples/dna_viewer_export_fbx.py)
- [Propagate changes from Maya scene to dna](/examples/dna_viewer_grab_changes_from_scene_and_propagate_to_dna.py)
- [Simple UI](/examples/dna_viewer_run_in_maya.py)


## Usage from code
There are two [APIs](dna_viewer_api.md):
  - [build_meshes](dna_viewer_api_build_meshes.md)
  - [build_rig](dna_viewer_api_build_rig.md)

## Usage in Maya 
Usage in Maya is explained [here](/docs/dna_viewer_maya.md)


## Folder structure

- [builder](/dna_viewer/builder) - Contains the builder classes, which are used for easily adding configuration options
and building the scene, configurations, meshes, etc..
- [dnalib](/dna_viewer/dnalib) - Contains classes for nicer API accessing DNA file.
- [ui](/dna_viewer/ui) - Contains the classes needed for the Maya UI.

## How it works

The general flow is the following:

![image](img/flow_general.png)

The flow of the scene building process is the following:

![image](img/flow_scene_build.png)

The flow of the rig building process is the following:

![image](img/flow_character_build.png)

Legend:
- <span style="color:blue">blue: builder-related</span>.
- <span style="color:green">green: config-related</span>.
- <span style="color:brown">brown: model-related</span>.
- <span style="color:purple">purple: reader-related</span>.

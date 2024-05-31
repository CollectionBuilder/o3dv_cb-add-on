# o3dv_cb-add-on

CollectionBuilder-CSV Add-on: Online 3D Viewer

This repository provides template files to add an Online3DViewer option into a CollectionBuilder-CSV project. The files in this directory structure can be copied directly into a CB-CSV repository to add the new features.

*note: only compatible with CB-CSV out of the box, not other templates*

## Online 3D Viewer

[Online 3D Viewer](https://github.com/kovacsv/Online3DViewer) is a library for rendering 3D model files on a web page.
You can test your models in their browser-based viewer [3dviewer.net](https://3dviewer.net/).

This add-on uses the [o3dv library](https://kovacsv.github.io/Online3DViewer/index.html) to allow embedding an interactive 3d model into pages in your collection project.
All assets are self-contained in the add-on files with no external dependencies.

## How To Use

Add to CB-CSV project:

- Start a CollectionBuilder-CSV project
- Download this add-on to your computer (click "Code" > "Download ZIP", then unzip package)
- Copy all content in the add-on (all files and folders except the README.md) and paste into your existing CollectionBuilder-CSV project. The folder structure in this add-on should match up with your CB-CSV template, adding new files in the correct places (do not delete or overwrite anything in your existing CB project!).

General 3D model tips:

- Test loading your model files at [3dviewer.net](https://3dviewer.net/).
- o3dv supports many formats: 3dm, 3ds, 3mf, amf, bim, brep, dae, fbx, fcstd, gltf, ifc, iges, step, stl, obj, off, ply, wrl. However, we have only tested it with obj, stl, and glb/gltf.
- Ensure your model files are a reasonable size to load on the web page. If they are really big, implement a button giving your users a choice to load the model.
- Put your model files in the "objects" folder or other web accessible location. 

### Embed on Content Page

Use the feature/o3dv-embed.html include, e.g.
`{% include item/o3dv-embed.html model="/objects/example.obj" %}`

### Add to Item Pages

To create item pages containing a 3D model embed:

- set up your items with the path to the 3d model file in the "object_location" column. 
- use the "display_template" value of "3d_model".
- create an alternative description of the model in the "image_alt_text" column if desired.

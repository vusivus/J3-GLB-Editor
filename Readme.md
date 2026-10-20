# J3 GLB Editor

**Open, preview, and edit GLB and glTF assets with the familiar tools and appearance of J3 Asset Manager.**

J3 GLB Editor is a desktop application for working with glTF 2.0 models, materials, textures, skeletons, and animations. It brings model inspection and animation editing into one workspace, using J3 Controls for its interface and J3 Runtime for animation playback and retargeting.

## Model and material editing

![Model and material editing in J3 GLB Editor](images/Model%20Editing.png)

- Open **`.glb` and `.gltf`** files, including animation-only assets.
- Inspect the scene hierarchy and preview models in a navigable 3D viewport.
- Adjust PBR material properties, including base color, metallic, roughness, opacity, emissive color, normal scale, occlusion strength, and double-sided rendering.
- Replace or remove base-color, normal, metallic-roughness, occlusion, and emissive texture maps.
- Preview, resize, and convert textures with the built-in texture tools, or edit them in a configured external application and reload the result.
- Toggle the grid, lighting, and skeleton display, and frame the loaded model or skeleton.

## Animation editing

![Animation editing in J3 GLB Editor](images/Animation%20Editing.png)

Preview and edit embedded animation clips using the shared J3 animation timeline and editing services.

- Play, loop, scrub, step through frames, and change playback speed.
- Create, duplicate, rename, reverse, mirror, and trim animation clips.
- Insert translation, rotation, and scale keys; move or delete selected keys.
- Edit rotation curves and apply rotation offsets to a selected joint.
- Remove root travel to create an in-place animation, using J3's root-motion and grounding workflow.
- Undo and redo document edits, including material, texture, and animation changes.

### Skeletons, J3 Rigs, and retargeting

Inspect skeletal assets with visible joint guides and the scene hierarchy. Skeleton setup is offered for assets that contain a skeleton and can be skipped.

Create a reusable **J3 Rig** with automatic humanoid mapping, manual joint assignments, and Bind, T, or A reference poses. Save rigs as `.j3rig` files and load them as retargeting preview targets.

The animation preview defaults to the source model. Choose the bundled **J3 Mannequin** or a saved J3 Rig when you want to preview an animation on another character. Preview selection does not replace the source asset or bake retargeting into its exports.

## Save and export

Save your complete document as **GLB or glTF**, or create a separate export with the components you need:

- Meshes
- Materials and textures
- Skeleton and skin data
- Animations
- A selected hierarchy branch

For a **skeleton-only export**, include the skeleton and omit meshes, materials, and textures. Include animations as well if the exported skeleton should retain its clips.

## Video

[![Watch J3 GLB Editor on YouTube](https://img.youtube.com/vi/9mEoKYVm6rg/hqdefault.jpg)](https://youtu.be/9mEoKYVm6rg)

**[Watch the video on YouTube](https://youtu.be/9mEoKYVm6rg)**

## Getting started

1. Extract the distribution for your platform, keeping the application and its `libraries` folder together.
2. Install **64-bit Java 21 or later**.
3. On Windows, launch `J3 GLB Editor.exe`. On Linux, run `sh launch.sh` from the extracted folder, or `java -jar "J3 GLB Editor.jar"`.
4. Open a `.glb` or `.gltf` file, then select a material or animation clip to begin editing.

Linux also requires a graphical desktop, GTK 3, X11/XWayland, and compatible OpenGL drivers. The Linux bundle includes Linux x86_64 native libraries.

When opening an existing `.gltf` file, keep its referenced buffers and textures available beside it in their original relative locations. glTF files saved by this editor embed their buffers and textures.

## Built on J3

J3 GLB Editor reuses **J3 Asset Manager Controls**, **J3 Runtime**, and the shared animation editing services used by **J3 Animation Editor**. Its interface follows the J3 desktop toolset, with an icon toolbar, scene hierarchy, material inspector, 3D viewport, and animation timeline.

The editor focuses on asset inspection, materials, textures, and animation editing. Mesh modeling, IK authoring, and animation blend-layer authoring are outside its current scope.

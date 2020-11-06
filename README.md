# InterpolatedCamera3D add-on

This add-on restores a node similar to the built-in InterpolatedCamera3D
(which is being removed in Godot 4.0). On top of that, it provides more control
over smoothing by letting you use different factors for translation, rotation,
FOV changes, and near/far plane changes.

Note that this add-on is *not* a 100% compatible drop-in replacement to the
InterpolatedCamera3D node, as this add-on provides some features that are
backwards-incompatible.

This repository only contains the add-on. See
[godot-extended-libraries/godot-interpolated-camera3d-demo](https://github.com/godot-extended-libraries/godot-interpolated-camera3d-demo)
for the demonstration project.

## Installation

### Using the Asset Library

- Open the Godot editor.
- Navigate to the **AssetLib** tab at the top of the editor and search for
  "lod".
- Install the
  [*InterpolatedCamera3D*](https://godotengine.org/asset-library/asset/739)
  plugin. Keep all files checked during installation.
- In the editor, open **Project > Project Settings**, go to **Plugins**
  and enable the **InterpolatedCamera3D** plugin.

### Manual installation

Manual installation lets you use pre-release versions of this add-on by following its
`master` branch.

1. Clone this Git repository:

```bash
git clone https://github.com/godot-extended-libraries/godot-interpolated-camera3d.git
```

Alternatively, you can
[download a ZIP archive](https://github.com/godot-extended-libraries/godot-interpolated-camera3d/archive/master.zip)
if you do not have Git installed.

2. Move the `addons/` folder to your project folder.
3. In the editor, open **Project > Project Settings**, go to **Plugins**
   and enable the **InterpolatedCamera3D** plugin.

## Usage

1. After enabling the plugin (see above), add an InterpolatedCamera3D node
   to your scene.
2. Select the InterpolatedCamera3D node, go to the inspector and define a Target node.
   The target node must be a node inheriting from Node3D. If the target node a Camera3D,
   the InterpolatedCamera3D will smoothly acquire its FOV and near/far plane distance values
   as well.
3. Configure the InterpolatedCamera3D's smoothing values to your liking.
   Higher values will interpolate faster.

## License

Copyright © 2020 Hugo Locurcio and contributors

Unless otherwise specified, files in this repository are licensed under the
MIT license. See [LICENSE.md](LICENSE.md) for more information.

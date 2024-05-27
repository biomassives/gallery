#gallery (digital gallery)

![cover.jpg](./cover.jpg)

## introduce
The technology stack used in this project is `three.js`, and `blender` is used for modeling. Finally, the scene texture is baked and rendered, and the `glb` map format is exported for rendering on the Web.  
This project is only a demo project of the digital exhibition hall concept. Please forgive me if there are any imperfections. If you have any questions, you can raise an issue.

## How to operate?
Walking: `W`/`S`/`A`/`D`

Mobile walking operation: `virtual joystick`

Jump: `space`

Control perspective: `left mouse button drag`

## Directory structure description
```text
├── src # source code
│ ├── assets # Resource folder (audio, textures, models)
│ │── audio # Audio class (create positional audio)
| │── character # Character class (character model control)
| │── controlManage # Keyboard control class (keyboard button or virtual joystick status management)
| │── core # Core basic classes (including camera, renderer, scene, etc.)
| │── css3DRenderer # Responsible for combining DOM elements with WebGL content (rendering iframe elements on the computer screen)
| │── environment # Scene class (create map model, exhibition map, ground specular reflection)
| │── lib # three.js related extension library
| │── loader # Loader class (glb, texture, audio, etc. loader management)
| │── rayCasterControls # Ray casting class (interaction between character and frame triggers detection)
| │── ui # UI class (responsible for controlling part of the UI of the rendering page, such as loading progress page, details window, virtual joystick)
| │── utils # Utility function
| | │── Emitter.ts # Event distribution class (distribution of various events)
| | └── typeAssert.ts #Type derivation tool function
| │── world # Game core class (used to manage core elements in the game world, including environment, characters, interaction detection, audio and other components)
| │── main.ts # Page entry function
| └── Constants.ts # Constant definition (define model/map/media resource address, distribution event name, etc.)
```

## Personal thoughts on this open source project:
Inspired by the threejs official website demo project, I tried many solutions when developing this project and saw many similar projects. However, most of these projects were sold with clearly marked prices (the layout was too small). In contrast, looking at the github of foreigners On the Internet, there are a large number of excellent 3D open source projects, which is why other people's technology develops so rapidly.
Therefore, I still feel that we should not be stingy about contributing technology, and open up more open source projects to inspire more people and help each other to better promote the development of the industry.

> Open source is not easy, Duoduo Star⭐⭐⭐

## Donate
Open source is not easy, your support is my constant motivation! This project is an open source project and donations are voluntary.
### How to donate?
[Love Power⚡](https://afdian.net/a/twimark)

## 🎇feature：
1. High performance collision detection:
Because there are not many application scenarios for physics engines in this type of project, after unremitting technical solution research, a high-performance dynamic collision detection solution that does not rely on physics engines was used. The performance is several times better than the `Octree` solution on the `three.js` official website.
2. Art exhibition interaction:
Use ray casting for object detection to trigger interactive effects.
3. Location Audio:
Positional audio is added to simulate auditory transmission in reality, making the music in the scene more spatial and improving the browsing experience.

## Run
To setup a dev environment:
```text
# Clone the repository

#Install dependencies
npm i

# Run the local dev server
npm rundev
```
To serve a production build:
```text
# Install dependencies if not already done - 'npi i'

#Build for production
npm run build
```
Send feedback

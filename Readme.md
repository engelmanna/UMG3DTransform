# UMG 3D Transform
This project demos a technique to deform UMG widgets in such a manner that they look like they are rotating in 3D space. 

[Video Demo of Project](https://youtu.be/Rqgipoc6PYE)

I was inspired by the Unrealfest 2022 UMG talk: https://youtu.be/dSTdAToJ7Gg. Specifically about the ability to pan a UMG widget around via the material's ScreenPosition input. I wanted to take it a step further and try to get it working with 3D transforms. After some trial and error, I got it working and created a small demo project to share for others that want to use the functionality as well.

Most of the work is done in the HLSL node within the material. The technique works by getting the vertex's local position, then doing some matrix math to rotate the vertex position around 3D space, and apply some perspective. Then it generates some data into packed UV channels to build perspective corrected UVs.

This project was built in Unreal 5.1. It'll probably work in older versions, but you will need to manually port the assets over.

See more of my work at: https://alexengelmann.com
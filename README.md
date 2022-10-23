
# Godot Engine + Custom Terrain Module
![Kiku](simple_demo/simple_scene.jpg)
Custom Godot Engine Build with Terrain Module

To start testing, download or clone this repo [grab the compiled engine in the release section](https://github.com/ozzr/godot_terrain/tags) and open the project.
## Description
Over the last year I have worked in this project. My idea was to create a Terrain system inside godot that worked under both backends GLES3 - GLES2.
### What you get:
* Full In Editor terrain editor
* Endless Patched terrain
* Complex Biomes Rendering
* AND THE BEST: It works under GLES2 the same way as it does under GLES3 so you can target low end devices ( that was my most important objective all the time )
* More to come ...

### Where are the export templates?
I am releasing the editor for free. The export templates will be available for purchase at a reasonable price soon or if you want to compile the module your self, you can purchase the source code too. 

### Where are the Tutorials?
Tutorials will be available soon. I am working on them.

### Where can I report Issues?
Use this Page. 

# Important!
I am releasing the editor sooner so you can enjoy, or test, I still have some utilities to add and methods to expose to gdscript. Also, you should notice that terrain rendering is not a cheap task, so, target your low end devices wisely.

### Getting Started:
1. Add a Terrain Node into the Scene
2. Save the TerrainData as a separate File (is in the Storage group)
3. Go to the Terrain Menu (it is the Terrain Icon in the top left of the new side bar that appeared in your Spatial Vieport View) and Hit "Bake Globalmap"
4. Decide beforehand what sizes do you want for the textures. Downscaling is fine but when upscaling you get artifacts in the textures and the borders will no longer match. Use with care.
5. The new tool bar has a lot of buttons, hover them to know what they do. At the bottom of the column there are popup buttons: Brush Selector (B), Color Selector (C), Paint Texture Selecttor (T), Biome Selector (I), Simulation Selector (R). Test each one of them.
6. Good luck! I will release a Tutorial Video Soon


# ROADMAP
#### Stage 0
* [X] Add SmartTexture class (I love this class is everywhere in the module)
* [X] Add TerrainRenderer abstract class
  * Add Subrenderers:
    * [X] CDLODRendrerer
* [X] Add Erosion Simulation and Filters
  * [X] Hydraulic Erosion
  * [X] Thermal Erosion
  * [X] Wind Erosion
  * [X] Gaussian Blur Filter
* [X] Add Biomes
  * [X] Add PoissonGenerator and PoissonMixer classes for "pretty" entity placement
  * [X] Add BiomeItem types: DECAL, GRASS, SHRUB, OBJECT, TREE
* [X] Add BiomeRenderer abstract class
  * Add Subrenderers:
    * [X] GridRendrerer
* [X] Overhaul TerrainEditor class
  * [X] Add capability to export the images stored inside the Terrain Data to the file system with acustom .import attatched (Use it before releasing the game. The Terraindata class is really heavy in size and can and will slow down your load times)  
#### Stage 1
* [X] Add a Terrain Material class ( used by the BiomeItems to access each patch texture independently)
* [X] Add Biome Blocker Node
* [X] Add Surface Editor Node ( To edit the shadows heightmap and block biomes with custom meshes
* [ ] Write Documentation
* [ ] Release Initial Tutorials


#### Stage 2
* [ ] Add Surface Regional Texture Proxy ( Just something to read more than one patch texture as one) (Maybe use a viewport?) 
* [ ] Add Navigation
* [ ] Add Path Painter
  * [ ] Add Roads
  * [ ] Add Rivers
* [ ] Update Documentation

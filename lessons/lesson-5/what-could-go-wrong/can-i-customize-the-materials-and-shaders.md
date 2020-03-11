# Can I customize the materials and shaders?

It is possible to replace the material used for either the terrain or the clipping volume wall.

When doing this, it is recommended to make a copy of the base shaders, which are imported as part of the NuGet package under _lib\unity\map\Resources_. Use the copies made of these shaders as the starting point for new materials.

 Importantly, the `ENABLE_ELEVATION_TEXTURE` keyword used by the shaders will need to be maintained. Certain draw calls for the terrain require an elevation texture while others do not.


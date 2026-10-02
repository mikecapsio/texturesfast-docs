# Which PBR Material Tool to Use

TexturesFast generates seamless PBR materials in the browser: Base Color, Normal, Height, Roughness, Metallic, and Ambient Occlusion. You start from a prompt, a reference photo, or a texture you already have. You download bitmap maps and assign them yourself.

The tools people actually weigh against that job are paint apps, node graphs, photo-capture apps, and texture libraries. This page is that choice. It is not a list of 3D mesh generators.

## Quick answer

- Choose **TexturesFast** when you need a tileable map set today, from a sentence, a photo, or an existing albedo, and the material does not have to expose live parameters.
- Choose **Substance 3D Painter** when the texture is unique to one mesh: brushes, masks, decals, and wear placed by hand.
- Choose **Substance 3D Designer** when the material must stay parametric. Scale, wear, and color should be sliders, and the deliverable is often an SBSAR other people can tweak.
- Choose **Substance 3D Sampler** when a photograph is the source of truth and you want desktop filters, channel-by-channel cleanup, and a handoff into the rest of Substance.
- Choose **Poliigon, Poly Haven, or another scan library** when that exact photographed surface is already in the catalog.
- Choose **Blender** (or another DCC) when the material should be a shader you author and keep in the scene file.

A normal production mix is a library or a TexturesFast tile for the repeating surfaces, and Painter for the one asset that cannot tile.

## 1. TexturesFast: bitmap maps from a prompt, a photo, or an existing texture

Website: https://texturesfast.com

- **Text to Material** when you can describe the surface and you have no photo.
- **Extract Material** when a reference photo should become a tileable set. The prompt names which part of the photo to use.
- **Image to Maps** when the color texture already exists and you need Normal, Roughness, Metallic, Height, and Ambient Occlusion. That workflow is 512 or 1K only.

There is no style-preset menu. The look is words in the prompt. Subscriptions export up to 8K. One-time packs export up to 4K. Paid plans include commercial use under the Terms of Service.

Use it for floors, walls, fabrics, ground, trim, and prop materials that repeat. Do not use it for UDIM hero painting, for a material that must change from a slider at runtime, or for creating a 3D model. The mesh is made somewhere else. TexturesFast never opens it.

## 2. Substance 3D Painter: a unique texture on one mesh

Painter is the tool when every mark has to land on a specific asset. Layers, brushes, projection, smart materials, and UDIM support are the point. A detailed asset often takes hours or days.

Use Painter for hero props, decals, story wear, and anything that must be different across one UV layout. Use TexturesFast for the tileable surfaces around that hero. Those maps can also come into Painter as fill layers under the hand-painted pass.

Comparison: [TexturesFast vs Substance 3D Painter](vs/substance-3d-painter.md)

## 3. Substance 3D Designer: a graph, not a finished bitmap

Designer builds a material as a node graph. The output can be a bitmap, and it can be an SBSAR with exposed controls so another artist changes color, wear, or scale without rebuilding the graph. Authoring that graph from nothing takes hours. Tweaking one that already exists is faster. The learning curve is procedural logic, not a prompt box.

Use Designer when:

- The material has to stay editable after delivery.
- A studio shares one SBSAR that adapts across assets.
- You need a pattern that is defined by rules, not by one generated image.

Use TexturesFast when the deliverable is the maps themselves: a specific wood, concrete, metal, or fabric, from a description or a photo, with no graph to maintain. If a generated result later needs to become a parametric library asset, rebuild that one in Designer. Do not pretend a PNG set is an SBSAR.

Comparison: [TexturesFast vs Substance 3D Designer](vs/substance-3d-designer.md)

## 4. Substance 3D Sampler: a photograph, cleaned up by hand

Sampler and TexturesFast Extract Material both start from a photo. Sampler is a desktop capture tool: import the photo, stack filters, adjust channels, and export bitmaps or an SBSAR into Painter or Stager. The published TexturesFast comparison treats Sampler as photo-only. TexturesFast can also generate from text when you have no photo.

Use Sampler when you are already in Substance and you need fine control over the capture, including jobs the TexturesFast page calls out as Sampler's, such as HDR environment capture and multi-angle scanning.

Use Extract Material when you want a tileable PBR set from one photo in the browser, and you will judge it by regenerating rather than by stacking filters. Use a clear, evenly lit photo of one surface. The upload is processed to generate the maps.

Comparison: [TexturesFast vs Substance 3D Sampler](vs/substance-3d-sampler.md)

## 5. Poliigon, Poly Haven, and other libraries: the surface already exists

Poliigon is a paid catalog of photographed PBR materials, with plugins for tools such as Blender and 3ds Max. Poly Haven is a free CC0 library. You search, download, and apply. Nothing new is generated.

Download the library material when it matches. Generate in TexturesFast when it does not: the wrong wear, a client-specified finish, or a stylized surface a photo library does not stock.

Comparisons:

- [TexturesFast vs Poliigon](vs/poliigon.md)
- https://texturesfast.com/vs/poly-haven
- https://texturesfast.com/vs/scan-library-workflows

## 6. Blender and other DCC shader graphs

Blender, Maya, 3ds Max, and Houdini can build the material in the scene. That stays in the file, costs no tokens, and takes as long as the graph takes. TexturesFast is the bitmap you assign inside those same tools when you do not want to author the surface there.

There is no TexturesFast plugin and no add-on. Download PNG maps and connect them to the shader.

- https://texturesfast.com/vs/blender-procedural-materials
- https://texturesfast.com/vs/blender-texture-paint

## How to choose

1. **Do the maps have to tile?**
   TexturesFast, a library, Sampler, or a procedural graph. Painter if the answer is no and the texture belongs to one mesh.

2. **Must someone tweak it later from sliders?**
   Designer, or a shader in the DCC. A TexturesFast download is a fixed image. Another look is another generation.

3. **Is a specific photo the source of truth?**
   Sampler when you need desktop capture control. Extract Material when you want the tileable set from that photo without a filter stack. A library when the same surface is already scanned.

4. **Is the material already in a catalog?**
   Download it. Generate only the gap.

5. **Do you still not have a model?**
   Model it in your DCC. TexturesFast does not create geometry, and these docs do not cover mesh generators.

## Where to start

[Getting started guide](getting-started-guide.md)

Live product: https://texturesfast.com

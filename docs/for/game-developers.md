# TexturesFast for Game Developers

Game environments, modular kits, and prop materials eat time when every surface is painted by hand or hunted down from mixed libraries. TexturesFast is a browser generator for seamless PBR materials: describe the surface, extract it from a photo, or expand a texture you already have, then drop the maps into Unity, Unreal Engine, Godot, or Blender.

It produces materials, not meshes, and not a unique paint job for one UV layout. Hero weapons and characters with hand-placed wear still belong in a paint tool. Floors, walls, ground, trim, and reusable prop surfaces are the job here.

Official page: https://texturesfast.com/for/game-developers

## Where the time goes

- Textures pulled from several free and paid sources rarely share one art direction.
- A Substance round-trip for every material change stalls gameplay work.
- Mid-production art-direction changes mean redoing surfaces that were already finished.
- Solo developers and small teams often have no dedicated material artist.

## What you generate

A full set can include:

- Base Color
- Normal
- Height
- Roughness
- Metallic
- Ambient Occlusion

You can turn maps off. Fewer maps cost fewer tokens.

Resolutions run from 512 to 8K on Starter, Pro, Ultra, and Max. Use 512 or 1K while the prompt is still moving. Use 4K or 8K for surfaces the camera will meet. One-time packs stop at 4K. Image to Maps stops at 1K.

Tiling can be both directions, horizontal only (planks, brick courses), or vertical only.

## A practical game workflow

1. List the surfaces the level actually repeats: ground, wall, metal trim, fabric, sci-fi panel, roof tile.
2. Write one prompt pattern for the game's look and reuse it. Example: "stylized hand-painted stone, warm grey blocks, teal mortar, simplified cracks, readable at mobile scale."
3. There is no style-preset menu. The words in the prompt are the style. Keep them stable across the set so the level feels like one game.
4. Generate at 512 or 1K. Preview the tile in the dashboard.
5. Import into the engine and look at the surface in the real lighting.
6. Regenerate the approved prompts at the resolution that matches draw distance.
7. Paint unique damage, decals, and story wear in your DCC for the few assets that cannot tile.

### Unity

Assign the PNG maps to a URP or HDRP Lit material. Mark the Normal map in the importer. Unity uses Smoothness, so invert Roughness when the material looks too glossy. Height and AO are optional and should respect the frame budget, especially on mobile.

### Unreal Engine

Import the textures, drive them through a master Material, and instance that material per surface. Nanite and Lumen will show a weak Normal and a wrong Roughness at close range, so check hero surfaces at 4K or 8K under the level's lighting. Megascans still covers many photoreal scans. TexturesFast covers the stylized, fictional, and missing finishes those scans do not include.

### Godot

StandardMaterial3D takes albedo, normal, roughness, metallic, height, and AO directly. That is the whole handoff. You stay in the browser for generation and in Godot for the scene.

## Three ways to start

- **Text to Material** when you can describe the surface and you have no photo. This is the default for fictional and stylized games.
- **Extract Material** when you have a photo of real stone, fabric, or metal and you need it to tile. Name the surface in the prompt. Upload only images you are allowed to use.
- **Image to Maps** when an albedo already exists and you need Normal, Roughness, and the rest. The source should already tile. Output is 512 or 1K.

## Tokens and shipping

Each generation spends tokens based on workflow, resolution, and map count. The button shows the cost. A 512 six-map Text to Material set is 21 tokens, which is the estimate behind the pricing page's "materials per month" line. An 8K full set is hundreds of tokens. Test cheap, export expensive.

Paid plans include a commercial-use license under the Terms of Service. You still review maps before they ship, and you still need rights to every prompt and upload.

Public plan names are Starter, Pro, Ultra, and Max, plus one-time packs if you do not want a renewal. Details: https://texturesfast.com/pricing

## What to keep in a paint tool

- Decals, labels, and faction markings
- Unique edge wear on a hero prop
- UDIM sets for film-scale or first-person hero assets
- Anything that must be different on every polygon of one mesh

Generate the tileable family in TexturesFast. Finish the unique asset in Painter, ArmorPaint, Blender, or Photoshop.

## Related pages

- Getting started: [getting started guide](../getting-started-guide.md)
- Unity: https://texturesfast.com/for/unity-developers
- Unreal Engine: https://texturesfast.com/for/unreal-engine-developers
- Godot: https://texturesfast.com/for/godot-engine-developers
- Solo indie: https://texturesfast.com/for/solo-indie-devs
- Versus Painter: [TexturesFast vs Substance 3D Painter](../vs/substance-3d-painter.md)

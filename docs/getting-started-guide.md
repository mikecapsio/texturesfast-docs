# TexturesFast Getting Started Guide

TexturesFast generates seamless PBR materials in the browser. You describe a surface, extract one from a photo, or expand a texture you already have into a full map set. Then you download Base Color, Normal, Height, Roughness, Metallic, and Ambient Occlusion and assign them in your DCC or engine.

TexturesFast does not open a 3D model. Bring your own mesh in Blender, Unity, Unreal Engine, Godot, or another tool, and apply the maps there.

The basic path is:

1. Sign in and confirm you have tokens.
2. Pick a workflow.
3. Describe the material, and upload an image if that workflow needs one.
4. Choose maps, resolution, tiling, and format.
5. Generate, preview, and download.
6. Hook the maps up in the target tool and check them under real lighting.

## Before you start

You need:

- A TexturesFast account.
- Tokens from a subscription, a one-time pack, or a subscriber top-up. The generate button shows the cost before it runs.
- A clear material direction.
- A place to use the maps: Blender, Unity, Unreal Engine, Godot, 3ds Max, Maya, or another PBR tool.

You do not need a UV-unwrapped model inside TexturesFast, a desktop install, or a style-preset pack. Write the look into the prompt.

Plan limits that affect the first session:

- Without a paid plan, resolution stops at 1K.
- Starter, Pro, Ultra, and Max subscriptions go up to 8K.
- One-time packs go up to 4K and the tokens do not expire.
- Image to Maps offers only 512 and 1K.

Current prices and allowances: https://texturesfast.com/pricing and https://texturesfast.com/pricing-packs

## Step 1: Open the workspace

Go to https://texturesfast.com, sign in, and open the texturing dashboard.

You will see three workflows:

- **Text to Material** — a seamless material from a prompt. No upload.
- **Extract Material** — a seamless material from a reference photo, guided by a prompt.
- **Image to Maps** — companion PBR maps from a texture you already have. The source image should already tile.

Pick the workflow before you spend time on settings. Changing workflow changes which uploads and resolutions are available.

## Step 2: Write a useful prompt

Describe the surface, not a vague object.

Include:

- Material
- Color
- Finish (matte, satin, gloss, oiled, brushed)
- Age and wear
- Pattern or grain
- Art direction, written as words in the same prompt

Weak prompt:

> Metal

More useful prompt:

> Brushed stainless steel with fine horizontal grain, soft satin reflections, light edge wear, and darker grime in recessed areas.

For a game environment:

> Stylized hand-painted stone, warm grey blocks, teal mortar, simplified cracks, readable shapes for a mobile fantasy game.

For ArchViz:

> Wide-plank European oak flooring, natural oil finish, subtle grain, warm honey-brown color, light foot-traffic wear.

Keep wording consistent across a family of materials when a level or a room should feel like one set. Prompts accept up to 1,000 characters.

**Prompt expansion** can rewrite a short line into a richer description. Leave it on when you want more detail. Turn it off when the exact words matter.

**Seed** repeats a result when you enter the same number. Leave it empty for a new variation. After a run, copy the last seed if you want the next attempt to start from the same point.

Avoid confidential client names, unreleased titles, and personal data in the prompt unless your own policy allows it.

## Step 3: Upload an image when the workflow needs one

### Extract Material

Upload a photo of the surface you want. JPG, PNG, and WebP are the formats the product describes. Stay inside the size limit shown on the upload control.

Better photos:

- One dominant surface
- Even lighting
- Little blur
- Little perspective distortion
- Enough detail to see grain, weave, or pitting

Write a prompt that points at the region, such as "brick on the wall" or "linen on the chair."

**Strength** balances the photo and the prompt. The default in the UI is 0.75. Lower values stay closer to the photo. Higher values follow the prompt and move away from the photo.

Upload only images you are allowed to process.

### Image to Maps

Upload an existing texture, ideally one that already tiles. This workflow predicts maps from that image. It does not rebuild the color texture into a new design, and it will not remove seams that are already in the file.

Resolution choices here are 512 and 1K.

### Text to Material

Skip the upload. The prompt is the source.

## Step 4: Choose maps, resolution, tiling, and format

### Maps

Select the channels the shader will use:

- Base Color
- Normal
- Height
- Roughness
- Metallic
- Ambient Occlusion

At least one map is required. Turning maps off makes the run cheaper and faster. The dashboard shows the token cost for the maps and resolution you picked.

### Resolution

| Choice | Who can use it | Notes |
| --- | --- | --- |
| 512 | Any signed-in workflow that lists it | Lowest cost. Good for tests. |
| 1K | Any signed-in workflow that lists it | Highest resolution without a paid plan. |
| 2K | Subscriptions and one-time packs | |
| 4K | Subscriptions and one-time packs | Highest resolution on one-time packs. |
| 8K | Starter, Pro, Ultra, and Max only | Highest cost. Use it for hero surfaces. |

Image to Maps stops at 1K.

Generate a direction at 512 or 1K first. Move to 2K, 4K, or 8K after the prompt is right. Higher resolutions cost more tokens. The generate button shows the number.

### Tiling

- **Both** — seamless left-right and top-bottom. Use this for floors, walls, and generic surfaces.
- **Horizontal** — seamless left-right only. Useful for planks and brick courses.
- **Vertical** — seamless top-bottom only.

### Format

Download as PNG, JPEG, or WebP. PNG is lossless and is the right default for Normal and Height. JPEG is smaller and lossy. WebP is smaller and close to lossless.

## Step 5: Generate and preview

Press Generate. The control shows the token cost first.

If generation fails before it finishes, the app states that no tokens were deducted. Typical causes are an empty prompt, a missing image, an unsupported file, a resolution your plan cannot use, or not enough tokens.

When the maps return, inspect them in the viewport, not only as flat thumbnails. Check:

- Whether the tile repeats without an obvious seam
- Whether Normal, Roughness, and Height agree with the color
- Whether the pattern scale feels right for the surface
- Whether metallic areas are actually metal

Height intensity in the viewport is a preview multiplier. It does not rewrite the downloaded Height map.

If the direction is wrong, change the prompt, the photo, the strength, or the seed and run again before you spend tokens on 4K or 8K.

History, when your plan includes it, stays in that browser. Clearing site data or changing machines can remove it. Download anything you need to keep.

## Step 6: Download

Download single maps or a ZIP material pack. Rename files by material and channel before they enter source control, for example `oak_floor_basecolor.png` and `oak_floor_normal.png`.

## Step 7: Import into Blender

On a Principled BSDF:

- Base Color → Base Color
- Normal → a Normal Map node, then Normal. Set the image color space to Non-Color.
- Roughness → Roughness
- Metallic → Metallic
- Height → a Bump node or a displacement setup, with Non-Color on the image
- Ambient Occlusion → a mix or multiply on the color, or leave it unused if the shader does not need it

Set the material to repeat the image in the mapping node when you want the texture to tile across a large surface. Match the tiling mode you generated. A horizontal-only map will show a seam if you repeat it vertically.

## Step 8: Import into Unity

For URP or HDRP:

1. Put the files in `Assets`.
2. Set the Normal texture type to Normal map.
3. Create a Lit material.
4. Assign Base Color to Base Map.
5. Assign the Normal map.
6. Unity's Lit shader uses Smoothness. Invert or remap Roughness if the surface looks glossy when it should be matte.
7. Use Height and AO only when the shader and the frame budget allow them.

Use 512 or 1K for distant and mobile surfaces. Keep 4K and 8K for surfaces the camera will touch.

## Step 9: Import into Unreal Engine

1. Import the PNG files.
2. Create or reuse a master Material.
3. Expose texture parameters.
4. Make a Material Instance per surface.
5. Connect Base Color, Normal, and Roughness.
6. Add Height or AO only where the material features need them.

Check Roughness under the level's lighting. A thumbnail is a poor judge.

The same map assignment works in Godot's StandardMaterial3D: albedo, normal, roughness, metallic, height, and AO slots.

## Step 10: Iterate

1. Test at 512 or 1K.
2. Preview tiling in TexturesFast.
3. Drop the maps into the real scene.
4. Adjust the prompt, photo, strength, or seed.
5. Regenerate the approved look at the resolution the shot needs.
6. Hand-paint hero detail in Blender, Substance, Photoshop, or another editor when a unique mesh needs it.

TexturesFast is the reusable surface. A one-off hero prop with decals, damage masks, and unique wear still belongs in a paint tool. Many teams generate the tileable base here and finish the unique asset elsewhere.

## Common problems

### Generation will not start

Confirm the prompt is filled in. Extract Material needs a reference image. Image to Maps needs a source texture. Check that the resolution is unlocked for your plan.

### Not enough tokens

Lower the resolution, turn off maps you do not need, or wait for the monthly renewal. One-time packs and subscriber top-ups add tokens without changing the plan. Extract Material spends more tokens than Text to Material at the same size.

### Seams

Use tiling mode Both for surfaces that repeat in every direction. Horizontal and Vertical are intentionally open on one axis. On Extract Material, start from a flatter, more evenly lit photo. On Image to Maps, seams in the source remain in the maps.

### The material looks noisy or mushy

Shorten the prompt. Name larger forms. Inspect the surface at the distance it will be seen. Prompt expansion can add detail you did not ask for; turn it off and try the short prompt again.

### Roughness looks inverted in Unity

Unity Lit materials expect Smoothness. Invert the Roughness map in the material or in an image editor.

### A map is missing

It was deselected, or the download used a format that crushed Normal or Height. Re-download those two as PNG.

### History disappeared

History is stored in the browser. Download the ZIP when a material is approved.

## Next steps

- [TexturesFast FAQ](faq.md)
- [TexturesFast for game developers](for/game-developers.md)
- [Which PBR material tool to use](pbr-material-tools.md)
- [TexturesFast for ArchViz professionals](for/archviz-professionals.md)
- Pricing: https://texturesfast.com/pricing
- One-time packs: https://texturesfast.com/pricing-packs
- Privacy FAQ: https://texturesfast.com/faq/are-my-models-and-prompts-kept-private

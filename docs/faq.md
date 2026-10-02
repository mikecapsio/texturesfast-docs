# TexturesFast FAQ

Short answers from the public TexturesFast site: the FAQ, the About page, the pricing pages, the Privacy Policy, and the Terms of Service. If a price or limit here drifts, the live page wins.

- FAQ hub: https://texturesfast.com/faq
- About: https://texturesfast.com/about
- Pricing: https://texturesfast.com/pricing
- One-time packs: https://texturesfast.com/pricing-packs
- Privacy: https://texturesfast.com/privacy
- Terms: https://texturesfast.com/terms

## Product

### What is TexturesFast?

TexturesFast is an AI PBR material generator. It creates seamless texture map sets from a text prompt, a reference photo, or an existing texture image. Paid plans include commercial use of the outputs, subject to the Terms of Service.

It was founded in 2026 by Mike Caps (@mikecaps). The same maker also ships TextureFast, for texturing UV-unwrapped 3D models, and TrimSheetFast, for trim sheets. Those are separate products.

### How does TexturesFast work?

Choose Text to Material, Extract Material, or Image to Maps. Enter a prompt and, when needed, upload a reference photo or a source texture. Select resolution, maps, format, and the other settings in the dashboard. TexturesFast returns seamless PBR materials you can preview and export.

### What is an AI texture generator?

A system that creates texture maps from a prompt, a reference photo, or an existing image, instead of painting every pixel by hand. TexturesFast focuses on seamless PBR materials through the three workflows above.

### What is PBR, and does TexturesFast support it?

Physically based rendering uses maps that describe how a surface responds to light, so the material stays believable when the lighting changes. TexturesFast can output Base Color (albedo), Normal, Height, Roughness, Metallic, and Ambient Occlusion. You assign those files to the matching channels in Unity, Unreal Engine, Blender, Godot, and other PBR tools.

### What is an albedo, base color, or diffuse map?

The color of the material without baked lighting or shine. It is the foundation of the set. Roughness, Normal, and the other maps describe response and relief around that color.

### What workflows are available?

- **Text to Material.** A prompt becomes a tileable PBR set. No image.
- **Extract Material.** A reference photo becomes a tileable PBR material. The prompt names the surface in the photo.
- **Image to Maps.** An existing texture gains companion maps. The source should already be tileable. Resolution is 512 or 1K.

### Does TexturesFast generate 3D models?

No. It generates materials. You apply them to models you already have.

### Is TexturesFast the same as TextureFast?

No. TextureFast textures a specific UV-unwrapped model and keeps that model in the browser. TexturesFast never takes a mesh. It exports standalone tileable maps.

### Is TexturesFast friendly for beginners?

The workspace is a browser dashboard: pick a workflow, describe the surface or upload an image, generate, and download. You do not need a node graph or a paint app to get a first material. You still need to know which map goes into which slot in your engine.

### Who is it for?

Game developers, 3D artists, technical artists, interior designers, ArchViz teams, product designers, and people making personal or freelance work who need materials faster than a manual paint pass. Role pages live at https://texturesfast.com/for.

### Does TexturesFast have style presets?

No separate preset menu in the current dashboard. Put the style in the prompt: photoreal, stylized, handpainted, pixel art, weathered, clean sci-fi, and similar words. Reference images, resolution, map selection, prompt expansion, and seed are the other controls.

### Can generated textures contain problems?

Yes. Vague prompts, a poor photo, or a resolution that does not match the shot can produce seams, odd detail, or a roughness response that looks wrong in-engine. Generation is fast enough that the usual fix is a tighter prompt or a clearer photo, then another run. The Terms describe outputs as provided as-is. Review them before production use.

### What resolution are the textures?

The UI offers 512, 1K, 2K, 4K, and 8K (8192×8192).

- No paid plan: up to 1K.
- Subscriptions (Starter, Pro, Ultra, Max): up to 8K.
- One-time packs: up to 4K.
- Image to Maps: 512 and 1K only.

PNG export is the recommended format when you need lossless Normal and Height maps. JPEG and WebP are also available.

### How do I get Normal or Roughness maps?

Select those maps before you generate. Base Color can be generated alone, and the other channels can be added in the same run. Deselecting a map reduces the token cost.

## Using the maps

### How do I export into 3D software?

Download PNG files (or JPEG or WebP), import them, and assign each file to the matching material channel. A ZIP pack is available from the dashboard.

### Can I use TexturesFast with Blender?

Yes. Generate the maps, then connect them to a Principled BSDF: Base Color, Normal (through a Normal Map node, Non-Color), Roughness, Metallic, and Height or AO if you need them. There is no TexturesFast Blender add-on. The Blender add-on belongs to TextureFast, the other product.

### Can I use it with Unity or Unreal Engine?

Yes. The maps are standard images. Unity URP/HDRP and Unreal accept them. Unity's Lit shader uses Smoothness, so you may need to invert Roughness. No extra file conversion is required beyond the usual texture import settings, such as marking the Normal map.

### How do I create materials for games?

Decide the surface: stone, wood, metal, fabric, ground, wall, or a reusable prop material. Use Text to Material for a prompt, Extract Material for a photo, or Image to Maps for a texture you already have. Export the channels your shader uses and assign them in Unity, Unreal, Godot, or Blender. Check the result under the game's lighting before you ship it. Unique hero damage and decals still belong in a paint tool.

### Is TexturesFast a fit for game developers?

Yes, for environment surfaces, modular kits, and prop materials that can tile. It is a weak fit when every texel on one mesh must be painted by hand.

### Is TexturesFast a fit for architects and ArchViz?

Yes, for wood, stone, metal, fabric, concrete, tile, and wall finishes. Export the maps into Blender, 3ds Max, Revit, V-Ray, Corona, Lumion, Enscape, or a similar tool, and regenerate when a client changes the finish. Upload only reference photos you are allowed to process.

## Plans, tokens, and billing

### How do tokens work?

Each generation spends tokens. The cost depends on the workflow, the resolution, and the number of maps. The dashboard shows the number before you generate. Subscription allowances renew on the billing cycle. One-time pack tokens do not expire.

A public estimate on the pricing page treats one full 512 Text to Material set (six maps) as 21 tokens. Extract Material and higher resolutions cost more, so you will get fewer materials than that headline number if you work at 4K or 8K.

### What are the plans?

Public subscription names:

- Starter — $39 / month, or $19 / month billed yearly ($229 / year), 1,500 tokens
- Pro — $99 / month, or $49 / month billed yearly ($599 / year), 4,000 tokens
- Ultra — $299 / month, or $149 / month billed yearly ($1,799 / year), 13,000 tokens
- Max — $699 / month, or $349 / month billed yearly ($4,199 / year), 32,000 tokens

All four include the three workflows, full map generation, history, commercial use, and up to 8K. Confirm the live table at https://texturesfast.com/pricing.

One-time packs start at $19, cap resolution at 4K, and do not renew: https://texturesfast.com/pricing-packs

Subscribers can buy extra token packs in account settings. Enterprise volume is requested through the contact form.

### Can I use the textures commercially?

Yes. Textures generated on paid plans include a commercial license. The public FAQ names games, films, ads, and other commercial projects. You still need rights to your prompts and uploads, and you still need to review the output. Read the Terms before you ship client work.

### Does TexturesFast support teams?

Business-scale use is the Max plan (higher token allowance, priority support, WhatsApp) plus the commercial license that all paid plans include. Custom or enterprise needs go through the contact form. There is no separate onboarding call for Starter, Pro, Ultra, or Max.

### Is payment secure?

Payments run through a third-party processor. TexturesFast does not store card details. Public FAQ copy says cards include Visa, Mastercard, and American Express, plus other methods the checkout offers.

### How do I cancel?

Log in, open Settings, and cancel from the subscription controls. You do not need to email support to stop a monthly plan. One-time packs have no renewal.

### What is the refund policy?

The Terms say refund requests are reviewed case by case and should be submitted within 14 days of purchase. Refunds may be refused for fraud or abuse. Because the product is digital, the Terms also say the right to cancel can end once generation, token use, or a download starts.

### Is TexturesFast available in my country?

The app is on the web. Whether checkout works depends on your region and the payment provider. If you can open the site and finish sign-up, you can use the product.

## Privacy

### Are my prompts and uploads kept private?

They are processed to create the maps you asked for. Reference photos and source textures are uploaded only for Extract Material and Image to Maps. Generated maps return to your browser for preview, download, and optional browser-local history.

Public policy says TexturesFast does not sell prompts, uploads, generated maps, or account data, and does not build advertising profiles from them. It does not store your card. It does not claim ownership of your prompts, uploads, or maps. Other users cannot open your private generations.

A prompt still has to be processed, and an image workflow still uploads the image. Do not put confidential names in a prompt unless your own rules allow it.

### Does my 3D model get uploaded?

TexturesFast does not take a 3D model. If you need the mesh to stay on your machine while a tool paints its UVs, look at TextureFast, not TexturesFast.

### What does "NDA-safe" on the pricing page mean?

It is the public label for the commitments above: no sale of creative inputs, no advertising profiles, no card storage, no ownership claim. It is not a promise that generation happens entirely offline. Read https://texturesfast.com/privacy and your contract.

### Who owns the output?

You retain ownership of your prompts, uploaded images, generated maps, and downloaded packs. You grant TexturesFast a limited license to process them so the service can run.

## Comparisons

### Is TexturesFast better than Substance 3D Painter?

They do different jobs. Painter is for pixel-level control on a specific mesh, and that work takes time. TexturesFast is for a tileable PBR set from a sentence or a photo, in a browser, without a paint session. Use TexturesFast for environments, prototypes, and material libraries. Use Painter when the hero asset needs brushes, masks, and decals.

Full comparison: https://texturesfast.com/vs/substance-3d-painter

### How does TexturesFast compare with Quixel Mixer?

Mixer blended existing material layers by hand. TexturesFast generates materials from a prompt or a photo. Mixer is a legacy tool. Use it only if you still maintain an older project built on it.

### How is this different from manual texturing?

Manual texturing in Painter, Photoshop, or a node graph gives you direct control and costs hours. TexturesFast trades that control for speed on reusable surfaces. Keep the manual pass for hero assets.

### How does TexturesFast compare with a texture library?

Poliigon, Poly Haven, and similar catalogs give you an existing scan or photo material. TexturesFast generates a surface from a description, including looks those libraries do not stock. Many teams use both.

## Support

### How do I contact TexturesFast?

Email team@texturesfast.com, message @texturesfast on X, or use the contact form at https://texturesfast.com/contact. Public copy says support email is typically answered within 24 hours.

Starter and Pro include email support. Ultra adds priority email. Max adds priority support and WhatsApp.

### Why did generation fail?

Common causes: not enough tokens, a missing prompt, a missing image, an unsupported file, a resolution above your plan, a content-policy block, a temporary outage, or an upload over the limit shown in the UI. If the run fails before completion, the UI says no tokens were deducted. The error panel includes a code you can send to support.

### How do I get better results?

Use a specific prompt, a clear photo of one surface, and a resolution that matches the shot. Turn prompt expansion off when you need your exact wording. Review the maps in the renderer you will ship, then regenerate.

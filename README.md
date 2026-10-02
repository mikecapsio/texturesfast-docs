# TexturesFast Public Documentation

TexturesFast is a browser-based AI generator for seamless PBR materials. Describe a surface, extract one from a reference photo, or turn an existing texture into companion maps. Preview the material, then download Base Color, Normal, Height, Roughness, Metallic, and Ambient Occlusion for game, visualization, and design work.

TexturesFast makes tileable materials you apply to models you already have. It does not build 3D meshes, and it does not paint a unique texture onto one model's UV layout.

A related product from the same maker, [TextureFast](https://texturefast.com), textures UV-unwrapped 3D models. [TrimSheetFast](https://trimsheetfast.com) covers trim sheets. This repository is only about TexturesFast.

## Documentation

- [Which PBR material tool to use](docs/pbr-material-tools.md)
- [Getting started guide](docs/getting-started-guide.md)
- [Frequently asked questions](docs/faq.md)
- [TexturesFast for game developers](docs/for/game-developers.md)
- [TexturesFast for ArchViz professionals](docs/for/archviz-professionals.md)
- [TexturesFast vs Substance 3D Painter](docs/vs/substance-3d-painter.md)
- [TexturesFast vs Substance 3D Designer](docs/vs/substance-3d-designer.md)
- [TexturesFast vs Substance 3D Sampler](docs/vs/substance-3d-sampler.md)
- [TexturesFast vs Poliigon](docs/vs/poliigon.md)

## At a glance

- Open the dashboard in the browser. There is no desktop install.
- Choose one of three workflows: Text to Material, Extract Material, or Image to Maps.
- Describe the surface in plain language. Style lives in the prompt (photoreal, stylized, handpainted, weathered, and similar words). There is no separate style-preset menu.
- For Extract Material, upload a reference photo and tell the generator which surface to use.
- For Image to Maps, upload a texture you already have and generate the missing PBR channels. That workflow is limited to 512 and 1K.
- Select which maps to generate. Fewer maps cost fewer tokens.
- Choose a resolution from 512 through 8K. Every subscription plan can export up to 8K. One-time packs stop at 4K. Accounts without a paid plan stop at 1K.
- Set tiling to both directions, horizontal only, or vertical only.
- Preview the material on a 3D surface in the browser, then download maps or a ZIP pack as PNG, JPEG, or WebP. PNG is the safer choice for Normal and Height.
- Assign the maps in Blender, Unity, Unreal Engine, Godot, and other tools that accept standard PBR channels.
- Paid plans include a commercial-use license, subject to the Terms of Service.

## Current map and resolution notes

A full set can include:

- Base Color / Albedo
- Normal
- Height
- Roughness
- Metallic
- Ambient Occlusion

Subscription plans (Starter, Pro, Ultra, and Max) unlock resolutions up to 8K (8192×8192). One-time token packs unlock up to 4K. Image to Maps stays at 512 or 1K because that workflow does not upscale.

Token cost depends on the workflow, the resolution, and how many maps you select. The dashboard shows the cost before you generate. The public "materials per month" figures on the pricing page are estimates for a 512 Text to Material set with all six maps (21 tokens). Extract Material and higher resolutions use more tokens, so the real count is lower.

Check the live product UI if a control, limit, or price looks different from this file.

## Privacy and commercial-use notes

Generation processes the prompt, the settings you choose, and an image only when the workflow needs one. Extract Material and Image to Maps upload that image. Text to Material does not. Generated maps come back to the browser for preview, download, and optional browser-local history.

Public legal copy says TexturesFast does not sell prompts, uploaded images, generated maps, or account data, and does not build advertising profiles from that content. TexturesFast does not store payment card details and does not claim ownership of your prompts, uploads, or generated maps.

Pricing labels paid plans NDA-safe. That label matches those public commitments. It does not mean a prompt or reference image never leaves your browser. Keep confidential names out of prompts, and upload only images you are allowed to process. Read the Privacy Policy and your own contract before you put client material into a prompt or an upload.

You keep ownership of prompts, uploads, and generated outputs. Paid plans add a commercial-use license for those outputs, subject to the Terms of Service. Review every map in the target renderer before you ship it. AI output can contain seams, odd detail, or lighting that does not match the scene.

## Pricing snapshot

These figures match the current product source. The live pricing pages override them if they change.

Monthly subscriptions, also available yearly at a lower monthly rate:

| Plan | Monthly | Yearly rate | Yearly total | Tokens / month | About this many 512 full sets |
| --- | --- | --- | --- | --- | --- |
| Starter | $39 | $19 / month | $229 | 1,500 | 71 |
| Pro | $99 | $49 / month | $599 | 4,000 | 190 |
| Ultra | $299 | $149 / month | $1,799 | 13,000 | 619 |
| Max | $699 | $349 / month | $4,199 | 32,000 | 1,523 |

All four include the three workflows, full map generation, history, commercial use, and up to 8K. Starter and Pro include email support. Ultra adds priority email. Max adds priority support and WhatsApp.

One-time packs have no renewal. The tokens do not expire, and the resolution cap is 4K:

| Pack | Price | Tokens | About this many 512 full sets |
| --- | --- | --- | --- |
| Starter | $19 | 500 | 23 |
| Pro | $39 | 1,000 | 47 |
| Ultra | $49 | 2,000 | 95 |

Subscribers can also buy extra token packs in account settings. Current packs are 500 tokens for $15, 1,000 for $25, 2,500 for $55, and 5,000 for $100. Enterprise volume is arranged through the contact form, not self-serve checkout.

Cancel a subscription anytime from Settings. One-time packs have nothing to cancel.

## Official sources

- Website: https://texturesfast.com
- About: https://texturesfast.com/about
- FAQ: https://texturesfast.com/faq
- Pricing: https://texturesfast.com/pricing
- One-time packs: https://texturesfast.com/pricing-packs
- Comparisons: https://texturesfast.com/vs
- Workflows by role: https://texturesfast.com/for
- Public product guide: https://texturesfast.com/llms.txt
- Privacy Policy: https://texturesfast.com/privacy
- Terms of Service: https://texturesfast.com/terms
- Contact: https://texturesfast.com/contact
- Support email: team@texturesfast.com

The live TexturesFast website is authoritative for current pricing, plan access, feature availability, file limits, and legal terms.

## How to publish this folder

Copy the contents of this folder into an empty public repository. Keep this layout:

- `README.md` at the repository root
- `llms.txt` at the repository root
- `docs/` for the guides, role pages, and comparisons

Do not commit `.env` files, credentials, or anything from the TexturesFast application repository. This folder is public product copy only.

# TexturesFast for ArchViz Professionals

Architectural visualization needs specific finishes: a honed stone, a particular brick bond, a wood floor with the right oil and wear. Stock libraries cover many of those surfaces and miss the one the client just described. Photographing a sample and building PBR maps by hand is the slow path.

TexturesFast generates a seamless PBR set from a written description or from a reference photo, then you assign the PNG maps in the renderer you already use.

Official page: https://texturesfast.com/for/archviz-professionals

## Where the time goes

- The catalog rarely has the exact veining, aggregate, or bond the drawing calls for.
- Turning a site photo into tileable albedo, normal, and roughness maps is a manual job on every surface.
- Clients change finishes late. The schedule does not grow with them.

## What you get

Maps you can assign in 3ds Max, Blender, Revit, V-Ray, Corona, D5 Render, Lumion, Enscape, and other tools that accept standard PBR images:

- Base Color
- Normal
- Height
- Roughness
- Metallic
- Ambient Occlusion

Subscriptions export up to 8K, which is the range that holds up when a camera moves close to a facade or a floor. One-time packs stop at 4K. Test the prompt at 1K before you spend an 8K generation.

Tiling mode **Both** is the default for floors and walls that repeat in every direction. Use **Horizontal** when a plank or brick course should seam only on the long axis.

## A practical ArchViz workflow

1. Name the finish the way you would brief a library search: "honed Carrara marble, soft grey veining, low sheen" or "exposed aggregate concrete, warm grey, fine pits."
2. If you have a photo of the real material, use **Extract Material**. Point the prompt at the surface in the frame. Prefer an evenly lit photo of one material, with little perspective. A phone snapshot can work. A blurry, mixed-material photo usually will not.
3. If you have no photo, use **Text to Material** and put finish, color, and wear in the sentence.
4. Preview the tile in the browser. Look for a seam and for a roughness level that matches the spec (honed, matte, oiled, gloss).
5. Download PNG maps. Keep Normal and Height as PNG.
6. Assign them in the renderer and adjust scale in the material, not by regenerating, when the only issue is texel size.
7. When the client swaps the finish, change the prompt or the photo and generate again.

Interior presentation work follows the same steps for herringbone oak, bouclé, honed quartz, and painted plaster. Product visualization uses it for plastics, brushed metal, and leather when the material is a repeating surface on the model. Those role pages:

- https://texturesfast.com/for/interior-designers
- https://texturesfast.com/for/product-designers
- https://texturesfast.com/for/real-estate-visualization

## Photos and client material

Extract Material uploads the photo so the material can be generated. Upload only images you are allowed to process. Keep project names, client names, and unreleased addresses out of the prompt unless your contract allows it.

Public policy says TexturesFast does not sell prompts, uploads, or generated maps, and does not build advertising profiles from them. The pricing page labels paid plans NDA-safe on that basis. Read the Privacy Policy and the client agreement before you upload a site photo: https://texturesfast.com/privacy

## Libraries still matter

Poliigon and similar catalogs are the right first stop when the exact photographic material is already in the library and the plugin import saves time. TexturesFast is the path when the library is close but wrong: different wear, a stylized presentation, or a finish the client described and nobody has scanned.

Comparison: [TexturesFast vs Poliigon](../vs/poliigon.md)

## Commercial use and review

Paid plans include a commercial-use license under the Terms of Service. You still look at the material in the final lighting. Marble veining, roughness, and repeat scale are the usual things to correct with another prompt or a small edit in the renderer. AI output is provided as-is.

## Related pages

- Getting started: [getting started guide](../getting-started-guide.md)
- FAQ: [faq.md](../faq.md)
- Pricing: https://texturesfast.com/pricing
- Versus scan libraries: https://texturesfast.com/vs/scan-library-workflows

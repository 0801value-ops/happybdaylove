# Fondos mejorados

## Versiones finales proporcionadas por el usuario

Se sustituyeron únicamente us girls version y 10 Things I Hate About You por las dos imágenes mejoradas que el usuario entregó. Los PNG exactos se conservan como bubbles-user.png y 10-things-user.png. La web usa bubbles-user.jpg y 10-things-user.jpg, conversiones de alta calidad sin recorte ni reescalado (`ffmpeg -frames:v 1 -q:v 2`). Estas versiones reemplazan las mejoras tradicionales anteriores descritas abajo. El resto de la página no cambió.

## Última actualización: los dos fondos pendientes

El usuario autorizó explícitamente mejorar sin IA us girls version (bubbles) y 10 Things I Hate About You tras los rechazos de imagegen. Ahora los 15 fondos tienen una versión mejorada: 13 mediante reconstrucción con IA y estos dos con procesamiento tradicional.

Archivos guardados aquí: bubbles-enhanced.png, bubbles-enhanced.jpg, 10-things-enhanced.png y 10-things-enhanced.jpg. Los originales bubbles.jpeg y 10-things.jpeg siguen intactos.

Método: FFmpeg, reescalado Lanczos a 1920 píxeles de ancho manteniendo la proporción y nitidez suave. Filtro exacto: `scale=1920:-2:flags=lanczos,unsharp=5:5:0.35:3:3:0`. Maestro PNG sin pérdidas; versión JPG con `-q:v 2`. Este procedimiento suaviza el escalado, pero no inventa ni recupera detalle que no esté en el original. El exportador web conserva versiones optimizadas de hasta 1600 píxeles de ancho para respetar el límite de tamaño.

Los apartados siguientes documentan el proceso anterior.

## Actualización: fondos restantes

Se usó la herramienta integrada imagegen en modo edición, una solicitud por imagen. Se conservaron los originales. Las reconstrucciones con IA pueden variar ligeramente en detalles; no son una recuperación exacta de píxeles originales.

Nuevos archivos guardados en esta carpeta, cada uno con maestro PNG y versión JPG de alta calidad para la web:

- mixed-media-enhanced
- strawberry-garden-enhanced
- tommy-enhanced
- secretary-enhanced
- starry-night-enhanced
- silence-of-the-lambs-enhanced
- love-story-enhanced
- frankenstein-enhanced
- kittens-enhanced
- together-enhanced
- eternal-sunshine-enhanced

En total hay 13 de 15 fondos mejorados, contando Kamisama Kiss y Polka dots. La herramienta rechazó las solicitudes de Burbujitas y 10 Things I Hate About You; para esos dos fondos se mantienen los originales. No se intentó el modo CLI/API, que requiere una clave OPENAI_API_KEY y autorización explícita para ese modo.

Prompt común usado en las once nuevas mejoras y las dos solicitudes rechazadas:

> Use case: identity-preserve. Asset type: existing website wallpaper restoration. Input image is the exact edit target. Restore this same image at higher resolution, around 1800 pixels wide, preserving its original aspect ratio and full uncropped composition. Improve clarity, reduce JPEG blocks and jagged edges, gently recover detail. Preserve all faces, identities, poses, objects, lighting, original colors, film grain/artistic textures and existing handwriting, captions, doodles and overlays exactly. Do not redraw or beautify faces, invent details, add text, remove elements or change the style. The result should look like a cleaner higher-resolution copy of this precise original, not a reinterpretation.

## Primeras dos mejoras

Herramienta utilizada: generación/edición de imágenes integrada (imagegen). Versiones PNG de 1672 × 941; originales JPEG conservados. Son reconstrucciones con IA y pueden variar ligeramente respecto del original.

## kamisama-kiss-enhanced.png

Prompt: Faithful restoration and upscaling of this exact anime wallpaper. Preserve the original composition, character faces and expressions, framing, pastel colors, flowers, every existing Japanese and English letter on the sign verbatim. Remove JPEG artifacts, improve clarity of linework, smooth jagged edges without changing the artwork or adding anything. Landscape 16:9 high resolution, ideally 2048x1152 or larger. Input is edit target, not loose inspiration.

## polka-dots-enhanced.png

Prompt: Restore and upscale this exact pale blush pink wallpaper with tiny dark brown/black polka dots. Clean flat pale blush background, crisp evenly spaced tiny circular dots in the same staggered rows and same density as reference. Preserve color, scale and layout; remove compression and jagged edges, no texture or gradient, no text or decorations. Landscape 16:9, high resolution ideally 2048x1152 or larger. Input is edit target.

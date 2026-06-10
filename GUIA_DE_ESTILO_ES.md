# Guía de estilo — Traducción al español de Umineko Catbox

Referencia única para mantener coherencia a lo largo de ~72.800 líneas, a través de muchas sesiones.
Basada en las decisiones de la **localización oficial inglesa** (The Witch Hunt / MangaGamer), única localización oficial existente (no hay oficial en español).

## 1. Honoríficos: SE MANTIENEN
Se conservan tal cual, como en la versión oficial inglesa y como ya aparecen en el script:
`-san`, `-kun`, `-chan`, `-sama`, `nii-san`, `nee-san`, `aniki`, `oji-san`, `oba-san`, etc.
- Ejemplos del propio juego: "George nii-saaan", "Battler-kun", "aniki".
- Razón: codifican dinámicas de relación y jerarquía sin equivalente limpio en español.

## 2. Nombres propios y términos: FORMA ORIGINAL
No se adaptan fonéticamente.
- Personajes: **Battler, Beatrice, Kinzo, Jessica, George, Maria, Rosa, Eva, Hideyoshi, Rudolf, Krauss, Natsuhi, Genji, Shannon, Kanon, Kumasawa, Gohda, Nanjo, Rena (no), …** (se escriben como en inglés).
- Conceptos clave:
  - **verdad roja** (red truth) — el texto en rojo `@c900.` que es siempre verdad. *Nunca* alterar la precisión lógica de estas frases.
  - **verdad dorada** / **verdad azul**.
  - **Bruja** (Witch), **Maestra del juego** / **Game Master**, **epitafio** (epitaph), **culado/sacrificio** según contexto.
  - "And so on, and so forth." de Lambdadelta, "uu~" de Maria, etc. → mantener tics característicos.

## 3. Tratamiento (tú / usted)
El inglés no distingue, así que decidimos por jerarquía interna:
- **tú** por defecto: entre primos (Battler, George, Jessica, Maria), entre hermanos adultos, entre iguales.
- **usted**: sirvientes hacia la familia Ushiromiya y hacia Kinzo (Genji, Shannon, Kanon, Kumasawa, Gohda, Nanjo cuando corresponde). También hacia Beatrice/figuras de autoridad según la escena.
- Beatrice ↔ Battler: el "tú" desafiante encaja con su dinámica de duelo.

## 4. Voz de cada personaje (consistencia de tono)
- **Battler**: desenfadado, descarado, coloquial. Usa muletillas, bromea.
- **Kinzo**: solemne, arcaico, grandilocuente, obsesivo con Beatrice.
- **Maria**: habla infantil, "uu~", repeticiones, inocente pero inquietante.
- **Beatrice**: teatral, altiva, cruel-juguetona; se ríe ("Ufufu", "Kihihi").
- **Natsuhi**: formal, tensa, orgullosa.
- **Rosa / Eva**: adultas, a veces cortantes.
- **Sirvientes (Shannon, Kanon)**: corteses, formales pero con calidez juvenil.

## 5. Reglas técnicas de escritura (recordatorio)
- Escribir acentos **naturales** (`á é í ó ú ü ñ ¿ ¡`); el build los convierte.
- Apóstrofo en `.rb`: escapar con `\'`.
- No tocar etiquetas `@r @k @w @v… @c… @z… @{ @} @| @y`. Misma cantidad y posición.
- Abrir signos de apertura en español: `¿…?` y `¡…!` (ya soportados).
- Comillas de diálogo: mantener las `"…"` rectas que usa el script (no cambiar por « » salvo decisión explícita).

## 6. Decisiones pendientes (anotar aquí cuando surjan)
- (Se irán registrando dudas resueltas: términos del epitafio, juegos de palabras, nombres de hechizos, etc.)

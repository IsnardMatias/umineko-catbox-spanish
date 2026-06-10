# Proyecto: Traducción al español de Umineko Catbox (Saku)

Fork de `Lovahi/umineko-catbox-spanish`, a su vez basado en `Foxdear/umineko-catbox-X-english`.
Objetivo: traducir al español el port de consola **Umineko no Naku Koro ni Saku** (Switch / Entergram).
Fork del usuario: `IsnardMatias/umineko-catbox-spanish`.

## Estado de la traducción
- El guión está casi **sin traducir**: solo el prólogo (aprox. líneas 18474–18626 de `script.rb`) está en español.
- **Primera línea pendiente: `script.rb` línea 18668** (escena del avión, Battler). De ahí hacia abajo, todo en inglés.
- Total: ~72.800 líneas de diálogo en EP1–8 + Tsubasa + Hane + Saku + extras.

## Dónde vive el texto
- `script.rb` — guión principal (464.540 líneas, **incluye datos binarios incrustados**; editar SOLO con VS Code / herramientas que preserven los bytes NUL).
- `exefs_texts.txt` — texto de interfaz incrustado en el ejecutable (TSV: offset⟶inglés⟶japonés). Solo editar la columna inglesa. Límite duro: la traducción debe ocupar **≤ bytes UTF-8** que el japonés original o el reemplazo falla.
- Imágenes con texto (`.txa`/`.pic`) en `romfs/` — se editan con `repack/enter_extractor` (las `.txa` se guardan con paleta de 256 colores).

## Reglas de edición de `script.rb` (INNEGOCIABLES)
Solo se traduce el texto visible dentro de `s.layout('...')`, en líneas que empiezan con `s.ins 0x86`. Todo lo demás se deja idéntico.
- **Acentos: escribir en español natural** (`á é í ó ú ü ñ ¿ ¡`). El build ejecuta `node replace_chars.js` que los convierte a `@u<código>.` automáticamente. NO escribir las etiquetas `@u` a mano. (Las líneas ya traducidas las tienen "crudas" porque ya se les pasó el script; es indiferente.)
- **Apóstrofo: se escapa con barra `\'`** (es un .rb). Ej: `can't` → `can\'t`. En español casi no aplica.
- **NO tocar las etiquetas `@`:**
  - `@r` = salto de línea (separa nombre de personaje del diálogo)
  - `@k` = espera clic · `@w500.` = pausa (500 ms) · `@e` = termina línea sin clic (deben ser los 2 últimos caracteres)
  - `@t` = texto antes y después aparece a la vez (personajes hablando encima)
  - `@v10/10100001.` = voz (apunta a `voice/10/10100001.nxa` — dejar EXACTO, no mover ni borrar)
  - `@c900.` = color rojo ("verdad roja", crítica en Umineko; código RGB decimal 000=negro…999=blanco) · `@c.` = blanco · `@z70.` = tamaño fuente (100=normal) · `@{...@}` = negrita · `@[...@]` = mostrar al instante
  - `@btexto.@<...@>` = furigana. **⚠️ NO funciona con caracteres especiales (acentos): en español usar paréntesis en su lugar.**
  - **`@|` y `@y` ejecutan código externo (efectos/sprites). Conservar misma CANTIDAD y POSICIÓN que el original o el juego se rompe.**

## Pruebas (testing)
- Forma rápida: en el juego, elegir el Episodio → abrir el backlog con el botón **X** → saltar a las líneas cambiadas y revisarlas.
- ⚠️ Un error en el script puede **borrar por completo las partidas guardadas**. Hacer copias de seguridad de los saves.

### Ejemplo de línea traducida (mecánica)
Original (línea 18668):
```
s.ins 0x86, ushort(163), byte(0), byte(1), s.layout('Battler@r@v10/10100001."Whoa...@k@v10/10100002. Things sure move with the times..."')
```
Traducida (solo cambia el texto entre comillas; esqueleto idéntico):
```
s.ins 0x86, ushort(163), byte(0), byte(1), s.layout('Battler@r@v10/10100001."Guau...@k@v10/10100002. Cómo cambian los tiempos..."')
```

## Compilación
- **Recomendado: GitHub Actions.** Cada `push` dispara `.github/workflows/test.yml` (build de prueba). `release.yml` genera releases. Si fallan los release: Settings → Actions → General → Workflow Permissions → "Read & Write".
- Local: necesita Linux/WSL con Python 3.8+, Ruby 2.7+, Node, zip → `./build.sh`. En Windows hay `build.bat` / `docker_build.bat`.
- `build.sh` línea 11 corre `node replace_chars.js` (in-place) antes de empaquetar. Es idempotente.

## Criterio de traducción
Ver `GUIA_DE_ESTILO_ES.md`. Resumen: **mantener honoríficos** (-san, -kun, nii-san, aniki…) y **nombres originales** (Battler, Beatrice, Kinzo…), como hizo la localización oficial inglesa (Witch Hunt / MangaGamer). Tratamiento **tú** por defecto, **usted** según jerarquía (sirvientes → familia Ushiromiya y Kinzo).

## Flujo de trabajo con Claude
Traducir por tramos (escena a escena, 20–50 líneas). Avanzar en orden desde la línea 18668 hacia abajo. Mantener coherencia con el glosario de la guía de estilo.

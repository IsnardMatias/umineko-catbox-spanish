# Progreso de la traducción al español

Traducción al español del parche de **Umineko no Naku Koro ni Saku ~Nekobako to Musou no Koukyoukyoku~** (port de consola, Entergram).
Basada en el proyecto inglés de [andOlga / umineko-catbox-english](https://andolga.github.io/umineko-catbox-english) (enlace canónico) y en el fork de Lovahi.

> **Estado general:** 🟡 En curso — fase inicial. La infraestructura, el build automático y los menús del sistema están listos; la traducción del guion principal está empezando.

_Última actualización: 2026-06-09_

**Avance EP1:** ✅ **COMPLETO** (~7.460 líneas, 100%). Episodio 1 "Leyenda de la Bruja Dorada" totalmente traducido al español. Próximo: EP2 (desde línea 48132).

---

## Resumen rápido

| Parte | Estado | Detalle |
|---|---|---|
| Infraestructura / build (GitHub Actions) | ✅ Listo | Compila y genera parche descargable |
| Caracteres del español (acentos, ¿ ¡) | ✅ Listo | Renderizan correctamente en el juego |
| Menús y mensajes del sistema (guardar, cargar, config, Sí/No…) | ✅ ~Completo | Falta solo algún término menor |
| **Guion — Episodio 1** | ✅ Completo | Episodio 1 entero traducido (~7.460 líneas) |
| Guion — Episodios 2–8 | ⬜ Pendiente | — |
| Tsubasa / Hane / contenido extra de Saku | ⬜ Pendiente | — |
| Juego de deducción de Bernkastel (EP8, texto de exefs) | ⬜ Pendiente | 1 de ~34 bloques |
| Imágenes con texto (logos, botones) | ⬜ Pendiente | — |

## Detalle del guion (script.rb)

Total de líneas de diálogo del juego: **~72.850**.

| Episodio | Rango aprox. | Estado | Líneas traducidas |
|---|---|---|---|
| EP1 — Leyenda de la Bruja Dorada | 18434–48131 | ✅ Completo | Episodio entero traducido (prólogo → fiesta del té de Beatrice → Bernkastel) |
| EP2–EP8 | — | ⬜ Pendiente | 0 |
| Extras (Tsubasa, Hane, Saku) | — | ⬜ Pendiente | 0 |

## Registro de avances

- **2026-06-09** — Puesta a punto del entorno (fork, build CI v4, guía de estilo). Traducida la escena de la avioneta del EP1 (líneas 18668–18708, charla Battler/George). Confirmado en el juego que los acentos renderizan bien.
- **2026-06-09** — Corregido bug de título ("ÉEpisodio"→"Episodio") y completados los menús de sistema. Validado el workflow multi-agente de traducción: 1.ª oleada del EP1 (300 líneas, 18714–19910: presentación de Battler, George, Hideyoshi, Eva, Kyrie) traducida y aplicada con validación de etiquetas.
- **2026-06-10** — ✅ **Episodio 1 completado** (~7.460 líneas) mediante 7 oleadas del workflow multi-agente. Incluye la llegada a Rokkenjima, la cena, los crímenes de los crepúsculos, la carta y la cláusula de Beatrice, y la fiesta del té con Bernkastel. Control de calidad: tildes/eñes, etiquetas de voz `@v`, `@|`/`@y`, comillas rectas y vocales no duplicadas. Cada oleada validada y compilada en CI.

---

### Criterio de traducción
Se mantienen honoríficos (-san, -kun, nii-san, aniki…) y nombres originales (Battler, Beatrice, Kinzo…), siguiendo la localización oficial inglesa. Ver [GUIA_DE_ESTILO_ES.md](GUIA_DE_ESTILO_ES.md).

### Cómo probar las versiones de prueba
Cada cambio genera una compilación en la pestaña **Actions** del repositorio; descarga el artefacto `patch_atmos` (Ryujinx/consola) o `patch_yuzu` (yuzu/Eden) e instálalo como el parche original.

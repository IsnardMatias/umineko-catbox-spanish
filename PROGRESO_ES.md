# Progreso de la traducción al español

Traducción al español del parche de **Umineko no Naku Koro ni Saku ~Nekobako to Musou no Koukyoukyoku~** (port de consola, Entergram).
Basada en el proyecto inglés de [andOlga / umineko-catbox-english](https://andolga.github.io/umineko-catbox-english) (enlace canónico) y en el fork de Lovahi.

> **Estado general:** 🟡 En curso — fase inicial. La infraestructura, el build automático y los menús del sistema están listos; la traducción del guion principal está empezando.

_Última actualización: 2026-06-12_

> **Mitad superada:** EP1–EP5 traducidos (5 de 8 episodios, ~37.300 líneas).

**EP1–EP5:** ✅ COMPLETOS. · Próximo: **EP6** (desde línea 250539).

---

## Resumen rápido

| Parte | Estado | Detalle |
|---|---|---|
| Infraestructura / build (GitHub Actions) | ✅ Listo | Compila y genera parche descargable |
| Caracteres del español (acentos, ¿ ¡) | ✅ Listo | Renderizan correctamente en el juego |
| Menús y mensajes del sistema (guardar, cargar, config, Sí/No…) | ✅ ~Completo | Falta solo algún término menor |
| **Guion — Episodios 1–5** | ✅ Completos | EP1–EP5 enteros traducidos (~37.300 líneas) |
| Guion — Episodios 6–8 | ⬜ Pendiente | — |
| Tsubasa / Hane / contenido extra de Saku | ⬜ Pendiente | — |
| Juego de deducción de Bernkastel (EP8, texto de exefs) | ⬜ Pendiente | 1 de ~34 bloques |
| Imágenes con texto (logos, botones) | ⬜ Pendiente | — |

## Detalle del guion (script.rb)

Total de líneas de diálogo del juego: **~72.850**.

| Episodio | Rango aprox. | Estado | Líneas traducidas |
|---|---|---|---|
| EP1 — Leyenda de la Bruja Dorada | 18434–48131 | ✅ Completo | Episodio entero traducido (prólogo → fiesta del té de Beatrice → Bernkastel) |
| EP2 — Turno de la Bruja Dorada | 48132–86343 | ✅ Completo | Episodio entero (acuario, propuesta de George, verdad roja, las tres brujas) |
| EP3 — Banquete de la Bruja Dorada | 86344–137226 | ✅ Completo | Episodio entero (Cuervo de Hempel, Eva-Beatrice, Ange en 1998) |
| EP4 — Alianza de la Bruja Dorada | 137227–195414 | ✅ Completo | Episodio entero (Ange, masacre del ritual de Kinzo, sacrificio de Ange, duelo final Battler/Beatrice, epílogo Bernkastel/Lambdadelta) |
| EP5 — Fin de la Bruja Dorada | 195415–250538 | ✅ Completo | Episodio entero (Beato muñeca, llegada de Erika, juicio de coartadas, verdad dorada, Battler nuevo Game Master) |
| EP6–EP8 | — | ⬜ Pendiente | 0 |
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
- **2026-06-10** — ✅ **Episodio 2 completado** (~7.200 líneas) en 5 oleadas: la cita de George/Shannon en el acuario, la propuesta de matrimonio, el ajedrez de Kinzo y Nanjo, la batalla de la verdad roja sobre el cuarto cerrado de la capilla, y la escena meta de las tres brujas (Beatrice, Bernkastel, Lambdadelta).
- **2026-06-11** — ✅ **Episodio 3 completado** (~7.300 líneas): el Cuervo de Hempel, el ascenso de Eva-Beatrice, los crímenes del banquete y la línea de Ange en 1998.
- **2026-06-12** — 🟡 **Episodio 4 al ~97%** mediante 7 oleadas: la alianza con Ange, la masacre del ritual de Kinzo, el sacrificio de Ange como «pieza», y el duelo final entre Battler y Beatrice (verdad azul vs. verdad roja, partida a partida).
- **2026-06-12** — ✅ **Episodio 4 completado** (~7.500 líneas). Cerradas las ~210 líneas que faltaban: el desmantelamiento de la tercera partida, la crucifixión de Beato con las estacas azules, su súplica de "mátame", y el epílogo de Bernkastel y Lambdadelta (la apuesta sobre el desenlace, el castigo de las gemas). Control de calidad: tildes/eñes, etiquetas `@v`/`@|`/`@y`, comillas rectas.
- **2026-06-12** — ✅ **Episodio 5 completado** (~7.800 líneas) en 6 oleadas: Beato reducida a muñeca, la llegada de la náufraga Furudo Erika, la llamada de chantaje a Natsuhi ("hace 19 años"), el duelo de Erika/Dlanor contra Beato en el estudio cerrado de Kinzo, el juicio de coartadas selladas, la masacre del ritual, el viaje de Battler por el Decálogo de Knox hasta la verdad, la **verdad dorada** que derrota a Dlanor, y Battler aceptando el puesto de Game Master para el EP6. Control de calidad reforzado: 4 lotes que volvieron sin tildes fueron re-traducidos, y se repararon etiquetas de voz `@v` y una animación letra-a-letra con `@y`.

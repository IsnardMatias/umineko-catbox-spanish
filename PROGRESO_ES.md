# Progreso de la traducción al español

Traducción al español del parche de **Umineko no Naku Koro ni Saku ~Nekobako to Musou no Koukyoukyoku~** (port de consola, Entergram).
Basada en el proyecto inglés de [andOlga / umineko-catbox-english](https://andolga.github.io/umineko-catbox-english) (enlace canónico) y en el fork de Lovahi.

> **Estado general:** 🟡 En curso — fase inicial. La infraestructura, el build automático y los menús del sistema están listos; la traducción del guion principal está empezando.

_Última actualización: 2026-06-12_

> **¡GUION COMPLETO!** Los 8 episodios + todos los extras (Tsubasa/Hane/Saku) traducidos (~70.000 líneas de diálogo), más los 172 títulos de sección en pantalla. No queda texto del guion sin traducir.

**EP1–EP8 + extras (Tsubasa/Hane/Saku):** ✅ **TODO EL GUION TRADUCIDO.** Incluidos los títulos de capítulo/sección en pantalla.

---

## Resumen rápido

| Parte | Estado | Detalle |
|---|---|---|
| Infraestructura / build (GitHub Actions) | ✅ Listo | Compila y genera parche descargable |
| Caracteres del español (acentos, ¿ ¡) | ✅ Listo | Renderizan correctamente en el juego |
| Menús y mensajes del sistema (guardar, cargar, config, Sí/No…) | ✅ ~Completo | Falta solo algún término menor |
| **Guion — Episodios 1–8** | ✅ Completos | Historia principal entera traducida (~63.400 líneas) |
| **Extras (Tsubasa/Hane/Saku)** | ✅ Completos | ~6.450 líneas (cartas, historias cortas, Saku) |
| **Títulos de sección/capítulo** | ✅ Completos | 172 títulos de las cards en pantalla |
| Tsubasa / Hane / contenido extra de Saku | 🟡 Siguiente | ~6.450 líneas (Tsubasa ~3.985, Saku ~1.901, Hane ~557) |
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
| EP6 — Amanecer de la Bruja Dorada | 250539–309875 | ✅ Completo | Episodio entero (las dos Beato, demonios Zepar/Furfur, cuarto cerrado de cadena, resurrección de Beatrice, Bernkastel y Featherine) |
| EP7 — Réquiem de la Bruja Dorada | 309876–356208 | ✅ Completo | Episodio entero (pasado de Kinzo y Bice, origen de Yasu/Beatrice, mundo de Lion, Will y Clair, masacre de Kyrie/Rudolf, el juego final para Ange) |
| EP8 — Crepúsculo de la Bruja Dorada | 356209–419565 | ✅ Completo | Episodio entero (la llave de Ange, fiesta de Halloween, batalla de la Tierra Dorada, Bern vs Lambda, el reencuentro de Ange con Tohya/Battler en 1998 y el epílogo de la Casa del Evangelio) |
| Extras (Tsubasa, Hane, Saku) | 419566–fin | ✅ Completo | Cartas y omakes de Tsubasa, Hane (Jessica/Falsificación), Saku (Flauros, ensayo de cuartos cerrados, entrevista del oro, doujin de Ange) |
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
- **2026-06-12** — ✅ **Episodio 6 completado** (~8.570 líneas) en 6 oleadas: la boda-burla de Erika, el nacimiento de las dos Beato (la joven y la "Elder BEATRICE"), los demonios del amor Zepar y Furfur y la prueba de las parejas (George/Shannon vs Jessica/Kanon), la apuesta de Bernkastel (Erika sin autoridad de detective), el duelo del **cuarto cerrado de la cadena** que Battler gana con una jugada milagrosa, la **resurrección triunfal de Beatrice** irrumpiendo en la recepción contra las tropas Chiester, y el encuentro de Bernkastel con su antigua maestra **Featherine** para iniciar la séptima partida. Se normalizó el hablante "Elder BEATRICE" y se repararon etiquetas de voz y apóstrofos.
- **2026-06-12** — ✅ **Episodio 7 completado** (~7.980 líneas) en 6 oleadas: el funeral de Beatrice, el trágico **pasado de Kinzo** (el oro italiano, la masacre, su amor por Bice), la verdad sobre **Yasu/Beatrice** (hija de Kinzo) y el origen de Shannon/Kanon/Lion en la Casa del Evangelio, el viaje de **Lion con Will** por los mundos alternativos, la coronación de Lion como BEATRICE y la muerte en paz de Kinzo, la **masacre de Kyrie y Rudolf** en la conferencia familiar, y el inicio del juego final que Battler narra a la pequeña **Ange**. Control de calidad: solo 2 apóstrofos sin escapar reparados; el resto limpio.
- **2026-06-13** — ✅ **Extras completados** (Tsubasa, Hane, Saku, ~6.450 líneas) en 5 oleadas, y **traducidos los 172 títulos de sección/capítulo** que se muestran en pantalla. Con esto **todo el guion del juego queda traducido al español**. Además se hizo una corrección global del signo `~` de alargamiento (113 casos movidos al final de la palabra, p. ej. "amo~r" → "amor~") en todo el script, por convención del español.
- **2026-06-13** — ✅ **Episodio 8 completado** (~9.490 líneas, el más largo) en 7 oleadas, ¡**cerrando la historia principal**! La llave dorada que Battler entrega a Ange, la fiesta de Halloween y el juego del rey, la fiesta final con todos los personajes, Ange descubriendo la masacre y siendo guiada por Bernkastel como **Bruja de la Verdad**, el asalto de las cabras a la **Tierra Dorada**, el sacrificio de **Lambdadelta contra Bernkastel**, el renacimiento de Ange como **ANGE BEATRICE** y el desbaratamiento del complot de Amakusa/Sumadera, y el conmovedor **reencuentro de Ange con Hachijo Tohya** (el cuerpo de Battler) en 1998, cerrando con el epílogo de la Casa del Evangelio reconstruida. Control de calidad: 2 oleadas reintentadas por límite de sesión, y un lote (deducción de Ange) re-traducido por venir sin tildes.

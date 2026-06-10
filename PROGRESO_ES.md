# Progreso de la traducción al español

Traducción al español del parche de **Umineko no Naku Koro ni Saku ~Nekobako to Musou no Koukyoukyoku~** (port de consola, Entergram).
Basada en el proyecto inglés de [andOlga / umineko-catbox-english](https://andolga.github.io/umineko-catbox-english) (enlace canónico) y en el fork de Lovahi.

> **Estado general:** 🟡 En curso — fase inicial. La infraestructura, el build automático y los menús del sistema están listos; la traducción del guion principal está empezando.

_Última actualización: 2026-06-09_

---

## Resumen rápido

| Parte | Estado | Detalle |
|---|---|---|
| Infraestructura / build (GitHub Actions) | ✅ Listo | Compila y genera parche descargable |
| Caracteres del español (acentos, ¿ ¡) | ✅ Listo | Renderizan correctamente en el juego |
| Menús y mensajes del sistema (guardar, cargar, config, Sí/No…) | ✅ ~Completo | Falta solo algún término menor |
| **Guion — Episodio 1** | 🟡 En curso | ~Apertura traducida (prólogo + escena de la avioneta) |
| Guion — Episodios 2–8 | ⬜ Pendiente | — |
| Tsubasa / Hane / contenido extra de Saku | ⬜ Pendiente | — |
| Juego de deducción de Bernkastel (EP8, texto de exefs) | ⬜ Pendiente | 1 de ~34 bloques |
| Imágenes con texto (logos, botones) | ⬜ Pendiente | — |

## Detalle del guion (script.rb)

Total de líneas de diálogo del juego: **~72.850**.

| Episodio | Rango aprox. | Estado | Líneas traducidas |
|---|---|---|---|
| EP1 — Legend of the Golden Witch | desde 18474 | 🟡 En curso | Prólogo (18474–18626) + escena avioneta (18668–18708) |
| EP2–EP8 | — | ⬜ Pendiente | 0 |
| Extras (Tsubasa, Hane, Saku) | — | ⬜ Pendiente | 0 |

## Registro de avances

- **2026-06-09** — Puesta a punto del entorno (fork, build CI v4, guía de estilo). Traducida la escena de la avioneta del EP1 (líneas 18668–18708, charla Battler/George). Confirmado en el juego que los acentos renderizan bien.

---

### Criterio de traducción
Se mantienen honoríficos (-san, -kun, nii-san, aniki…) y nombres originales (Battler, Beatrice, Kinzo…), siguiendo la localización oficial inglesa. Ver [GUIA_DE_ESTILO_ES.md](GUIA_DE_ESTILO_ES.md).

### Cómo probar las versiones de prueba
Cada cambio genera una compilación en la pestaña **Actions** del repositorio; descarga el artefacto `patch_atmos` (Ryujinx/consola) o `patch_yuzu` (yuzu/Eden) e instálalo como el parche original.

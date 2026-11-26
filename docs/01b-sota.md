# 01b · Estado del arte (SOTA) de mi proyecto

## 1. Problema y preguntas de búsqueda (CE 1c)

**Problema:** Los pilotos de sim racing no tienen un único sitio donde comparar tiempos por circuito/coche/simulador con el video y los consejos de la vuelta.

| # | Pregunta | Dónde busqué | Fecha |
|---|---|---|---|
| P1 | ¿Qué soluciones existen para registrar/comparar hotlaps? | Google, sitios oficiales de cada solución | 2026-11-19 |
| P2 | ¿Cómo ganan dinero esas soluciones? | Webs oficiales, páginas de precios | 2026-11-19 |
| P3 | ¿Qué tecnologías usan? | Webs oficiales, Wikipedia, LinkedIn | 2026-11-19 |
| P4 | ¿Qué no cubren y qué puede aportar SimRecords? | Videos y comentarios de las vueltas. | 2026-11-19 |

## 2. Soluciones existentes (CE 1a, 1c, 2a)

| Solución | Para quién | Qué hace | Modelo de precio | Enlace y fecha de acceso | Estado |
|---|---|---|---|---|---|
| iRacing | Pilotos competitivos | Leaderboards in-game por coche/circuito, carreras oficiales | Suscripción mensual/anual | https://www.iracing.com/ (2026-11-19) | leído |
| Assetto Corsa Competizione | Pilotos ACC | Leaderboards in-game por coche/circuito | Compra del juego | https://www.kunos-simulazioni.com/ (2026-11-19) | leído |
| SimGrid | Comunidades/ligas | Campeonatos, comunidades y leaderboards por comunidad | Freemium (Grid Pass de pago) | https://www.thesimgrid.com/ (2026-11-19) | leído |
| Low Fuel Motorsport | Pilotos ACC/AC/AMS2 | Carreras organizadas y hotlaps | Gratuito con donaciones/LFM+ | https://lowfuelmotorsport.com/ (2026-11-19) | leído |
| Simracing.gp | Organizadores de campeonatos | Campeonatos multijuego con servidores dedicados | Gratuito para empezar | https://simracing.gp/ (2026-11-19) | leído |
| Sim Racing Alliance | Pilotos ACC | Leaderboards de hotlap por circuito/coche | Gratuito | https://www.simracingalliance.com/leaderboards/hot_lap (2026-11-19) | leído |
| ACCReplay | Pilotos ACC | Track records y telemetría | Gratuito | https://www.accreplay.com/leaderboards (2026-11-19) | leído |
| TheTenths | Pilotos multi-sim | Hotlaps multi-sim con cliente Windows y telemetría | Gratuito (cliente) | https://www.thetenths.com/leaderboard (2026-11-19) | leído |
| Coach Dave Academy | Pilotos ACC | Leaderboards ACC + setups | Freemium (setups de pago) | https://coachdaveacademy.com/acc-lap-times/ (2026-11-19) | leído |
| Hoja de cálculo (Google Sheets) | Ligas pequeñas | Registro manual de tiempos | Gratuito | No aplica (no digital) | sin leer |

## 3. Modelos de negocio (CE 1d, 1e)

| Patrón | Soluciones que lo usan | Ventaja | Riesgo |
|---|---|---|---|
| Suscripción | iRacing | Ingresos recurrentes | Barrera de entrada |
| Freemium | SimGrid (Grid Pass), LFM+ | Base amplia de usuarios | Conversión baja |
| Gratuito con donaciones/publicidad | Low Fuel Motorsport | Crecimiento rápido | Sostenibilidad |
| Venta de setups/contenidos | Coach Dave Academy, GO Setups | Ingresos por valor añadido | Depende de partners |
| Gratuito (cliente) | TheTenths, ACCReplay | Adopción rápida | Costes de infraestructura |

Modelo de SimRecords: proyecto académico sin ánimo de lucro. Si se publicara, se plantea **freemium con donaciones** y sin venta de datos personales. Pendiente de confirmar.

## 4. Herramientas y tecnologías (CE 2a, 2b)

| Decisión | Opción | Madurez | Licencia | Coste | Curva | Encaje con ciclo | Elegida |
|---|---|---|---|---|---|---|---|
| Lenguaje backend | Java 21 | Alta | Open source | Bajo | Media | Alto (visto en ciclo) | Sí |
| Lenguaje backend | Node.js | Alta | Open source | Bajo | Baja | Medio | No |
| Framework backend | Spring Boot | Alta | Open source | Bajo | Media | Alto | Sí (tentativo) |
| Base de datos | MySQL | Alta | Open source | Bajo | Baja | Alto | Sí |
| Base de datos | PostgreSQL | Alta | Open source | Bajo | Baja | Medio | No |
| Base de datos | MongoDB | Alta | Open source | Bajo | Media | Bajo | No |
| Frontend | JavaScript (vanilla) | Alta | Open source | Bajo | Baja | Alto | Pendiente |
| Frontend | React | Alta | Open source | Bajo | Media | Medio | Pendiente |
| Despliegue | Docker + plataforma cloud | Alta | Open source | Bajo/medio | Media | Medio | Tentativo |
| Autenticación | JWT | Alta | Open source | Bajo | Baja | Medio | Tentativo |

## 5. Hueco y diferenciación (CE 1e)

Las soluciones existentes cubren leaderboards por circuito/coche, pero dispersan la información: el video está en YouTube, el setup en foros y la guía en otro sitio. SimRecords unifica en una sola ficha el tiempo, el video y los comentarios/guía de la vuelta, con filtros por simulador/circuito/coche y acceso gratuito y abierto. Se reconoce que TheTenths ya cubre hotlaps multi-sim con telemetría y que los leaderboards in-game son más fiables para verificar tiempos; el valor de SimRecords está en la ficha con comentarios/guía y la comunidad.

## 6. Decisiones derivadas (CE 1e, 1f, 2b)

- Tipo de proyecto elegido: aplicación web full-stack (enlace: 01-analisis.md §3).
- Requisitos que salen del estudio: RF-01, RF-02, RF-03, RF-04, RNF-01, RNF-02 (01-analisis.md §4).
- Decisiones técnicas: Java 21 + Spring Boot + MySQL (tentativas); frontend y despliegue pendientes de confirmar. Archivos en `decisiones/` pendientes de crear en H2.

## 7. Fuentes y calidad (CE 2a)

| # | Fuente (enlace) | Tipo | Fecha de acceso | Fiabilidad |
|---|---|---|---|---|
| F1 | https://www.iracing.com/ | Oficial | 2026-11-19 | Alta |
| F2 | https://www.kunos-simulazioni.com/ | Oficial | 2026-11-19 | Alta |
| F3 | https://studio-397.com/about/ | Oficial | 2026-11-19 | Alta |
| F4 | https://pits.thesimgrid.com/about-us | Oficial | 2026-11-19 | Alta |
| F5 | https://simracing.gp/ | Oficial | 2026-11-19 | Alta |
| F6 | https://lowfuelmotorsport.com/ | Oficial | 2026-11-19 | Alta |
| F7 | https://www.simracingalliance.com/leaderboards/hot_lap | Oficial | 2026-11-19 | Media |
| F8 | https://www.accreplay.com/leaderboards | Oficial | 2026-11-19 | Media |
| F9 | https://www.thetenths.com/leaderboard | Oficial | 2026-11-19 | Media |
| F10 | https://sim.racing/sim-racing-communities/ | Artículo sectorial | 2026-11-19 | Media |

## 8. Límites

- No se han verificado precios exactos de suscripciones (iRacing, Grid Pass) ni condiciones de LFM+; consultar fuentes oficiales.
- La empresa tipo y su organigrama son una estimación, no datos reales de una empresa concreta.
- El stack frontend y el despliegue quedan pendientes de confirmar.
- No se ha comprobado la existencia de una API pública en las soluciones estudiadas.
- Los datos de usuarios de las plataformas son declaraciones de las propias empresas, no auditados.

---

## Criterios de evaluación que alimenta este documento (texto literal)

- **1a)** Se han clasificado las empresas del sector por sus características organizativas y el tipo de producto o servicio que ofrecen.
- **1c)** Se han identificado las necesidades más demandadas a las empresas.
- **1d)** Se han valorado las oportunidades de negocio previsibles en el sector.
- **1e)** Se ha identificado el tipo de proyecto requerido para dar respuesta a las demandas previstas.
- **1f)** Se han determinado las características específicas requeridas al proyecto.
- **2a)** Se ha recopilado información relativa a los aspectos que van a ser tratados en el proyecto.
- **2b)** Se ha realizado el estudio de viabilidad técnica del mismo.

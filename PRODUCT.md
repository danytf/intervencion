# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Responsables de equipo y de zona de Wesser (RE/RP) que acompañan en campo a captadores/as nuevos o con dificultades. La usan sobre todo en el móvil (iPhone), durante o justo después de una sesión de acompañamiento, para registrar lo observado, evaluar y decidir la siguiente intervención.

## Product Purpose

Herramienta de intervención: ficha del captador/a, evaluación (mentalidad, técnica, hábitos), acompañamiento por fases de integración, diagnóstico y seguimiento del equipo. Sirve para que el acompañamiento se base en evidencia y patrones, y no solo en el número de socios. Funciona bien cuando el responsable sale de cada sesión con una lectura clara, unas prioridades concretas y un historial fiable.

## Positioning

Orienta sin predecir: un índice de atención, no una probabilidad de baja; las lecturas R1–R13 siguen el ciclo Evidencia → Lectura → Intervención → Revisión. La decisión, incluida una posible salida, es siempre del responsable, contrastada con el RP/RE.

## Operating Context

- En la calle o en el punto de captación, con el móvil y a veces con prisa; también en el ordenador.
- Cinco secciones: Captador · Evaluación · Acompañamiento · Diagnóstico (con la Decisión al final) · Equipo (Resumen · Historial · Evolución). Recursos (biblioteca y plantillas) va en una pantalla aparte.
- Cada sesión se guarda como ficha. Las fichas con el mismo NIP forman un historial; sin NIP se agrupan por nombre.
- Salidas: PDF de la sesión y exportación/importación JSON como copia de seguridad.

## Capabilities and Constraints

- La app es un único `index.html`, sin servidor y sin ficheros aparte. Publicada en GitHub Pages (repo danytf/intervencion, rama main).
- Ya incluye una instalación básica en el móvil: manifiesto y service worker mínimo generados dentro del propio fichero, sin caché sin conexión, y el aviso «Instalar Wesser». Queda descartado ampliarla: ni modo sin conexión real ni service worker o manifiesto en ficheros aparte.
- Los datos viven solo en el `localStorage` de ese navegador. Un fallo de lectura o datos dañados nunca se toman por «no hay datos» ni se sobrescriben.
- Varias pestañas abiertas: al guardar se fusionan los cambios en tres vías.
- Los bloques de contenido (PLANTILLAS, BIBLIOTECA, GUIA_FASES, MATRIZ_REGLAS…) son datos de producto; se adaptan al mostrarlos, no se reescriben.
- Pendientes ya identificados, sin decidir: calibrar los pesos y umbrales del índice de atención; las señales de alarma no se guardan con la ficha.

## Brand Commitments

- Nombre: «Wesser · Intervención».
- Tono: profesional, ético y no punitivo. Se habla de acompañar, no de juzgar.
- El aspecto visual sigue la guía `proyectos ia/GUIA_DISENO_WESSER.md` y sus apps de referencia (gestor emocional, rebatidapp, bibliowesser). Si la guía y una app chocan, manda la app.

## Evidence on Hand

No hay testimonios, métricas de uso ni casos reales documentados; no se deben inventar. La prueba con 1–3 responsables en iPhone está pendiente.

## Product Principles

1. Evidencia antes que número: el diagnóstico se basa en patrones observados.
2. La persona decide: la app orienta y nunca predice ni decide una salida.
3. Ningún dato se pierde en silencio: cualquier fallo se avisa y no se confirma nada que no haya quedado guardado.
4. Los datos personales (nombre, NIP, valoraciones) no salen del dispositivo salvo por exportación explícita.
5. Hecha para el campo: rápida y legible en el móvil y con prisa.

## Accessibility & Inclusion

WCAG 2.2 AA: contraste, teclado, lectores de pantalla y uso táctil en móvil.

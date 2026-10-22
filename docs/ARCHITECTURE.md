# Arquitectura — MVP

## Enfoque
Monolito modular Java 21 + Spring Boot. Separación entre:
- `domain`: reglas y modelos puros.
- `application`: casos de uso y puertos.
- `api`: contratos REST y validación de entradas.
- `infrastructure`: persistencia, motor de guiones, TTS y renderizado.

## Flujo esperado
`POST /api/videos` → validar proyecto → guardar → crear guion → revisión de fuentes → narración → assets con derechos → FFmpeg → control de calidad → aprobación → exportación.

## Reglas
- No escribir datos de salida en el repositorio.
- La generación y el renderizado son trabajos asíncronos, con estados y logging.
- No usar contenido de terceros sin respetar licencia/atribución.
- Videos no se publican sin aprobación humana.
- Integraciones externas tienen adapters intercambiables.

## Etapas
1. MF-001 a MF-004: fundamento API y persistencia.
2. MF-005 a MF-010: pipeline multimedia.
3. MF-011 a MF-015: orquestación, panel, publicación supervisada, CI.

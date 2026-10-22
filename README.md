# Misteria Factory

Fábrica local y de código abierto para producir videos originales de historias y misterios documentados.

## Objetivo del MVP

Crear un video vertical MP4 (1080x1920) a partir de un proyecto, con guion verificado, narración, recursos visuales con licencias claras, subtítulos, renderizado FFmpeg y aprobación humana previa a publicar.

## Stack

Java 21 · Spring Boot · Maven · H2 (MVP) · PostgreSQL (posterior) · Ollama (opcional) · Piper TTS · FFmpeg · React (fase posterior).

## Principios

- Presupuesto de servicios: $0 MXN/mes al inicio; ejecución local.
- Documentar fuentes, derechos de uso y procedencia del material.
- No presentar ficción como hecho ni publicar automáticamente sin revisión.
- Monolito modular con separación entre dominio, aplicación, API e infraestructura.
- Aprendizaje incremental: resolver issues y probar antes de integrar.

## Flujo de trabajo

`Master` es la rama inicial creada en GitHub; desarrollaremos en `develop` y ramas `feature/MF-XXX-descripcion`. Los cambios llegan a `develop` mediante Pull Request.

## Roadmap

Consultar la pestaña **Issues**: MF-001 a MF-015, organizados por entregables.

## Inicio

1. Resolver MF-001 para generar y compilar el proyecto Spring Boot.
2. Resolver MF-002 para crear el modelo de dominio.
3. Implementar REST, persistencia, guiones, voz, medios y renderizado en los siguientes issues.

**Estado:** documentación y planificación inicial; la aplicación aún no está implementada.

# AGENTS.md

Guía para agentes de IA que trabajen en este repositorio.

## Propósito del repositorio

Este repositorio documenta **únicamente decisiones técnicas** sobre la digitalización de Kaiku. No contiene código de producto ni implementación; contiene documentación, diagramas y registros de decisiones.

## Estructura

```
.
├── README.md
├── AGENTS.md
├── .gitignore
└── docs/                          # Documentación por entregable grande
    └── <entregable>-v<X.Y.Z>/     # Toda la documentación va dentro del entregable
        ├── README.md              # Qué se hizo, herramientas, decisiones
        ├── c4/                    # Diagramas C4 del entregable
        │   ├── 1-context/
        │   ├── 2-container/
        │   ├── 3-component/
        │   └── 4-code/            # Solo si hace falta
        └── adr/                   # Decisiones del entregable
            └── NNNN-titulo-corto.md
```

Cada entregable es autocontenido: sus diagramas C4 y sus ADR viven dentro de su propio directorio, no en la raíz del repositorio.

## Convenciones

### docs/ — Documentación por entregable

- Un directorio por entregable grande, con nombre en `kebab-case` y versión: `landing-page-v1.0.0/`, `onboarding-v1.0.0/`.
- Cada directorio debe contener un `README.md` con, como mínimo, estas secciones:
  1. **Qué se hizo** — alcance y resultado del entregable.
  2. **Herramientas tecnológicas** — tecnologías y servicios elegidos.
  3. **Decisiones técnicas** — decisiones tomadas y su justificación, enlazando a los ADR correspondientes.
  4. **Diagramas** — enlaces a los diagramas C4 relevantes.
- Crear un nuevo directorio por cada entregable; no mezclar entregables en un mismo documento.

### docs/<entregable>/c4/ — Diagramas C4

- Organizar los diagramas por nivel en subdirectorios numerados: `1-context`, `2-container`, `3-component`, `4-code`.
- Nivel 1 (Contexto) y 2 (Contenedores) son obligatorios. Nivel 3 (Componentes) y 4 (Código) solo cuando aporten valor.
- Formato recomendado: **Mermaid** dentro de archivos `.md` para que se rendericen en GitHub. Alternativamente, imágenes `.png`/`.svg` con su fuente.
- Un archivo `.md` por nivel y sistema, con una breve explicación del diagrama antes del bloque.

### docs/<entregable>/adr/ — Architecture Decision Records

- Un archivo por decisión, con nombre `NNNN-titulo-corto.md` (numeración secuencial de 4 dígitos: `0001`, `0002`, ...).
- Usar la plantilla:

```markdown
# NNNN. Título de la decisión

- **Fecha:** YYYY-MM-DD
- **Estado:** propuesta | aceptada | reemplazada por ADR-XXXX | obsoleta
- **Contexto:** sistema/entregable al que aplica

## Contexto

Situación y fuerzas en juego que motivan la decisión.

## Decisión

Qué se decide, en una frase afirmativa.

## Consecuencias

Resultados esperados, trade-offs y consecuencias negativas.
```

- Un ADR **no se edita** una vez aceptado: si cambia la decisión, se crea un ADR nuevo y se marca el anterior como `reemplazada por ADR-XXXX`.
- Enlazar los ADR desde el `README.md` del entregable correspondiente.

## Reglas para agentes

- Escribir la documentación en **español**.
- No inventar decisiones, herramientas ni hechos: documentar solo lo que se indique o exista en el repositorio.
- Mantener el estilo y la estructura descritos aquí; crear directorios y archivos que falten según sea necesario.
- Usar `kebab-case` para nombres de archivos y directorios.
- No crear código de aplicación en este repositorio.
- Al añadir un entregable o un ADR, actualizar los enlaces correspondientes en los `README.md` afectados.
- El `README.md` raíz documenta **cómo se lee el proyecto** (punto de entrada, orden de lectura y estructura). Si se agrega o cambia cualquier forma de lectura del proyecto, **actualizar siempre el `README.md`** en el mismo cambio.

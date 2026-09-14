# kaiku-technical-docs

Repositorio de **decisiones técnicas** sobre la digitalización de Kaiku. No contiene código de producto: solo documentación, diagramas C4 y registros de decisiones (ADR).

## Cómo leer este repositorio

1. **`README.md`** (este archivo) — punto de entrada y estructura general del repositorio.
2. **`docs/<entregable>-v<X.Y.Z>/README.md`** — documentación de cada entregable: qué se hizo, herramientas tecnológicas, decisiones técnicas y enlaces a diagramas. Empezar por el entregable de interés.
3. **`docs/<entregable>-v<X.Y.Z>/c4/`** — diagramas C4 del entregable, ordenados por nivel: `1-context`, `2-container`, `3-component`, `4-code`.
4. **`docs/<entregable>-v<X.Y.Z>/adr/`** — Architecture Decision Records del entregable, numerados secuencialmente.

## Estructura

```
.
├── README.md
├── AGENTS.md
├── .gitignore
└── docs/
    └── <entregable>-v<X.Y.Z>/
        ├── README.md
        ├── c4/
        │   ├── 1-context/
        │   ├── 2-container/
        │   ├── 3-component/
        │   └── 4-code/
        └── adr/
            └── NNNN-titulo-corto.md
```

Las convenciones detalladas (plantilla de entregable, niveles C4, plantilla de ADR) están en [`AGENTS.md`](./AGENTS.md).

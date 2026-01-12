# Corrupcion Data

Base de datos abierta y colaborativa de casos de corrupcion politica en Espana.

**Sitio web:** [corrupcion-ppsoe.es](https://corrupcion-ppsoe.es)

## Sobre este repositorio

Este repositorio contiene los datos estructurados de casos de corrupcion de los principales partidos politicos espanoles (PP y PSOE). Los datos estan en formato Markdown con metadatos YAML (frontmatter).

### Estadisticas actuales

| Partido | Casos documentados |
|---------|-------------------|
| PP      | 261               |
| PSOE    | 135               |
| **Total** | **396**         |

## Estructura del repositorio

```
corrupcion-data/
├── casos/
│   ├── pp/                    # Casos del Partido Popular
│   │   └── {nombre-caso}.md
│   └── psoe/                  # Casos del PSOE
│       └── {nombre-caso}.md
├── instituciones/             # Instituciones comprometidas
│   └── {nombre-institucion}.md
├── PLANTILLA_CASO.md          # Plantilla para nuevos casos
├── PLANTILLA_INSTITUCION.md   # Plantilla para instituciones
└── CONTRIBUTING.md            # Guia de contribucion
```

## Como contribuir

¡Toda ayuda es bienvenida! Puedes contribuir de varias formas:

### 1. Anadir un nuevo caso

1. Copia la plantilla `PLANTILLA_CASO.md`
2. Renombrala con el nombre del caso (ej: `caso-gurtel.md`)
3. Rellena los campos con informacion verificable
4. Coloca el archivo en `casos/pp/` o `casos/psoe/` segun corresponda
5. Abre un Pull Request

### 2. Completar casos existentes

Muchos casos tienen la marca `completado: false`. Puedes:
- Anadir cronologia de eventos
- Incluir mas implicados
- Actualizar el estado del caso
- Anadir fuentes y URLs

### 3. Corregir errores

Si encuentras informacion incorrecta:
- Abre un Issue describiendo el error
- O directamente un Pull Request con la correccion

### 4. Anadir instituciones

Documenta instituciones que consideres comprometidas politicamente:
- Usa la plantilla `PLANTILLA_INSTITUCION.md`
- Incluye fuentes oficiales (BOE, leyes, etc.)
- Documenta problemas concretos con evidencias

## Requisitos para contribuciones

**Obligatorio:**
- Toda informacion debe estar respaldada por fuentes verificables
- URLs a noticias, sentencias, BOE u otras fuentes oficiales
- Fechas en formato `YYYY-MM-DD`
- Redaccion neutral y objetiva

**Recomendado:**
- Fuentes primarias (BOE, sentencias) sobre fuentes secundarias (noticias)
- Multiples fuentes para hechos importantes
- Cronologia detallada con fechas exactas

## Formato de los datos

### Casos de corrupcion

Los casos usan frontmatter YAML con los siguientes campos:

```yaml
---
nombre: "Caso Ejemplo"
partido: PP  # o PSOE
completado: false  # true cuando este completo
ano: 2020
fechaInicio: 2020-01-15
fechaFin: ""  # vacio si sigue activo
estado: "en investigacion"  # cerrado con condenas, sobreseimiento, etc.
resumen: "Breve descripcion del caso"
coste: 1000000  # en euros
lugar: "Madrid, Espana"
tribunal:
  - "Audiencia Nacional"
implicados:
  - nombre: "Nombre Apellido"
    cargo: "Cargo publico"
    rol: "Rol en el caso"
tags:
  - "corrupcion"
  - "malversacion"
cronologia:
  - fecha: 2020-01-15
    titulo: "Evento importante"
    descripcion: "Descripcion del evento"
    urls:
      - "https://fuente.ejemplo.com/noticia"
    type: "investigacion"  # denuncia, sentencia, detencion, etc.
---

Contenido detallado del caso en Markdown...
```

### Instituciones

Ver `PLANTILLA_INSTITUCION.md` para el formato completo.

## Licencia

Los datos de este repositorio se publican bajo [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

Esto significa que puedes:
- Compartir y redistribuir el material
- Adaptarlo para cualquier proposito

Siempre que:
- Des credito apropiado
- Compartas derivados bajo la misma licencia

## Contacto

- **Web:** [corrupcion-ppsoe.es](https://corrupcion-ppsoe.es)
- **Issues:** Usa los issues de GitHub para reportar errores o sugerir mejoras

---

*Este proyecto busca la transparencia y la rendicion de cuentas en la politica espanola. No tiene afiliacion con ningun partido politico.*

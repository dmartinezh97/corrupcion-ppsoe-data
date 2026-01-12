# Guia de Contribucion

Gracias por tu interes en contribuir a este proyecto. Esta guia te ayudara a hacer contribuciones efectivas.

## Principios fundamentales

1. **Veracidad**: Solo informacion verificable con fuentes
2. **Neutralidad**: Redaccion objetiva, sin opiniones
3. **Completitud**: Mejor poco y verificado que mucho sin fuentes
4. **Respeto**: Este es un proyecto informativo, no partidista

## Tipos de contribucion

### Anadir un caso nuevo

1. **Verifica que no existe**: Busca en `/casos/pp/` y `/casos/psoe/`
2. **Copia la plantilla**: Usa `PLANTILLA_CASO.md`
3. **Nombre del archivo**: Usa minusculas, guiones, sin tildes
   - Correcto: `caso-gurtel.md`, `ere-andalucia.md`
   - Incorrecto: `Caso Gurtel.md`, `ERE_Andalucia.md`
4. **Rellena los campos**: Al menos nombre, partido, y resumen
5. **Anade fuentes**: URLs verificables para cada afirmacion
6. **Crea el PR**: Con descripcion clara de lo anadido

### Completar casos existentes

Muchos casos tienen `completado: false`. Puedes ayudar con:

- **Cronologia**: Anade eventos con fechas y fuentes
- **Implicados**: Nuevas personas con cargo y rol
- **Actualizaciones**: Estado actual, sentencias, etc.
- **Fuentes**: URLs a noticias o documentos oficiales

### Corregir informacion

Si encuentras errores:

1. Abre un Issue primero si no estas seguro
2. Para correcciones claras, abre directamente un PR
3. Incluye la fuente que respalda la correccion

## Formato de datos

### Fechas

Siempre en formato ISO: `YYYY-MM-DD`

```yaml
fechaInicio: 2015-03-21
fechaFin: 2020-11-15  # o "" si sigue activo
```

### Costes economicos

En euros, sin separadores de miles:

```yaml
coste: 1500000  # 1.5 millones de euros
```

### Estados del caso

Usa uno de estos valores:

- `en investigacion`
- `cerrado con condenas`
- `sobreseimiento`
- `prescrito`
- `activo`
- `archivado`
- `pendiente de juicio`

### Tipos de eventos (cronologia)

- `denuncia`
- `investigacion`
- `detencion`
- `registro`
- `imputacion`
- `juicio`
- `sentencia`
- `recurso`
- `indulto`

### Relevancia de eventos

- `alta`: Eventos cruciales (sentencias, detenciones principales)
- `media`: Eventos importantes (imputaciones, declaraciones clave)
- `baja`: Eventos secundarios (tramites, aplazamientos)

## Fuentes aceptables

### Preferidas (fuentes primarias)

- BOE (Boletin Oficial del Estado)
- Sentencias judiciales
- Informes del Tribunal de Cuentas
- Documentos oficiales de fiscalia

### Aceptables (fuentes secundarias)

- Periodicos nacionales: El Pais, El Mundo, ABC, La Vanguardia
- Agencias: EFE, Europa Press
- Medios especializados: El Confidencial, infoLibre

### No aceptables

- Blogs personales
- Redes sociales
- Medios sin identificar
- Fuentes anonimas

## Proceso de revision

1. **Automatico**: Se verifica el formato YAML
2. **Manual**: Un mantenedor revisa las fuentes
3. **Merge**: Si todo esta correcto, se incorpora

Los PRs pueden tardar unos dias en revisarse. Se paciente.

## Codigo de conducta

- Respeta a otros contribuidores
- Discute ideas, no personas
- Acepta criticas constructivas
- Manten el foco en la documentacion objetiva

## Dudas frecuentes

### ¿Puedo anadir casos de otros partidos?

Por ahora el proyecto se centra en PP y PSOE por ser los partidos con mas casos documentados y que han gobernado Espana. Podria ampliarse en el futuro.

### ¿Que hago si no tengo toda la informacion?

Anade lo que tengas con `completado: false`. Otros contribuidores pueden completarlo.

### ¿Como cito una sentencia?

```yaml
cronologia:
  - fecha: 2020-05-15
    titulo: "Sentencia Audiencia Nacional"
    descripcion: "Condena a X anos de prision por malversacion"
    urls:
      - "https://www.poderjudicial.es/..."
    type: "sentencia"
```

---

¿Mas dudas? Abre un Issue y te ayudamos.

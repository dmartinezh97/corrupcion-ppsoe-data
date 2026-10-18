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

Cada caso declara tres campos estructurados, además del detalle libre `estado`.
No uses explicaciones largas como etiquetas ni deduzcas el resultado por palabras.

- `estadoPrincipal`: En investigación · Pendiente de juicio · En juicio · Pendiente de sentencia · Condenado · Absuelto · Sobreseído / archivado · Resultados mixtos · Resolución no penal · Sin procedimiento judicial · Sin determinar.
- `recursoPendiente`: Sin recurso pendiente · En apelación · En casación · Otro recurso · Varios recursos · Sin determinar.
- `firmeza`: Firme · No firme · Parcial · Sin determinar · No procede.

Usa el resultado vigente documentado. Una condena revocada no permanece como
`Condenado`; una retroacción usa la fase de retorno, o `Sin determinar` si no consta.
Diferencias entre personas o piezas van a `Resultados mixtos`, contando el caso una
sola vez. Absolver de algún delito a alguien que mantiene una condena por otro no
basta por sí solo para clasificarlo como resultado mixto.

La firmeza se refiere a la resolución que sustenta el estado principal. Usa
`No procede` cuando aún no hay una resolución cuya firmeza se clasifique y
`Parcial` solo si constan diferencias entre personas o piezas. No deduzcas firmeza
ni ausencia de recursos por antigüedad o falta de noticias. Confirmaciones en
apelación o casación son antecedentes, no recursos pendientes. Los recursos
anunciados no equivalen a recursos presentados.

`Resolución no penal` recoge un resultado civil, contable o administrativo sin
resultado penal aplicable; `Sin procedimiento judicial` requiere documentación
expresa. Las lagunas van a `Sin determinar` y se explican en el detalle.

La clasificación inicial según el contenido existente se registra en
`REVISION_ESTADOS.tsv`. No acredita una nueva comprobación de las fuentes ni el
estado de hoy: conserva los límites y fechas documentados en cada ficha.

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

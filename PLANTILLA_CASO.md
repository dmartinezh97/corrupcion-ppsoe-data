---
nombre: "Caso [Nombre del Caso]"
partido: PP  # PP o PSOE
completado: false
año: 2024
fechaInicio: 2024-01-01
fechaFin: ""  # Dejar vacío si el caso sigue activo
estado: "en investigación"  # Valores: activo, en investigación, cerrado con condenas, sobreseimiento, archivado, prescrito, pendiente de juicio
descripcion: |
  Descripción detallada del caso de corrupción. Esta sección debe explicar:
  - Qué ocurrió y cómo se descubrió
  - Principales irregularidades detectadas
  - Contexto político en el que se desarrolló
  - Estado actual del caso

  Puedes usar varios párrafos. El formato con | permite texto multilínea.
resumen: "Breve descripción del caso en 1-2 líneas para mostrar en listados"
coste: 0  # Cantidad en euros (número entero, sin separadores)
lugar: "Ciudad, Comunidad Autónoma"
tribunal:
  - "Audiencia Nacional - Juzgado Central de Instrucción nº X - Juez [Nombre] - Fiscalía Anticorrupción"
  # Puedes añadir más tribunales si el caso pasa por varios
numeroSentencia: ""  # Ej: "STS 123/2024" o "SAN 13/2022"
implicados:
  - nombre: "Nombre Apellido Apellido"
    cargo: "Cargo público que ocupaba (ej: Alcalde de X, Consejero de Y)"
    rol: "Papel en el caso: investigado, condenado a X años, absuelto, colaborador..."

  - nombre: "Segundo Implicado"
    cargo: "Cargo del segundo implicado"
    rol: "Descripción de su participación en la trama"
  # Añade más implicados según sea necesario
tags:
  - "corrupción"
  - "malversación"
  - "prevaricación"
  # Otros: cohecho, tráfico de influencias, blanqueo de capitales, urbanismo, financiación ilegal, organización criminal
impactoSocial: "Descripción del impacto que tuvo el caso en la sociedad: repercusión mediática, dimisiones, cambios legislativos, efecto electoral, etc."
documentos: null
# Si hay documentos PDF, usar este formato:
# documentos:
#   - fecha: "2024-01-15"
#     titulo: "Sentencia Audiencia Nacional"
#     filetype: "pdf"
#     paginas: 120
#     nombre_fichero: "sentencia_caso.pdf"
cronologia:
  - fecha: 2024-01-15
    titulo: "Título del evento (ej: Detención de los principales implicados)"
    descripcion: "Descripción detallada del evento. Incluye contexto y relevancia para el caso."
    type: "investigación"  # Valores: denuncia, investigación, detención, registro, imputación, juicio, sentencia, recurso, indulto, resumen
    relevancia: "media"  # alta, media, baja
    urls:
      - "https://ejemplo.com/noticia-fuente"
      - "https://otra-fuente.com/articulo"

  - fecha: 2024-03-20
    titulo: "Segundo evento importante"
    descripcion: "Descripción del segundo evento."
    type: "sentencia"
    relevancia: "alta"
    urls:
      - "https://ejemplo.com/sentencia"
  # Añade más eventos en orden cronológico
---

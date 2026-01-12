---
title: "Nombre de la Institución"
description: "Descripción completa de la institución y su función oficial"
descripcionBreve: "Descripción breve de por qué está comprometida políticamente y cuál es el problema principal"
icon: "Scale"  # Opciones: Scale (justicia), FileText (documentos), Tv (medios), AlertTriangle (alerta), Shield (seguridad)
status: "Politizado"  # Valores: Bloqueado, Politizado, Controlado, Repartido, Dependiente, Vacante, Opaco, Influenciado, Manipulado
statusColor: "destructive"
order: 1  # Orden de visualización (1 = primero)
issues:
  # Primer problema identificado
  - descripcionCorta: "Problema resumido en una línea para mostrar en listados"
    descripcionBreve: "Descripción más detallada del problema, incluyendo contexto y consecuencias"
    sources:
      # Fuente oficial (BOE, leyes, etc.) - PREFERIDA
      - title: "Real Decreto X/2024 por el que se nombra..."
        url: "https://www.boe.es/diario_boe/txt.php?id=BOE-A-2024-XXXXX"
        tipo: "oficial"
        fecha: "2024-01-15"
        partido: "PSOE"  # Partido en el gobierno cuando se produjo

      # Fuente de noticia
      - title: "Titular de la noticia que documenta el problema"
        url: "https://ejemplo.com/noticia"
        tipo: "noticia"
        fecha: "2024-02-20"
        partido: ""  # Dejar vacío si no aplica a un partido concreto

  # Segundo problema identificado
  - descripcionCorta: "Otro problema de la institución"
    descripcionBreve: "Descripción detallada del segundo problema"
    sources:
      - title: "Fuente que documenta este problema"
        url: "https://ejemplo.com/fuente"
        tipo: "noticia"
        fecha: "2023-06-10"
        partido: "PP"

  # Tercer problema (si aplica)
  - descripcionCorta: "Tercer problema identificado"
    descripcionBreve: "Este problema afecta a ambos partidos por igual"
    sources:
      - title: "Fuente sobre el problema compartido"
        url: "https://ejemplo.com/problema-bipartidista"
        tipo: "noticia"
        fecha: "2022-03-15"
        partido: "ambos"  # Cuando PP y PSOE comparten responsabilidad
---

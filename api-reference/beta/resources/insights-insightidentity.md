---
title: insightIdentity
description: Tipo complejo que contiene las propiedades de los elementos compartidos.
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: a263caa68280128a67a027b75682407fd4932605
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938940"
---
# <a name="insightidentity"></a>insightIdentity

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Tipo complejo que contiene las propiedades de los elementos [compartidos](insights-shared.md) . 

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso

```json
{
  "displayName": "string",
  "id": "string",
  "address": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad              | Tipo          | Descripción  |
| -------------         |-----------    | -------------|
| displayName       | Cadena          | El nombre para mostrar del usuario que comparte el elemento. |
| id              | Cadena        | El identificador del usuario que comparte el elemento.     |
| address             | Cadena      | La dirección de correo electrónico del usuario que comparte el elemento.  |

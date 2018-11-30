---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: CreateAction
ms.openlocfilehash: 4b5d6a50c37c04b1c708e798820b8295d89ebf80
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084478"
---
# <a name="createaction-resource-type"></a>Tipo de recurso CreateAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

La presencia del recurso **CreateAction** en un recurso [**itemActivity**][activity] indica que la actividad ha creado un elemento.

**Nota**: Aunque actualmente este recurso está vacío, en futuras revisiones de la API, puede rellenarse con propiedades adicionales.

[activity]: itemactivity.md

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.createAction"
}-->

```json
{
}
```

## <a name="properties"></a>Propiedades

Ninguna. Esta faceta es un valor NULL o no NULL y no contiene propiedades.

## <a name="remarks"></a>Comentarios

Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.

<!-- {
  "type": "#page.annotation",
  "description": "The CreateAction object provides information about the creation of an item.",
  "keywords": "activities,activity,action,create,creation",
  "section": "documentation",
  "tocPath": "Resources/CreateAction"
} -->

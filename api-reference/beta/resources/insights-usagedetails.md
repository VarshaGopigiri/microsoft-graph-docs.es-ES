---
title: tipo de recurso usageDetails
description: Tipo complejo que contiene las propiedades de elementos utilizados. Obtener información sobre cuándo obtuvo acceso por última vez el recurso (ver) y modificar (Editar) por el usuario.
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: 466308ad1b6290c2b96335f94c586eb35c6cac28
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950023"
---
# <a name="usagedetails-resource-type"></a>tipo de recurso usageDetails

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Tipo complejo que contiene las propiedades de los elementos [se usa](insights-used.md) . Obtener información sobre cuándo obtuvo acceso por última vez el recurso (ver) y modificar (Editar) por el usuario.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

```json
{
  "lastAccessedDateTime": "DateTimeOffset",
  "lastModifiedDateTime": "DateTimeOffset"
}
```

## <a name="properties"></a>Propiedades

| Propiedad              | Tipo          | Descripción  |
| -------------         |---------------| -------------|
| lastAccessedDateTime                  | DateTimeOffset        | Fecha y hora de que último acceso el recurso por el usuario. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `2014-01-01T00:00:00Z`. Solo lectura.                      |
| lastModifiedDateTime              | DateTimeOffset        | La fecha y hora que se modificó por última vez el recurso por el usuario. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `2014-01-01T00:00:00Z`. Solo lectura.       |

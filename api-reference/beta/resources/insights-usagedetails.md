---
title: tipo de recurso usageDetails
description: Tipo complejo que contiene las propiedades de elementos utilizados. Obtener información sobre cuándo obtuvo acceso por última vez el recurso (ver) y modificar (Editar) por el usuario.
author: simonhult
ms.openlocfilehash: ef5efcfce439e9d08784637cb02657d7cd37adf7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349353"
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
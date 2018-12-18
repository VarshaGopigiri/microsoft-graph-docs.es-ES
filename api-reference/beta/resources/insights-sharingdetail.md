---
title: tipo de recurso sharingDetail
description: 'Tipo complejo que contiene las propiedades de los elementos compartidos. '
author: simonhult
ms.openlocfilehash: 8454fd451f0659ff3ccad270df3414a850bee180
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353378"
---
# <a name="sharingdetail-resource-type"></a>tipo de recurso sharingDetail

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Tipo complejo que contiene las propiedades de los elementos [compartidos](insights-shared.md) . 

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso

```json
{
  "sharedDateTime": "dateTimeOffset",
  "sharingSubject": "string",
  "sharingType": "string",
  "sharedBy": "insightIdentity",
  "resourceReference": "resourceReference"
}
```

## <a name="properties"></a>Propiedades

| Propiedad              | Tipo          | Descripción  |
| -------------         |-----------    | -------------|
| sharedDateTime        | DateTimeOffset| La fecha y la hora que el archivo por última vez se ha compartido. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `2014-01-01T00:00:00Z`. Solo lectura.  |
| sharingSubject        | String          | El asunto con el que se comparte el documento. |
| sharingType             | String        | Determina la forma en el documento se ha compartido, puede ser un "Vínculo", "Datos adjuntos", "Grupo", "Sitio".     |
| sharedBy                | [insightIdentity](insights-insightidentity.md)      | El usuario que comparte el documento.  |
| sharingReference        | [resourceReference](insights-resourcereference.md)      |  |
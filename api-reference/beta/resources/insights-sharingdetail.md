---
title: tipo de recurso sharingDetail
description: 'Tipo complejo que contiene las propiedades de los elementos compartidos. '
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: add63a89a451b742778dda1d6d313d58f675a642
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918766"
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
| sharingSubject        | Cadena          | El asunto con el que se comparte el documento. |
| sharingType             | Cadena        | Determina la forma en el documento se ha compartido, puede ser un "Vínculo", "Datos adjuntos", "Grupo", "Sitio".     |
| sharedBy                | [insightIdentity](insights-insightidentity.md)      | El usuario que comparte el documento.  |
| sharingReference        | [resourceReference](insights-resourcereference.md)      |  |

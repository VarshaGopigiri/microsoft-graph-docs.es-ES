---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Cuota
ms.openlocfilehash: f4518021da8ad180b91472feb52199678c2edc83
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089194"
---
# <a name="quota-resource-type"></a>tipo de recurso de cuota

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso de **cuota** proporciona detalles acerca del espacio restringe en un recurso de [unidad](drive.md) .

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@odata.type": "microsoft.graph.quota"
}-->

```json
{
  "deleted": 1024,
  "remaining": 1024,
  "state": "normal | nearing | critical | exceeded",
  "storagePlanInformation": {
    "upgradeAvailable": true
  },
  "total": 1024,
  "used": 1024
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad | Tipo   | Descripción                                                                 |
|:--------------|:-------|:----------------------------------------------------------------------------|
| total         | Int64  | Espacio total de almacenamiento permitido, en bytes. Solo lectura.                           |
| used          | Int64  | Espacio total usado, en bytes. Solo lectura.                                      |
| remaining     | Int64  | Espacio total restante antes de alcanzar el límite de cuota, en bytes. Solo lectura. |
| deleted       | Int64  | Espacio total consumido por los archivos de la Papelera de reciclaje, en bytes. Solo lectura.      |
| estado         | string | Valor de enumeración que indica el estado del espacio de almacenamiento. Solo lectura. |
| storagePlanInformation  | [storagePlanInformation](storageplaninformation.md) | Información acerca de los planes de cuota de almacenamiento de información de la unidad. Sólo en OneDrive Personal.|

### <a name="state-enumeration-values"></a>Valores de estado (enumeración)

| Valor      | Descripción                                                                                                                                                                 |
|:-----------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `normal`   | A la unidad le queda mucha cuota restante.                                                                                                                               |
| `nearing`  | La cuota restante es inferior al 10 % del espacio total de cuota.                                                                                                                      |
| `critical` | La cuota restante es inferior al 1 % del espacio total de cuota.                                                                                                                       |
| `exceeded` | La cuota usada ha superado la cuota total. No se pueden agregar nuevos archivos ni carpetas en la unidad hasta que esté por debajo de la cantidad total de cuota o se adquiera más espacio de almacenamiento. |

<!-- {
  "type": "#page.annotation",
  "description": "The quota facet provides information about how much space the OneDrive has available.",
  "keywords": "quota,available,remaining,used",
  "section": "documentation",
  "tocPath": "Facets/Quota"
} -->

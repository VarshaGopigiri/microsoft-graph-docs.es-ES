---
title: tipo de recurso educationCsvDataProvider
description: 'Se usa para configurar el perfil de sincronización de datos de school cuando los archivos CSV son el origen de entrada.  '
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: cb4d08a2a6750310a825f66ecfb0017abacd36fb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27878574"
---
# <a name="educationcsvdataprovider-resource-type"></a>tipo de recurso educationCsvDataProvider

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Se usa para configurar el perfil de sincronización de datos de school cuando los archivos CSV son el origen de entrada.  

Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:-|:-|:-|
| **personalizaciones** | [educationSynchronizationCustomizations](educationsynchronizationcustomizations.md) | Personalizaciones opcionales que se aplicará a los perfiles de sincronización.|

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationCsvDataProvider"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationCsvDataProvider",
    "customizations": { "@odata.type": "microsoft.graph.educationSynchronizationCustomizations" }
}
```

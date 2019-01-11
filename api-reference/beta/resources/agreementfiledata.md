---
title: tipo de recurso agreementFileData
description: Representa el blob de Azure Active Directory términos (Azure AD) de utilizar el archivo de contrato.
localization_priority: Normal
ms.openlocfilehash: 64de3a72ad648225f24429987f5729f76ed8a2e7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815221"
---
# <a name="agreementfiledata-resource-type"></a>tipo de recurso agreementFileData

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el blob de Azure Active Directory términos (Azure AD) de utilizar el archivo de contrato.

## <a name="properties"></a>Propiedades
| Método       | Tipo de valor devuelto | Descripción |
|:-------------|:------------|:------------|
|data|Binario|Datos que representan las condiciones de usar un documento PDF. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreementFileData"
}-->

```json
{
  "data": "Binary"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "agreementFileData resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

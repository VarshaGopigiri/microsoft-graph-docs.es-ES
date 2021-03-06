---
title: Tipo de recurso internetMessageHeader
description: 'Un par de clave y valor que representa un encabezado de mensaje de Internet, tal como se define por RFC5322, que proporciona '
localization_priority: Normal
ms.openlocfilehash: b4bc08a03d9d37738b84f7f1c9938278fb921a37
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828500"
---
# <a name="internetmessageheader-resource-type"></a>Tipo de recurso internetMessageHeader

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Par de clave y valor que representa un encabezado de mensaje de Internet, tal y como se define con [RFC5322](https://www.ietf.org/rfc/rfc5322.txt), que proporciona los detalles de la ruta de acceso a la red que sigue un mensaje del remitente al destinatario. 

Para examinar ejemplos de un encabezado de mensaje de Internet, consulte [Ver encabezados de mensajes de internet](https://support.office.com/en-us/article/View-e-mail-message-headers-CD039382-DC6E-4264-AC74-C048563D212C#bm4).


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|name|string|Representa la clave de un par de clave y valor.|
|value|string|Valor de un par de clave y valor.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.internetMessageHeader"
}-->

```json
{
  "name": "string",
  "value": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "internetMessageHeader resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

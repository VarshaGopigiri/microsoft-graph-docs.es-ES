---
title: Tipo de recurso mailboxSettings
description: Configuración del buzón principal del usuario que inició sesión.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 53ded2d60161d833f70a3b747e0ec35953d5bd39
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937085"
---
# <a name="mailboxsettings-resource-type"></a>Tipo de recurso mailboxSettings

Configuración del buzón principal del usuario que inició sesión.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|archiveFolder|string|Identificador de una carpeta de archivo del usuario.|
|automaticRepliesSetting|[automaticRepliesSetting](automaticrepliessetting.md)|Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión.|
|language|[localeInfo](localeinfo.md)|Representación de la configuración regional del usuario, como el idioma preferido y el país o región.|
|timeZone|string|La zona horaria predeterminada del buzón del usuario.|
|workingHours|[workingHours](workinghours.md)|Días de la semana y horas de la zona horaria específica en la que trabaja el usuario.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "archiveFolder"
  ],
  "@odata.type": "microsoft.graph.mailboxSettings"
}-->

```json
{
  "archiveFolder": "string",
  "automaticRepliesSetting": {"@odata.type": "microsoft.graph.automaticRepliesSetting"},
  "language": {"@odata.type": "microsoft.graph.localeInfo"},
  "timeZone": "string",
  "workingHours": {"@odata.type": "microsoft.graph.workingHours"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailboxSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

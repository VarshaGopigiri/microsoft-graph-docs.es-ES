---
title: Crear una configuración de grupo
description: Use esta API para crear una nueva configuración basada en las plantillas disponibles en groupSettingTemplates. Esta configuración puede establecerse a nivel de arrendatario o de grupo. La solicitud de creación debe proporcionar settingValues para toda la configuración establecida en la plantilla. Para configuraciones específicas de grupos, solo se puede establecer la configuración que indique si los miembros de un grupo pueden invitar a otros usuarios como invitados o no. Esto establecerá este comportamiento una vez que esté disponible de forma general la posibilidad de agregar usuarios como invitados.
localization_priority: Normal
ms.openlocfilehash: c5ba428380e6503f8d54682709d36e12b7ff4de3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894540"
---
# <a name="create-a-group-setting"></a>Crear una configuración de grupo

Use esta API para crear una nueva configuración basada en las plantillas disponibles en [groupSettingTemplates](../resources/groupsettingtemplate.md). Esta configuración puede establecerse a nivel de arrendatario o de grupo. La solicitud de creación debe proporcionar [settingValues](../resources/settingvalue.md) para toda la configuración establecida en la plantilla. Para configuraciones específicas de grupos, solo se puede establecer la configuración que indique si los miembros de un grupo pueden invitar a otros usuarios como invitados o no. Esto establecerá este comportamiento una vez que esté disponible de forma general la posibilidad de agregar usuarios como invitados.

Para obtener una lista de plantillas y las propiedades que admiten en v1.0, utilizar una [consulta de groupSettingTemplate](https://developer.microsoft.com/graph/graph-explorer?request=groupSettingTemplates&version=v1.0) (para beta extremos, llamada [directorySettingTemplates](https://developer.microsoft.com/graph/graph-explorer?request=directorySettingTemplates&version=beta).)

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groupSettings
POST /groups/{id}/settings
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre | Descripción |
|:---------------|:----------|
| Authorization | {token} de portador. Obligatorio. |
| Content-Type | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupSetting](../resources/groupsetting.md). Sin embargo, el nombre para mostrar de la configuración se establecerá según el nombre de la plantilla de configuración a la que se hace referencia.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [groupSetting](../resources/groupsetting.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "create_groupsetting_from_groupsettings"
}-->
```http
POST https://graph.microsoft.com/v1.0/groupSettings
Content-type: application/json
Content-length: 215

{
  "displayName": "displayName-value",
  "templateId": "templateId-value",
  "values": [
    {
      "name": "name-value",
      "value": "value-value"
    }
  ]
}
```
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupSetting](../resources/groupsetting.md).
##### <a name="response"></a>Respuesta

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupSetting"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 238

{
  "displayName": "displayName-value",
  "templateId": "templateId-value",
  "values": [
    {
      "name": "name-value",
      "value": "value-value"
    }
  ],
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create groupsetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

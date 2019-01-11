---
title: Crear una configuración de Active directory
description: Utilice esta API para crear una nueva configuración, en función de las plantillas disponibles en directorySettingTemplates. Esta configuración puede ser en el nivel de inquilino o en un nivel de objeto (actualmente únicamente para los grupos). La solicitud de creación debe proporcionar settingValues para toda la configuración definida en la plantilla. Para la configuración específica de grupo, se puede establecer sólo la configuración que rigen si los miembros de un grupo pueden invitar a los usuarios invitados. Una vez que esté disponible la capacidad de agregar los usuarios invitados a un grupo que rige este comportamiento.
localization_priority: Normal
ms.openlocfilehash: 692ca0d68522b5b268e9ee670c694e5a5c6bee90
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848723"
---
# <a name="create-a-directory-setting"></a>Crear una configuración de Active directory

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Utilice esta API para crear una nueva configuración, en función de las plantillas disponibles en directorySettingTemplates. Esta configuración puede ser en el nivel de inquilino o en un nivel de objeto (actualmente únicamente para los grupos). La solicitud de creación debe proporcionar settingValues para toda la configuración definida en la plantilla. Para la configuración específica de grupo, se puede establecer sólo la configuración que rigen si los miembros de un grupo pueden invitar a los usuarios invitados. Una vez que esté disponible la capacidad de agregar los usuarios invitados a un grupo que rige este comportamiento.

> **Nota**: la versión de /beta de esta API es sólo se aplica a los grupos. Se ha cambiado la versión /v1.0 de esta API para *crear groupSettings*.

Para obtener una lista de plantillas y las propiedades que se admiten en la versión beta, utilice una [consulta de directorySettingTemplate](https://developer.microsoft.com/graph/graph-explorer?request=directorySettingTemplates&version=beta). (Para los extremos de v1.0, llamada [groupSettingTemplates](https://developer.microsoft.com/graph/graph-explorer?request=groupSettingTemplates&version=v1.0)).


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
POST /settings
POST /groups/{id}/settings
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio.|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [establecer](../resources/directorysetting.md) .  Sin embargo, el nombre para mostrar para la configuración se establecerá en función en el nombre de la plantilla de configuración que se hace referencia.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `201 Created` objeto de código y [establecer](../resources/directorysetting.md) de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_directorysetting_from_settings"
}-->
```http
POST https://graph.microsoft.com/beta/settings
Content-type: application/json
Content-length: 222

{
  "templateId": "templateId-value",
  "values": [
    {
      "name": "name-value",
      "value": "value-value"
    }
  ]
}
```
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [establecer](../resources/directorysetting.md) .
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directorySetting"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 244

{
    "@odata.context": "https://graph.microsoft.com/stagingbeta/$metadata#settings/$entity",
    "id": "id-value",
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create directorySetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

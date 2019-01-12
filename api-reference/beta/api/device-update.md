---
title: Actualizar device
description: Actualizar las propiedades de un dispositivo.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 42471e32eac050b84e36477c1cd48fd06feb4244
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916379"
---
# <a name="update-device"></a>Actualizar device

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar las propiedades de un dispositivo.

Solo algunas propiedades de un dispositivo pueden actualizarse a través de aplicaciones aprobadas de administración de dispositivos móviles (MDM).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.ReadWrite.All, Directory.AccessAsUser.All |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación | No se admite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```

> Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|accountEnabled|Booleano| **true** si la cuenta está habilitada; en caso contrario, **false**. |
|operatingSystem|String|Tipo de sistema operativo del dispositivo.|
|operatingSystemVersion|String|Versión del sistema operativo del dispositivo.|
|displayName|String|Nombre para mostrar del dispositivo.|
|isCompliant|Boolean|**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**. Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows. |
|isManaged|Boolean|**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**. Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows. |

Puesto que el recurso de **dispositivo** es compatible con [las extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia de **dispositivo** existente.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "update_device"
}-->
```http
PATCH https://graph.microsoft.com/beta/devices/{id}
Content-type: application/json
Content-length: 31

{
  "accountEnabled": false
}
```
##### <a name="response"></a>Respuesta

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](/graph/extensibility-open-users)
- [Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

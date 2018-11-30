---
title: Lista los dispositivos de usuario
description: Obtener una lista de los dispositivos de usuario que admiten las capacidades de Roma de proyecto. Esto incluye la capacidad para iniciar una aplicación, o de mensajes o enviar datos a una aplicación. Una vez que se realice una llamada GET en Windows Millennium Edition / dispositivos, pase el identificador del dispositivo para enviar un comando al dispositivo.
ms.openlocfilehash: b9e6132af0e16deae1a4175bfc811f74c18e1ae6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090278"
---
# <a name="list-user-devices"></a>Lista los dispositivos de usuario

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtener una lista de los dispositivos de usuario que admiten las capacidades de Roma de proyecto. Esto incluye la capacidad para iniciar una aplicación, o de mensajes o enviar datos a una aplicación. Una vez que se realice una llamada GET en Windows Millennium Edition / dispositivos, pase el identificador del dispositivo para [Enviar un comando](send-device-command.md) al dispositivo.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | No admitida.    |
|Delegado (cuenta personal de Microsoft) | Device.Read    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET me/devices
```

## <a name="request-headers"></a>Encabezados de solicitud

| Encabezado |Valor
|:----|:------|
|Authorization| {token} de portador. Obligatorio. |
|Aceptar | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se realiza correctamente, este método devuelve un código de 200 respuesta y las propiedades de dispositivo de usuario en el cuerpo de la respuesta.

<!-- { "blockType": "ignored" } -->

```http
HTTP/1.1 200 OK
```

<!-- { "blockType": "ignored" } -->

```json
{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#devices",
  "value": [
    {
      "name": "name",
      "id": "id",
      "status": "status",
      "platform": "platform",
      "kind": "formFactor",
      "model": "model",
      "manufacturer": "manufacturer",
    }
  ]
}
```

## <a name="example"></a>Ejemplo
En este ejemplo se devolverá la lista de dispositivos para un usuario. Para el uso de un dispositivo de comando `me/devices/{id}/command`, deberá obtener el identificador del dispositivo que se devuelve.

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "ignored",
  "name": "list_devices"
}-->

```http
GET me/devices
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8
```

#### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán desde una llamada real.

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.device",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 140

{
  "value": [
    {
      "Name": "JimSurface",
      "id": "6841b3db-2b55-467b-ad84-79a41a4ef665",
      "Manufacturer": "Microsoft Corporation",
      "Model": "Surface Book",
      "Kind": "Tablet",
      "Status": "Unknown",
      "Platform": "Windows"
    }
  ]
}
```

---
title: Obtener el estado del comando de dispositivo
description: Obtener el estado de un comando en un dispositivo. Para obtener la lista completa de códigos de estado, vea la lista de actionStatus.
ms.openlocfilehash: 1e51d3b4366e87d9802518a50fe348d3ba0f250d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083023"
---
# <a name="get-device-command-status"></a>Obtener el estado del comando de dispositivo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtener el estado de un comando en un dispositivo. Para obtener la lista completa de códigos de estado, vea la [lista de actionStatus](#list-of-actionstatus).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | No admitida.    |
|Delegado (cuenta personal de Microsoft) | Device.Command    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET me/devices/{id}/commands/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Encabezado |Valor
|:----|:------|
|Authorization| {token} de portador. Obligatorio. |
|Aceptar | application/json |

## <a name="response"></a>Respuesta
<!-- { "blockType": "ignored" } -->

```http
HTTP/1.1 200 OK
```
<!-- { "blockType": "ignored" } -->

```json
  {
    "id": "0",
    "status": "requesting",
    "type": "null",
    "appServiceName": "null",
    "packageFamilyName": "null",
    "error": "null",
    "responsepayload": "null",
    "payload": "null",
    "permissionTicket": "null",
    "postBackUri": "null"
  }
```

## <a name="list-of-actionstatus"></a>Lista de actionStatus

- solicitar, / / comando se ha creado y está esperando que va a procesar
- sentToTarget, / / comando se ha enviado al dispositivo de destino
- ejecución, / / confirma la recepción del comando de dispositivo de destino y lo ejecute
- completado, / / completada la ejecución de comandos
- failedToSend, / / el servicio no pudo enviar el comando al dispositivo de destino
- executionFailed, / / error en la ejecución de comandos
- commandDropped, / / comando colocada por cliente si el dispositivo se encuentra en estado de ConnectedStandby
- Cancelar, / / cancelar el comando
- Si cancela, / / cancelar el comando
- Canceled, / / se ha cancelado el comando
- Vuelva a intentar, / / servicio está reintentando para enviar comandos al destino
- ha expirado, / / procesamiento de comandos se ha excedido el tiempo de caducidad
- error, / / interno error al procesar el comando
- personalizado / / personalizadas estado

## <a name="example"></a>Ejemplo

En este ejemplo, necesitará el identificador del dispositivo y el identificador del comando al que se ha emitido a un dispositivo. El dispositivo identificador se devuelve cuando se emite un GET llamar a `/me/devices`, y el comando identificador se devuelve cuando se realiza una devolución de llamada en `/me/devices/{id}/command`.

#### <a name="request"></a>Solicitud

En el ejemplo siguiente se muestra la solicitud.

<!-- {
  "blockType": "ignored",
  "name": "get_command"
} -->
```http
GET me/devices/{id}/commands/{id}
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8
```

#### <a name="response"></a>Respuesta

En el ejemplo siguiente se muestra la respuesta.
<!-- {
  "blockType": "ignored",
  "truncated": false,
  "@odata.type": "microsoft.graph.commandobject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK

{
  "value":
  {
    "id": "0158355AD4D680CC4E2994CC009EFFD7337D1335FCA6ED266…",
    "status": "completed",
    "type": null,
    "appServiceName": null,
    "packageFamilyName": null,
    "error": null,
    "permissionTicket": null,
    "postBackUri": null,
    "payload": null
  }
}
```


## <a name="get-command-payload"></a>Obtener la carga de comando

Obtenga una carga de respuesta para una acción específica en un dispositivo. La carga de respuesta se usa al consultar un servicio de aplicación para transportar datos atrás.


### <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | No admitida.    |
|Delegado (cuenta personal de Microsoft) | Device.Command    |
|Aplicación | No admitida. |

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET me/devices/{id}/command/{id}/responsePayload
```

### <a name="request-headers"></a>Encabezados de solicitud

| Encabezado |Valor
|:----|:------|
|Authorization| {token} de portador. Obligatorio. |
|Aceptar | application/json |

### <a name="response"></a>Respuesta
<!-- { "blockType": "ignored" } -->

```http
HTTP/1.1 200 OK
```
<!-- { "blockType": "ignored" } -->

```json
{
  "@odata.context": "https://graph.microsoft.com/devices/$metadata#microsoft.graph.PayloadResponse",
  "MsIgnoredParameter":0,
  "CreationDate":"date-time",
  "Type":"Ok"
}
```

### <a name="example"></a>Ejemplo

En este ejemplo, necesitará el identificador del dispositivo y el identificador del comando al que se ha emitido a un dispositivo. El dispositivo identificador se devuelve cuando se emite un GET llamar en `/me/devices`, y el comando identificador se devuelve cuando se realiza una devolución de llamada en `/me/devices/{id}/command`.

#### <a name="request"></a>Solicitud

En el ejemplo siguiente se muestra la solicitud.

<!-- { 
  "blockType": "ignored",
  "name": "get_command_payload"
} -->
```http
GET me/devices/{id}/commands/{id}
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8
```

#### <a name="response"></a>Respuesta

En el ejemplo siguiente se muestra la respuesta.

<!-- {
  "blockType": "ignored",
  "truncated": false,
  "@odata.type": "microsoft.graph.commandobject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK

{
  "@odata.context": "https://graph.microsoft.com/devices/$metadata#microsoft.graph.PayloadResponse",
  "MsIgnoredParameter":0,
  "CreationDate":"04/27/2017",
  "Type":"Ok"
}
```

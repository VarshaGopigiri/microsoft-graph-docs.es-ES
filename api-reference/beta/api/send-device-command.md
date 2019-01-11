---
title: Enviar comando de dispositivo
description: 'Esta API permite capacidades de Roma de proyecto a un dispositivo asociado con una cuenta de Microsoft de comando. Después de realizar una llamada GET en `me/devices`, pase el identificador del dispositivo para emitir un comando al dispositivo. Se admiten dos tipos de comandos: LaunchURI y AppServices. Si está utilizando LaunchURI, especifique los parámetros de *tipo* y la *carga* . Para una llamada AppService, especifique el '
localization_priority: Normal
ms.openlocfilehash: 54349e2f43a776523614b0cd2abbc209e89305fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891990"
---
# <a name="send-device-command"></a>Enviar comando de dispositivo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Esta API permite capacidades de Roma de proyecto a un dispositivo asociado con una cuenta de Microsoft de comando. Después de realizar una llamada GET en `me/devices`, pase el identificador del dispositivo para emitir un comando al dispositivo. Se admiten dos tipos de comandos: LaunchURI y AppServices. Si está utilizando LaunchURI, especifique los parámetros de *tipo* y la *carga* . Para una llamada AppService, especifique el *tipo de* *carga*, *packageFamilyName*, *appServiceName* los parámetros y.

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
POST me/devices/{id}/commands
```

## <a name="request-headers"></a>Encabezados de solicitud


| Encabezado |Valor
|:----|:------|
|Authorization| {token} de portador. Obligatorio. |
|Aceptar | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcionar una representación JSON de las propiedades de comando.

```json
{
  "type": "appService",
  "payload": "payload-JSON",
  "packageFamilyName": "packageFamilyName",
  "appServiceName": "appServiceName",
  "postbackURI": "postbackURI"
}
```

## <a name="response"></a>Respuesta

```http
HTTP/1.1 201 OK
```

```json
{
  "id": "0",
  "status": "requesting",
  "type": "appService",
  "appServiceName": "appServiceName",
  "packageFamilyName": "packageFamilyName",
  "error": "null",
  "responsePayload": "null",
  "payload": "payload-JSON",
  "permissionTicket": "null",
  "postBackUri": "postbackURI"
}
```
## <a name="command-properties"></a>Propiedades del comando 

|**Name**|**Tipo**|**Descripción**|
|:----|:------|:------|
|carga útil | Microsoft.Graph.JSON| Carga de enviar a un servicio de aplicación o para iniciar un identificador URI en un dispositivo. |
|responsePayload | Microsoft.Graph.JSON| Carga devuelto desde el dispositivo de destino. |
|postBackURI | Cadena | Entrada de hacer una copia de URI que se va a enviar notificaciones posteriores de actualizaciones. |
|packageFamilyName | Cadena | Nombre de familia de Windows paquete de aplicación. |
|appServiceName | Cadena | Nombre del servicio de aplicación definido por la aplicación de destino. Requerido si iniciar un servicio de aplicación. |
|type| Cadena | LaunchURI o AppService. |
|id| Cadena | El identificador de un comando que se ha enviado al dispositivo. |
|actionStatus | Cadena | El [estado](get-device-command-status.md) de un comando. |
|error| Cadena| Cualquier error asociado con la solicitud de la aplicación de destino. |

## <a name="launch-uri-example"></a>Ejemplo URI de inicio

Este es un ejemplo de una solicitud de LaunchURI; se iniciará un URI o una aplicación en el dispositivo de destino. Para iniciar un URI o una aplicación, emitir una entrada con el identificador del dispositivo (obtenida de haciendo una llamada GET en `me/devices`). Establezca los parámetros de *tipo* en *LaunchURI* y proporcione un valor URI como https://bing.com.

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "ignored",
  "name": "post_command"
} -->

```http

POST me/devices/{id}/commands
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8

{ "type" : "LaunchUri", "payload" : {"uri":"https://bing.com"}}

```

#### <a name="response"></a>Respuesta 

Aquí tiene un ejemplo de la respuesta.

<!-- {
  "blockType": "ignored",
  "truncated": false,
  "@odata.type": "microsoft.graph.commandobject",
  "isCollection": true
} -->

```http
HTTP/1.1 201 OK

{
  "id": "0158355AD4D680CC4E2994CC009EFFD7337D1B...",
  "status": "requesting",
  "type": null,
  "appServiceName": null,
  "packageFamilyName": null,
  "error": null,
  "permissionTicket": null,
  "postBackUri": null,
  "payload": {
    "uri": "https://bing.com"
  }
}

```


## <a name="app-service-example"></a>Ejemplo de aplicación de servicio

Este es un ejemplo de la consulta a un servicio de aplicación en un dispositivo. Para usar un servicio de aplicación debe realizar una llamada de entrada mediante el identificador del dispositivo (obtenida de haciendo una llamada GET en `me/devices`). Para utilizar el ejemplo siguiente, debe instalar la [aplicación de Roma](https://aka.ms/romanapp) en su dispositivo de destino.

En la llamada, se deben establecer varias propiedades adicionales. *Tipo* se debe establecer en *AppService*, *AppServiceName* debe establecerse en el nombre del servicio de aplicación definido en la aplicación, *PackageFamilyName* debe establecerse en el nombre de la familia de paquete definido en el manifiesto de la aplicación y *carga* contiene las claves y valores para el servicio que se está llamando dentro de la aplicación de destino.

#### <a name="request"></a>Solicitud

<!-- {
  "blockType": "ignored",
  "name": "post_command_2"
} -->

```http

POST me/devices/{id}/commands
Authorization: Bearer Eaeou....
Content-Type: application/json; charset=utf-8

{
  "type" : "AppService",
  "appServiceName" : "com.microsoft.test.cdppingpongservice",
  "packageFamilyName" : "5085ShawnHenry.RomanTestApp_jsjw7knzsgcce",
  "payload" : {
    "Type":"Toast","Title":"Hello","Subtitle":"World!"}
  }
```

#### <a name="response"></a>Respuesta

Este es un ejemplo de la respuesta.

<!-- {
  "blockType": "ignored",
  "truncated": false,
  "@odata.type": "microsoft.graph.commandobject",
  "isCollection": true
} -->

```http
HTTP/1.1 201 OK

{
  "id": "0158355AD4D680CC4E2994CC009EFFD7EADA8307E96FF1C8D19B..",
  "status": "requesting",
  "type": null,
  "appServiceName": "com.microsoft.randomnumbergenerator",
  "packageFamilyName": "Microsoft.SDKSamples.AppServicesProvider.CS_8wekyb3d8bbwe",
  "error": null,
  "permissionTicket": null,
  "postBackUri": null,
  "payload": {
    "Type": "Toast",
    "Title": "Hello",
    "Subtitle": "World!"
  }
}
```

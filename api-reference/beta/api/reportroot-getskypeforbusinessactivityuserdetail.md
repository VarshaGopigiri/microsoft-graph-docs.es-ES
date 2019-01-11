---
title: 'reportRoot: getSkypeForBusinessActivityUserDetail'
description: Obtiene información sobre la actividad de Skype Empresarial por usuario.
localization_priority: Normal
ms.openlocfilehash: 43bf2d7f08bc9a0033bd04f98687c7d03be5f2ea
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27872635"
---
# <a name="reportroot-getskypeforbusinessactivityuserdetail"></a>reportRoot: getSkypeForBusinessActivityUserDetail

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtiene información sobre la actividad de Skype Empresarial por usuario.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso                        | Permisos (de menos a más privilegiados) |
| :------------------------------------- | :--------------------------------------- |
| Delegado (cuenta profesional o educativa)     | Reports.Read.All                         |
| Delegado (cuenta personal de Microsoft) | No admitida.                           |
| Aplicación                            | Reports.Read.All                         |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessActivityUserDetail(period='{period_value}')
GET /reports/getSkypeForBusinessActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a>Parámetros de función

En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.

| Parámetro | Tipo   | Descripción                              |
| :-------- | :----- | :--------------------------------------- |
| period    | cadena | Especifica la duración de tiempo durante la que se agrega el informe. Los valores admitidos para {period_value} son: D7, D30, D90 y D180. Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe. |
| date      | Fecha   | Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad. {date_value} necesita tener el formato de AAAA-MM-DD. Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo. |

> **Nota:** Necesita establecer un período o una fecha en la URL.

Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta. El tipo de salida predeterminado es texto o csv. Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre          | Descripción               |
| :------------ | :------------------------ |
| Authorization | {token} de portador. Obligatorio. |

## <a name="response"></a>Respuesta

### <a name="csv"></a>CSV

Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe. La URL se encuentra en el encabezado `Location` de la respuesta.

Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.

El archivo CSV tiene los siguientes encabezados de columna.

- Fecha de actualización del informe
- Nombre principal de usuario
- Eliminado
- Fecha de eliminación
- Fecha de la última actividad
- Número total de sesiones de punto a punto
- Número total de conferencias organizadas
- Número total de conferencias en las que participó
- Fecha de la última actividad de punto a punto
- Fecha de la última actividad de una conferencia organizada
- Fecha de la última actividad de una conferencia en la que participó
- Números de mensajes instantáneos de punto a punto
- Número de sesiones de audio de punto a punto
- Minutos de audio de punto a punto
- Número de sesiones de vídeo de punto a punto
- Minutos de vídeo de punto a punto
- Número de sesiones de uso compartido de aplicaciones de punto a punto
- Número de transferencias de archivos de punto a punto
- Número de mensajes instantáneos de conferencia organizada
- Número de sesiones de audio o vídeo de conferencia organizada
- Minutos de sesiones de audio o vídeo de conferencia organizada
- Número de sesiones de uso compartido de aplicaciones se conferencia organizada
- Número de sesiones web de conferencia organizada
- Número de conferencias de acceso telefónico local o aceptación de llamada organizadas por terceros
- Número de conferencias de acceso telefónico local o aceptación de llamada organizadas por Microsoft
- Minutos de conferencias de acceso telefónico local organizadas por Microsoft
- Minutos de conferencias por aceptación de llamada organizadas por Microsoft
- Recuento de mensajería instantánea de conferencias participó
- Número de sesiones de audio o vídeo de conferencias en las que participó
- Minutos de audio o vídeo de conferencias en las que participó
- Número de sesiones de uso compartido de aplicaciones de conferencias en las que participó
- Número de sesiones web de conferencias en las que participó
- Número de conferencias de acceso telefónico local o aceptación de llamada de terceros en las que participó
- Productos asignados
- Período del informe

### <a name="json"></a>JSON

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[skypeForBusinessActivityUserDetail](../resources/skypeforbusinessactivityuserdetail.md)** en el cuerpo de la respuesta.

El tamaño de página predeterminado para esta solicitud es 200 artículos.

## <a name="example"></a>Ejemplo

### <a name="csv"></a>CSV

El siguiente es un ejemplo que muestra los resultados CSV.

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessactivityuserdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessActivityUserDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a>Respuesta

Este es un ejemplo de la respuesta.

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Is Deleted,Deleted Date,Last Activity Date,Total Peer-to-peer Session Count,Total Organized Conference Count,Total Participated Conference Count,Peer-to-peer Last Activity Date,Organized Conference Last Activity Date,Participated Conference Last Activity Date,Peer-to-peer IM Count,Peer-to-peer Audio Count,Peer-to-peer Audio Minutes,Peer-to-peer Video Count,Peer-to-peer Video Minutes,Peer-to-peer App Sharing Count,Peer-to-peer File Transfer Count,Organized Conference IM Count,Organized Conference Audio/Video Count,Organized Conference Audio/Video Minutes,Organized Conference App Sharing Count,Organized Conference Web Count,Organized Conference Dial-in/out 3rd Party Count,Organized Conference Dial-in/out Microsoft Count,Organized Conference Dial-in Microsoft Minutes,Organized Conference Dial-out Microsoft Minutes,Participated Conference IM Count,Participated Conference Audio/Video Count,Participated Conference Audio/Video Minutes,Participated Conference App Sharing Count,Participated Conference Web Count,Participated Conference Dial-in/out 3rd Party Count,Assigned Products,Report Period
```

### <a name="json"></a>JSON

El siguiente es un ejemplo que devuelve JSON.

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessactivityuserdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessActivityUserDetail(period='D7')?$format=application/json
```

#### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

> **Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.skypeForBusinessActivityUserDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1419

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.skypeForBusinessActivityUserDetail)", 
  "value": [
    {
      "totalPeerToPeerSessionCount": 12, 
      "totalOrganizedConferenceCount": 0, 
      "totalParticipatedConferenceCount": 1, 
      "peerToPeerLastActivityDate": "2017-09-01", 
      "organizedConferenceLastActivityDate": null, 
      "participatedConferenceLastActivityDate": "2017-08-31", 
      "peerToPeerIMCount": 12, 
      "peerToPeerAudioCount": 0, 
      "peerToPeerAudioMinutes": 0, 
      "peerToPeerVideoCount": 0, 
      "peerToPeerVideoMinutes": 0, 
      "peerToPeerAppSharingCount": 0, 
      "peerToPeerFileTransferCount": 0, 
      "organizedConferenceIMCount": 0, 
      "organizedConferenceAudioVideoCount": 0, 
      "organizedConferenceAudioVideoMinutes": 0, 
      "organizedConferenceAppSharingCount": 0, 
      "organizedConferenceWebCount": 0, 
      "organizedConferenceDialInOut3rdPartyCount": 0, 
      "organizedConferenceCloudDialInOutMicrosoftCount": 0, 
      "organizedConferenceCloudDialInMicrosoftMinutes": 0, 
      "organizedConferenceCloudDialOutMicrosoftMinutes": 0, 
      "participatedConferenceIMCount": 0, 
      "participatedConferenceAudioVideoCount": 1, 
      "participatedConferenceAudioVideoMinutes": 69, 
      "participatedConferenceAppSharingCount": 0, 
      "participatedConferenceWebCount": 0, 
      "participatedConferenceDialInOut3rdPartyCount": 0, 
      "reportRefreshDate": "2017-09-06", 
      "userPrincipalName": "userPrincipalName-value", 
      "isDeleted": false, 
      "deletedDate": null, 
      "lastActivityDate": "2017-09-01", 
      "assignedProducts": [
        "OFFICE 365 ENTERPRISE E5", 
      ], 
      "reportPeriod": "7"
    }
  ]
}
```

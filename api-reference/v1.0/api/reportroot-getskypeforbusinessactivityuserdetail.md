---
title: 'reportRoot: getSkypeForBusinessActivityUserDetail'
description: Obtiene información sobre la actividad de Skype Empresarial por usuario.
ms.openlocfilehash: c5bc32441b65bf55ff5114c161bd9a85bf795fbe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032540"
---
# <a name="reportroot-getskypeforbusinessactivityuserdetail"></a>reportRoot: getSkypeForBusinessActivityUserDetail

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

<!-- { "blockType": "samples" } --> 

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

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre          | Descripción                              |
| :------------ | :--------------------------------------- |
| Authorization | {token} de portador. Obligatorio.                |
| If-None-Match | Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`. Opcional. |

## <a name="response"></a>Respuesta

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
- Número de mensajes instantáneos de conferencias en la que participó
- Número de sesiones de audio o vídeo de conferencias en las que participó
- Minutos de audio o vídeo de conferencias en las que participó
- Número de sesiones de uso compartido de aplicaciones de conferencias en las que participó
- Número de sesiones web de conferencias en las que participó
- Número de conferencias de acceso telefónico local o aceptación de llamada de terceros en las que participó
- Productos asignados
- Período del informe

## <a name="example"></a>Ejemplo

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessActivityUserDetail(period='D7')
```

#### <a name="response"></a>Respuesta

Este es un ejemplo de la respuesta.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Is Deleted,Deleted Date,Last Activity Date,Total Peer-to-peer Session Count,Total Organized Conference Count,Total Participated Conference Count,Peer-to-peer Last Activity Date,Organized Conference Last Activity Date,Participated Conference Last Activity Date,Peer-to-peer IM Count,Peer-to-peer Audio Count,Peer-to-peer Audio Minutes,Peer-to-peer Video Count,Peer-to-peer Video Minutes,Peer-to-peer App Sharing Count,Peer-to-peer File Transfer Count,Organized Conference IM Count,Organized Conference Audio/Video Count,Organized Conference Audio/Video Minutes,Organized Conference App Sharing Count,Organized Conference Web Count,Organized Conference Dial-in/out 3rd Party Count,Organized Conference Dial-in/out Microsoft Count,Organized Conference Dial-in Microsoft Minutes,Organized Conference Dial-out Microsoft Minutes,Paricipated Conference IM Count,Participated Conference Audio/Video Count,Participated Conference Audio/Video Minutes,Participated Conference App Sharing Count,Participated Conference Web Count,Participated Conference Dial-in/out 3rd Party Count,Assigned Products,Report Period
```

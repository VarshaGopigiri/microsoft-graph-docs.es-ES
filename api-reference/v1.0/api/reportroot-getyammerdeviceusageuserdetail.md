---
title: 'reportRoot: función getYammerDeviceUsageUserDetail'
description: Obtiene información sobre el uso de dispositivos de Yammer por usuario.
ms.openlocfilehash: c112ba0948adb07dbb5264ab73f6458f2ef97b09
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030759"
---
# <a name="reportroot-getyammerdeviceusageuserdetail-function"></a>reportRoot: función getYammerDeviceUsageUserDetail

Obtiene información sobre el uso de dispositivos de Yammer por usuario.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de dispositivos de Yammer](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).

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
GET /reports/getYammerDeviceUsageUserDetail(period='{period_value}')
GET /reports/getYammerDeviceUsageUserDetail(date={date_value})
```

## <a name="function-parameters"></a>Parámetros de función

En la URL de la solicitud, especifique el parámetro de consulta seleccionado con un valor válido.

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
- Nombre para mostrar
- Estado del usuario
- Fecha de cambio de estado
- Fecha de la última actividad
- Web usada
- Windows Phone usado
- Teléfono Android usado
- iPhone usado
- iPad usado
- Otros usados
- Período del informe

## <a name="example"></a>Ejemplo

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getyammerdeviceusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerDeviceUsageUserDetail(period='D7')
```

#### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.report" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

#### <a name="request"></a>Solicitud

Si se llama a con el `date` parámetro, el informe se limita al uso en la fecha determinada.

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getyammerdeviceusageuserdetail_date"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerDeviceUsageUserDetail(date='2018-03-05')
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

Report Refresh Date,User Principal Name,Display Name,User State,State Change Date,Last Activity Date,Used Web,Used Windows Phone,Used Android Phone,Used iPhone,Used iPad,Used Others,Report Period
```

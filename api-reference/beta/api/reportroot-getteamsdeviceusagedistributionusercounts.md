---
title: 'reportRoot: getTeamsDeviceUsageDistributionUserCounts'
description: Obtenga el número de usuarios únicos de Microsoft Teams por tipo de dispositivo durante el período de tiempo seleccionado.
ms.openlocfilehash: b2416b8a4aa257f49807efb3f320fcf16cea4920
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088699"
---
# <a name="reportroot-getteamsdeviceusagedistributionusercounts"></a>reportRoot: getTeamsDeviceUsageDistributionUserCounts

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtenga el número de usuarios únicos de Microsoft Teams por tipo de dispositivo durante el período de tiempo seleccionado.

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
GET /reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')
```

## <a name="function-parameters"></a>Parámetros de función

En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.

| Parámetro | Tipo   | Descripción                              |
| :-------- | :----- | :--------------------------------------- |
| period    | cadena | Especifica la duración de tiempo durante la que se agrega el informe. Los valores admitidos para {period_value} son: D7, D30, D90 y D180. Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe. Necesario. |

Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta. El tipo de salida predeterminado es texto o csv. Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.

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
- Web
- Windows Phone
- Teléfono Android
- iOS
- Mac
- Windows
- Período del informe

### <a name="json"></a>JSON

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[teamsDeviceUsageDistributionUserCounts](../resources/teamsdeviceusagedistributionusercounts.md)** en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="csv"></a>CSV

El siguiente es un ejemplo que muestra los resultados CSV.

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusagedistributionusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')?$format=text/csv
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

Report Refresh Date,Web,Windows Phone,Android Phone,iOS,Mac,Windows,Report Period
```

### <a name="json"></a>JSON

El siguiente es un ejemplo que devuelve JSON.

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusagedistributionusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

> **Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamsDeviceUsageDistributionUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 243

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.teamsDeviceUsageDistributionUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "web": 51, 
      "windowsPhone": 2, 
      "androidPhone": 34, 
      "ios": 76, 
      "mac": 40, 
      "windows": 491, 
      "reportPeriod": "7"
    }
  ]
}
```

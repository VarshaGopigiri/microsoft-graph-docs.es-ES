---
title: Respuestas de error de la API de seguridad de Microsoft Graph
description: Errores en la API de seguridad de Microsoft Graph se devuelven mediante el código de estado HTTP 206 parcial contenido estándar y se entregan a través de un encabezado de advertencia.
author: Preetikr
ms.openlocfilehash: 6685d69f202696e33422d9bd3a877cba02fd10dd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334422"
---
# <a name="microsoft-graph-security-api-error-responses"></a>Respuestas de error de la API de seguridad de Microsoft Graph

Errores en la API de seguridad de Microsoft Graph se devuelven mediante el código de estado HTTP 206 parcial contenido estándar y se entregan a través de un encabezado de advertencia.

## <a name="errors"></a>Errores

La API de seguridad de Microsoft Graph es un servicio federado que recibe varias respuestas de todos los proveedores de datos. Cuando se recibe un error HTTP por la API de seguridad de Microsoft Graph, bien va a volver a enviar un encabezado de advertencia en el siguiente formato:<!-- { "blockType": "ignored" } -->

```http
{Vendor}/{Provider}/{StatusCode}/{LatencyInMs}
```

Este encabezado de advertencia sólo se envía a los clientes cuando uno de los proveedores de datos devuelve un código de error que no sean 2xx o 404. Por ejemplo:

- Es posible que se devuelva HttpStatusCode.Forbidden (403) si no se concede el acceso al recurso.
- Si un proveedor de tiempo de espera, se devuelve HttpStatusCode.GatewayTimeout (504) en el encabezado de advertencia.
- Si se produce un error interno del proveedor, se usa HttpStatusCode.InternalServerError (500) en el encabezado de advertencia.

Si un proveedor de datos devuelve 2xx o 404, no se muestra en el encabezado de advertencia debido a que se esperan que estos códigos para el éxito o cuando no se encontraron datos respectivamente. En un sistema federado, se prevé un error 404 no se encontró como número de veces que los datos sólo se conocen a uno o varios, pero no todos los proveedores.

## <a name="example"></a>Ejemplo

Un usuario solicita `security/alerts/{alert_id}`.

    Provider 1: 404 (provider does not have a record of this alert ID)
    Provider 2: 504 (provider timed out)
    Provider 3: 200 (success)
    Provider 4: 403 (customer has not licensed this provider)

Dado que 404 y 200 son las condiciones previstas, el encabezado de advertencia contiene lo siguiente:

```HTTP
Warning : 199 - "{Vendor2}/{Provider 2}/504/10000",    (usual timeout limit is set at 10 seconds)
          199 - "{Vendor4}/{Provider 4}/403/10"       (Provider 4 rejected the request in 10 ms)
```

> **Nota:** Cada encabezado HTTP es una colección de subelementos, por lo que los usuarios pueden enumerar el encabezado de advertencia y compruebe todos los elementos.

## <a name="constraints"></a>Restricciones

El `$top` parámetro de consulta de OData tiene un límite de 1000 alertas y una combinación de `$top`  +  `$skip` parámetros no pueden superar los 6000 alertas de consulta de OData. Por ejemplo, `/security/alerts?$top=10&$skip=5990` devolverá un `200 OK` código de respuesta, pero `/security/alerts?$top=10&$skip=5991` devolverá un `400 Bad Request` código de respuesta.

Una solución alternativa para este límite es usar el `$filter` parámetro de consulta de OData con la `eventDateTime` de la entidad de alerta de la API de seguridad de Microsoft Graph, con `?$filter=eventDateTime gt {YYYY-MM-DDT00:00:00.000Z}` y reemplazar el valor de fecha y hora con la última alerta (6000th). También puede establecer un intervalo para la `eventDateTime`; Por ejemplo, *filtro de $ alerts? = eventDateTime **gt** 2018-11 -**11**T00:00:00.000Z & eventDateTime **lt** 2018-11 -**12**T00:00:00.000Z*

## <a name="see-also"></a>Vea también

Si tiene problemas con la autorización, vea [autorización y la API de seguridad de Microsoft Graph](/graph/security-authorization).

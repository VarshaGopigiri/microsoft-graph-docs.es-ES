---
title: Respuestas de error de la API de seguridad de Microsoft Graph
description: Errores en la API de seguridad de Microsoft Graph se devuelven mediante código de estado HTTP 206 parcial contenido estándar y se entregan por medio de un encabezado de advertencia.
ms.openlocfilehash: a67023a8a21687e357e6b6eff1ffa47f026ccd68
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084946"
---
# <a name="microsoft-graph-security-api-error-responses"></a>Respuestas de error de la API de seguridad de Microsoft Graph

Errores en la API de seguridad de Microsoft Graph se devuelven mediante código de estado HTTP 206 parcial contenido estándar y se entregan por medio de un encabezado de advertencia.

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

Un usuario solicita `/alerts/{alert-id}`.

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

## <a name="see-also"></a>Vea también

Si tiene problemas con la autorización, consulte nuestro [blog post](https://techcommunity.microsoft.com/t5/Using-Microsoft-Graph-Security/Authorization-and-Microsoft-Graph-Security-API/m-p/184376#M2).

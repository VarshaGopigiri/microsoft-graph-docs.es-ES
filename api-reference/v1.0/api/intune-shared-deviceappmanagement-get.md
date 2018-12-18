---
title: Obtener deviceAppManagement
description: Lea las propiedades y las relaciones del objeto deviceAppManagement.
author: tfitzmac
ms.openlocfilehash: 269e749c7fae0b2eeb397d86907a7cf2d6653ee7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314199"
---
# <a name="get-deviceappmanagement"></a>Obtener deviceAppManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).

## <a name="prerequisites"></a>Requisitos previos

Uno de los siguientes permisos se requiere para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).  Tenga en cuenta que el permiso adecuado varía según el flujo de trabajo.

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All |
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) en el cuerpo de la respuesta.

## <a name="example-request"></a>Ejemplo de solicitud

``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement
```

## <a name="example-response"></a>Respuesta de ejemplo
El objeto de respuesta que se muestra aquí es posible que esté truncado por razones de brevedad. Se devolverán todas las propiedades de una llamada real.

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 133

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceAppManagement",
    "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
  }
}
```




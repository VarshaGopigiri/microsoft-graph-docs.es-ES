---
title: Obtener usuario
description: Lea las propiedades y las relaciones del objeto user.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ccdcc272a0fa92e56d271d4befdd18629913f80d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991249"
---
# <a name="get-user"></a>Obtener usuario

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Lea las propiedades y las relaciones del objeto [user](../resources/intune-shared-user.md).
## <a name="prerequisites"></a>Requisitos previos
Uno de los siguientes permisos se requiere para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).  El permiso específico depende del contexto.

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)| _varía según el contexto_|
| &nbsp;&nbsp; Administración de dispositivos | DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All |
| &nbsp;&nbsp; MAM | DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All |
| &nbsp;&nbsp; Incorporación | DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All |
| &nbsp;&nbsp; Solución de problemas | DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All |
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/intune-shared-user.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

``` http
GET https://graph.microsoft.com/v1.0/users/{usersId}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 118

{
  "value": {
    "@odata.type": "#microsoft.graph.user",
    "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
  }
}
```




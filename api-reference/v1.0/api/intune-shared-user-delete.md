---
title: Eliminar usuario
description: Elimina un user.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: cc1979284cada76f76a98acc8956271b7224aa53
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837838"
---
# <a name="delete-user"></a>Eliminar usuario

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Elimina un [user](../resources/intune-shared-user.md).
## <a name="prerequisites"></a>Requisitos previos
Uno de los siguientes permisos se requiere para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).  Los permisos específicos necesarios depende de contexto.

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)| _varía según el contexto_|
| &nbsp;&nbsp; Dispositivos | DeviceManagementManagedDevices.ReadWrite.All |
| &nbsp;&nbsp; MAM | DeviceManagementApps.ReadWrite.All |
| &nbsp;&nbsp; Incorporación | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp;&nbsp; Solución de problemas | DeviceManagementManagedDevices.ReadWrite.All |
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /users/{usersId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

``` http
DELETE https://graph.microsoft.com/v1.0/users/{usersId}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

``` http
HTTP/1.1 204 No Content
```




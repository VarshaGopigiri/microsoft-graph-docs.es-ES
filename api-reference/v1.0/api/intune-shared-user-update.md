---
title: Actualizar usuario
description: Actualiza las propiedades de un objeto de usuario.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 455a3e0c68fadc9768c434f5893dbc950a371bab
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922525"
---
# <a name="update-user"></a>Actualizar usuario

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [user](../resources/intune-shared-user.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)| _varía según el contexto_|
| &nbsp;&nbsp; Administración de dispositivos | DeviceManagementManagedDevices.ReadWrite.All |
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
PATCH /users/{usersId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [user](../resources/intune-shared-user.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [user](../resources/intune-shared-user.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único del usuario.|
|**Incorporación de redes**|
|deviceEnrollmentLimit|Int32|El límite del número máximo de dispositivos que el usuario puede inscribir. Los valores permitidos son 5 o 1000.|

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/intune-shared-user.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

``` http
PATCH https://graph.microsoft.com/v1.0/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```




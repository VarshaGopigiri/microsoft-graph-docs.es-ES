---
title: Acción syncMicrosoftStoreForBusinessApps
description: Sincroniza la cuenta de Intune con Microsoft Store para Empresas
ms.openlocfilehash: a293c170dea23469b12a8862b8510fe8ce67be41
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030613"
---
# <a name="syncmicrosoftstoreforbusinessapps-action"></a>Acción syncMicrosoftStoreForBusinessApps

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Sincroniza la cuenta de Intune con Microsoft Store para Empresas
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)| 
| &nbsp;&nbsp; _Incorporación_ | DeviceManagementApps.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.

## <a name="example-request"></a>Ejemplo de solicitud

``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

### <a name="response"></a>Respuesta

El objeto de respuesta que se muestra aquí es posible que esté truncado por razones de brevedad. Todas las propiedades se devolverán desde una llamada real.

``` http
HTTP/1.1 204 No Content
```




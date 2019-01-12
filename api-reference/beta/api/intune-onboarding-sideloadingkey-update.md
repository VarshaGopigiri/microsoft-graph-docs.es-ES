---
title: Actualizar sideLoadingKey
description: Actualizar las propiedades de un objeto sideLoadingKey.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 116034afff02ac41647d781bbd85ec6f8dcaeec4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969936"
---
# <a name="update-sideloadingkey"></a>Actualizar sideLoadingKey

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementServiceConfig.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/sideLoadingKeys/{sideLoadingKeyId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Lado cargar clave identificador único.|
|valor|String|Valor de clave de carga del lado, es valor de 5 x 5, separados por hiphens.|
|displayName|String|Lado carga de clave de nombre que se muestra a la ITPro Admins.|
|descripción|String|Clave de carga de descripción en el que se muestra a la ITPro Admins..|
|totalActivation|Int32|Lado carga Total activación de la clave que se muestra a la ITPro Admins.|
|lastUpdatedDateTime|String|Lado cargar clave última actualizado fecha que se muestra a la ITPro Admins.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/sideLoadingKeys/{sideLoadingKeyId}
Content-type: application/json
Content-length: 193

{
  "value": "Value value",
  "displayName": "Display Name value",
  "description": "Description value",
  "totalActivation": 15,
  "lastUpdatedDateTime": "Last Updated Date Time value"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 295

{
  "@odata.type": "#microsoft.graph.sideLoadingKey",
  "id": "21c4a3ff-a3ff-21c4-ffa3-c421ffa3c421",
  "value": "Value value",
  "displayName": "Display Name value",
  "description": "Description value",
  "totalActivation": 15,
  "lastUpdatedDateTime": "Last Updated Date Time value"
}
```






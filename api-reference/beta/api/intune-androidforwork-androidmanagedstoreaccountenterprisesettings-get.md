---
title: Obtener androidManagedStoreAccountEnterpriseSettings
description: Leer las propiedades y las relaciones del objeto androidManagedStoreAccountEnterpriseSettings.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 07478ab9ddab3aa2a8be43bc65ef713ca8f80f7c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950658"
---
# <a name="get-androidmanagedstoreaccountenterprisesettings"></a>Obtener androidManagedStoreAccountEnterpriseSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Leer las propiedades y las relaciones del objeto [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/androidManagedStoreAccountEnterpriseSettings
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/androidManagedStoreAccountEnterpriseSettings
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 635

{
  "value": {
    "@odata.type": "#microsoft.graph.androidManagedStoreAccountEnterpriseSettings",
    "id": "b71357c9-57c9-b713-c957-13b7c95713b7",
    "bindStatus": "bound",
    "lastAppSyncDateTime": "2016-12-31T23:57:22.8606813-08:00",
    "lastAppSyncStatus": "credentialsNotValid",
    "ownerUserPrincipalName": "Owner User Principal Name value",
    "ownerOrganizationName": "Owner Organization Name value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "enrollmentTarget": "all",
    "targetGroupIds": [
      "Target Group Ids value"
    ],
    "deviceOwnerManagementEnabled": true
  }
}
```






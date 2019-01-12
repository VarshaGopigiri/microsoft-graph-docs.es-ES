---
title: Crear telecomExpenseManagementPartner
description: Cree un objeto telecomExpenseManagementPartner.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ca3a94da0c908bec0af44075dcb15b6fa4f007a9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984804"
---
# <a name="create-telecomexpensemanagementpartner"></a>Crear telecomExpenseManagementPartner

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Cree un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).
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
POST /deviceManagement/telecomExpenseManagementPartners
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto telecomExpenseManagementPartner.

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto telecomExpenseManagementPartner.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único del partner de TEM.|
|displayName|Cadena|Nombre para mostrar del partner de TEM.|
|url|Cadena|Dirección URL del panel de control administrativo del partner de TEM, donde un administrador puede configurar el servicio de su TEM.|
|appAuthorized|Booleano|Si se ha autorizado a la aplicación de AAD del partner para que obtenga acceso a Intune.|
|enabled|Booleano|Si la conexión de Intune al servicio de TEM está habilitada o deshabilitada.|
|lastConnectionDateTime|DateTimeOffset|Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/telecomExpenseManagementPartners
Content-type: application/json
Content-length: 248

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 297

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "id": "47a3b399-b399-47a3-99b3-a34799b3a347",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```




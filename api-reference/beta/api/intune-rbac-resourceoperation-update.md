---
title: Actualizar resourceOperation
description: Actualice las propiedades de un objeto resourceOperation.
author: tfitzmac
ms.openlocfilehash: 8050b91aee679f9dd29e78cbbad62f9f6352343e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317825"
---
# <a name="update-resourceoperation"></a>Actualizar resourceOperation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementRBAC.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/resourceOperations/{resourceOperationId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la operación de recursos. Solo lectura, generada automáticamente.|
|resource|String|Categoría de recurso al que pertenece esta operación.|
|resourceName|String|Nombre del recurso en el que se realiza esta operación.|
|actionName|String|Tipo de acción que va a realizar esta operación. El actionName debe ser conciso y limitado al menor número de palabras posible.|
|description|String|Descripción de la operación de recursos. La descripción se usa en el texto al pasar el mouse para la operación si se muestra en Azure Portal.|
|enabledForScopeValidation|Boolean|Determina si el permiso se valida para ámbitos definidos por la asignación de roles.|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/resourceOperations/{resourceOperationId}
Content-type: application/json
Content-length: 193

{
  "resource": "Resource value",
  "resourceName": "Resource Name value",
  "actionName": "Action Name value",
  "description": "Description value",
  "enabledForScopeValidation": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 298

{
  "@odata.type": "#microsoft.graph.resourceOperation",
  "id": "232b8fee-8fee-232b-ee8f-2b23ee8f2b23",
  "resource": "Resource value",
  "resourceName": "Resource Name value",
  "actionName": "Action Name value",
  "description": "Description value",
  "enabledForScopeValidation": true
}
```






---
title: Crear managementConditionStatement
description: Crear un nuevo objeto managementConditionStatement.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0c884f1b7239dc2f73438c007202ab783a5bdf1d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919158"
---
# <a name="create-managementconditionstatement"></a>Crear managementConditionStatement

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crear un nuevo objeto [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/managementConditionStatements
POST /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto managementConditionStatement.

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el managementConditionStatement.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único de la instrucción de condición de administración. Valor asignado al crear generada por el sistema.|
|displayName|Cadena|El nombre definido de administración de la instrucción de condición de administración.|
|descripción|Cadena|El administrador define la descripción de la instrucción de condición de administración.|
|createdDateTime|DateTimeOffset|La hora en que se creó la instrucción de condición de administración. Servicio generado al lado.|
|modifiedDateTime|DateTimeOffset|La hora en que se modificó por última vez la instrucción de condición de administración. Se actualizó el lado de servicio.|
|expresión|[managementConditionExpression](../resources/intune-fencing-managementconditionexpression.md)|La expresión de instrucción de condición de administración que se usa para evaluar si una administración condición instrucción estaba activada o desactivada.|
|eTag|Cadena|ETag de la instrucción de condición de administración. Se actualizó el lado de servicio.|
|applicablePlatforms|colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)|Las plataformas aplicables para esta instrucción de condición de administración.
Esto se calcula a partir de ¿está buscando las condiciones de administración asociadas a la administración de la condición de la instrucción y buscar la intersección de plataformas aplicables. Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/managementConditionStatements
Content-type: application/json
Content-length: 323

{
  "@odata.type": "#microsoft.graph.managementConditionStatement",
  "displayName": "Display Name value",
  "description": "Description value",
  "expression": {
    "@odata.type": "microsoft.graph.managementConditionExpression"
  },
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ]
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 491

{
  "@odata.type": "#microsoft.graph.managementConditionStatement",
  "id": "bedb0c00-0c00-bedb-000c-dbbe000cdbbe",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "expression": {
    "@odata.type": "microsoft.graph.managementConditionExpression"
  },
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ]
}
```






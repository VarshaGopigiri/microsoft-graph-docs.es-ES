---
title: Actualizar governanceRoleSetting
description: Actualizar las propiedades de governanceRoleSetting.
ms.openlocfilehash: 2d9417c99e63b1b4c7302c2afdda4c272b2fce82
ms.sourcegitcommit: 82f9d0d10388572a3073b2dde8ca0a7b409135b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/07/2018
ms.locfileid: "27191119"
---
# <a name="update-governancerolesetting"></a>Actualizar governanceRoleSetting

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar las propiedades de [governanceRoleSetting](../resources/governancerolesetting.md).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

>**Nota:** Esta API también requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.

|Tipo de permiso      | Permisos              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | PrivilegedAccess.ReadWrite.AzureResources  |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | PrivilegedAccess.ReadWrite.AzureResources |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /privilegedAccess/azureResources/roleSettings/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:-----------|:-----------|
| Autorización  | Portador {código}|
| Tipo de contenido  | application/json|


## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporciona los valores para [governanceRuleSettings](../resources/governancerulesetting.md) que necesitan actualizarse. 

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|adminEligibleSettings|[governanceRuleSetting](../resources/governancerulesetting.md)|La configuración de la regla que se evalúa cuando un administrador intenta agregar una asignación de rol aptos.|
|adminMemberSettings|[governanceRuleSetting](../resources/governancerulesetting.md)|La configuración de la regla que se evalúa cuando un administrador intenta agregar una asignación de rol miembro directo.|
|userEligibleSettings|[governanceRuleSetting](../resources/governancerulesetting.md)|La configuración de la regla que se evalúa cuando un usuario intenta agregar una asignación de rol optan. Esto no es compatible con `pimforazurerbac` escenario por ahora y pueden estar disponibles en las situaciones futuras.|
|userMemberSettings|[governanceRuleSetting](../resources/governancerulesetting.md)|La configuración de la regla que se evalúa cuando un usuario intenta activar su asignación de roles.|

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `204 NoContent`. No devuelve nada en el cuerpo de la respuesta. 

### <a name="error-codes"></a>Códigos de error
Esta API devuelve los códigos de error HTTP estándares. Además, devuelve los siguientes códigos de error personalizado.

|Código de error     | Mensaje de error         | Detalles             |
|:--------------| :---------------------|:--------------------|
| 400 BadRequest| RoleSettingNotFound   | La [governanceRoleSetting](../resources/governancerolesetting.md) no existe en el sistema.
| 400 BadRequest| InvalidRoleSetting    | Los valores de [governanceRuleSettings](../resources/governancerulesetting.md) proporcionados en el cuerpo de la solicitud no son válidos.

## <a name="example"></a>Ejemplo 
En este ejemplo se actualiza la configuración de rol para 3 de rol personalizada en la suscripción Wingtip Toys - Prod.
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "update_governancerolesetting"
}-->
```http
PATCH https://graph.microsoft.com/beta/privilegedAccess/pimforazurerbac/roleSettings/5fb5aef8-1081-4b8e-bb16-9d5d0385bab5
Content-type: application/json
Content-length: 350

{
  "adminEligibleSettings":[{"ruleIdentifier":"ExpirationRule","setting":"{\"permanentAssignment\":false,\"maximumGrantPeriodInMinutes\":129600}"}]
}
```
##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update governanceRoleSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

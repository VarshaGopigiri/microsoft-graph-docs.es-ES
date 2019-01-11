---
title: tipo de recurso secureScoreControlProfiles
description: Representa la puntuación de seguro de un inquilino por los datos del control. De forma predeterminada, devuelve todos los controles de un inquilino y puede extraer explícitamente los controles individuales.
localization_priority: Normal
ms.openlocfilehash: 866b2086ff5160744f848292cedf30c3cedf6daa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866223"
---
# <a name="securescorecontrolprofiles-resource-type"></a>tipo de recurso secureScoreControlProfiles

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la puntuación de seguro de un inquilino por los datos del control. De forma predeterminada, devuelve todos los controles de un inquilino y puede extraer explícitamente los controles individuales.


## <a name="methods"></a>Métodos

| Método   | Tipo de valor devuelto|Descripción|
|:---------------|:--------|:----------|
|[Lista secureScoreControlProfiles](../api/securescorecontrolprofiles-list.md) | [secureScoreControlProfiles](securescorecontrolprofiles.md) |Lea las propiedades y los metadatos de un objeto secureScoreControlProfiles.|


## <a name="properties"></a>Propiedades

|Nombre |Tipo |Description |
|:--|:--|:--|
|   azureTenantId   |   Cadena  |   Identificador de cadena GUID para el inquilino.  |
|   controlName |   Cadena  |   Nombre del control. |
|   title   |   Cadena  |   Título del control.   |
| complianceInformation | colección de [complianceInformation](complianceinformation.md) | La recopilación de información de cumplimiento de normas asociado con garantizar el control de puntuación |
|   controlCategory |   Cadena  |   Categoría de acción de control (cuenta, datos, dispositivos, aplicaciones, infraestructura).  |
|   actionType  |   String  |   Controlar el tipo de acción (Config, revisión, comportamiento). |
|   service |   Cadena  |   Servicio que posee el control (Exchange, Sharepoint, Azure AD). |
|   maxScore |  Cadena  |   Actual había obtenido puntuación máxima en la fecha especificada.   |
|   nivel |  Cadena  |   Nivel de control (doble núcleo, la estrategia de defensa en profundidad, avanzada.)    |
|   userImpact |    Cadena  | Impacto de usuario de la implementación de control (bajo, moderado, alta).    |
|   implementationCost |    Cadena  |   Costo de recurso de control de implemmentating (bajo, moderado, alta). |
|   rank |  Int32   |   Pila de Microsoft de clasificación de control.   |
|   amenazas |   Colección de cadenas   |   Lista de las amenazas que mitiga el control (accountBreach, dataDeletion, dataExfiltration, dataSpillage, elevationOfPrivilege, maliciousInsider, passwordCracking, phishingOrWhaling, suplantación de identidad). |
|   en desuso |    Booleano |   Marcar para indicar si se ha eliminado un control.   |
|   corrección |   Cadena  |   Descripción de lo que el control le ayudará a corregir. |
|   remediationImpact | Cadena  |   Descripción del impacto en los usuarios de la corrección. |
|   actionUrl | Cadena  |   Dirección URL donde el control puede ser ejecutado. |
|   controlStateUpdates |   colección de [secureScoreControlStateUpdate](securescorecontrolstateupdate.md) |    Marca para indicar que el inquilino ha marcado un control (omitir, otros, revisado) (admite [Actualizar](../api/securescorecontrolprofiles-update.md)). |

## <a name="relationships"></a>Relaciones

Ninguna.

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.secureScores"
}-->

```json
{
"title": "String", 
"azureTenantId": "Guid", 
"referenceId": "String", 
"controlName": "String", 
"maxScore": "Int32",
"actionCategory": "Collection(microsoft.graph.SecureScore.actionCategory)",
"actionType": "Collection(microsoft.graph.SecureScore.actionType)",
"service": "String",
"tier": "Collection(microsoft.graph.SecureScore.tier)",
"userImpact": "Collection(microsoft.graph.SecureScore.ranking)",
"implementationCost ": "Collection(microsoft.graph.SecureScore.ranking)",
"rank ": "Int32",
"threats": "Collection(microsoft.graph.SecureScore.threat)",
"deprecated ": "Boolean",
"remediation": "String",
"remediationImpact ": "String",
"actionUrl": "String",
"controlStateUpdates": "Collection(microsoft.graph.SecureScore.controlStateUpdates)",
"tenantNotes": "String",
"upn": "String",
"comments": "String",
}


```


<!-- {
  "type": "#page.annotation",
  "description": "secureScoreControlProfiles resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

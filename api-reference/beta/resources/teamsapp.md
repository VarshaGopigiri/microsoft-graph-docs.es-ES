---
title: tipo de recurso teamsApp
description: Una aplicación en el catálogo de aplicaciones de Microsoft Teams.
ms.openlocfilehash: bb9081306cbcc5d8537c86e7f3f59afff89a03b0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086149"
---
# <a name="teamsapp-resource-type"></a>tipo de recurso teamsApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una aplicación en el catálogo de aplicaciones de [Los equipos de Microsoft](teams-api-overview.md) .

Los usuarios pueden ver estas aplicaciones en la Store Teams Microsoft, y estas aplicaciones se pueden instalar en [los equipos](team.md) mediante el método de [aplicación de agregar al equipo](../api/teamsappinstallation-add.md) .

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Lista de aplicaciones publicadas](../api/teamsapp-list.md) | colección de [teamsApp](teamsapp.md) | Lista de aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams.|
|[Publicar una aplicación](../api/teamsapp-publish.md) | [teamsApp](teamsapp.md) | Publicar una aplicación al catálogo de aplicaciones de la organización.|
|[Actualizar una aplicación publicada](../api/teamsapp-update.md) | [teamsApp](teamsapp.md) | Actualizar una aplicación publicada en el catálogo de aplicaciones de la organización.|
|[Quitar una aplicación publicada](../api/teamsapp-delete.md) | Ninguno | Quitar una aplicación publicada de catálogo de aplicaciones de la organización.|

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo     | Descripción |
|:------------------- |:-------- |:----------- |
| id                  | string   | La aplicación de catálogo genera el identificador de la aplicación (diferente desde el identificador proporcionado para desarrolladores en el [paquete de la aplicación de los equipos de Microsoft zip](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package). |
| externalId          | string   | El identificador del catálogo proporcionado por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package). |
| displayName                | string   | El nombre de la aplicación de catálogo proporcionada por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package). |
| distributionMethod  | teamsAppDistributionMethod     | El método de distribución para la aplicación. |

### <a name="teamsappdistributionmethod-values"></a>valores de teamsAppDistributionMethod

|Member|Valor|Descripción|
|:---|:---|:---|
|almacén|0| La aplicación está disponible para todos los inquilinos a través de la tienda de aplicaciones Microsoft Teams.|
|organización|1|La aplicación sólo está disponible en este inquilino.|
|sideloaded|2|La aplicación sólo está disponible para el usuario o equipo instalado a.|

## <a name="relationships"></a>Relaciones

| Relación | Tipo   | Descripción |
|:---------------|:--------|:----------|
|appDefinitions|colección de [teamsAppDefinition](teamsappdefinition.md)| Los detalles de cada versión de la aplicación. |

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsApp",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string",
  "externalId": "string",
  "displayName": "Test App",
  "distributionMethod": "Organization"
}
```

# <a name="see-also"></a>Vea también

- [teamsAppInstallation](teamsappinstallation.md)
- [teamsAppDefinition](teamsappdefinition.md)
- [teamsTab](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


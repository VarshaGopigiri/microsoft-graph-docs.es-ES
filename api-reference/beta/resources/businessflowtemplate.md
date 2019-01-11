---
title: tipo de recurso businessFlowTemplate
description: En el anuncio de Azure access revisa la característica, el `businesFlowTemplate` representa una plantilla de flujo de profesionales de Azure AD. El identificador de una plantilla, por ejemplo, para revisar a los miembros de invitado de un grupo, se proporciona el autor de la llamada al crear una revisión de access.
localization_priority: Normal
ms.openlocfilehash: cad361d6c2d2aba70b2623ddf272e1eba42fd93b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889029"
---
# <a name="businessflowtemplate-resource-type"></a>tipo de recurso businessFlowTemplate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](accessreviews-root.md) Azure AD, el `businesFlowTemplate` representa una plantilla de flujo de profesionales de Azure AD. El identificador de una plantilla, por ejemplo, para revisar a los miembros de invitado de un grupo, se proporciona el autor de la llamada al crear una revisión de access.

Los objetos de plantilla de flujo de negocios se generan automáticamente cuando el onboards el inquilino de para usar el acceso de administrador global revisa la característica.  No hay plantillas de flujo de negocio adicionales se pueden crear.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista businessFlowTemplates](../api/businessflowtemplate-list.md) | colección de [businessFlowTemplate](businessflowtemplate.md)| Obtener las plantillas de flujo de negocio adecuados tener acceso a las revisiones.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
| `id`                     |`String`                | El identificador asignado a la característica de la plantilla de flujo de negocio                                      |
| `displayName`            |`String`                | El nombre de la plantilla de flujo de negocio                                                             |


## <a name="relationships"></a>Relaciones

Ninguno.

## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear accessReview](../api/accessreview-create.md) | [accessReview](accessreview.md) |   Crear un nuevo accessReview. |


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.businessFlowTemplate"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "businessFlowTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

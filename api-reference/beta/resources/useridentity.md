---
title: tipo de IdentidadDeUsuario
description: 'Para AD Azure access revisiones, este tipo representa una identidad de usuario de Azure AD para un revisor de una revisión de access.  '
localization_priority: Normal
ms.openlocfilehash: 5b629fff4c5cecd513777cc5004646aac5f1c85b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839644"
---
# <a name="useridentity-type"></a>tipo de IdentidadDeUsuario

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Para el AD Azure [access revisa](accessreviews-root.md), este tipo representa una identidad de usuario de Azure AD para un revisor de una revisión de acceso.  
En el contexto de un registro de auditoría de Azure AD, esto representa la información del usuario que inició o se ve afectada por una actividad de auditoría.

Este tipo hereda de [identidad](identity.md) y tiene una propiedad adicional, el nombre principal de usuario del usuario.

## <a name="methods"></a>Métodos

Ninguno.  Debe incluir los objetos de este tipo en el cuerpo de una solicitud al [crear un accessReview](../api/accessreview-create.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
| `displayName` | `String` | Nombre para mostrar de la identidad. Tenga en cuenta que esto es posible que no siempre esté disponible o actualizado.    |
| `id`          | `String` | Identificador único de la identidad.  |
| `ipAddress`| `String`| Indica la dirección IP del cliente usada por el usuario que realiza la actividad (solo registro de auditoría).|
| `userPrincipalName`|`String` | El atributo userPrincipalName del usuario. |

## <a name="remarks"></a>Comentarios

En algunas circunstancias, puede que el identificador único del actor no esté disponible. En este caso, se devuelve la propiedad **displayName** de la identidad, pero faltará la propiedad **id** del recurso.

## <a name="relationships"></a>Relaciones

Ninguno.

## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener los revisores accessReview](../api/accessreview-listreviewers.md) |       colección de [IdentidadDeUsuario](useridentity.md)| Obtenga los revisores de un accessReview. |
|[Agregar revisor accessReview](../api/accessreview-addreviewer.md) |      Ninguno.   |   Agregar un revisor a una accessReview. |
|[Quitar accessReview revisor](../api/accessreview-removereviewer.md) | Ninguno.  |   Quitar un revisor de un accessReview. |

## <a name="json-representation"></a>Representación JSON

Aquí es una representación de JSON del tipo.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
"displayName", "thumbnails"
  ],
  "@odata.type": "microsoft.graph.userIdentity"
}-->

```json
{
  "displayName": "string",
  "id": "string",
 "userPrincipalName": "String"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "userIdentity type",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

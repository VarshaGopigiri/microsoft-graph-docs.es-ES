---
title: tipo de recurso accessReviewDecision
description: En el anuncio de Azure access revisa la característica, el `accessReviewDecision` representa una decisión de revisión de Azure AD acceso de acceso de una entidad determinada.  Dentro de una revisión de access, o una instancia de una revisión periódica de acceso, hay una `accessReviewDecision` por usuario revisado.  Por ejemplo, si un grupo tiene dos invitados y que no sean uno Invitado como miembros y una revisión de acceso de los invitados se realiza para dicho grupo, a continuación, habrá dos objetos de toma de decisiones de revisión de access.  Si un revisor cambia su decisión o reemplaza a otro revisor, entonces el `accessReviewDecision` se ha actualizado.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: b6b10a53726e12c37a598f8df735a3f70174c807
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977559"
---
# <a name="accessreviewdecision-resource-type"></a>tipo de recurso accessReviewDecision

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](accessreviews-root.md) Azure AD, el `accessReviewDecision` representa una decisión de revisión de Azure AD acceso de acceso de una entidad determinada.  Dentro de una revisión de access, o una instancia de una revisión periódica de acceso, hay una `accessReviewDecision` por usuario revisado.  Por ejemplo, si un grupo tiene dos invitados y que no sean uno Invitado como miembros y una revisión de acceso de los invitados se realiza para dicho grupo, a continuación, habrá dos objetos de toma de decisiones de revisión de access.  Si un revisor cambia su decisión o reemplaza a otro revisor, entonces el `accessReviewDecision` se ha actualizado.


## <a name="methods"></a>Métodos

Ninguno.  Objetos de este tipo se crean automáticamente por la característica cuando revise Inicializa un acceso y no se puede eliminar.  Se pueden recuperar desde una revisión de access con las relaciones de [las decisiones](../api/accessreview-listdecisions.md) y [mydecisions](../api/accessreview-listmydecisions.md) .

## <a name="properties"></a>Propiedades

Esta tabla muestra las propiedades de objetos de este tipo de bases. 

| Propiedad                        | Tipo                         | Descripción                                                                                            |
| :------------------------------ | :-----------------------     | :----------------------------------------------------------------------------------------------------- |
| `id`                            |`String`                      | El identificador de la decisión dentro de la revisión de access.                                                                                     |
| `accessReviewId`                |`String`                      | El identificador generado por la característica de la revisión de access.                                                                                       |
| `reviewedBy`                    |[IdentidadDeUsuario](useridentity.md)| La identidad del revisor.                                                                                       |
| `reviewedDate`                  |`DateTimeOffset`              | Se ha proporcionado la fecha y hora de la revisión más reciente de este derecho de acceso.                                                                         |
| `reviewResult`                  |`String`                      | El resultado de la revisión.                                                                                    |
| `justification`                 |`String`                      | Justificación del negocio del revisor, si proporciona.                                                                         |
| `appliedBy`                     |[IdentidadDeUsuario](useridentity.md)| Cuando se completa la revisión, si los resultados se han aplicado manualmente, la identidad de usuario del usuario que se aplica la decisión.                                                           |
| `appliedDateTime`               |`DateTimeOffset`              | La fecha y la hora cuando se aplicó la decisión de revisión.                                                          |
| `applyResult`                   |`String`                      | El resultado de la aplicación de la decisión, uno de `NotApplied`, `Success`, `Failed`, `NotFound` o `NotSupported`.                      |
| `accessRecommendation`          |`String`                      | La recomendación de característica-generado se muestra para el revisor, uno de `Approve`, `Deny` o `NotAvailable`. |


Además, las propiedades adicionales pueden estar presentes según el tipo de objeto del objeto que poseen el acceso a la que se ha decidido.  Por ejemplo, si la decisión de revisión de acceso es la pertenencia a grupos de un usuario en particular o acceso a la aplicación, el usuario que potencialmente se va a tener su acceso se ha quitado se identifica a través de estas propiedades:

| Propiedad                        | Tipo                         | Descripción                                                                                            |
| :------------------------------ | :-----------------------     | :----------------------------------------------------------------------------------------------------- |
| `userId`                            |`String`                      | El identificador de usuario cuyo acceso se ha revisado.                                                                                    |
| `userDisplayName`                            |`String`                      | El nombre para mostrar del usuario cuyo acceso se ha revisado.                                                                                     |
| `userPrincipalName`                            |`String`                      | El nombre principal de usuario del usuario cuyo acceso se ha revisado.                                                                                     |



## <a name="relationships"></a>Relaciones

Ninguno.  Objetos de este tipo se pueden recuperar desde una revisión de access con las relaciones de [las decisiones](../api/accessreview-listdecisions.md) y [mydecisions](../api/accessreview-listmydecisions.md) del objeto [accessReview](accessreview.md) .

## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista decisiones de accessReview](../api/accessreview-listdecisions.md) |      colección de [accessReviewDecision](accessreviewdecision.md)| Obtenga las decisiones de un accessReview.|
|[Mis decisiones accessReview de lista](../api/accessreview-listmydecisions.md) |     colección de [accessReviewDecision](accessreviewdecision.md)| Como revisor, obtener Mis decisiones de un accessReview.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.accessReviewDecision"
}-->

```json
{
"id": "string (identifier)",
"accessReviewId": "string (identifier)",
"reviewedBy": "microsoft.graph.userIdentity",
"reviewedDate": "string (timestamp)",
"reviewResult": "string",
"justification": "string",
"appliedBy": "microsoft.graph.userIdentity",
"appliedDateTime": "string (timestamp)",
"applyResult": "string",
"accessRecommendation": "string",
"userId": "string",
"userDisplayName": "string",
"userPrincipalName": "string"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "accessReviewDecision resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

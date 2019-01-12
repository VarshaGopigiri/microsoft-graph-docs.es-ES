---
title: tipo de recurso accessReview
description: 'En el anuncio de Azure access revisa la característica, el `accessReview` representa una revisión de access.  '
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 6d97382957b7c61625ec54af4c572962be839b4a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950665"
---
# <a name="accessreview-resource-type"></a>tipo de recurso accessReview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](accessreviews-root.md) Azure AD, el `accessReview` representa una revisión de access.  


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener accessReview](../api/accessreview-get.md) |   [accessReview](accessreview.md) |   Obtenga una revisión de access con un identificador específico. |
|[Crear accessReview](../api/accessreview-create.md) | [accessReview](accessreview.md) |   Crear un nuevo accessReview. |
|[Eliminar accessReview](../api/accessreview-delete.md) | Ninguno.   | Eliminar un accessReview. |
|[Actualizar accessReview](../api/accessreview-update.md) | [accessReview](accessreview.md) | Actualizar un accessReview. |
|[Revisores accessReview de lista](../api/accessreview-listreviewers.md) |      colección de [IdentidadDeUsuario](useridentity.md)| Obtenga los revisores de un accessReview. |
|[Agregar revisor accessReview](../api/accessreview-addreviewer.md) |      Ninguno.   |   Agregar un revisor a una accessReview. |
|[Quitar accessReview revisor](../api/accessreview-removereviewer.md) | Ninguno.  |   Quitar un revisor de un accessReview. |
|[Lista decisiones de accessReview](../api/accessreview-listdecisions.md) |      colección de [accessReviewDecision](accessreviewdecision.md)| Obtenga las decisiones de un accessReview.|
|[Mis decisiones accessReview de lista](../api/accessreview-listmydecisions.md) |     colección de [accessReviewDecision](accessreviewdecision.md)| Como revisor, obtener Mis decisiones de un accessReview.|
|[Enviar aviso de accessReview](../api/accessreview-sendreminder.md) |        Ninguno.   |   Enviar un aviso a los revisores de un accessReview. |
|[Detener accessReview](../api/accessreview-stop.md) |     Ninguno.   |   Detener una accessReview. |
|[Restablecer las decisiones de accessReview](../api/accessreview-reset.md) |     Ninguno.   |   Restablecer las decisiones en un accessReview en curso.|
|[Aplicar decisiones accessReview](../api/accessreview-apply.md) |     Ninguno.   |   Se aplican las decisiones de un accessReview completado.|

## <a name="permissions"></a>Permisos

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | AccessReview.Read.All, AccessReview.ReadWrite.All |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| `id`                      |`String`                                                        | El identificador único asignado a la característica de una revisión de access. |
| `displayName`             |`String`                                                        | Nombre de la revisión de acceso. Necesarios en crear. |
| `startDateTime`           |`DateTimeOffset`                                                | La fecha y hora cuando la revisión está programada para que se inicie.  Esto podría ser una fecha en el futuro.  Necesarios en crear. |
| `endDateTime`             |`DateTimeOffset`                                                | La fecha y hora cuando la revisión está programada para finalizar. Esto debe ser al menos un día posterior a la fecha de inicio.  Necesarios en crear. |
| `status`                  |`String`                                                        | Este campo de sólo lectura especifica el estado actual de un accessReview. Los Estados típicos incluyen `Initializing`, `NotStarted`, `Starting`,`InProgress`, `Completing`, `Completed`, `AutoReviewing`, y `AutoReviewed`. |
| `description`             |`String`                                                        | La descripción proporcionada por el creador de la revisión de access, para mostrar a los revisores. |
| `businessFlowTemplateId`  |`String`                                                        | El identificador de plantilla de flujo de negocio. Necesarios en crear. |
| `reviewerType`            |`String`                                                        | El tipo de relación de revisor al objeto de destino, uno de `self`, `delegate` o `entityOwners`. Necesarios en crear. | 
| `createdBy`               |[IdentidadDeUsuario](useridentity.md)                                 | El usuario que ha creado esta revisión. |
| `reviewedEntity`          |`microsoft.graph.identity`                                      | Es el objeto para el que se revisa el acceso de las asignaciones de derechos de acceso, como la pertenencia a grupos de usuarios a un grupo o las asignaciones de usuarios a una aplicación. Necesarios en crear. | 
| `settings`                |`microsoft.graph.accessReviewSettings`             | La configuración de un accessReview, vea la definición de tipo que aparece a continuación. |



## <a name="relationships"></a>Relaciones




| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
| `reviewers`               |colección de [IdentidadDeUsuario](useridentity.md)                     | La colección de los revisores de una revisión de access, si access revisión reviewerType es del tipo `delegate`. |
| `decisions`               |colección de [accessReviewDecision](accessreviewdecision.md) | La colección de decisiones para esta revisión de access. |
| `myDecisions`             |colección de [accessReviewDecision](accessreviewdecision.md) | La colección de decisiones para el autor de la llamada, si el autor de la llamada es un revisor. |
| `instances`               |colección de [accessReview](accessreview.md)         | La colección de las revisiones de acceso de instancias pasado, presente y futuro, si este objeto es una revisión periódica de access. |

Si hay relaciones presentes en un objeto, dependen de si el objeto es una revisión de acceso única, la serie de una revisión periódica de acceso o una instancia de una revisión periódica de access.

| Escenario | ¿Tiene revisores? | ¿Tiene las decisiones y myDecisions? | ¿Tiene instancias? |
|:---------|:---------------|:---------------|:---------------|
|Revisión de acceso única|Sí | Sí, una vez iniciado | No |
| Revisión periódica de access | Sí | No | Sí |
| Instancia de una revisión periódica de access | Sí | Sí, una vez iniciado | No |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.accessReview"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string",
 "startDateTime": "string (timestamp)",
 "endDateTime": "string (timestamp)",
 "status": "string",
 "description": "string",
 "businessFlowTemplateId": "string (identifier)",
 "reviewerType": "string",
 "createdBy": "microsoft.graph.userIdentity",
 "reviewedEntity": "microsoft.graph.identity",
 "settings": "microsoft.graph.accessReviewSettings",
 "reviewers": "Collection(microsoft.graph.userIdentity)"
}

```

## <a name="the-accessreviewsettings-type"></a>El tipo de accessReviewSettings

El `accessReviewSettings` proporciona una configuración adicional al crear una revisión de acceso para controlar el comportamiento de la característica cuando se inicia una revisión de access.  Este tipo tiene las siguientes propiedades: 

| Propiedad                     | Tipo                      | Descripción |
| :--------------------------- | :------------------------ | :---------- |
| `mailNotificationsEnabled`|`Boolean`                | Marcar para indicar si está habilitado el envío de mensajes de correo electrónico a los revisores y el creador de la revisión.                |
| `remindersEnabled`|`Boolean`       | Marcar para indicar si están habilitados los correos electrónicos de aviso envío a los revisores.       |
| `justificationRequiredOnApproval`|`Boolean` | Marcar para indicar si los revisores son necesarios para proporcionar una justificación al revisar el acceso.|
| `activityDurationInDays`|`Int64` | El número de días de actividades de usuario para mostrar a los revisores. |
| `autoReviewEnabled`|`Boolean` | Indicador para indicar si la característica debe establecer una decisión de si el revisor no proporcionó uno, para su uso con auto-apply, está habilitado. |
| `autoReviewSettings`|`microsoft.graph.autoReviewSettings` | Configuración detallada de cómo la característica debe establecer la decisión de revisión, para su uso con auto-apply, que se describe a continuación. |
| `recurrenceSettings`|`microsoft.graph.accessReviewRecurrenceSettings` | Configuración detallada de periodicidad, que se describe a continuación. |
| `autoApplyReviewResultsEnabled`|`Boolean` | Marca para indicar si se aplican automático capacidad para cambiar automáticamente el recurso de acceso del objeto de destino, está habilitada.  Si no está habilitado, un usuario posteriormente debe aplicar el cambio de la revisión de acceso una vez finalizada la revisión de access. |
| `accessRecommendationsEnabled`|`Boolean` | Marcar para indicar si está habilitada la opción Mostrar recomendaciones a los revisores. |



## <a name="the-autoreviewsettings-type"></a>El tipo de autoReviewSettings

El `autoReviewSettings` está incrustada dentro de la configuración de la revisión de acceso y especifica el comportamiento de la característica cuando se completa una revisión de access.  El tipo tiene una propiedad, `notReviewedResult`.

| Propiedad                     | Tipo     | Descripción                          |
| :--------------------------- | :------  | :----------                          |
| `notReviewedResult`          |`String`  | Debe ser `Approve`, `Deny` o `Recommendation`. |


## <a name="the-accessreviewrecurrencesettings-type"></a>El tipo de accessReviewRecurrenceSettings

El `accessReviewRecurrenceSettings` está incrustada dentro de la configuración de la revisión de acceso y especifica que la revisión de access se repite a intervalos regulares.  Este tipo tiene las siguientes propiedades:

| Propiedad                     | Tipo                                                                                                          | Descripción |
| :--------------------------- | :------------------------------------------------------------------------------------------------------------ | :---------- |
| `recurrenceType`|`String`    | El intervalo de periodicidad, que debe ser uno de `onetime`, `weekly`, `monthly`, `quarterly` o `annual`.                                                                   |
| `recurrenceEndType`|`String` | Cómo la periodicidad finalizará. Puede ser una de `Never`, que no hay ningún fin explícito de la serie de periodicidad, `Endby`, que la periodicidad finaliza en una fecha determinada, y `occurrences`, que la serie finaliza después de haber completado cierto número de instancias de la revisión. |
| `durationInDays`|`Int32`     | La duración en días de periodicidad.                                                                              |
| `recurrenceCount`|`Int32`    | El recuento de las repeticiones, si el valor de `recurrenceEndType` es `occurrences`.                                                        |



<!-- {
  "type": "#page.annotation",
  "description": "accessReview resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

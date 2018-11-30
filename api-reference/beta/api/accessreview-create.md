---
title: Crear accessReview
description: En Azure AD tener acceso a la característica de revisiones, crear un nuevo objeto accessReview.
ms.openlocfilehash: 9d8e8b246c3c43e4f69172ea59715a8718d39d1e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083709"
---
# <a name="create-accessreview"></a>Crear accessReview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, cree un nuevo objeto [accessReview](../resources/accessreview.md) .

Antes de realizar esta solicitud, el llamador debe tener anteriormente [recupera la lista de plantillas de flujo de negocio](businessflowtemplate-list.md), para que el valor de `businessFlowTemplateId` para incluir en la solicitud.

Después de realizar esta solicitud, el llamador debe [crear un programControl](programcontrol-create.md), para vincular la revisión de acceso a un programa.  

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | AccessReview.ReadWrite.All y también deben tener ProgramControl.ReadWrite.All a un escenario completo con la siguiente llamada para crear un programControl |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /accessReviews
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Authorization | string | Bearer \{token\}. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [accessReview](../resources/accessreview.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea un accessReview.

| Propiedad     | Tipo        | Descripción |
|:-------------|:------------|:------------|
| `displayName`             |`String`                                                        | Nombre de la revisión de acceso.  |
| `startDateTime`           |`DateTimeOffset`                                                | La fecha y hora cuando la revisión está programada para que se inicie.  Esto debe ser una fecha en el futuro.   |
| `endDateTime`             |`DateTimeOffset`                                                | La fecha y hora cuando la revisión está programada para finalizar. Esto debe ser al menos un día posterior a la fecha de inicio.   |
| `description`             |`String`                                                        | La descripción, para mostrar a los revisores. |
| `businessFlowTemplateId`  |`String`                                                        | El negocio flujo identificador de plantilla, obtenido de un [businessFlowTemplate](../resources/businessflowtemplate.md).  |
| `reviewerType`            |`String`                                                        | El tipo de relación de revisor a los derechos de acceso del objeto revisado, uno de `self`, `delegate` o `entityOwners`. | 
| `reviewedEntity`          |`microsoft.graph.identity`                                      | El objeto para el que se crea una revisión de acceso, como una pertenencia a grupos de un grupo o las asignaciones de los usuarios a una aplicación. | 


Si el reviewerType se proporciona tiene el valor `delegate`, a continuación, el autor de la llamada también debe incluir el `reviewers` (propiedad), con una colección de [IdentidadDeUsuario](../resources/useridentity.md) de los revisores.

Además, el autor de la llamada puede incluir la configuración, para crear una serie periódica de revisión o para cambiar el comportamiento predeterminado de la revisión. En concreto, para crear una revisión periódica, el autor de la llamada debe incluir la `accessReviewRecurrenceSettings` en el acceso a revisar la configuración,


## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201, Created` código de respuesta y un objeto [accessReview](../resources/accessreview.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

Éste es un ejemplo de creación de una revisión de access (no periódica) única especificación explícita de dos usuarios como los revisores.

##### <a name="request"></a>Solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [accessReview](../resources/accessreview.md) .

<!-- {
  "blockType": "request",
  "name": "create_accessReview_from_accessReviews"
}-->
```http
POST https://graph.microsoft.com/beta/accessReviews
Content-type: application/json

{
    "displayName":"TestReview",
    "startDateTime":"2017-02-10T00:35:53.214Z",
    "endDateTime":"2017-03-12T00:35:53.214Z",
    "reviewedEntity": {
        "id": "99025615-a0b1-47ec-9117-35377b10998b",
    },
    "reviewerType" : "delegate",
    "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "description":"Sample description",
    "reviewers":
    [
        {
            "id":"f260246a-09b1-4fd5-8d18-daed736071ec"
        },
        {
            "id":"5a4e184c-4ee5-4883-96e9-b371f8da88e3"
        }
    ],
    "settings":
    {
        "justificationRequiredOnApproval": true,
        "activityHistoryInDays":30,
        "mailNotificationsEnabled":true,
        "remindersEnabled":true
    }
}
```

##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReview"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "id": "006111db-0810-4494-a6df-904d368bd81b",
    "displayName": "TestReview",
    "startDateTime": "2017-02-10T00:35:53.214Z",
    "endDateTime": "2017-03-12T00:35:53.214Z",
    "status": "Initializing",
    "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "reviewerType": "delegate",
    "description": "Sample description"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "Create accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

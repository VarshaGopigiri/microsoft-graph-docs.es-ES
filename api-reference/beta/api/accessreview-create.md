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
# <a name="create-accessreview"></a><span data-ttu-id="a7f47-103">Crear accessReview</span><span class="sxs-lookup"><span data-stu-id="a7f47-103">Create accessReview</span></span>

> <span data-ttu-id="a7f47-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a7f47-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a7f47-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a7f47-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a7f47-106">En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, cree un nuevo objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f47-106">In the Azure AD [access reviews](../resources/accessreviews-root.md) feature, create a new [accessReview](../resources/accessreview.md) object.</span></span>

<span data-ttu-id="a7f47-107">Antes de realizar esta solicitud, el llamador debe tener anteriormente [recupera la lista de plantillas de flujo de negocio](businessflowtemplate-list.md), para que el valor de `businessFlowTemplateId` para incluir en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7f47-107">Prior to making this request, the caller must have previously [retrieved the list of business flow templates](businessflowtemplate-list.md), to have the value of `businessFlowTemplateId` to include in the request.</span></span>

<span data-ttu-id="a7f47-108">Después de realizar esta solicitud, el llamador debe [crear un programControl](programcontrol-create.md), para vincular la revisión de acceso a un programa.</span><span class="sxs-lookup"><span data-stu-id="a7f47-108">After making this request, the caller should [create a programControl](programcontrol-create.md), to link the access review to a program.</span></span>  

## <a name="permissions"></a><span data-ttu-id="a7f47-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="a7f47-109">Permissions</span></span>
<span data-ttu-id="a7f47-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7f47-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a7f47-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7f47-112">Permission type</span></span>                        | <span data-ttu-id="a7f47-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7f47-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="a7f47-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7f47-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="a7f47-115">AccessReview.ReadWrite.All y también deben tener ProgramControl.ReadWrite.All a un escenario completo con la siguiente llamada para crear un programControl</span><span class="sxs-lookup"><span data-stu-id="a7f47-115">AccessReview.ReadWrite.All, and should also have ProgramControl.ReadWrite.All to complete scenario with the subsequent call to create a programControl</span></span> |
|<span data-ttu-id="a7f47-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7f47-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a7f47-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7f47-117">Not supported.</span></span> |
|<span data-ttu-id="a7f47-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7f47-118">Application</span></span>                            | <span data-ttu-id="a7f47-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7f47-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a7f47-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7f47-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /accessReviews
```
## <a name="request-headers"></a><span data-ttu-id="a7f47-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7f47-121">Request headers</span></span>
| <span data-ttu-id="a7f47-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7f47-122">Name</span></span>         | <span data-ttu-id="a7f47-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7f47-123">Type</span></span>        | <span data-ttu-id="a7f47-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7f47-124">Description</span></span> |
|:-------------|:------------|:------------|
| <span data-ttu-id="a7f47-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="a7f47-125">Authorization</span></span> | <span data-ttu-id="a7f47-126">string</span><span class="sxs-lookup"><span data-stu-id="a7f47-126">string</span></span> | <span data-ttu-id="a7f47-127">Bearer \{token\}.</span><span class="sxs-lookup"><span data-stu-id="a7f47-127">Bearer \{token\}.</span></span> <span data-ttu-id="a7f47-128">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7f47-128">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a7f47-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7f47-129">Request body</span></span>
<span data-ttu-id="a7f47-130">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f47-130">In the request body, supply a JSON representation of an [accessReview](../resources/accessreview.md) object.</span></span>

<span data-ttu-id="a7f47-131">La siguiente tabla muestran las propiedades que son necesarias cuando se crea un accessReview.</span><span class="sxs-lookup"><span data-stu-id="a7f47-131">The following table shows the properties that are required when you create an accessReview.</span></span>

| <span data-ttu-id="a7f47-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7f47-132">Property</span></span>     | <span data-ttu-id="a7f47-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7f47-133">Type</span></span>        | <span data-ttu-id="a7f47-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7f47-134">Description</span></span> |
|:-------------|:------------|:------------|
| `displayName`             |`String`                                                        | <span data-ttu-id="a7f47-135">Nombre de la revisión de acceso.</span><span class="sxs-lookup"><span data-stu-id="a7f47-135">The access review name.</span></span>  |
| `startDateTime`           |`DateTimeOffset`                                                | <span data-ttu-id="a7f47-136">La fecha y hora cuando la revisión está programada para que se inicie.</span><span class="sxs-lookup"><span data-stu-id="a7f47-136">The DateTime when the review is scheduled to be start.</span></span>  <span data-ttu-id="a7f47-137">Esto debe ser una fecha en el futuro.</span><span class="sxs-lookup"><span data-stu-id="a7f47-137">This must be a date in the future.</span></span>   |
| `endDateTime`             |`DateTimeOffset`                                                | <span data-ttu-id="a7f47-138">La fecha y hora cuando la revisión está programada para finalizar.</span><span class="sxs-lookup"><span data-stu-id="a7f47-138">The DateTime when the review is scheduled to end.</span></span> <span data-ttu-id="a7f47-139">Esto debe ser al menos un día posterior a la fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="a7f47-139">This must be at least one day later than the start date.</span></span>   |
| `description`             |`String`                                                        | <span data-ttu-id="a7f47-140">La descripción, para mostrar a los revisores.</span><span class="sxs-lookup"><span data-stu-id="a7f47-140">The description, to show to the reviewers.</span></span> |
| `businessFlowTemplateId`  |`String`                                                        | <span data-ttu-id="a7f47-141">El negocio flujo identificador de plantilla, obtenido de un [businessFlowTemplate](../resources/businessflowtemplate.md).</span><span class="sxs-lookup"><span data-stu-id="a7f47-141">The business flow template identifier, obtained from a [businessFlowTemplate](../resources/businessflowtemplate.md).</span></span>  |
| `reviewerType`            |`String`                                                        | <span data-ttu-id="a7f47-142">El tipo de relación de revisor a los derechos de acceso del objeto revisado, uno de `self`, `delegate` o `entityOwners`.</span><span class="sxs-lookup"><span data-stu-id="a7f47-142">The relationship type of reviewer to the access rights of the reviewed object, one of `self`, `delegate` or `entityOwners`.</span></span> | 
| `reviewedEntity`          |`microsoft.graph.identity`                                      | <span data-ttu-id="a7f47-143">El objeto para el que se crea una revisión de acceso, como una pertenencia a grupos de un grupo o las asignaciones de los usuarios a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a7f47-143">The object for which an access review is created, such as a memberships of an group or the assignments of users to an application.</span></span> | 


<span data-ttu-id="a7f47-144">Si el reviewerType se proporciona tiene el valor `delegate`, a continuación, el autor de la llamada también debe incluir el `reviewers` (propiedad), con una colección de [IdentidadDeUsuario](../resources/useridentity.md) de los revisores.</span><span class="sxs-lookup"><span data-stu-id="a7f47-144">If the reviewerType being supplied has the value `delegate`, then the caller must also include the `reviewers` property, with a collection of [userIdentity](../resources/useridentity.md) of the reviewers.</span></span>

<span data-ttu-id="a7f47-145">Además, el autor de la llamada puede incluir la configuración, para crear una serie periódica de revisión o para cambiar el comportamiento predeterminado de la revisión.</span><span class="sxs-lookup"><span data-stu-id="a7f47-145">In addition, the caller can include settings, to create a recurring review series or to change from the default review behavior.</span></span> <span data-ttu-id="a7f47-146">En concreto, para crear una revisión periódica, el autor de la llamada debe incluir la `accessReviewRecurrenceSettings` en el acceso a revisar la configuración,</span><span class="sxs-lookup"><span data-stu-id="a7f47-146">In particular, to create a recurring review, the caller must include the `accessReviewRecurrenceSettings` within the access review settings,</span></span>


## <a name="response"></a><span data-ttu-id="a7f47-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7f47-147">Response</span></span>
<span data-ttu-id="a7f47-148">Si tiene éxito, este método devuelve una `201, Created` código de respuesta y un objeto [accessReview](../resources/accessreview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7f47-148">If successful, this method returns a `201, Created` response code and an [accessReview](../resources/accessreview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7f47-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7f47-149">Example</span></span>

<span data-ttu-id="a7f47-150">Éste es un ejemplo de creación de una revisión de access (no periódica) única especificación explícita de dos usuarios como los revisores.</span><span class="sxs-lookup"><span data-stu-id="a7f47-150">This is an example of creating a one-time (not recurring) access review, explicitly specifying two users as the reviewers.</span></span>

##### <a name="request"></a><span data-ttu-id="a7f47-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7f47-151">Request</span></span>
<span data-ttu-id="a7f47-152">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [accessReview](../resources/accessreview.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f47-152">In the request body, supply a JSON representation of the [accessReview](../resources/accessreview.md) object.</span></span>

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

##### <a name="response"></a><span data-ttu-id="a7f47-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7f47-153">Response</span></span>
><span data-ttu-id="a7f47-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7f47-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

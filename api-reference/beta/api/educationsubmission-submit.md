---
title: 'educationSubmission: enviar'
description: . Durante el proceso de envío, todos los recursos se copiarán en el cubo de submittedResources. El profesor buscará en la lista de recursos enviado para la clasificación.
ms.openlocfilehash: 566948278ffacb1169842c49aa11c78cba0a5f3f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084902"
---
# <a name="educationsubmission-submit"></a><span data-ttu-id="b02dc-105">educationSubmission: enviar</span><span class="sxs-lookup"><span data-stu-id="b02dc-105">educationSubmission: submit</span></span>

> <span data-ttu-id="b02dc-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b02dc-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b02dc-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b02dc-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b02dc-108">Una acción que indica que un estudiante se realiza con el trabajo y está listo para proporcionar en la asignación.</span><span class="sxs-lookup"><span data-stu-id="b02dc-108">An action that indicates that a student is done with the work and is ready to hand in the assignment.</span></span> <span data-ttu-id="b02dc-109">Esta acción sólo puede consultarse por el alumno.</span><span class="sxs-lookup"><span data-stu-id="b02dc-109">This action can only be taken by the student.</span></span> <span data-ttu-id="b02dc-110">Esto cambiará el estado de la presentación de "trabajando" a "enviado".</span><span class="sxs-lookup"><span data-stu-id="b02dc-110">This will change the status of the submission from "working" to "submitted".</span></span> <span data-ttu-id="b02dc-111">Durante el proceso de envío, todos los recursos se copiarán en el cubo de submittedResources.</span><span class="sxs-lookup"><span data-stu-id="b02dc-111">During the submit process, all the resources will be copied to the submittedResources bucket.</span></span> <span data-ttu-id="b02dc-112">El profesor buscará en la lista de recursos enviado para la clasificación.</span><span class="sxs-lookup"><span data-stu-id="b02dc-112">The teacher will be looking at the submitted resources list for grading.</span></span>

## <a name="permissions"></a><span data-ttu-id="b02dc-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="b02dc-113">Permissions</span></span>
<span data-ttu-id="b02dc-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b02dc-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b02dc-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b02dc-116">Permission type</span></span>      | <span data-ttu-id="b02dc-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b02dc-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b02dc-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b02dc-118">Delegated (work or school account)</span></span> |  <span data-ttu-id="b02dc-119">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b02dc-119">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="b02dc-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b02dc-120">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="b02dc-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b02dc-121">Not supported.</span></span>  |
|<span data-ttu-id="b02dc-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b02dc-122">Application</span></span> | <span data-ttu-id="b02dc-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b02dc-123">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="b02dc-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b02dc-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/submissions/{id}/submit

```
## <a name="request-headers"></a><span data-ttu-id="b02dc-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b02dc-125">Request headers</span></span>
| <span data-ttu-id="b02dc-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b02dc-126">Header</span></span>       | <span data-ttu-id="b02dc-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b02dc-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b02dc-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="b02dc-128">Authorization</span></span>  | <span data-ttu-id="b02dc-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b02dc-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b02dc-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b02dc-131">Request body</span></span>
<span data-ttu-id="b02dc-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b02dc-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b02dc-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b02dc-133">Response</span></span>
<span data-ttu-id="b02dc-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b02dc-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b02dc-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b02dc-136">Example</span></span>
<span data-ttu-id="b02dc-137">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b02dc-137">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b02dc-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b02dc-138">Request</span></span>
<span data-ttu-id="b02dc-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b02dc-139">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationsubmission_submit"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/submit
```

##### <a name="response"></a><span data-ttu-id="b02dc-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b02dc-140">Response</span></span>
<span data-ttu-id="b02dc-141">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b02dc-141">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignment"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSubmission: submit",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
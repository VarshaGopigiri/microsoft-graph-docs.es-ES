---
title: 'educationSubmission: enviar'
description: Una acción que indica que un estudiante se realiza con el trabajo y está listo para proporcionar en la asignación. Esta acción sólo puede consultarse por el alumno.
author: dipakboyed
ms.openlocfilehash: 25fc24823081c6f148617ad31d0f7b797b0e2a80
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343333"
---
# <a name="educationsubmission-submit"></a><span data-ttu-id="0af57-104">educationSubmission: enviar</span><span class="sxs-lookup"><span data-stu-id="0af57-104">educationSubmission: submit</span></span>

> <span data-ttu-id="0af57-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0af57-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0af57-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0af57-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0af57-107">Una acción que indica que un estudiante se realiza con el trabajo y está listo para proporcionar en la asignación.</span><span class="sxs-lookup"><span data-stu-id="0af57-107">An action that indicates that a student is done with the work and is ready to hand in the assignment.</span></span> <span data-ttu-id="0af57-108">Esta acción sólo puede consultarse por el alumno.</span><span class="sxs-lookup"><span data-stu-id="0af57-108">This action can only be taken by the student.</span></span> <span data-ttu-id="0af57-109">Esto cambiará el estado de la presentación de "trabajando" a "enviado".</span><span class="sxs-lookup"><span data-stu-id="0af57-109">This will change the status of the submission from "working" to "submitted".</span></span> <span data-ttu-id="0af57-110">Durante el proceso de envío, todos los recursos se copiarán en el cubo de submittedResources.</span><span class="sxs-lookup"><span data-stu-id="0af57-110">During the submit process, all the resources will be copied to the submittedResources bucket.</span></span> <span data-ttu-id="0af57-111">El profesor buscará en la lista de recursos enviado para la clasificación.</span><span class="sxs-lookup"><span data-stu-id="0af57-111">The teacher will be looking at the submitted resources list for grading.</span></span>

## <a name="permissions"></a><span data-ttu-id="0af57-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="0af57-112">Permissions</span></span>
<span data-ttu-id="0af57-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0af57-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0af57-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0af57-115">Permission type</span></span>      | <span data-ttu-id="0af57-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0af57-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0af57-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0af57-117">Delegated (work or school account)</span></span> |  <span data-ttu-id="0af57-118">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0af57-118">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="0af57-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0af57-119">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="0af57-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0af57-120">Not supported.</span></span>  |
|<span data-ttu-id="0af57-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0af57-121">Application</span></span> | <span data-ttu-id="0af57-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0af57-122">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="0af57-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0af57-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/submissions/{id}/submit

```
## <a name="request-headers"></a><span data-ttu-id="0af57-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0af57-124">Request headers</span></span>
| <span data-ttu-id="0af57-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0af57-125">Header</span></span>       | <span data-ttu-id="0af57-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0af57-126">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0af57-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="0af57-127">Authorization</span></span>  | <span data-ttu-id="0af57-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0af57-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0af57-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0af57-130">Request body</span></span>
<span data-ttu-id="0af57-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0af57-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0af57-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0af57-132">Response</span></span>
<span data-ttu-id="0af57-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0af57-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0af57-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0af57-135">Example</span></span>
<span data-ttu-id="0af57-136">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0af57-136">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0af57-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0af57-137">Request</span></span>
<span data-ttu-id="0af57-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0af57-138">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationsubmission_submit"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/submit
```

##### <a name="response"></a><span data-ttu-id="0af57-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0af57-139">Response</span></span>
<span data-ttu-id="0af57-140">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0af57-140">The following is an example of the response.</span></span>

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
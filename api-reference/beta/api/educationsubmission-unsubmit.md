---
title: 'educationSubmission: unsubmit'
description: 'Una acción que indica que desea trabajar en el envío de la asignación después de se ha activado un estudiante. Esta acción sólo puede consultarse por el alumno. '
author: dipakboyed
localization_priority: Normal
ms.openlocfilehash: 853dce22c7c79ffda7b823794259fa7be0363d02
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829221"
---
# <a name="educationsubmission-unsubmit"></a><span data-ttu-id="55890-104">educationSubmission: unsubmit</span><span class="sxs-lookup"><span data-stu-id="55890-104">educationSubmission: unsubmit</span></span>

> <span data-ttu-id="55890-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="55890-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="55890-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="55890-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="55890-107">Una acción que indica que desea trabajar en el envío de la asignación después de se ha activado un estudiante.</span><span class="sxs-lookup"><span data-stu-id="55890-107">An action that indicates that a student wants to work on the submission of the assignment after it was turned in.</span></span> <span data-ttu-id="55890-108">Esta acción sólo puede consultarse por el alumno.</span><span class="sxs-lookup"><span data-stu-id="55890-108">This action can only be taken by the student.</span></span> <span data-ttu-id="55890-109">Esto cambiará el estado de la presentación de "enviada" a "trabajo".</span><span class="sxs-lookup"><span data-stu-id="55890-109">This will change the status of the submission from "submitted" to "working".</span></span> <span data-ttu-id="55890-110">Durante el proceso de envío, se copiarán todos los recursos de submittedResources al depósito workingResources.</span><span class="sxs-lookup"><span data-stu-id="55890-110">During the submit process, all the resources will be copied from submittedResources to the workingResources bucket.</span></span> <span data-ttu-id="55890-111">El profesor buscará en la lista de recursos de trabajo para la clasificación.</span><span class="sxs-lookup"><span data-stu-id="55890-111">The teacher will be looking at the working resources list for grading.</span></span>

## <a name="permissions"></a><span data-ttu-id="55890-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="55890-112">Permissions</span></span>
<span data-ttu-id="55890-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="55890-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="55890-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55890-115">Permission type</span></span>      | <span data-ttu-id="55890-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55890-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="55890-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55890-117">Delegated (work or school account)</span></span> |  <span data-ttu-id="55890-118">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="55890-118">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="55890-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55890-119">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="55890-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55890-120">Not supported.</span></span>  |
|<span data-ttu-id="55890-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55890-121">Application</span></span> | <span data-ttu-id="55890-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55890-122">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="55890-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55890-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/submissions/{id}/unsubmit

```
## <a name="request-headers"></a><span data-ttu-id="55890-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55890-124">Request headers</span></span>
| <span data-ttu-id="55890-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55890-125">Header</span></span>       | <span data-ttu-id="55890-126">Valor</span><span class="sxs-lookup"><span data-stu-id="55890-126">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="55890-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="55890-127">Authorization</span></span>  | <span data-ttu-id="55890-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55890-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="55890-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55890-130">Request body</span></span>
<span data-ttu-id="55890-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="55890-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="55890-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55890-132">Response</span></span>
<span data-ttu-id="55890-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55890-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55890-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55890-135">Example</span></span>
<span data-ttu-id="55890-136">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="55890-136">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="55890-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55890-137">Request</span></span>
<span data-ttu-id="55890-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55890-138">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationsubmission_unsubmit"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/unsubmit
```

##### <a name="response"></a><span data-ttu-id="55890-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55890-139">Response</span></span>
<span data-ttu-id="55890-140">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55890-140">The following is an example of the response.</span></span>

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
  "description": "educationSubmission: unsubmit",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

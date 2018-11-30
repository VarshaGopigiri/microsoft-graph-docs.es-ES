---
title: 'educationSubmission: devolver'
description: " indica que se proporcionan comentarios o puntuar se lleva a cabo. Esta acción sólo puede realizarse por el profesor."
ms.openlocfilehash: de81f5429119556753462781f701fb7c936826b1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083041"
---
# <a name="educationsubmission-return"></a><span data-ttu-id="77c39-104">educationSubmission: devolver</span><span class="sxs-lookup"><span data-stu-id="77c39-104">educationSubmission: return</span></span>

> <span data-ttu-id="77c39-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77c39-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77c39-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77c39-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="77c39-107">Esta acción hace que la calificación y comentarios asociados con este envío disponible para los estudiantes.</span><span class="sxs-lookup"><span data-stu-id="77c39-107">This action makes the grade and feedback associated with this submission available to the student.</span></span> <span data-ttu-id="77c39-108">Esto cambiará el estado de la presentación de "enviada" a "devuelto" y se indica que se proporcionan comentarios o puntuar se lleva a cabo.</span><span class="sxs-lookup"><span data-stu-id="77c39-108">This will change the status of the submission from "submitted" to "returned" and indicates that feedback is provided or grading is done.</span></span> <span data-ttu-id="77c39-109">Esta acción sólo puede realizarse por el profesor.</span><span class="sxs-lookup"><span data-stu-id="77c39-109">This action can only be done by the teacher.</span></span>

## <a name="permissions"></a><span data-ttu-id="77c39-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="77c39-110">Permissions</span></span>
<span data-ttu-id="77c39-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77c39-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="77c39-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77c39-113">Permission type</span></span>      | <span data-ttu-id="77c39-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77c39-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="77c39-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77c39-115">Delegated (work or school account)</span></span> |  <span data-ttu-id="77c39-116">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="77c39-116">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>   |
|<span data-ttu-id="77c39-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77c39-117">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="77c39-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77c39-118">Not supported.</span></span>  |
|<span data-ttu-id="77c39-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77c39-119">Application</span></span> | <span data-ttu-id="77c39-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77c39-120">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="77c39-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77c39-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/submissions/{id}/return

```
## <a name="request-headers"></a><span data-ttu-id="77c39-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77c39-122">Request headers</span></span>
| <span data-ttu-id="77c39-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77c39-123">Header</span></span>       | <span data-ttu-id="77c39-124">Valor</span><span class="sxs-lookup"><span data-stu-id="77c39-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="77c39-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="77c39-125">Authorization</span></span>  | <span data-ttu-id="77c39-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77c39-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="77c39-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77c39-128">Request body</span></span>
<span data-ttu-id="77c39-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="77c39-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="77c39-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77c39-130">Response</span></span>
<span data-ttu-id="77c39-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77c39-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77c39-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77c39-133">Example</span></span>
<span data-ttu-id="77c39-134">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="77c39-134">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="77c39-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77c39-135">Request</span></span>
<span data-ttu-id="77c39-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77c39-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationsubmission_return"
}-->

```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/return
```

##### <a name="response"></a><span data-ttu-id="77c39-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77c39-137">Response</span></span>
<span data-ttu-id="77c39-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77c39-138">The following is an example of the response.</span></span>

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
  "description": "educationSubmission: return",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
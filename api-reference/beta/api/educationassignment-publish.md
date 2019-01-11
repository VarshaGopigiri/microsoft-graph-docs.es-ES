---
title: 'educationAssignment: publicar'
description: Esta acción cambia el estado de una asignación de su estado de borrador original para el estado publicado. Sólo un profesor en la clase puede realizar esta llamada. Cuando una asignación se encuentra en estado de borrador, los alumnos no verán la asignación ni se producirá ningún objeto de envío. Cuando se llama a esta API, se crean objetos de envío y la asignación aparece en la lista de student.
localization_priority: Normal
ms.openlocfilehash: 09261da506113f53c6b6b9ff98af69c7dba4c784
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854743"
---
# <a name="educationassignment-publish"></a><span data-ttu-id="e98a9-106">educationAssignment: publicar</span><span class="sxs-lookup"><span data-stu-id="e98a9-106">educationAssignment: publish</span></span>

> <span data-ttu-id="e98a9-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e98a9-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e98a9-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e98a9-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e98a9-109">Esta acción cambia el estado de una asignación de su estado de borrador original para el estado publicado.</span><span class="sxs-lookup"><span data-stu-id="e98a9-109">This action changes the state of an assignment from its original draft status to the published status.</span></span> <span data-ttu-id="e98a9-110">Sólo un profesor en la clase puede realizar esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e98a9-110">Only a teacher in the class can make this call.</span></span> <span data-ttu-id="e98a9-111">Cuando una asignación se encuentra en estado de borrador, los alumnos no verán la asignación ni se producirá ningún objeto de envío.</span><span class="sxs-lookup"><span data-stu-id="e98a9-111">When an assignment is in draft status, students will not see the assignment, nor will there be any submission objects.</span></span> <span data-ttu-id="e98a9-112">Cuando se llama a esta API, se crean objetos de envío y la asignación aparece en la lista de student.</span><span class="sxs-lookup"><span data-stu-id="e98a9-112">When you call this API, submission objects are created and the assignment appears in the student's list.</span></span>

## <a name="permissions"></a><span data-ttu-id="e98a9-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="e98a9-113">Permissions</span></span>
<span data-ttu-id="e98a9-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e98a9-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e98a9-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e98a9-116">Permission type</span></span>      | <span data-ttu-id="e98a9-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e98a9-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e98a9-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e98a9-118">Delegated (work or school account)</span></span> |  <span data-ttu-id="e98a9-119">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e98a9-119">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="e98a9-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e98a9-120">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="e98a9-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e98a9-121">Not supported.</span></span>  |
|<span data-ttu-id="e98a9-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e98a9-122">Application</span></span> | <span data-ttu-id="e98a9-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e98a9-123">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e98a9-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e98a9-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/publish

```
## <a name="request-headers"></a><span data-ttu-id="e98a9-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e98a9-125">Request headers</span></span>
| <span data-ttu-id="e98a9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e98a9-126">Header</span></span>       | <span data-ttu-id="e98a9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e98a9-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e98a9-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="e98a9-128">Authorization</span></span>  | <span data-ttu-id="e98a9-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e98a9-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e98a9-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e98a9-131">Request body</span></span>
<span data-ttu-id="e98a9-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e98a9-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e98a9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e98a9-133">Response</span></span>
<span data-ttu-id="e98a9-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e98a9-p106">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e98a9-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e98a9-136">Example</span></span>
<span data-ttu-id="e98a9-137">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e98a9-137">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e98a9-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e98a9-138">Request</span></span>
<span data-ttu-id="e98a9-139">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="e98a9-139">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationassignment_publish"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/publish
```

##### <a name="response"></a><span data-ttu-id="e98a9-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e98a9-140">Response</span></span>
<span data-ttu-id="e98a9-141">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="e98a9-141">The following is an example of a response.</span></span> 

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
  "description": "educationAssignment: publish",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

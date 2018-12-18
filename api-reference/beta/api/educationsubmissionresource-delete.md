---
title: Eliminar educationSubmissionResource
description: Elimina un recurso de la presentación. Esto puede realizarse sólo por el alumno. Si el recurso se copió desde la asignación, se creará una nueva copia del recurso después de que se elimina la copia actual.
author: dipakboyed
ms.openlocfilehash: d56df6cee3884556186554d9c24ae09ed802c4f0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313275"
---
# <a name="delete-educationsubmissionresource"></a><span data-ttu-id="f0b3b-105">Eliminar educationSubmissionResource</span><span class="sxs-lookup"><span data-stu-id="f0b3b-105">Delete educationSubmissionResource</span></span>

> <span data-ttu-id="f0b3b-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f0b3b-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f0b3b-108">Elimina un recurso de la presentación.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-108">Deletes a resource from the submission.</span></span> <span data-ttu-id="f0b3b-109">Esto puede realizarse sólo por el alumno.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-109">This can only be done by the student.</span></span> <span data-ttu-id="f0b3b-110">Si el recurso se copió desde la asignación, se creará una nueva copia del recurso después de que se elimina la copia actual.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-110">If the resource was copied from the assignment, a new copy of the resource will be created after the current copy is deleted.</span></span> <span data-ttu-id="f0b3b-111">Esto permite "Restablecer" el recurso a su estado original.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-111">This allows you to "reset" the resource to its original state.</span></span> <span data-ttu-id="f0b3b-112">Si el recurso no se ha copiado de la asignación, pero se agregó desde el alumno, simplemente se elimina el recurso.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-112">If the resource was not copied from the assignment but was added from the student, the resource is simply deleted.</span></span>

## <a name="permissions"></a><span data-ttu-id="f0b3b-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="f0b3b-113">Permissions</span></span>
<span data-ttu-id="f0b3b-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f0b3b-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f0b3b-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f0b3b-116">Permission type</span></span>      | <span data-ttu-id="f0b3b-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f0b3b-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f0b3b-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f0b3b-118">Delegated (work or school account)</span></span> |  <span data-ttu-id="f0b3b-119">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f0b3b-119">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="f0b3b-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f0b3b-120">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="f0b3b-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-121">Not supported.</span></span>  |
|<span data-ttu-id="f0b3b-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f0b3b-122">Application</span></span> | <span data-ttu-id="f0b3b-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-123">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="f0b3b-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f0b3b-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /educationClasses/assignments/{id}/submissions/{id}/resources/{id}

```
## <a name="request-headers"></a><span data-ttu-id="f0b3b-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f0b3b-125">Request headers</span></span>
| <span data-ttu-id="f0b3b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0b3b-126">Header</span></span>       | <span data-ttu-id="f0b3b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f0b3b-127">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f0b3b-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="f0b3b-128">Authorization</span></span>  | <span data-ttu-id="f0b3b-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="f0b3b-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f0b3b-131">Request body</span></span>
<span data-ttu-id="f0b3b-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-132">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="f0b3b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0b3b-133">Response</span></span>
<span data-ttu-id="f0b3b-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-p106">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f0b3b-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f0b3b-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f0b3b-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f0b3b-137">Request</span></span>
<span data-ttu-id="f0b3b-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-138">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationsubmissionresource"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/resources/f2387c3b-ec39-4bf2-a399-d7242677f024
```
##### <a name="response"></a><span data-ttu-id="f0b3b-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0b3b-139">Response</span></span>
<span data-ttu-id="f0b3b-140">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0b3b-140">The following is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete educationSubmissionResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
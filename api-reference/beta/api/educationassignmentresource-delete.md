---
title: Eliminar educationAssignmentResource
description: .
ms.openlocfilehash: 9a9798170e8aab9d167a305a8815c26aec8eed13
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084988"
---
# <a name="delete-educationassignmentresource"></a><span data-ttu-id="2735d-103">Eliminar educationAssignmentResource</span><span class="sxs-lookup"><span data-stu-id="2735d-103">Delete educationAssignmentResource</span></span>

> <span data-ttu-id="2735d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2735d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2735d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2735d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2735d-106">Eliminar un recurso de una asignación.</span><span class="sxs-lookup"><span data-stu-id="2735d-106">Delete a resource from an assignment.</span></span> <span data-ttu-id="2735d-107">Sólo los profesores en la clase pueden quitar un recurso.</span><span class="sxs-lookup"><span data-stu-id="2735d-107">Only teachers in the class can remove a resource.</span></span> <span data-ttu-id="2735d-108">Cuando se haya publicado una asignación a los alumnos, profesores no pueden quitar recursos que están marcados como "distributeToStudents".</span><span class="sxs-lookup"><span data-stu-id="2735d-108">After an assignment has been published to students, teachers cannot remove resources that are marked as "distributeToStudents".</span></span>

## <a name="permissions"></a><span data-ttu-id="2735d-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="2735d-109">Permissions</span></span>
<span data-ttu-id="2735d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2735d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2735d-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2735d-112">Permission type</span></span>      | <span data-ttu-id="2735d-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2735d-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2735d-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2735d-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="2735d-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2735d-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="2735d-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2735d-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="2735d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2735d-117">Not supported.</span></span>  |
|<span data-ttu-id="2735d-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2735d-118">Application</span></span> | <span data-ttu-id="2735d-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2735d-119">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="2735d-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2735d-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /educationClasses/assignments/{id}/resources/{id}

```
## <a name="request-headers"></a><span data-ttu-id="2735d-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2735d-121">Request headers</span></span>
| <span data-ttu-id="2735d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2735d-122">Header</span></span>       | <span data-ttu-id="2735d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2735d-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2735d-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="2735d-124">Authorization</span></span>  | <span data-ttu-id="2735d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2735d-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2735d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2735d-127">Request body</span></span>
<span data-ttu-id="2735d-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2735d-128">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="2735d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2735d-129">Response</span></span>
<span data-ttu-id="2735d-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2735d-p105">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2735d-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2735d-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2735d-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2735d-133">Request</span></span>
<span data-ttu-id="2735d-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2735d-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationassignmentresource"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/resources/22002
```
##### <a name="response"></a><span data-ttu-id="2735d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2735d-135">Response</span></span>
<span data-ttu-id="2735d-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2735d-136">The following is an example of the response.</span></span> 


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
  "description": "Delete educationAssignmentResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
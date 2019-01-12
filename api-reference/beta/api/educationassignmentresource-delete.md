---
title: Eliminar educationAssignmentResource
description: .
author: dipakboyed
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: c8154cc9112d62b06d2a93366f01fba3ea7907f2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979589"
---
# <a name="delete-educationassignmentresource"></a><span data-ttu-id="fea02-103">Eliminar educationAssignmentResource</span><span class="sxs-lookup"><span data-stu-id="fea02-103">Delete educationAssignmentResource</span></span>

> <span data-ttu-id="fea02-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fea02-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fea02-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fea02-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fea02-106">Eliminar un recurso de una asignación.</span><span class="sxs-lookup"><span data-stu-id="fea02-106">Delete a resource from an assignment.</span></span> <span data-ttu-id="fea02-107">Sólo los profesores en la clase pueden quitar un recurso.</span><span class="sxs-lookup"><span data-stu-id="fea02-107">Only teachers in the class can remove a resource.</span></span> <span data-ttu-id="fea02-108">Cuando se haya publicado una asignación a los alumnos, profesores no pueden quitar recursos que están marcados como "distributeToStudents".</span><span class="sxs-lookup"><span data-stu-id="fea02-108">After an assignment has been published to students, teachers cannot remove resources that are marked as "distributeToStudents".</span></span>

## <a name="permissions"></a><span data-ttu-id="fea02-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="fea02-109">Permissions</span></span>
<span data-ttu-id="fea02-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fea02-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fea02-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fea02-112">Permission type</span></span>      | <span data-ttu-id="fea02-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fea02-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fea02-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fea02-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="fea02-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fea02-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="fea02-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fea02-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="fea02-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fea02-117">Not supported.</span></span>  |
|<span data-ttu-id="fea02-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fea02-118">Application</span></span> | <span data-ttu-id="fea02-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fea02-119">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="fea02-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fea02-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /educationClasses/assignments/{id}/resources/{id}

```
## <a name="request-headers"></a><span data-ttu-id="fea02-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fea02-121">Request headers</span></span>
| <span data-ttu-id="fea02-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fea02-122">Header</span></span>       | <span data-ttu-id="fea02-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fea02-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="fea02-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="fea02-124">Authorization</span></span>  | <span data-ttu-id="fea02-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fea02-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="fea02-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fea02-127">Request body</span></span>
<span data-ttu-id="fea02-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fea02-128">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="fea02-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fea02-129">Response</span></span>
<span data-ttu-id="fea02-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fea02-p105">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fea02-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fea02-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fea02-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fea02-133">Request</span></span>
<span data-ttu-id="fea02-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fea02-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationassignmentresource"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/resources/22002
```
##### <a name="response"></a><span data-ttu-id="fea02-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fea02-135">Response</span></span>
<span data-ttu-id="fea02-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fea02-136">The following is an example of the response.</span></span> 


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

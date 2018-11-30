---
title: Eliminar educationAssignment
description: Eliminar una asignación existente. Sólo los profesores dentro de una clase pueden eliminar las asignaciones.
ms.openlocfilehash: e9965efa458459cff0c3914dbc12b37153a6ab51
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088067"
---
# <a name="delete-educationassignment"></a><span data-ttu-id="0e1c9-104">Eliminar educationAssignment</span><span class="sxs-lookup"><span data-stu-id="0e1c9-104">Delete educationAssignment</span></span>

> <span data-ttu-id="0e1c9-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0e1c9-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0e1c9-107">Eliminar una asignación existente.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-107">Delete an existing assignment.</span></span> <span data-ttu-id="0e1c9-108">Sólo los profesores dentro de una clase pueden eliminar las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-108">Only teachers within a class can delete assignments.</span></span>

## <a name="permissions"></a><span data-ttu-id="0e1c9-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="0e1c9-109">Permissions</span></span>
<span data-ttu-id="0e1c9-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e1c9-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0e1c9-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e1c9-112">Permission type</span></span>      | <span data-ttu-id="0e1c9-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e1c9-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0e1c9-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e1c9-114">Delegated (work or school account)</span></span>| <span data-ttu-id="0e1c9-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0e1c9-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span> |
|<span data-ttu-id="0e1c9-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e1c9-116">Delegated (personal Microsoft account)</span></span> |   <span data-ttu-id="0e1c9-117">No se admite.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-117">Not Supported.</span></span> |
|<span data-ttu-id="0e1c9-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e1c9-118">Application</span></span> | <span data-ttu-id="0e1c9-119">No se admite.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-119">Not Supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="0e1c9-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e1c9-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /education/classes/<id>/assignments/<id>
```
## <a name="request-headers"></a><span data-ttu-id="0e1c9-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e1c9-121">Request headers</span></span>
| <span data-ttu-id="0e1c9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e1c9-122">Header</span></span>       | <span data-ttu-id="0e1c9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0e1c9-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0e1c9-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e1c9-124">Authorization</span></span>  | <span data-ttu-id="0e1c9-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0e1c9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e1c9-127">Request body</span></span>
<span data-ttu-id="0e1c9-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-128">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="0e1c9-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e1c9-129">Response</span></span>
<span data-ttu-id="0e1c9-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-p106">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e1c9-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e1c9-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="0e1c9-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e1c9-133">Request</span></span>
<span data-ttu-id="0e1c9-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-134">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_educationassignment"
}-->

```http
DELETE https://graph.microsoft.com/beta/education/classes/11014/assignments/19002
```
### <a name="response"></a><span data-ttu-id="0e1c9-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e1c9-135">Response</span></span>
<span data-ttu-id="0e1c9-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e1c9-136">The following is an example of the response.</span></span> 


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
  "description": "Delete educationAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
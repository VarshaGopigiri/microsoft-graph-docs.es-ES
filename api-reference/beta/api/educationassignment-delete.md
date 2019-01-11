---
title: Eliminar educationAssignment
description: Eliminar una asignación existente. Sólo los profesores dentro de una clase pueden eliminar las asignaciones.
author: dipakboyed
localization_priority: Normal
ms.openlocfilehash: 09365c44bef4f12ad9be24f8ed30cfb0efc5c6f3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874994"
---
# <a name="delete-educationassignment"></a><span data-ttu-id="f2a84-104">Eliminar educationAssignment</span><span class="sxs-lookup"><span data-stu-id="f2a84-104">Delete educationAssignment</span></span>

> <span data-ttu-id="f2a84-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f2a84-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f2a84-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f2a84-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f2a84-107">Eliminar una asignación existente.</span><span class="sxs-lookup"><span data-stu-id="f2a84-107">Delete an existing assignment.</span></span> <span data-ttu-id="f2a84-108">Sólo los profesores dentro de una clase pueden eliminar las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="f2a84-108">Only teachers within a class can delete assignments.</span></span>

## <a name="permissions"></a><span data-ttu-id="f2a84-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="f2a84-109">Permissions</span></span>
<span data-ttu-id="f2a84-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f2a84-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f2a84-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f2a84-112">Permission type</span></span>      | <span data-ttu-id="f2a84-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f2a84-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f2a84-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f2a84-114">Delegated (work or school account)</span></span>| <span data-ttu-id="f2a84-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2a84-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span> |
|<span data-ttu-id="f2a84-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f2a84-116">Delegated (personal Microsoft account)</span></span> |   <span data-ttu-id="f2a84-117">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f2a84-117">Not Supported.</span></span> |
|<span data-ttu-id="f2a84-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f2a84-118">Application</span></span> | <span data-ttu-id="f2a84-119">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f2a84-119">Not Supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="f2a84-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f2a84-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /education/classes/<id>/assignments/<id>
```
## <a name="request-headers"></a><span data-ttu-id="f2a84-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f2a84-121">Request headers</span></span>
| <span data-ttu-id="f2a84-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2a84-122">Header</span></span>       | <span data-ttu-id="f2a84-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f2a84-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f2a84-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="f2a84-124">Authorization</span></span>  | <span data-ttu-id="f2a84-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f2a84-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="f2a84-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f2a84-127">Request body</span></span>
<span data-ttu-id="f2a84-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f2a84-128">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="f2a84-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2a84-129">Response</span></span>
<span data-ttu-id="f2a84-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2a84-p106">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f2a84-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2a84-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="f2a84-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f2a84-133">Request</span></span>
<span data-ttu-id="f2a84-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2a84-134">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_educationassignment"
}-->

```http
DELETE https://graph.microsoft.com/beta/education/classes/11014/assignments/19002
```
### <a name="response"></a><span data-ttu-id="f2a84-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2a84-135">Response</span></span>
<span data-ttu-id="f2a84-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2a84-136">The following is an example of the response.</span></span> 


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

---
title: 'educationSubmission: recuperación'
description: 'Indica que un estudiante desea recuperar un envío. Esta acción sólo puede realizarse mediante un estudiante. '
author: dipakboyed
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 9e9155244522d7f1f8c61263aff6de4c87faab4e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984412"
---
# <a name="educationsubmission-recall"></a><span data-ttu-id="04416-104">educationSubmission: recuperación</span><span class="sxs-lookup"><span data-stu-id="04416-104">educationSubmission: recall</span></span>

> <span data-ttu-id="04416-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="04416-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="04416-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="04416-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="04416-107">Indica que un estudiante desea recuperar un envío.</span><span class="sxs-lookup"><span data-stu-id="04416-107">Indicates that a student wants to take back a submission.</span></span> <span data-ttu-id="04416-108">Esta acción sólo puede realizarse mediante un estudiante.</span><span class="sxs-lookup"><span data-stu-id="04416-108">This action can only be done by a student.</span></span> <span data-ttu-id="04416-109">Cambiará el estado de la presentación de "enviada" a "trabajo".</span><span class="sxs-lookup"><span data-stu-id="04416-109">It will change the status of the submission from "submitted" back to "working".</span></span>

## <a name="permissions"></a><span data-ttu-id="04416-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="04416-110">Permissions</span></span>
<span data-ttu-id="04416-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="04416-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="04416-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04416-113">Permission type</span></span>      | <span data-ttu-id="04416-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04416-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="04416-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04416-115">Delegated (work or school account)</span></span> |  <span data-ttu-id="04416-116">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="04416-116">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="04416-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04416-117">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="04416-118">No admitido</span><span class="sxs-lookup"><span data-stu-id="04416-118">Not supported</span></span>  |
|<span data-ttu-id="04416-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04416-119">Application</span></span> |<span data-ttu-id="04416-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04416-120">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="04416-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04416-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/<id>/assignments/{id}/submissions/{id}/recall

```
## <a name="request-headers"></a><span data-ttu-id="04416-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="04416-122">Request headers</span></span>
| <span data-ttu-id="04416-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04416-123">Header</span></span>       | <span data-ttu-id="04416-124">Valor</span><span class="sxs-lookup"><span data-stu-id="04416-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="04416-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="04416-125">Authorization</span></span>  | <span data-ttu-id="04416-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="04416-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="04416-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04416-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="04416-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04416-129">Response</span></span>
<span data-ttu-id="04416-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04416-p106">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04416-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04416-132">Example</span></span>
<span data-ttu-id="04416-133">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="04416-133">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="04416-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04416-134">Request</span></span>
<span data-ttu-id="04416-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04416-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationsubmission_recall"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/recall
```

##### <a name="response"></a><span data-ttu-id="04416-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04416-136">Response</span></span>
<span data-ttu-id="04416-137">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04416-137">The following is an example of the response.</span></span>

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
  "description": "educationSubmission: recall",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

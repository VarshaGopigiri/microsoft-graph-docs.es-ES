---
title: 'educationSubmission: versión'
description: " indica que se ha realizado la clasificación. Esta acción sólo puede realizarse por el profesor."
author: dipakboyed
localization_priority: Normal
ms.openlocfilehash: a2723684f734a9e31dc08fb97d1e184400cac387
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859013"
---
# <a name="educationsubmission-release"></a><span data-ttu-id="274bd-104">educationSubmission: versión</span><span class="sxs-lookup"><span data-stu-id="274bd-104">educationSubmission: release</span></span>

> <span data-ttu-id="274bd-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="274bd-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="274bd-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="274bd-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="274bd-107">Esta acción hace que la calificación y comentarios asociados con este envío disponible para los estudiantes.</span><span class="sxs-lookup"><span data-stu-id="274bd-107">This action makes the grade and feedback associated with this submission available to the student.</span></span> <span data-ttu-id="274bd-108">Esto cambiará el estado de la presentación de "enviada" a "publicada" y se indica que se ha realizado la clasificación.</span><span class="sxs-lookup"><span data-stu-id="274bd-108">This will change the status of the submission from "submitted" to "released" and indicates that grading is done.</span></span> <span data-ttu-id="274bd-109">Esta acción sólo puede realizarse por el profesor.</span><span class="sxs-lookup"><span data-stu-id="274bd-109">This action can only be done by the teacher.</span></span>

## <a name="permissions"></a><span data-ttu-id="274bd-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="274bd-110">Permissions</span></span>
<span data-ttu-id="274bd-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="274bd-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="274bd-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="274bd-113">Permission type</span></span>      | <span data-ttu-id="274bd-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="274bd-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="274bd-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="274bd-115">Delegated (work or school account)</span></span> |  <span data-ttu-id="274bd-116">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="274bd-116">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>   |
|<span data-ttu-id="274bd-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="274bd-117">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="274bd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="274bd-118">Not supported.</span></span>  |
|<span data-ttu-id="274bd-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="274bd-119">Application</span></span> | <span data-ttu-id="274bd-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="274bd-120">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="274bd-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="274bd-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/submissions/{id}/release

```
## <a name="request-headers"></a><span data-ttu-id="274bd-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="274bd-122">Request headers</span></span>
| <span data-ttu-id="274bd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="274bd-123">Header</span></span>       | <span data-ttu-id="274bd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="274bd-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="274bd-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="274bd-125">Authorization</span></span>  | <span data-ttu-id="274bd-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="274bd-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="274bd-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="274bd-128">Request body</span></span>
<span data-ttu-id="274bd-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="274bd-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="274bd-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="274bd-130">Response</span></span>
<span data-ttu-id="274bd-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="274bd-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="274bd-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="274bd-133">Example</span></span>
<span data-ttu-id="274bd-134">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="274bd-134">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="274bd-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="274bd-135">Request</span></span>
<span data-ttu-id="274bd-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="274bd-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationsubmission_release"
}-->

```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/release
```

##### <a name="response"></a><span data-ttu-id="274bd-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="274bd-137">Response</span></span>
<span data-ttu-id="274bd-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="274bd-138">The following is an example of the response.</span></span>

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
  "description": "educationSubmission: release",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

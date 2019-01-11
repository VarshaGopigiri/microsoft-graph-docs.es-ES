---
title: 'educationSubmission: devolver'
description: Esta acción hace que la calificación y comentarios asociados con este envío disponible para los estudiantes.
author: dipakboyed
localization_priority: Normal
ms.openlocfilehash: e4e5802e819543679158a3940fcf35ca624bad71
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887734"
---
# <a name="educationsubmission-return"></a><span data-ttu-id="97774-103">educationSubmission: devolver</span><span class="sxs-lookup"><span data-stu-id="97774-103">educationSubmission: return</span></span>

> <span data-ttu-id="97774-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="97774-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="97774-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="97774-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="97774-106">Esta acción hace que la calificación y comentarios asociados con este envío disponible para los estudiantes.</span><span class="sxs-lookup"><span data-stu-id="97774-106">This action makes the grade and feedback associated with this submission available to the student.</span></span> <span data-ttu-id="97774-107">Esto cambiará el estado de la presentación de "enviada" a "devuelto" y se indica que se proporcionan comentarios o puntuar se lleva a cabo.</span><span class="sxs-lookup"><span data-stu-id="97774-107">This will change the status of the submission from "submitted" to "returned" and indicates that feedback is provided or grading is done.</span></span> <span data-ttu-id="97774-108">Esta acción sólo puede realizarse por el profesor.</span><span class="sxs-lookup"><span data-stu-id="97774-108">This action can only be done by the teacher.</span></span>

## <a name="permissions"></a><span data-ttu-id="97774-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="97774-109">Permissions</span></span>
<span data-ttu-id="97774-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="97774-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="97774-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="97774-112">Permission type</span></span>      | <span data-ttu-id="97774-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="97774-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="97774-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="97774-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="97774-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="97774-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>   |
|<span data-ttu-id="97774-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="97774-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="97774-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97774-117">Not supported.</span></span>  |
|<span data-ttu-id="97774-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="97774-118">Application</span></span> | <span data-ttu-id="97774-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97774-119">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="97774-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="97774-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/submissions/{id}/return

```
## <a name="request-headers"></a><span data-ttu-id="97774-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="97774-121">Request headers</span></span>
| <span data-ttu-id="97774-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97774-122">Header</span></span>       | <span data-ttu-id="97774-123">Valor</span><span class="sxs-lookup"><span data-stu-id="97774-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="97774-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="97774-124">Authorization</span></span>  | <span data-ttu-id="97774-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="97774-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="97774-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="97774-127">Request body</span></span>
<span data-ttu-id="97774-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="97774-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="97774-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97774-129">Response</span></span>
<span data-ttu-id="97774-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="97774-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="97774-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97774-132">Example</span></span>
<span data-ttu-id="97774-133">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="97774-133">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="97774-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="97774-134">Request</span></span>
<span data-ttu-id="97774-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97774-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationsubmission_return"
}-->

```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/return
```

##### <a name="response"></a><span data-ttu-id="97774-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97774-136">Response</span></span>
<span data-ttu-id="97774-137">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="97774-137">The following is an example of the response.</span></span>

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

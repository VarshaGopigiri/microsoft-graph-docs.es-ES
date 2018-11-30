---
title: 'educationSubmission: recuperación'
description: .
ms.openlocfilehash: 8df134a6d8325e5b497baada89bc0fa16d0ee9e6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083995"
---
# <a name="educationsubmission-recall"></a><span data-ttu-id="e1722-103">educationSubmission: recuperación</span><span class="sxs-lookup"><span data-stu-id="e1722-103">educationSubmission: recall</span></span>

> <span data-ttu-id="e1722-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e1722-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e1722-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e1722-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e1722-106">Indica que un estudiante desea recuperar un envío.</span><span class="sxs-lookup"><span data-stu-id="e1722-106">Indicates that a student wants to take back a submission.</span></span> <span data-ttu-id="e1722-107">Esta acción sólo puede realizarse mediante un estudiante.</span><span class="sxs-lookup"><span data-stu-id="e1722-107">This action can only be done by a student.</span></span> <span data-ttu-id="e1722-108">Cambiará el estado de la presentación de "enviada" a "trabajo".</span><span class="sxs-lookup"><span data-stu-id="e1722-108">It will change the status of the submission from "submitted" back to "working".</span></span>

## <a name="permissions"></a><span data-ttu-id="e1722-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="e1722-109">Permissions</span></span>
<span data-ttu-id="e1722-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1722-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e1722-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1722-112">Permission type</span></span>      | <span data-ttu-id="e1722-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1722-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e1722-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1722-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="e1722-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e1722-115">EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite</span></span>  |
|<span data-ttu-id="e1722-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1722-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="e1722-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="e1722-117">Not supported</span></span>  |
|<span data-ttu-id="e1722-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1722-118">Application</span></span> |<span data-ttu-id="e1722-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1722-119">Not supported.</span></span>  | 

## <a name="http-request"></a><span data-ttu-id="e1722-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e1722-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/<id>/assignments/{id}/submissions/{id}/recall

```
## <a name="request-headers"></a><span data-ttu-id="e1722-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1722-121">Request headers</span></span>
| <span data-ttu-id="e1722-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1722-122">Header</span></span>       | <span data-ttu-id="e1722-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e1722-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e1722-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="e1722-124">Authorization</span></span>  | <span data-ttu-id="e1722-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e1722-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e1722-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e1722-127">Request body</span></span>

## <a name="response"></a><span data-ttu-id="e1722-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1722-128">Response</span></span>
<span data-ttu-id="e1722-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1722-p105">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e1722-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1722-131">Example</span></span>
<span data-ttu-id="e1722-132">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e1722-132">The following example shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e1722-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1722-133">Request</span></span>
<span data-ttu-id="e1722-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e1722-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "educationsubmission_recall"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11021/assignments/19002/submissions/850f51b7/recall
```

##### <a name="response"></a><span data-ttu-id="e1722-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1722-135">Response</span></span>
<span data-ttu-id="e1722-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1722-136">The following is an example of the response.</span></span>

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
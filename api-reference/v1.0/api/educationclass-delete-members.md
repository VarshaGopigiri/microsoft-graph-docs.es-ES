---
title: Quitar un alumno
description: Quita un educationUser de un educationClass
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 94a57c461cd461ae5903504fda2bdb3971117a64
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956377"
---
# <a name="remove-a-student"></a><span data-ttu-id="269ae-103">Quitar un alumno</span><span class="sxs-lookup"><span data-stu-id="269ae-103">Remove a student</span></span>

<span data-ttu-id="269ae-104">Quita un [educationUser](../resources/educationuser.md) de un [educationClass](../resources/educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="269ae-104">Removes an [educationUser](../resources/educationuser.md) from an [educationClass](../resources/educationclass.md)</span></span>

><span data-ttu-id="269ae-105">**Nota:** Los profesores _y_ los alumnos se encuentran en la colección **members** de la clase.</span><span class="sxs-lookup"><span data-stu-id="269ae-105">**Note:** Teachers _and_ students are in the class **members** collection.</span></span> <span data-ttu-id="269ae-106">Antes de llamar a esta API, asegúrese de que el **educationUser** que quita no es un profesor.</span><span class="sxs-lookup"><span data-stu-id="269ae-106">Before calling this API, insure that the **educationUser** you are removing is not a teacher.</span></span>  <span data-ttu-id="269ae-107">Obtenga la lista de profesores llamando a [educationclass_list_teachers](educationclass-list-teachers.md) y comprobando que el identificador de usuario del usuario que se va a quitar no se encuentra en la lista de profesores devuelta.</span><span class="sxs-lookup"><span data-stu-id="269ae-107">Get the list of teachers by calling [educationclass_list_teachers](educationclass-list-teachers.md) and verifying the user Id of the user to be removed is not in the returned teacher list.</span></span>

## <a name="permissions"></a><span data-ttu-id="269ae-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="269ae-108">Permissions</span></span>
<span data-ttu-id="269ae-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="269ae-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="269ae-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="269ae-111">Permission type</span></span>      | <span data-ttu-id="269ae-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="269ae-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="269ae-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="269ae-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="269ae-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="269ae-114">Not supported.</span></span>  |
|<span data-ttu-id="269ae-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="269ae-115">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="269ae-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="269ae-116">Not supported.</span></span>  |
|<span data-ttu-id="269ae-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="269ae-117">Application</span></span> | <span data-ttu-id="269ae-118">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="269ae-118">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="269ae-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="269ae-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}/members/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="269ae-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="269ae-120">Request headers</span></span>
| <span data-ttu-id="269ae-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="269ae-121">Header</span></span>       | <span data-ttu-id="269ae-122">Valor</span><span class="sxs-lookup"><span data-stu-id="269ae-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="269ae-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="269ae-123">Authorization</span></span>  | <span data-ttu-id="269ae-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="269ae-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="269ae-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="269ae-126">Request body</span></span>
<span data-ttu-id="269ae-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="269ae-127">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="269ae-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="269ae-128">Response</span></span>
<span data-ttu-id="269ae-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="269ae-129">If successful, this method returns a `204 No Content` response code and an empty response body.</span></span>

## <a name="example"></a><span data-ttu-id="269ae-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="269ae-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="269ae-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="269ae-131">Request</span></span>
<span data-ttu-id="269ae-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="269ae-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/classes/{class-id}/members/{member-id}
```

##### <a name="response"></a><span data-ttu-id="269ae-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="269ae-133">Response</span></span>
<span data-ttu-id="269ae-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="269ae-134">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

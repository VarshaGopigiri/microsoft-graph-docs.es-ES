---
title: Quitar un alumno
description: Quita un educationUser de un educationClass
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: d5d0a51f7687c0ccab6da1a85dd5407faf08fd50
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883856"
---
# <a name="remove-a-student"></a><span data-ttu-id="b6207-103">Quitar un alumno</span><span class="sxs-lookup"><span data-stu-id="b6207-103">Remove a student</span></span>

<span data-ttu-id="b6207-104">Quita un [educationUser](../resources/educationuser.md) de un [educationClass](../resources/educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="b6207-104">Removes an [educationUser](../resources/educationuser.md) from an [educationClass](../resources/educationclass.md)</span></span>

><span data-ttu-id="b6207-105">**Nota:** Los profesores _y_ los alumnos se encuentran en la colección **members** de la clase.</span><span class="sxs-lookup"><span data-stu-id="b6207-105">**Note:** Teachers _and_ students are in the class **members** collection.</span></span> <span data-ttu-id="b6207-106">Antes de llamar a esta API, asegúrese de que el **educationUser** que quita no es un profesor.</span><span class="sxs-lookup"><span data-stu-id="b6207-106">Before calling this API, insure that the **educationUser** you are removing is not a teacher.</span></span>  <span data-ttu-id="b6207-107">Obtenga la lista de profesores llamando a [educationclass_list_teachers](educationclass-list-teachers.md) y comprobando que el identificador de usuario del usuario que se va a quitar no se encuentra en la lista de profesores devuelta.</span><span class="sxs-lookup"><span data-stu-id="b6207-107">Get the list of teachers by calling [educationclass_list_teachers](educationclass-list-teachers.md) and verifying the user Id of the user to be removed is not in the returned teacher list.</span></span>

## <a name="permissions"></a><span data-ttu-id="b6207-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="b6207-108">Permissions</span></span>
<span data-ttu-id="b6207-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6207-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6207-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6207-111">Permission type</span></span>      | <span data-ttu-id="b6207-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6207-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b6207-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6207-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="b6207-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6207-114">Not supported.</span></span>  |
|<span data-ttu-id="b6207-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6207-115">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="b6207-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6207-116">Not supported.</span></span>  |
|<span data-ttu-id="b6207-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6207-117">Application</span></span> | <span data-ttu-id="b6207-118">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6207-118">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="b6207-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6207-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}/members/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="b6207-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6207-120">Request headers</span></span>
| <span data-ttu-id="b6207-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6207-121">Header</span></span>       | <span data-ttu-id="b6207-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b6207-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b6207-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6207-123">Authorization</span></span>  | <span data-ttu-id="b6207-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6207-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b6207-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6207-126">Request body</span></span>
<span data-ttu-id="b6207-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6207-127">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="b6207-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6207-128">Response</span></span>
<span data-ttu-id="b6207-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="b6207-129">If successful, this method returns a `204 No Content` response code and an empty response body.</span></span>

## <a name="example"></a><span data-ttu-id="b6207-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6207-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b6207-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6207-131">Request</span></span>
<span data-ttu-id="b6207-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6207-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/classes/{class-id}/members/{member-id}
```

##### <a name="response"></a><span data-ttu-id="b6207-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6207-133">Response</span></span>
<span data-ttu-id="b6207-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6207-134">The following is an example of the response.</span></span> 
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

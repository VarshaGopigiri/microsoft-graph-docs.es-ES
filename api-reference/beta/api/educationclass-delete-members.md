---
title: Quitar un alumno
description: Quita un educationUser de un educationClass
author: mmast-msft
ms.openlocfilehash: 39defb72f4b0d01171ff92730a8e86b24c43a8ae
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348147"
---
# <a name="remove-a-student"></a><span data-ttu-id="dd712-103">Quitar un alumno</span><span class="sxs-lookup"><span data-stu-id="dd712-103">Remove a student</span></span>

> <span data-ttu-id="dd712-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dd712-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dd712-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dd712-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dd712-106">Quita un [educationUser](../resources/educationuser.md) de un [educationClass](../resources/educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="dd712-106">Removes an [educationUser](../resources/educationuser.md) from an [educationClass](../resources/educationclass.md)</span></span>

><span data-ttu-id="dd712-107">**Nota:** Los profesores _y_ los alumnos se encuentran en la colección **members** de la clase.</span><span class="sxs-lookup"><span data-stu-id="dd712-107">**Note:** Teachers _and_ students are in the class **members** collection.</span></span> <span data-ttu-id="dd712-108">Antes de llamar a esta API, asegúrese de que el **educationUser** que quita no es un profesor.</span><span class="sxs-lookup"><span data-stu-id="dd712-108">Before calling this API, insure that the **educationUser** you are removing is not a teacher.</span></span>  <span data-ttu-id="dd712-109">Obtenga la lista de profesores llamando a [educationclass_list_teachers](educationclass-list-teachers.md) y comprobando que el identificador de usuario del usuario que se va a quitar no se encuentra en la lista de profesores devuelta.</span><span class="sxs-lookup"><span data-stu-id="dd712-109">Get the list of teachers by calling [educationclass_list_teachers](educationclass-list-teachers.md) and verifying the user Id of the user to be removed is not in the returned teacher list.</span></span>

## <a name="permissions"></a><span data-ttu-id="dd712-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="dd712-110">Permissions</span></span>
<span data-ttu-id="dd712-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dd712-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dd712-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dd712-113">Permission type</span></span>      | <span data-ttu-id="dd712-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dd712-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dd712-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dd712-115">Delegated (work or school account)</span></span> |  <span data-ttu-id="dd712-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd712-116">Not supported.</span></span>  |
|<span data-ttu-id="dd712-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dd712-117">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="dd712-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd712-118">Not supported.</span></span>  |
|<span data-ttu-id="dd712-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dd712-119">Application</span></span> | <span data-ttu-id="dd712-120">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dd712-120">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="dd712-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dd712-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}/members/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="dd712-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd712-122">Request headers</span></span>
| <span data-ttu-id="dd712-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd712-123">Header</span></span>       | <span data-ttu-id="dd712-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dd712-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="dd712-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="dd712-125">Authorization</span></span>  | <span data-ttu-id="dd712-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd712-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="dd712-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dd712-128">Request body</span></span>
<span data-ttu-id="dd712-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dd712-129">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="dd712-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd712-130">Response</span></span>
<span data-ttu-id="dd712-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content` y un cuerpo de la respuesta vacío.</span><span class="sxs-lookup"><span data-stu-id="dd712-131">If successful, this method returns a `204 No Content` response code and an empty response body.</span></span>

## <a name="example"></a><span data-ttu-id="dd712-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd712-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dd712-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dd712-133">Request</span></span>
<span data-ttu-id="dd712-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd712-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/classes/11003/members/14008
```

##### <a name="response"></a><span data-ttu-id="dd712-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd712-135">Response</span></span>
<span data-ttu-id="dd712-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd712-136">The following is an example of the response.</span></span> 
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

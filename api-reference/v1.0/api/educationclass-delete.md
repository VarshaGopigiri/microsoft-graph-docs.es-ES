---
title: Eliminar educationClass
description: Elimine una clase. Dado que una clase es también un grupo universal, al eliminar una clase se elimina el grupo.
ms.openlocfilehash: a0afd0175d1bfe79711e442182990ddb50088fb8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029413"
---
# <a name="delete-educationclass"></a><span data-ttu-id="eadaf-104">Eliminar educationClass</span><span class="sxs-lookup"><span data-stu-id="eadaf-104">Delete educationClass</span></span>

<span data-ttu-id="eadaf-105">Elimine una clase.</span><span class="sxs-lookup"><span data-stu-id="eadaf-105">Delete a class.</span></span> <span data-ttu-id="eadaf-106">Dado que una clase es también un grupo universal, al eliminar una clase se elimina el grupo.</span><span class="sxs-lookup"><span data-stu-id="eadaf-106">Because a class is also a universal group, deleting a class deletes the group.</span></span>

## <a name="permissions"></a><span data-ttu-id="eadaf-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="eadaf-107">Permissions</span></span>
<span data-ttu-id="eadaf-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eadaf-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eadaf-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eadaf-110">Permission type</span></span>      | <span data-ttu-id="eadaf-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eadaf-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eadaf-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eadaf-112">Delegated (work or school account)</span></span> |  <span data-ttu-id="eadaf-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eadaf-113">Not supported.</span></span>  |
|<span data-ttu-id="eadaf-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eadaf-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="eadaf-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eadaf-115">Not supported.</span></span>  |
|<span data-ttu-id="eadaf-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eadaf-116">Application</span></span> | <span data-ttu-id="eadaf-117">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eadaf-117">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="eadaf-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eadaf-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}

```
## <a name="request-headers"></a><span data-ttu-id="eadaf-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eadaf-119">Request headers</span></span>
| <span data-ttu-id="eadaf-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eadaf-120">Header</span></span>       | <span data-ttu-id="eadaf-121">Valor</span><span class="sxs-lookup"><span data-stu-id="eadaf-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="eadaf-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="eadaf-122">Authorization</span></span>  | <span data-ttu-id="eadaf-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eadaf-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="eadaf-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eadaf-125">Request body</span></span>
<span data-ttu-id="eadaf-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eadaf-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="eadaf-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eadaf-127">Response</span></span>
<span data-ttu-id="eadaf-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eadaf-p105">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eadaf-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eadaf-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eadaf-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eadaf-131">Request</span></span>
<span data-ttu-id="eadaf-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eadaf-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationclass"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/classes/{class-id}
```
##### <a name="response"></a><span data-ttu-id="eadaf-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eadaf-133">Response</span></span>
<span data-ttu-id="eadaf-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eadaf-134">The following is an example of the response.</span></span> 

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
  "description": "Delete educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
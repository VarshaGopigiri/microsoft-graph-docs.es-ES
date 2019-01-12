---
title: Eliminar educationClass
description: Elimine una clase. Dado que una clase es también un grupo universal, al eliminar una clase se elimina el grupo.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 9b25e95dfa109ef48d67374ba7569a32af22ba50
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935069"
---
# <a name="delete-educationclass"></a><span data-ttu-id="eab62-104">Eliminar educationClass</span><span class="sxs-lookup"><span data-stu-id="eab62-104">Delete educationClass</span></span>

> <span data-ttu-id="eab62-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eab62-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eab62-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eab62-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eab62-107">Elimine una clase.</span><span class="sxs-lookup"><span data-stu-id="eab62-107">Delete a class.</span></span> <span data-ttu-id="eab62-108">Dado que una clase es también un grupo universal, al eliminar una clase se elimina el grupo.</span><span class="sxs-lookup"><span data-stu-id="eab62-108">Because a class is also a universal group, deleting a class deletes the group.</span></span>

## <a name="permissions"></a><span data-ttu-id="eab62-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="eab62-109">Permissions</span></span>
<span data-ttu-id="eab62-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eab62-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eab62-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eab62-112">Permission type</span></span>      | <span data-ttu-id="eab62-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eab62-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eab62-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eab62-114">Delegated (work or school account)</span></span> |  <span data-ttu-id="eab62-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eab62-115">Not supported.</span></span>  |
|<span data-ttu-id="eab62-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eab62-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="eab62-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eab62-117">Not supported.</span></span>  |
|<span data-ttu-id="eab62-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eab62-118">Application</span></span> | <span data-ttu-id="eab62-119">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eab62-119">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="eab62-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eab62-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}

```
## <a name="request-headers"></a><span data-ttu-id="eab62-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eab62-121">Request headers</span></span>
| <span data-ttu-id="eab62-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eab62-122">Header</span></span>       | <span data-ttu-id="eab62-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eab62-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="eab62-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="eab62-124">Authorization</span></span>  | <span data-ttu-id="eab62-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eab62-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="eab62-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eab62-127">Request body</span></span>
<span data-ttu-id="eab62-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eab62-128">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="eab62-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eab62-129">Response</span></span>
<span data-ttu-id="eab62-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eab62-p106">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eab62-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eab62-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eab62-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eab62-133">Request</span></span>
<span data-ttu-id="eab62-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eab62-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationclass"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/classes/11022
```
##### <a name="response"></a><span data-ttu-id="eab62-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eab62-135">Response</span></span>
<span data-ttu-id="eab62-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eab62-136">The following is an example of the response.</span></span> 

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

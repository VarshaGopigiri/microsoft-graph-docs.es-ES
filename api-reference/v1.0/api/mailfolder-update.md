---
title: Update mailfolder
description: Actualiza las propiedades del objeto mailfolder.
author: angelgolfer-ms
ms.openlocfilehash: 2c740d72557204d01abea4e2582467c740295197
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315053"
---
# <a name="update-mailfolder"></a><span data-ttu-id="aa6d3-103">Update mailfolder</span><span class="sxs-lookup"><span data-stu-id="aa6d3-103">Update mailfolder</span></span>

<span data-ttu-id="aa6d3-104">Actualiza las propiedades del objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-104">Update the properties of mailfolder object.</span></span>
## <a name="permissions"></a><span data-ttu-id="aa6d3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="aa6d3-105">Permissions</span></span>
<span data-ttu-id="aa6d3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aa6d3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aa6d3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aa6d3-108">Permission type</span></span>      | <span data-ttu-id="aa6d3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aa6d3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="aa6d3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aa6d3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="aa6d3-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aa6d3-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="aa6d3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aa6d3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="aa6d3-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aa6d3-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="aa6d3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aa6d3-114">Application</span></span> | <span data-ttu-id="aa6d3-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aa6d3-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="aa6d3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa6d3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="aa6d3-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa6d3-117">Request headers</span></span>
| <span data-ttu-id="aa6d3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa6d3-118">Header</span></span>       | <span data-ttu-id="aa6d3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="aa6d3-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="aa6d3-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="aa6d3-120">Authorization</span></span>  | <span data-ttu-id="aa6d3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="aa6d3-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="aa6d3-123">Content-Type</span></span>  | <span data-ttu-id="aa6d3-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="aa6d3-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa6d3-126">Request body</span></span>
<span data-ttu-id="aa6d3-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="aa6d3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa6d3-130">Property</span></span>     | <span data-ttu-id="aa6d3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa6d3-131">Type</span></span>   |<span data-ttu-id="aa6d3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa6d3-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="aa6d3-133">displayName</span><span class="sxs-lookup"><span data-stu-id="aa6d3-133">displayName</span></span>|<span data-ttu-id="aa6d3-134">String</span><span class="sxs-lookup"><span data-stu-id="aa6d3-134">String</span></span>|<span data-ttu-id="aa6d3-135">Nombre para mostrar del objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-135">The mailFolder's display name.</span></span>|

## <a name="response"></a><span data-ttu-id="aa6d3-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa6d3-136">Response</span></span>

<span data-ttu-id="aa6d3-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailFolder](../resources/mailfolder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-137">If successful, this method returns a `200 OK` response code and updated [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="aa6d3-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa6d3-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="aa6d3-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa6d3-139">Request</span></span>
<span data-ttu-id="aa6d3-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_mailfolder"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/mailFolders/{id}
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
}
```
##### <a name="response"></a><span data-ttu-id="aa6d3-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa6d3-141">Response</span></span>
<span data-ttu-id="aa6d3-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa6d3-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update mailfolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

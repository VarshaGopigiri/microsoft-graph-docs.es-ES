---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Cambiar los permisos de uso compartido
localization_priority: Normal
ms.openlocfilehash: 44f98d559ab6dc4c81a4efede2f3f60020c2f944
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859685"
---
# <a name="update-sharing-permission"></a><span data-ttu-id="47108-102">Actualizar permisos de uso compartido</span><span class="sxs-lookup"><span data-stu-id="47108-102">Update sharing permission</span></span>

> <span data-ttu-id="47108-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="47108-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="47108-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="47108-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="47108-105">Actualice las propiedades de un permiso de uso compartido al aplicar revisiones al recurso del permiso.</span><span class="sxs-lookup"><span data-stu-id="47108-105">Update the properties of a sharing permission by patching the permission resource.</span></span>

<span data-ttu-id="47108-106">Solo se puede modificar de esta forma la propiedad **roles**.</span><span class="sxs-lookup"><span data-stu-id="47108-106">Only the **roles** property can be modified this way.</span></span>

## <a name="permissions"></a><span data-ttu-id="47108-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="47108-107">Permissions</span></span>

<span data-ttu-id="47108-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="47108-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="47108-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47108-110">Permission type</span></span>      | <span data-ttu-id="47108-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="47108-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="47108-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="47108-112">Delegated (work or school account)</span></span> | <span data-ttu-id="47108-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="47108-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="47108-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47108-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="47108-115">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="47108-115">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="47108-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47108-116">Application</span></span> | <span data-ttu-id="47108-117">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="47108-117">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="47108-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="47108-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
PATCH /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
PATCH /me/drive/items/{item-id}/permissions/{perm-id}
PATCH /sites/{site-id}/drive/items/{item-id}/permissions/{perm-id}
PATCH /users/{user-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="47108-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="47108-119">Optional request headers</span></span>

| <span data-ttu-id="47108-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="47108-120">Name</span></span>          | <span data-ttu-id="47108-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="47108-121">Type</span></span>   | <span data-ttu-id="47108-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="47108-122">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47108-123">if-match</span><span class="sxs-lookup"><span data-stu-id="47108-123">if-match</span></span>      | <span data-ttu-id="47108-124">string</span><span class="sxs-lookup"><span data-stu-id="47108-124">string</span></span> | <span data-ttu-id="47108-125">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="47108-125">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |

## <a name="request-body"></a><span data-ttu-id="47108-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="47108-126">Request body</span></span>

<span data-ttu-id="47108-127">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="47108-127">In the request body, supply the values for relevant fields that should be updated.</span></span>

<span data-ttu-id="47108-128">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="47108-128">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span>
<span data-ttu-id="47108-129">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="47108-129">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="47108-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="47108-130">Property</span></span>     | <span data-ttu-id="47108-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="47108-131">Type</span></span>   | <span data-ttu-id="47108-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="47108-132">Description</span></span>                   |
|:-------------|:-------|:------------------------------|
| <span data-ttu-id="47108-133">**roles**</span><span class="sxs-lookup"><span data-stu-id="47108-133">**roles**</span></span>    | <span data-ttu-id="47108-134">String</span><span class="sxs-lookup"><span data-stu-id="47108-134">String</span></span> | <span data-ttu-id="47108-135">Matriz de tipos de permisos.</span><span class="sxs-lookup"><span data-stu-id="47108-135">An array of permission types.</span></span> |

## <a name="response"></a><span data-ttu-id="47108-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47108-136">Response</span></span>

<span data-ttu-id="47108-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [permission](../resources/permission.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="47108-137">If successful, this method returns a `200 OK` response code and updated [permission](../resources/permission.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="47108-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47108-138">Example</span></span>

<span data-ttu-id="47108-139">Aquí tiene un ejemplo de la solicitud que cambia el rol en el permiso de uso compartido a solo lectura.</span><span class="sxs-lookup"><span data-stu-id="47108-139">Here is an example of the request that changes the role on the sharing permission to read-only.</span></span>

<!-- {"blockType": "request", "name": "update-permission", "@odata.type": "microsoft.graph.permission", "scopes": "files.readwrite"} -->

```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{item-id}/permissions/{perm-id}
Content-type: application/json

{
  "roles": [ "read" ]
}
```

### <a name="response"></a><span data-ttu-id="47108-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47108-140">Response</span></span>

<span data-ttu-id="47108-141">Si se ejecuta correctamente, este método devuelve un recurso [Permission](../resources/permission.md) en el cuerpo de la respuesta que representa el estado actualizado del permiso.</span><span class="sxs-lookup"><span data-stu-id="47108-141">If successful, this method returns a [Permission](../resources/permission.md) resource in the response body that represents the updated state of the permission.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "grantedTo": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "efee1b77-fb3b-4f65-99d6-274c11914d12"
    }
  },
  "id": "1",
  "roles": [ "read" ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update an item's sharing permissions",
  "keywords": "permission, permissions, sharing, change permissions, update permission",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Update permission"
}-->

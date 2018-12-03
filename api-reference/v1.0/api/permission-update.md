---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Cambiar los permisos de uso compartido
ms.openlocfilehash: d6c710ca4d90bffba18cde316410480f1dde5821
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029882"
---
# <a name="update-sharing-permission"></a><span data-ttu-id="b8cbf-102">Actualizar permisos de uso compartido</span><span class="sxs-lookup"><span data-stu-id="b8cbf-102">Update sharing permission</span></span>

<span data-ttu-id="b8cbf-103">Actualice las propiedades de un permiso de uso compartido al aplicar revisiones al recurso del permiso.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-103">Update the properties of a sharing permission by patching the permission resource.</span></span>

<span data-ttu-id="b8cbf-104">Solo se puede modificar de esta forma la propiedad **roles**.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-104">Only the **roles** property can be modified this way.</span></span>

## <a name="permissions"></a><span data-ttu-id="b8cbf-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b8cbf-105">Permissions</span></span>

<span data-ttu-id="b8cbf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b8cbf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b8cbf-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b8cbf-108">Permission type</span></span>      | <span data-ttu-id="b8cbf-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b8cbf-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b8cbf-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b8cbf-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b8cbf-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b8cbf-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="b8cbf-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b8cbf-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b8cbf-113">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b8cbf-113">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="b8cbf-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b8cbf-114">Application</span></span> | <span data-ttu-id="b8cbf-115">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b8cbf-115">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b8cbf-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8cbf-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
PATCH /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
PATCH /me/drive/items/{item-id}/permissions/{perm-id}
PATCH /sites/{site-id}/drive/items/{item-id}/permissions/{perm-id}
PATCH /users/{user-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="b8cbf-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="b8cbf-117">Optional request headers</span></span>

| <span data-ttu-id="b8cbf-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b8cbf-118">Name</span></span>          | <span data-ttu-id="b8cbf-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8cbf-119">Type</span></span>   | <span data-ttu-id="b8cbf-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8cbf-120">Description</span></span>                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cbf-121">if-match</span><span class="sxs-lookup"><span data-stu-id="b8cbf-121">if-match</span></span>      | <span data-ttu-id="b8cbf-122">string</span><span class="sxs-lookup"><span data-stu-id="b8cbf-122">string</span></span> | <span data-ttu-id="b8cbf-123">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-123">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b8cbf-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8cbf-124">Request body</span></span>

<span data-ttu-id="b8cbf-125">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-125">In the request body, supply the values for relevant fields that should be updated.</span></span>

<span data-ttu-id="b8cbf-126">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-126">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span>
<span data-ttu-id="b8cbf-127">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-127">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b8cbf-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b8cbf-128">Property</span></span> | <span data-ttu-id="b8cbf-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8cbf-129">Type</span></span>              | <span data-ttu-id="b8cbf-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8cbf-130">Description</span></span>                   |
|:---------|:------------------|:------------------------------|
| <span data-ttu-id="b8cbf-131">roles</span><span class="sxs-lookup"><span data-stu-id="b8cbf-131">roles</span></span>    | <span data-ttu-id="b8cbf-132">Colección String</span><span class="sxs-lookup"><span data-stu-id="b8cbf-132">String collection</span></span> | <span data-ttu-id="b8cbf-133">Matriz de tipos de permisos.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-133">An array of permission types.</span></span> |

## <a name="response"></a><span data-ttu-id="b8cbf-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8cbf-134">Response</span></span>

<span data-ttu-id="b8cbf-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [permission](../resources/permission.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-135">If successful, this method returns a `200 OK` response code and updated [permission](../resources/permission.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8cbf-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8cbf-136">Example</span></span>

<span data-ttu-id="b8cbf-137">Aquí tiene un ejemplo de la solicitud que cambia el rol en el permiso de uso compartido a solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-137">Here is an example of the request that changes the role on the sharing permission to read-only.</span></span>

<!-- { "blockType": "request", "name": "update-permission", "@odata.type": "microsoft.graph.permission", "scopes": "files.readwrite", "tags": "service.graph" } -->

```http
PATCH /me/drive/items/{item-id}/permissions/{perm-id}
Content-type: application/json

{
  "roles": [ "read" ]
}
```

### <a name="response"></a><span data-ttu-id="b8cbf-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8cbf-138">Response</span></span>

<span data-ttu-id="b8cbf-139">Si se ejecuta correctamente, este método devuelve un recurso [Permission](../resources/permission.md) en el cuerpo de la respuesta que representa el estado actualizado del permiso.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-139">If successful, this method returns a [Permission](../resources/permission.md) resource in the response body that represents the updated state of the permission.</span></span>

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

## <a name="error-responses"></a><span data-ttu-id="b8cbf-140">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="b8cbf-140">Error responses</span></span>

<span data-ttu-id="b8cbf-141">Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-141">Read the [Error Responses][error-response] topic for more information about how errors are returned.</span></span>

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Update an item's sharing permissions",
  "keywords": "permission, permissions, sharing, change permissions, update permission",
  "section": "documentation",
  "tocPath": "Sharing/Update permission"
} -->
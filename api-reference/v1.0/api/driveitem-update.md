---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Actualizar un archivo o carpeta
ms.openlocfilehash: 5ad7779cd739ed423ba083aed7229852569dcd3e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029927"
---
# <a name="update-driveitem-properties"></a><span data-ttu-id="bde22-102">Actualizar propiedades de DriveItem</span><span class="sxs-lookup"><span data-stu-id="bde22-102">Update DriveItem properties</span></span>

<span data-ttu-id="bde22-103">Actualiza los metadatos de un [DriveItem](../resources/driveitem.md) por identificador o ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="bde22-103">Update the metadata for a [DriveItem](../resources/driveitem.md) by ID or path.</span></span>

<span data-ttu-id="bde22-104">También puede usar una actualización para [mover un elemento](driveitem-move.md) a otro elemento primario actualizando la propiedad **parentReference** del elemento.</span><span class="sxs-lookup"><span data-stu-id="bde22-104">You can also use update to [move an item](driveitem-move.md) to another parent by updating the item's **parentReference** property.</span></span>

## <a name="permissions"></a><span data-ttu-id="bde22-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bde22-105">Permissions</span></span>

<span data-ttu-id="bde22-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bde22-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bde22-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bde22-108">Permission type</span></span>      | <span data-ttu-id="bde22-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bde22-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bde22-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bde22-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bde22-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bde22-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="bde22-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bde22-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bde22-113">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bde22-113">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="bde22-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bde22-114">Application</span></span> | <span data-ttu-id="bde22-115">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bde22-115">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bde22-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bde22-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/items/{item-id}
PATCH /me/drive/items/{item-id}
PATCH /sites/{site-id}/drive/items/{item-id}
PATCH /users/{user-id}/drive/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="bde22-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="bde22-117">Optional request headers</span></span>

| <span data-ttu-id="bde22-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="bde22-118">Name</span></span>          | <span data-ttu-id="bde22-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="bde22-119">Type</span></span>   | <span data-ttu-id="bde22-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="bde22-120">Description</span></span>                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde22-121">if-match</span><span class="sxs-lookup"><span data-stu-id="bde22-121">if-match</span></span>      | <span data-ttu-id="bde22-122">String</span><span class="sxs-lookup"><span data-stu-id="bde22-122">String</span></span> | <span data-ttu-id="bde22-123">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="bde22-123">If this request header is included and the eTag (or cTag) provided does not match the current eTag on the folder, a `412 Precondition Failed` response is returned.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bde22-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bde22-124">Request body</span></span>

<span data-ttu-id="bde22-125">En el cuerpo de la solicitud, proporcione los valores de las propiedades que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="bde22-125">In the request body, supply the values for properties that should be updated.</span></span>

<span data-ttu-id="bde22-126">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="bde22-126">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span>
<span data-ttu-id="bde22-127">Para obtener el mejor rendimiento la aplicación no debe incluir propiedades que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="bde22-127">For best performance your app should not include properties that haven't changed.</span></span>

## <a name="response"></a><span data-ttu-id="bde22-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bde22-128">Response</span></span>

<span data-ttu-id="bde22-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bde22-129">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bde22-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bde22-130">Example</span></span>

<span data-ttu-id="bde22-131">Este ejemplo cambia el nombre del recurso DriveItem por "new-file-name.docx".</span><span class="sxs-lookup"><span data-stu-id="bde22-131">This example renames the DriveItem resource to "new-file-name.docx".</span></span>

<!-- { "blockType": "request", "name": "update-item", "tags": "service.graph" } -->

```http
PATCH /me/drive/items/{item-id}
Content-type: application/json

{
  "name": "new-file-name.docx"
}
```

### <a name="response"></a><span data-ttu-id="bde22-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bde22-132">Response</span></span>

<span data-ttu-id="bde22-133">Si se ejecuta correctamente, este método devuelve un recurso [driveItem][item-resource] en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bde22-133">If successful, this method returns an [driveItem][item-resource] resource in the response body.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "01NKDM7HMOJTVYMDOSXFDK2QJDXCDI3WUK",
  "name": "new-file-name.docx",
  "file": { }
}
```

## <a name="error-responses"></a><span data-ttu-id="bde22-134">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="bde22-134">Error responses</span></span>

<span data-ttu-id="bde22-135">Vea [Respuestas de error][error-response] para obtener los detalles sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="bde22-135">See [Error Responses][error-response] for details about how errors are returned.</span></span>

[error-response]: /graph/errors
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Update or replace the contents or properties of an item.",
  "keywords": "update,replace,contents,item",
  "section": "documentation",
  "tocPath": "Items/Update"
} -->

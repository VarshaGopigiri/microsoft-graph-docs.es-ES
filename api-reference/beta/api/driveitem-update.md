---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Actualizar un archivo o carpeta
localization_priority: Normal
ms.openlocfilehash: 4fed46618da22c859c769f5479517e80e82e2d90
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887356"
---
# <a name="update-driveitem-properties"></a><span data-ttu-id="5b4e7-102">Actualizar propiedades de DriveItem</span><span class="sxs-lookup"><span data-stu-id="5b4e7-102">Update DriveItem properties</span></span>

> <span data-ttu-id="5b4e7-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5b4e7-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5b4e7-105">Actualiza los metadatos de un [DriveItem](../resources/driveitem.md) por identificador o ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-105">Update the metadata for a [DriveItem](../resources/driveitem.md) by ID or path.</span></span>

<span data-ttu-id="5b4e7-106">También puede usar una actualización para [mover un elemento](driveitem-move.md) a otro elemento primario actualizando la propiedad **parentReference** del elemento.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-106">You can also use update to [move an item](driveitem-move.md) to another parent by updating the item's **parentReference** property.</span></span>

## <a name="permissions"></a><span data-ttu-id="5b4e7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5b4e7-107">Permissions</span></span>

<span data-ttu-id="5b4e7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5b4e7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5b4e7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5b4e7-110">Permission type</span></span>      | <span data-ttu-id="5b4e7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5b4e7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5b4e7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5b4e7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5b4e7-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5b4e7-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="5b4e7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5b4e7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5b4e7-115">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5b4e7-115">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="5b4e7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5b4e7-116">Application</span></span> | <span data-ttu-id="5b4e7-117">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5b4e7-117">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5b4e7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5b4e7-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/items/{item-id}
PATCH /me/drive/items/{item-id}
PATCH /sites/{site-id}/drive/items/{item-id}
PATCH /users/{user-id}/drive/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="5b4e7-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="5b4e7-119">Optional request headers</span></span>

| <span data-ttu-id="5b4e7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5b4e7-120">Name</span></span>          | <span data-ttu-id="5b4e7-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b4e7-121">Type</span></span>   | <span data-ttu-id="5b4e7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b4e7-122">Description</span></span>                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4e7-123">if-match</span><span class="sxs-lookup"><span data-stu-id="5b4e7-123">if-match</span></span>      | <span data-ttu-id="5b4e7-124">String</span><span class="sxs-lookup"><span data-stu-id="5b4e7-124">String</span></span> | <span data-ttu-id="5b4e7-125">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-125">If this request header is included and the eTag (or cTag) provided does not match the current eTag on the folder, a `412 Precondition Failed` response is returned.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5b4e7-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5b4e7-126">Request body</span></span>

<span data-ttu-id="5b4e7-127">En el cuerpo de la solicitud, proporcione los valores de las propiedades que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-127">In the request body, supply the values for properties that should be updated.</span></span>

<span data-ttu-id="5b4e7-128">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-128">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span>
<span data-ttu-id="5b4e7-129">Para obtener el mejor rendimiento la aplicación no debe incluir propiedades que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-129">For best performance your app should not include properties that haven't changed.</span></span>

## <a name="response"></a><span data-ttu-id="5b4e7-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b4e7-130">Response</span></span>

<span data-ttu-id="5b4e7-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-131">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5b4e7-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b4e7-132">Example</span></span>

<span data-ttu-id="5b4e7-133">Este ejemplo cambia el nombre del recurso DriveItem por "new-file-name.docx".</span><span class="sxs-lookup"><span data-stu-id="5b4e7-133">This example renames the DriveItem resource to "new-file-name.docx".</span></span>

<!-- { "blockType": "request", "name": "update-item" } -->

```http
PATCH /me/drive/items/{item-id}
Content-type: application/json

{
  "name": "new-file-name.docx"
}
```

### <a name="response"></a><span data-ttu-id="5b4e7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b4e7-134">Response</span></span>

<span data-ttu-id="5b4e7-135">Si se ejecuta correctamente, este método devuelve un recurso [driveItem][item-resource] en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-135">If successful, this method returns an [driveItem][item-resource] resource in the response body.</span></span>

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

## <a name="error-responses"></a><span data-ttu-id="5b4e7-136">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="5b4e7-136">Error responses</span></span>

<span data-ttu-id="5b4e7-137">Vea [Respuestas de error][error-response] para obtener los detalles sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-137">See [Error Responses][error-response] for details about how errors are returned.</span></span>

[error-response]: /graph/errors
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Update or replace the contents or properties of an item.",
  "keywords": "update,replace,contents,item",
  "section": "documentation",
  "tocPath": "Items/Update"
} -->

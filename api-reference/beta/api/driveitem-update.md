---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Actualizar un archivo o carpeta
ms.openlocfilehash: 90fab8a4cfafdbff888e53f968a67fa34c0599d6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088065"
---
# <a name="update-driveitem-properties"></a><span data-ttu-id="ef937-102">Actualizar propiedades de DriveItem</span><span class="sxs-lookup"><span data-stu-id="ef937-102">Update DriveItem properties</span></span>

> <span data-ttu-id="ef937-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ef937-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ef937-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ef937-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ef937-105">Actualiza los metadatos de un [DriveItem](../resources/driveitem.md) por identificador o ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="ef937-105">Update the metadata for a [DriveItem](../resources/driveitem.md) by ID or path.</span></span>

<span data-ttu-id="ef937-106">También puede usar una actualización para [mover un elemento](driveitem-move.md) a otro elemento primario actualizando la propiedad **parentReference** del elemento.</span><span class="sxs-lookup"><span data-stu-id="ef937-106">You can also use update to [move an item](driveitem-move.md) to another parent by updating the item's **parentReference** property.</span></span>

## <a name="permissions"></a><span data-ttu-id="ef937-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ef937-107">Permissions</span></span>

<span data-ttu-id="ef937-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ef937-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ef937-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ef937-110">Permission type</span></span>      | <span data-ttu-id="ef937-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ef937-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ef937-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ef937-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ef937-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ef937-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="ef937-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ef937-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ef937-115">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ef937-115">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="ef937-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ef937-116">Application</span></span> | <span data-ttu-id="ef937-117">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ef937-117">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ef937-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef937-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/items/{item-id}
PATCH /me/drive/items/{item-id}
PATCH /sites/{site-id}/drive/items/{item-id}
PATCH /users/{user-id}/drive/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="ef937-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ef937-119">Optional request headers</span></span>

| <span data-ttu-id="ef937-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef937-120">Name</span></span>          | <span data-ttu-id="ef937-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef937-121">Type</span></span>   | <span data-ttu-id="ef937-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef937-122">Description</span></span>                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef937-123">if-match</span><span class="sxs-lookup"><span data-stu-id="ef937-123">if-match</span></span>      | <span data-ttu-id="ef937-124">String</span><span class="sxs-lookup"><span data-stu-id="ef937-124">String</span></span> | <span data-ttu-id="ef937-125">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="ef937-125">If this request header is included and the eTag (or cTag) provided does not match the current eTag on the folder, a `412 Precondition Failed` response is returned.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ef937-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef937-126">Request body</span></span>

<span data-ttu-id="ef937-127">En el cuerpo de la solicitud, proporcione los valores de las propiedades que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="ef937-127">In the request body, supply the values for properties that should be updated.</span></span>

<span data-ttu-id="ef937-128">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ef937-128">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span>
<span data-ttu-id="ef937-129">Para obtener el mejor rendimiento la aplicación no debe incluir propiedades que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ef937-129">For best performance your app should not include properties that haven't changed.</span></span>

## <a name="response"></a><span data-ttu-id="ef937-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef937-130">Response</span></span>

<span data-ttu-id="ef937-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef937-131">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ef937-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef937-132">Example</span></span>

<span data-ttu-id="ef937-133">Este ejemplo cambia el nombre del recurso DriveItem por "new-file-name.docx".</span><span class="sxs-lookup"><span data-stu-id="ef937-133">This example renames the DriveItem resource to "new-file-name.docx".</span></span>

<!-- { "blockType": "request", "name": "update-item" } -->

```http
PATCH /me/drive/items/{item-id}
Content-type: application/json

{
  "name": "new-file-name.docx"
}
```

### <a name="response"></a><span data-ttu-id="ef937-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef937-134">Response</span></span>

<span data-ttu-id="ef937-135">Si se ejecuta correctamente, este método devuelve un recurso [driveItem][item-resource] en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef937-135">If successful, this method returns an [driveItem][item-resource] resource in the response body.</span></span>

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

## <a name="error-responses"></a><span data-ttu-id="ef937-136">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="ef937-136">Error responses</span></span>

<span data-ttu-id="ef937-137">Vea [Respuestas de error][error-response] para obtener los detalles sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="ef937-137">See [Error Responses][error-response] for details about how errors are returned.</span></span>

[error-response]: /graph/errors
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Update or replace the contents or properties of an item.",
  "keywords": "update,replace,contents,item",
  "section": "documentation",
  "tocPath": "Items/Update"
} -->

---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Mover un archivo o carpeta
ms.openlocfilehash: 4fdf9b079068f3a07a74f117c3e3ad6798a2cd1f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085891"
---
# <a name="move-a-driveitem-to-a-new-folder"></a><span data-ttu-id="b718b-102">Mover un objeto DriveItem a una carpeta nueva</span><span class="sxs-lookup"><span data-stu-id="b718b-102">Move a DriveItem to a new folder</span></span>

> <span data-ttu-id="b718b-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b718b-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b718b-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b718b-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b718b-105">Para mover un objeto DriveItem a un nuevo elemento primario, la aplicación solicita actualizar la **parentReference** del objeto DriveItem que se moverá.</span><span class="sxs-lookup"><span data-stu-id="b718b-105">To move a DriveItem to a new parent item, your app requests to update the **parentReference** of the DriveItem to move.</span></span>

<span data-ttu-id="b718b-106">Este es un caso especial del método [Update](driveitem-update.md).</span><span class="sxs-lookup"><span data-stu-id="b718b-106">This is a special case of the [Update](driveitem-update.md) method.</span></span>
<span data-ttu-id="b718b-107">La aplicación puede mover un elemento a un nuevo contenedor y actualizar otras propiedades del elemento en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="b718b-107">Your app can combine moving an item to a new container and updating other properties of the item into a single request.</span></span>

<span data-ttu-id="b718b-108">No se pueden mover elementos entre [Drives](../resources/drive.md) con esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="b718b-108">Items cannot be moved between [Drives](../resources/drive.md) using this request.</span></span>

## <a name="permissions"></a><span data-ttu-id="b718b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="b718b-109">Permissions</span></span>
<span data-ttu-id="b718b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b718b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b718b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b718b-112">Permission type</span></span>      | <span data-ttu-id="b718b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b718b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b718b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b718b-114">Delegated (work or school account)</span></span> | <span data-ttu-id="b718b-115">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b718b-115">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="b718b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b718b-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b718b-117">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b718b-117">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="b718b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b718b-118">Application</span></span> | <span data-ttu-id="b718b-119">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b718b-119">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b718b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b718b-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/{item-id}
PATCH /me/drive/items/{item-id}
PATCH /sites/{site-id}/drive/items/{item-id}
PATCH /users/{user-id}/drive/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="b718b-121">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="b718b-121">Optional request headers</span></span>

| <span data-ttu-id="b718b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b718b-122">Name</span></span>          | <span data-ttu-id="b718b-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="b718b-123">Type</span></span>   | <span data-ttu-id="b718b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b718b-124">Description</span></span>                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b718b-125">if-match</span><span class="sxs-lookup"><span data-stu-id="b718b-125">if-match</span></span>      | <span data-ttu-id="b718b-126">String</span><span class="sxs-lookup"><span data-stu-id="b718b-126">String</span></span> | <span data-ttu-id="b718b-127">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="b718b-127">If this request header is included and the eTag (or cTag) provided does not match the current eTag on the folder, a `412 Precondition Failed` response is returned.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b718b-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b718b-128">Request body</span></span>

<span data-ttu-id="b718b-p104">En el cuerpo de la solicitud, proporcione el nuevo valor de la propiedad **parentReference**. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b718b-p104">In the request body, supply the new value for the **parentReference** property. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

<span data-ttu-id="b718b-132">**Nota:** Al mover elementos a la raíz de una unidad, la aplicación no puede usar la sintaxis `"id:" "root"`.</span><span class="sxs-lookup"><span data-stu-id="b718b-132">**Note:** When moving items to the root of a drive your app cannot use the `"id:" "root"` syntax.</span></span>
<span data-ttu-id="b718b-133">La aplicación debe proporcionar el identificador real de la carpeta raíz para la referencia primaria.</span><span class="sxs-lookup"><span data-stu-id="b718b-133">Your app needs to provide the actual ID of the root folder for the parent reference.</span></span>

## <a name="response"></a><span data-ttu-id="b718b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b718b-134">Response</span></span>

<span data-ttu-id="b718b-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b718b-135">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b718b-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b718b-136">Example</span></span>

<span data-ttu-id="b718b-137">En este ejemplo, se mueve un elemento especificado mediante {item-id} a una carpeta en la unidad del usuario con el identificador `new-parent-folder-id`.</span><span class="sxs-lookup"><span data-stu-id="b718b-137">This example moves an item specified by {item-id} into a folder in the user's drive with the ID `new-parent-folder-id`.</span></span>

<!-- { "blockType": "request", "name": "move-item", "scopes": "files.readwrite" } -->

```http
PATCH /me/drive/items/{item-id}
Content-type: application/json

{
  "parentReference": {
    "id": "new-parent-folder-id"
  },
  "name": "new-item-name.txt"
}
```

### <a name="response"></a><span data-ttu-id="b718b-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b718b-138">Response</span></span>

<span data-ttu-id="b718b-139">En el ejemplo siguiente se muestra la respuesta de esta solicitud de movimiento.</span><span class="sxs-lookup"><span data-stu-id="b718b-139">The following example shows the response for this move request.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "0123456789abc",
  "name": "new-item-name.txt",
  "parentReference":
  {
    "driveId": "11231001",
    "path": "/drive/root:/Documents",
    "id": "1231203102!1011"
  }
}
```

## <a name="error-responses"></a><span data-ttu-id="b718b-140">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="b718b-140">Error responses</span></span>

<span data-ttu-id="b718b-141">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="b718b-141">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Move an item to another location or rename the item.",
  "keywords": "move,rename,mv,change location",
  "section": "documentation",
  "tocPath": "Items/Move"
} -->

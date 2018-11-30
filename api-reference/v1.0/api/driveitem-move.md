---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Mover un archivo o carpeta
ms.openlocfilehash: 656e5356e4ea3033b0e00a99f8f79378253158a4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030679"
---
# <a name="move-a-driveitem-to-a-new-folder"></a><span data-ttu-id="0846c-102">Mover un objeto DriveItem a una carpeta nueva</span><span class="sxs-lookup"><span data-stu-id="0846c-102">Move a DriveItem to a new folder</span></span>

<span data-ttu-id="0846c-103">Para mover un objeto DriveItem a un nuevo elemento primario, la aplicación solicita actualizar la **parentReference** del objeto DriveItem que se moverá.</span><span class="sxs-lookup"><span data-stu-id="0846c-103">To move a DriveItem to a new parent item, your app requests to update the **parentReference** of the DriveItem to move.</span></span>

<span data-ttu-id="0846c-104">Este es un caso especial del método [Update](driveitem-update.md).</span><span class="sxs-lookup"><span data-stu-id="0846c-104">This is a special case of the [Update](driveitem-update.md) method.</span></span>
<span data-ttu-id="0846c-105">La aplicación puede mover un elemento a un nuevo contenedor y actualizar otras propiedades del elemento en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="0846c-105">Your app can combine moving an item to a new container and updating other properties of the item into a single request.</span></span>

<span data-ttu-id="0846c-106">No se pueden mover elementos entre [Drives](../resources/drive.md) con esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="0846c-106">Items cannot be moved between [Drives](../resources/drive.md) using this request.</span></span>

## <a name="permissions"></a><span data-ttu-id="0846c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0846c-107">Permissions</span></span>
<span data-ttu-id="0846c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0846c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0846c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0846c-110">Permission type</span></span>      | <span data-ttu-id="0846c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0846c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0846c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0846c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0846c-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0846c-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="0846c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0846c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0846c-115">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0846c-115">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="0846c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0846c-116">Application</span></span> | <span data-ttu-id="0846c-117">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0846c-117">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0846c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0846c-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/{item-id}
PATCH /me/drive/items/{item-id}
PATCH /sites/{site-id}/drive/items/{item-id}
PATCH /users/{user-id}/drive/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="0846c-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="0846c-119">Optional request headers</span></span>

| <span data-ttu-id="0846c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0846c-120">Name</span></span>          | <span data-ttu-id="0846c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="0846c-121">Type</span></span>   | <span data-ttu-id="0846c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0846c-122">Description</span></span>                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0846c-123">if-match</span><span class="sxs-lookup"><span data-stu-id="0846c-123">if-match</span></span>      | <span data-ttu-id="0846c-124">String</span><span class="sxs-lookup"><span data-stu-id="0846c-124">String</span></span> | <span data-ttu-id="0846c-125">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="0846c-125">If this request header is included and the eTag (or cTag) provided does not match the current eTag on the folder, a `412 Precondition Failed` response is returned.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0846c-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0846c-126">Request body</span></span>

<span data-ttu-id="0846c-p103">En el cuerpo de la solicitud, proporcione el nuevo valor de la propiedad **parentReference**. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="0846c-p103">In the request body, supply the new value for the **parentReference** property. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

<span data-ttu-id="0846c-130">**Nota:** Al mover elementos a la raíz de una unidad, la aplicación no puede usar la sintaxis `"id:" "root"`.</span><span class="sxs-lookup"><span data-stu-id="0846c-130">**Note:** When moving items to the root of a drive your app cannot use the `"id:" "root"` syntax.</span></span>
<span data-ttu-id="0846c-131">La aplicación debe proporcionar el identificador real de la carpeta raíz para la referencia primaria.</span><span class="sxs-lookup"><span data-stu-id="0846c-131">Your app needs to provide the actual ID of the root folder for the parent reference.</span></span>

## <a name="response"></a><span data-ttu-id="0846c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0846c-132">Response</span></span>

<span data-ttu-id="0846c-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0846c-133">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0846c-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0846c-134">Example</span></span>

<span data-ttu-id="0846c-135">En este ejemplo, se mueve un elemento especificado mediante {item-id} a una carpeta en la unidad del usuario con el identificador `new-parent-folder-id`.</span><span class="sxs-lookup"><span data-stu-id="0846c-135">This example moves an item specified by {item-id} into a folder in the user's drive with the ID `new-parent-folder-id`.</span></span>

<!-- { "blockType": "request", "name": "move-item", "scopes": "files.readwrite", "tags": "service.graph" } -->

```http
PATCH /me/drive/items/{item-id}
Content-type: application/json

{
  "parentReference": {
    "id": "{new-parent-folder-id}"
  },
  "name": "new-item-name.txt"
}
```

### <a name="response"></a><span data-ttu-id="0846c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0846c-136">Response</span></span>

<span data-ttu-id="0846c-137">En el ejemplo siguiente se muestra la respuesta de esta solicitud de movimiento.</span><span class="sxs-lookup"><span data-stu-id="0846c-137">The following example shows the response for this move request.</span></span>

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

## <a name="error-responses"></a><span data-ttu-id="0846c-138">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="0846c-138">Error responses</span></span>

<span data-ttu-id="0846c-139">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="0846c-139">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Move an item to another location or rename the item.",
  "keywords": "move,rename,mv,change location",
  "section": "documentation",
  "tocPath": "Items/Move"
} -->

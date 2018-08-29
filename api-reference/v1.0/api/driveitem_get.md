---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un archivo o carpeta
ms.openlocfilehash: 9d45cf345981eb3da638d2f25bb51428ec40b7f9
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267986"
---
# <a name="get-a-driveitem-resource"></a><span data-ttu-id="2a00d-102">Get a DriveItem resource</span><span class="sxs-lookup"><span data-stu-id="2a00d-102">Get a DriveItem resource</span></span>

<span data-ttu-id="2a00d-103">Recupera los metadatos de un [DriveItem](../resources/driveitem.md) en un [Drive](../resources/drive.md) a través del identificador o ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="2a00d-103">Retrieve the metadata for a [DriveItem](../resources/driveitem.md) in a [Drive](../resources/drive.md) by file system path or ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="2a00d-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="2a00d-104">Permissions</span></span>

<span data-ttu-id="2a00d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2a00d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2a00d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2a00d-107">Permission type</span></span>      | <span data-ttu-id="2a00d-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2a00d-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2a00d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2a00d-109">Delegated (work or school account)</span></span> | <span data-ttu-id="2a00d-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2a00d-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="2a00d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2a00d-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2a00d-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2a00d-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="2a00d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2a00d-113">Application</span></span> | <span data-ttu-id="2a00d-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2a00d-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2a00d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2a00d-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}
GET /drives/{drive-id}/root:/{item-path}
GET /groups/{group-id}/drive/items/{item-id}
GET /groups/{group-id}/drive/root:/{item-path}
GET /me/drive/items/{item-id}
GET /me/drive/root:/{item-path}
GET /sites/{siteId}/drive/items/{itemId}
GET /sites/{siteId}/drive/root:/{item-path}
GET /users/{userId}/drive/items/{itemId}
GET /users/{userId}/drive/root:/{item-path}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="2a00d-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2a00d-116">Optional query parameters</span></span>

<span data-ttu-id="2a00d-117">Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$expand` y `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a00d-117">This method supports the `$expand` and `$select` [OData query parameters](../../../concepts/query_parameters.md) to customize the response.</span></span>

<span data-ttu-id="2a00d-118">Puede usar el [parámetro de cadena de consulta `$expand`](../../../concepts/query_parameters.md) para incluir los elementos secundarios de un elemento en la misma llamada al recuperar los metadatos de un elemento si el elemento tiene una relación **children**.</span><span class="sxs-lookup"><span data-stu-id="2a00d-118">You can use the [`$expand` query string parameter](../../../concepts/query_parameters.md) to include the children of an item in the same call as retrieving the metadata of an item if the item has a **children** relationship.</span></span>

## <a name="optional-request-headers"></a><span data-ttu-id="2a00d-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="2a00d-119">Optional request headers</span></span>

| <span data-ttu-id="2a00d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2a00d-120">Name</span></span>          | <span data-ttu-id="2a00d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2a00d-121">Value</span></span>  | <span data-ttu-id="2a00d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a00d-122">Description</span></span>                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a00d-123">if-none-match</span><span class="sxs-lookup"><span data-stu-id="2a00d-123">if-none-match</span></span> | <span data-ttu-id="2a00d-124">String</span><span class="sxs-lookup"><span data-stu-id="2a00d-124">String</span></span> | <span data-ttu-id="2a00d-125">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="2a00d-125">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="response"></a><span data-ttu-id="2a00d-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a00d-126">Response</span></span>

<span data-ttu-id="2a00d-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a00d-127">If successful, this method returns a `200 OK` response code and the [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2a00d-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a00d-128">Example</span></span>

### <a name="request"></a><span data-ttu-id="2a00d-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2a00d-129">Request</span></span>

<span data-ttu-id="2a00d-130">Aquí tiene un ejemplo de la solicitud a la carpeta raíz de OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="2a00d-130">Here is an example of the request to the root folder of the user's OneDrive.</span></span>

<!-- { "blockType": "request", "name": "get-drive-root", "tags": "service.graph" }-->

```http
GET /me/drive/root
```

## <a name="response"></a><span data-ttu-id="2a00d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a00d-131">Response</span></span>

<span data-ttu-id="2a00d-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a00d-132">Here is an example of the response.</span></span>

<!-- { "blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.driveItem" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "createdBy": {
      "user": {
          "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
          "displayName": "Ryan Gregg"
      }
  },
  "createdDateTime": "2016-03-21T20:01:37Z",
  "cTag": "\"c:{86EB4C8E-D20D-46B9-AD41-23B8868DDA8A},0\"",
  "eTag": "\"{86EB4C8E-D20D-46B9-AD41-23B8868DDA8A},1\"",
  "folder": { "childCount": 120 },
  "id": "01NKDM7HMOJTVYMDOSXFDK2QJDXCDI3WUK",
  "lastModifiedBy": {
      "user": {
          "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
          "displayName": "Ryan Gregg"
      }
  },
  "lastModifiedDateTime": "2016-03-21T20:01:37Z",
  "name": "OneDrive",
  "root": { },
  "size": 157286400,
  "webUrl": "https://contoso-my.sharepoint.com/personal/rgregg_contoso_com/Documents"
}
```

## <a name="remarks"></a><span data-ttu-id="2a00d-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a00d-133">Remarks</span></span>

<span data-ttu-id="2a00d-134">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="2a00d-134">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: ../../../concepts/errors.md
[odata-parameters]: ../../../concepts/query_parameters.md
[item-resource]: ../resources/driveitem.md
[special-folder]: ../api/drive_get_specialfolder.md

<!-- {
  "type": "#page.annotation",
  "description": "Retrieve metadata about an item and its children in OneDrive",
  "keywords": "retrieve,item,metadata",
  "section": "documentation",
  "tocPath": "Items/Get item"
} -->

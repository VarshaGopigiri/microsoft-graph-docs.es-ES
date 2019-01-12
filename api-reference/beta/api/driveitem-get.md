---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener un archivo o carpeta
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 977209dba7284bb8f4f1abe5037d229f4a5a34c0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945464"
---
# <a name="get-a-driveitem-resource"></a><span data-ttu-id="ffe65-102">Get a DriveItem resource</span><span class="sxs-lookup"><span data-stu-id="ffe65-102">Get a DriveItem resource</span></span>

> <span data-ttu-id="ffe65-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ffe65-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ffe65-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ffe65-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ffe65-105">Recupera los metadatos de un [DriveItem](../resources/driveitem.md) en un [Drive](../resources/drive.md) a través del identificador o ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="ffe65-105">Retrieve the metadata for a [DriveItem](../resources/driveitem.md) in a [Drive](../resources/drive.md) by file system path or ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="ffe65-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="ffe65-106">Permissions</span></span>

<span data-ttu-id="ffe65-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ffe65-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ffe65-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ffe65-109">Permission type</span></span>      | <span data-ttu-id="ffe65-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ffe65-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ffe65-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ffe65-111">Delegated (work or school account)</span></span> | <span data-ttu-id="ffe65-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffe65-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="ffe65-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ffe65-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ffe65-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffe65-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="ffe65-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ffe65-115">Application</span></span> | <span data-ttu-id="ffe65-116">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffe65-116">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ffe65-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ffe65-117">HTTP request</span></span>

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

## <a name="optional-query-parameters"></a><span data-ttu-id="ffe65-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ffe65-118">Optional query parameters</span></span>

<span data-ttu-id="ffe65-119">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$expand` y `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffe65-119">This method supports the `$expand` and `$select` [OData query parameters](/graph/query-parameters) to customize the response.</span></span>

<span data-ttu-id="ffe65-120">Puede usar el [parámetro de cadena de consulta `$expand`](/graph/query-parameters) para incluir los elementos secundarios de un elemento en la misma llamada al recuperar los metadatos de un elemento si el elemento tiene una relación **children**.</span><span class="sxs-lookup"><span data-stu-id="ffe65-120">You can use the [`$expand` query string parameter](/graph/query-parameters) to include the children of an item in the same call as retrieving the metadata of an item if the item has a **children** relationship.</span></span>

## <a name="optional-request-headers"></a><span data-ttu-id="ffe65-121">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ffe65-121">Optional request headers</span></span>

| <span data-ttu-id="ffe65-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="ffe65-122">Name</span></span>          | <span data-ttu-id="ffe65-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ffe65-123">Value</span></span>  | <span data-ttu-id="ffe65-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffe65-124">Description</span></span>                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe65-125">if-none-match</span><span class="sxs-lookup"><span data-stu-id="ffe65-125">if-none-match</span></span> | <span data-ttu-id="ffe65-126">String</span><span class="sxs-lookup"><span data-stu-id="ffe65-126">String</span></span> | <span data-ttu-id="ffe65-127">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="ffe65-127">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="response"></a><span data-ttu-id="ffe65-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffe65-128">Response</span></span>

<span data-ttu-id="ffe65-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffe65-129">If successful, this method returns a `200 OK` response code and the [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ffe65-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ffe65-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="ffe65-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ffe65-131">Request</span></span>

<span data-ttu-id="ffe65-132">Aquí tiene un ejemplo de la solicitud a la carpeta raíz de OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="ffe65-132">Here is an example of the request to the root folder of the user's OneDrive.</span></span>

<!-- { "blockType": "request", "name": "get-item-metadata" }-->

```http
GET /me/drive/root
```

## <a name="response"></a><span data-ttu-id="ffe65-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffe65-133">Response</span></span>

<span data-ttu-id="ffe65-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffe65-134">Here is an example of the response.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="ffe65-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ffe65-135">Remarks</span></span>

<span data-ttu-id="ffe65-136">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="ffe65-136">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: /graph/errors
[odata-parameters]: /graph/query-parameters
[item-resource]: ../resources/driveitem.md
[special-folder]: ../api/drive-get-specialfolder.md

<!-- {
  "type": "#page.annotation",
  "description": "Retrieve metadata about an item and its children in OneDrive",
  "keywords": "retrieve,item,metadata",
  "section": "documentation",
  "tocPath": "Items/Get item"
} -->

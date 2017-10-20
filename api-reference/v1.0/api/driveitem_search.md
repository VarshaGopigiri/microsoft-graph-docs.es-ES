---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Buscar archivos
ms.openlocfilehash: 1d4b4153f6c208390d928fc7833ecc5e1a9be094
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="search-for-a-driveitems-within-a-drive"></a><span data-ttu-id="b4d0b-102">Buscar objetos DriveItem dentro de una unidad</span><span class="sxs-lookup"><span data-stu-id="b4d0b-102">Search for a DriveItem within a drive</span></span>

<span data-ttu-id="b4d0b-103">Busque elementos que coincidan con una consulta en la jerarquía de elementos.</span><span class="sxs-lookup"><span data-stu-id="b4d0b-103">Search the hierarchy of items in OneDrive for items matching a query.</span></span>
<span data-ttu-id="b4d0b-104">Puede buscar en una jerarquía de carpetas, en una unidad entera o en los archivos que se comparten con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="b4d0b-104">Search the hierarchy of items for items matching a query. You can search within a folder hierarhcy, a whole drive, or files shared with the current user.</span></span>

## <a name="permissions"></a><span data-ttu-id="b4d0b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b4d0b-105">Permissions</span></span>

<span data-ttu-id="b4d0b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b4d0b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b4d0b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4d0b-108">Permission type</span></span>      | <span data-ttu-id="b4d0b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b4d0b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b4d0b-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4d0b-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="b4d0b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4d0b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b4d0b-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4d0b-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="b4d0b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4d0b-114">Application</span></span> | <span data-ttu-id="b4d0b-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4d0b-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b4d0b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4d0b-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/root/search(q='{search-text}')
GET /groups/{group-id}/drive/root/search(q='{search-text}')
GET /me/drive/root/search(q='{search-text}')
GET /sites/{site-id}/drive/root/search(q='{search-text}')
GET /users/{user-id}/drive/root/search(q='{search-text}')
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b4d0b-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b4d0b-117">Optional query parameters</span></span>

<span data-ttu-id="b4d0b-118">Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4d0b-118">This method supports the `$expand`, `$select`, `$skipToken`, `$top`, and `$orderby` [OData query parameters](../../../concepts/query_parameters.md) to customize the response.</span></span>

## <a name="function-parameters"></a><span data-ttu-id="b4d0b-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="b4d0b-119">Function parameters</span></span>

| <span data-ttu-id="b4d0b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b4d0b-120">Name</span></span> | <span data-ttu-id="b4d0b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b4d0b-121">Value</span></span>  | <span data-ttu-id="b4d0b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4d0b-122">Description</span></span>                                                                                                                          |
|:-----|:-------|:-------------------------------------------------------------------------------------------------------------------------------------|
| `q`  | <span data-ttu-id="b4d0b-123">string</span><span class="sxs-lookup"><span data-stu-id="b4d0b-123">string</span></span> | <span data-ttu-id="b4d0b-p103">El texto de la consulta usado para buscar elementos. Los valores pueden coincidir en varios campos, como el nombre de archivo, los metadatos y el contenido de los archivos.</span><span class="sxs-lookup"><span data-stu-id="b4d0b-p103">The query text used to search for items. Values may be matched across several fields including filename, metadata, and file content.</span></span> |

## <a name="example"></a><span data-ttu-id="b4d0b-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4d0b-126">Example</span></span>

### <a name="request"></a><span data-ttu-id="b4d0b-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b4d0b-127">Request</span></span>

<span data-ttu-id="b4d0b-128">Este es un ejemplo de la solicitud buscando en el OneDrive del usuario actual</span><span class="sxs-lookup"><span data-stu-id="b4d0b-128">Here is an example of the request searching the current user's OneDrive</span></span>

<!-- { "blockType": "request", "name": "item_search" }-->

```http
GET /me/drive/root/search(q='{search-query}')
```

### <a name="response"></a><span data-ttu-id="b4d0b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4d0b-129">Response</span></span>

<span data-ttu-id="b4d0b-p104">Este método devuelve un objeto que contiene una colección de objetos [DriveItem](../resources/driveitem.md) que coinciden con los criterios de búsqueda. Si no se han encontrado elementos, se devuelve una colección vacía.</span><span class="sxs-lookup"><span data-stu-id="b4d0b-p104">This method returns an object containing an collection of [DriveItems](../resources/driveitem.md) that match the search criteria. If no items were found, an empty collection is returned.</span></span>

<span data-ttu-id="b4d0b-p105">Si hay demasiadas coincidencias, se paginará la respuesta y una propiedad **@odata.nextLink** contendrá una dirección URL a la siguiente página de resultados. Puede usar el parámetro de consulta `$top` para especificar el número de elementos en la página.</span><span class="sxs-lookup"><span data-stu-id="b4d0b-p105">If there are too many matches the response will be paged and an **@odata.nextLink** property will contain a URL to the next page of results. You can use the `$top` query parameter to specify the number of items in the page.</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
      {
        "id": "0123456789abc!123",
        "name": "Contoso Project",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!123" }
      },
      {
        "id": "0123456789abc!456",
        "name": "Contoso Project 2016",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!456" }
      }
    ],
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/drive/root/search(query='contoso project')&skipToken=1asdlnjnkj1nalkm!asd"
}
```

## <a name="searching-for-items-a-user-can-access"></a><span data-ttu-id="b4d0b-134">Buscar elementos a los que puede acceder un usuario</span><span class="sxs-lookup"><span data-stu-id="b4d0b-134">Searching for items a user can access</span></span>

<span data-ttu-id="b4d0b-p106">Además de buscar elementos de una unidad, la aplicación puede buscar de forma más amplia para incluir elementos que se comparten con el usuario actual. Para ampliar el ámbito de búsqueda, use el método **search** en el recurso [Drive](../resources/drive.md).</span><span class="sxs-lookup"><span data-stu-id="b4d0b-p106">In addition to searching for items within a drive, your app can search more broadly to include items shared with the current user. To broaden the search scope, use the **search** method on the [Drive](../resources/drive.md) resource.</span></span>

### <a name="example"></a><span data-ttu-id="b4d0b-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4d0b-137">Example</span></span>

<!-- { "blockType": "request", "name": "item_search_all" }-->

```http
GET /me/drive/search(q='{search-query}')
```

### <a name="response"></a><span data-ttu-id="b4d0b-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4d0b-138">Response</span></span>

<span data-ttu-id="b4d0b-p107">Las respuestas al buscar desde el recurso **Drive** pueden incluir elementos fuera de la unidad (elementos compartidos con el usuario actual). Estos elementos incluirán la faceta [**remoteItem**](../resources/remoteitem.md) para indicar que se almacenan fuera de la unidad de destino.</span><span class="sxs-lookup"><span data-stu-id="b4d0b-p107">Responses when searching from the **drive** resource may include items outside of the drive (items shared with the current user). These items will include the [**remoteItem**](../resources/remoteitem.md) facet to indicate they are stored outside of the target drive.</span></span> 

<!-- { "blockType": "response", "truncated": true, "@odata.type": "Collection(microsoft.graph.driveItem)" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
      {
        "id": "0123456789abc!123",
        "name": "Contoso Project",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!123" },
        "remoteItem": { "id": "!23141901", "driveId": "s!1020101jlkjl12lx" }
      },
      {
        "id": "0123456789abc!456",
        "name": "Contoso Project 2016",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!456" }
      }
    ],
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/drive/root/search(query='contoso project')&skipToken=1asdlnjnkj1nalkm!asd"
}
```

## <a name="error-responses"></a><span data-ttu-id="b4d0b-141">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="b4d0b-141">Error responses</span></span>

<span data-ttu-id="b4d0b-142">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="b4d0b-142">See [Error Responses][error-response] for more information about how errors are returned.</span></span>

[error-response]: ../../../concepts/errors.md
[item-resource]: ../resources/driveitem.md
[odata-query-parameters]: ../../../concepts/query_parameters.md

<!-- {
  "type": "#page.annotation",
  "description": "Search for a file across a OneDrive.",
  "keywords": "search,query,bing,filename,content",
  "section": "documentation",
  "tocPath": "Items/Search"
} -->

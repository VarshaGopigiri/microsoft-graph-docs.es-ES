---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Mostrar el contenido de una carpeta
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: dea7edaa84076693b7217476f9ab2797296a5aef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972484"
---
# <a name="list-children-of-a-driveitem"></a><span data-ttu-id="e4616-102">Mostrar los elementos secundarios de un objeto driveItem</span><span class="sxs-lookup"><span data-stu-id="e4616-102">List children of a driveItem</span></span>

<span data-ttu-id="e4616-103">Devuelva una colección de objetos [DriveItem](../resources/driveitem.md) en la relación **children** de un objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="e4616-103">Return a collection of [DriveItems](../resources/driveitem.md) in the **children** relationship of a DriveItem.</span></span>

<span data-ttu-id="e4616-104">Los objetos DriveItem con una faceta **folder** o **package** que no es null pueden tener uno o varios objetos DriveItem secundarios.</span><span class="sxs-lookup"><span data-stu-id="e4616-104">DriveItems with a non-null **folder** or **package** facet can have one or more child DriveItems.</span></span>


## <a name="permissions"></a><span data-ttu-id="e4616-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e4616-105">Permissions</span></span>

<span data-ttu-id="e4616-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e4616-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e4616-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4616-108">Permission type</span></span>      | <span data-ttu-id="e4616-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4616-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e4616-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4616-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e4616-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e4616-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="e4616-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4616-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e4616-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e4616-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="e4616-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4616-114">Application</span></span> | <span data-ttu-id="e4616-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e4616-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e4616-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4616-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/children
GET /groups/{group-id}/drive/items/{item-id}/children
GET /me/drive/items/{item-id}/children
GET /sites/{site-id}/drive/items/{item-id}/children
GET /users/{user-id}/drive/items/{item-id}/children
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e4616-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e4616-117">Optional query parameters</span></span>

<span data-ttu-id="e4616-118">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4616-118">This method supports the `$expand`, `$select`, `$skipToken`, `$top` and `$orderby` [OData query parameters](/graph/query-parameters) to customize the response.</span></span>

### <a name="optional-request-headers"></a><span data-ttu-id="e4616-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="e4616-119">Optional request headers</span></span>

| <span data-ttu-id="e4616-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4616-120">Name</span></span>     | <span data-ttu-id="e4616-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e4616-121">Value</span></span> | <span data-ttu-id="e4616-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4616-122">Description</span></span>                                                                                                                                              |
|:----------------|:------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4616-123">_if-none-match_</span><span class="sxs-lookup"><span data-stu-id="e4616-123">_if-none-match_</span></span> | <span data-ttu-id="e4616-124">ETag</span><span class="sxs-lookup"><span data-stu-id="e4616-124">etag</span></span>  | <span data-ttu-id="e4616-125">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="e4616-125">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="examples"></a><span data-ttu-id="e4616-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e4616-126">Examples</span></span>

### <a name="list-children-in-the-root-of-the-current-users-drive"></a><span data-ttu-id="e4616-127">Mostrar los elementos secundarios de la raíz de la unidad del usuario actual</span><span class="sxs-lookup"><span data-stu-id="e4616-127">List children in the root of the current user's drive</span></span>

<span data-ttu-id="e4616-128">Para recuperar archivos en la raíz de la unidad, use la relación `root` en la unidad y, después, obtenga acceso a la relación secundaria.</span><span class="sxs-lookup"><span data-stu-id="e4616-128">To retrieve files in the root of the drive, use the `root` relationship on the drive, then access the children relationship.</span></span>

<!-- { "blockType": "request", "name": "list-children-root", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/root/children
```


### <a name="list-children-of-a-driveitem-with-a-known-id"></a><span data-ttu-id="e4616-129">Mostrar los elementos secundarios de un objeto DriveItem con un identificador conocido</span><span class="sxs-lookup"><span data-stu-id="e4616-129">List children of a DriveItem with a known ID</span></span>

<span data-ttu-id="e4616-130">Para recuperar archivos en la raíz de la unidad, use la relación `root` en la unidad y, después, obtenga acceso a la relación secundaria.</span><span class="sxs-lookup"><span data-stu-id="e4616-130">To retrieve files in the root of the drive, use the `root` relationship on the drive, then access the children relationship.</span></span>

<!-- { "blockType": "request", "name": "list-children", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}/items/{item-id}/children
```

### <a name="list-children-of-a-driveitem-with-a-known-path"></a><span data-ttu-id="e4616-131">Mostrar los elementos secundarios de un objeto DriveItem con una ruta de acceso conocida</span><span class="sxs-lookup"><span data-stu-id="e4616-131">List children of a DriveItem with a known path</span></span>

<!-- { "blockType": "request", "name": "list-children-from-path", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}/root:/{path-relative-to-root}:/children
```

## <a name="response"></a><span data-ttu-id="e4616-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4616-132">Response</span></span>

<span data-ttu-id="e4616-133">Si se realiza correctamente, este método devuelve la lista de elementos en la colección de elemento secundarios del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="e4616-133">If successful, this method returns the list of items in the children collection of the target item.</span></span>
<span data-ttu-id="e4616-134">La colección de elementos secundarios estará formada por recursos [driveItem][item-resource].</span><span class="sxs-lookup"><span data-stu-id="e4616-134">The children collection will be composed of [driveItem][item-resource] resources.</span></span>

<!-- { "blockType": "response", 
       "@odata.type": "Collection(microsoft.graph.driveItem)", 
       "truncated": true,
       "name": [ "list-children-root", "list-children", "list-children-from-path" ] } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {"name": "myfile.jpg", "size": 2048, "file": {} },
    {"name": "Documents", "folder": { "childCount": 4} },
    {"name": "Photos", "folder": { "childCount": 203} },
    {"name": "my sheet(1).xlsx", "size": 197 }
  ],
  "@odata.nextLink": "https://..."
}
```

<span data-ttu-id="e4616-135">**Nota:** Si una colección supera el tamaño de página predeterminado (200 elementos), se devuelve la propiedad **@odata.nextLink** en la respuesta para indicar que hay más elementos disponibles y proporcionar la dirección URL de solicitud de la siguiente página de elementos.</span><span class="sxs-lookup"><span data-stu-id="e4616-135">**Note:** If a collection exceeds the default page size (200 items), the **@odata.nextLink** property is returned in the response to indicate more items are available and provide the request URL for the next page of items.</span></span>

<span data-ttu-id="e4616-136">Puede controlar el tamaño de la página mediante los [parámetros de cadena de consulta opcionales](https://developer.microsoft.com/graph/docs/concepts/query_parameters)</span><span class="sxs-lookup"><span data-stu-id="e4616-136">You can control the page size through [optional query string parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters)</span></span>

### <a name="error-responses"></a><span data-ttu-id="e4616-137">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="e4616-137">Error responses</span></span>

<span data-ttu-id="e4616-138">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="e4616-138">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: /graph/errors
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "List the children of an item.",
  "keywords": "list,children,collection",
  "section": "documentation",
  "tocPath": "Items/List children"
} -->

---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Mostrar el contenido de una carpeta
localization_priority: Normal
ms.openlocfilehash: a8a35dad8da67d0fdf083e43f52689f463f5b3a4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859146"
---
# <a name="list-children-of-a-driveitem"></a><span data-ttu-id="d7614-102">Mostrar los elementos secundarios de un objeto driveItem</span><span class="sxs-lookup"><span data-stu-id="d7614-102">List children of a driveItem</span></span>

> <span data-ttu-id="d7614-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7614-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7614-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7614-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d7614-105">Devuelva una colección de objetos [DriveItem](../resources/driveitem.md) en la relación **children** de un objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="d7614-105">Return a collection of [DriveItems](../resources/driveitem.md) in the **children** relationship of a DriveItem.</span></span>

<span data-ttu-id="d7614-106">Los objetos DriveItem con una faceta **folder** o **package** que no es null pueden tener uno o varios objetos DriveItem secundarios.</span><span class="sxs-lookup"><span data-stu-id="d7614-106">DriveItems with a non-null **folder** or **package** facet can have one or more child DriveItems.</span></span>


## <a name="permissions"></a><span data-ttu-id="d7614-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d7614-107">Permissions</span></span>

<span data-ttu-id="d7614-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d7614-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d7614-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7614-110">Permission type</span></span>      | <span data-ttu-id="d7614-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7614-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d7614-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7614-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d7614-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d7614-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="d7614-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7614-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d7614-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d7614-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="d7614-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7614-116">Application</span></span> | <span data-ttu-id="d7614-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d7614-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d7614-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7614-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/children
GET /groups/{group-id}/drive/items/{item-id}/children
GET /me/drive/items/{item-id}/children
GET /sites/{site-id}/drive/items/{item-id}/children
GET /users/{user-id}/drive/items/{item-id}/children
```

## <a name="optional-query-parameters"></a><span data-ttu-id="d7614-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d7614-119">Optional query parameters</span></span>

<span data-ttu-id="d7614-120">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7614-120">This method supports the `$expand`, `$select`, `$skipToken`, `$top` and `$orderby` [OData query parameters](/graph/query-parameters) to customize the response.</span></span>

### <a name="optional-request-headers"></a><span data-ttu-id="d7614-121">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="d7614-121">Optional request headers</span></span>

| <span data-ttu-id="d7614-122">Nombre de encabezado</span><span class="sxs-lookup"><span data-stu-id="d7614-122">Header name</span></span>     | <span data-ttu-id="d7614-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d7614-123">Value</span></span> | <span data-ttu-id="d7614-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7614-124">Description</span></span>                                                                                                                                              |
|:----------------|:------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7614-125">_if-none-match_</span><span class="sxs-lookup"><span data-stu-id="d7614-125">_if-none-match_</span></span> | <span data-ttu-id="d7614-126">ETag</span><span class="sxs-lookup"><span data-stu-id="d7614-126">etag</span></span>  | <span data-ttu-id="d7614-127">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="d7614-127">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="examples"></a><span data-ttu-id="d7614-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d7614-128">Examples</span></span>

### <a name="list-children-in-the-root-of-the-current-users-drive"></a><span data-ttu-id="d7614-129">Mostrar los elementos secundarios de la raíz de la unidad del usuario actual</span><span class="sxs-lookup"><span data-stu-id="d7614-129">List children in the root of the current user's drive</span></span>

<span data-ttu-id="d7614-130">Para recuperar archivos en la raíz de la unidad, use la relación `root` en la unidad y, después, obtenga acceso a la relación secundaria.</span><span class="sxs-lookup"><span data-stu-id="d7614-130">To retrieve files in the root of the drive, use the `root` relationship on the drive, then access the children relationship.</span></span>

<!-- { "blockType": "request", "name": "list-children-root", "scopes": "files.read" } -->

```http
GET /me/drive/root/children
```


### <a name="list-children-of-a-driveitem-with-a-known-id"></a><span data-ttu-id="d7614-131">Mostrar los elementos secundarios de un objeto DriveItem con un identificador conocido</span><span class="sxs-lookup"><span data-stu-id="d7614-131">List children of a DriveItem with a known ID</span></span>

<span data-ttu-id="d7614-132">Para recuperar archivos en la raíz de la unidad, use la relación `root` en la unidad y, después, obtenga acceso a la relación secundaria.</span><span class="sxs-lookup"><span data-stu-id="d7614-132">To retrieve files in the root of the drive, use the `root` relationship on the drive, then access the children relationship.</span></span>

<!-- { "blockType": "request", "name": "list-children", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}/items/{item-id}/children
```

### <a name="list-children-of-a-driveitem-with-a-known-path"></a><span data-ttu-id="d7614-133">Mostrar los elementos secundarios de un objeto DriveItem con una ruta de acceso conocida</span><span class="sxs-lookup"><span data-stu-id="d7614-133">List children of a DriveItem with a known path</span></span>

<!-- { "blockType": "request", "name": "list-children-from-path", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}/root:/{path-relative-to-root}:/children
```

## <a name="response"></a><span data-ttu-id="d7614-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7614-134">Response</span></span>

<span data-ttu-id="d7614-135">Si se realiza correctamente, este método devuelve la lista de elementos en la colección de elemento secundarios del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="d7614-135">If successful, this method returns the list of items in the children collection of the target item.</span></span>
<span data-ttu-id="d7614-136">La colección de elementos secundarios estará formada por recursos [driveItem][item-resource].</span><span class="sxs-lookup"><span data-stu-id="d7614-136">The children collection will be composed of [driveItem][item-resource] resources.</span></span>

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

<span data-ttu-id="d7614-137">**Nota:** Si una colección supera el tamaño de página predeterminado (200 elementos), se devuelve la propiedad **@odata.nextLink** en la respuesta para indicar que hay más elementos disponibles y proporcionar la dirección URL de solicitud de la siguiente página de elementos.</span><span class="sxs-lookup"><span data-stu-id="d7614-137">**Note:** If a collection exceeds the default page size (200 items), the **@odata.nextLink** property is returned in the response to indicate more items are available and provide the request URL for the next page of items.</span></span>

<span data-ttu-id="d7614-138">Puede controlar el tamaño de la página mediante los [parámetros de cadena de consulta opcionales](https://developer.microsoft.com/graph/docs/concepts/query_parameters)</span><span class="sxs-lookup"><span data-stu-id="d7614-138">You can control the page size through [optional query string parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters)</span></span>

### <a name="error-responses"></a><span data-ttu-id="d7614-139">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="d7614-139">Error responses</span></span>

<span data-ttu-id="d7614-140">Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="d7614-140">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: /graph/errors
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "List the children of an item.",
  "keywords": "list,children,collection",
  "section": "documentation",
  "tocPath": "Items/List children"
} -->

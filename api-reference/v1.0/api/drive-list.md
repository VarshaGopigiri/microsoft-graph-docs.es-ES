---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar unidades
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: 678776f8215a35b6911a4253f055f43574289130
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937274"
---
# <a name="list-available-drives"></a><span data-ttu-id="502ce-102">List available drives</span><span class="sxs-lookup"><span data-stu-id="502ce-102">List available drives</span></span>

<span data-ttu-id="502ce-103">Recupera la lista de recursos [Drive](../resources/drive.md) disponibles para un User, Group o [Site](../resources/site.md) de destino.</span><span class="sxs-lookup"><span data-stu-id="502ce-103">Retrieve the list of [Drive](../resources/drive.md) resources available for a target User, Group, or [Site](../resources/site.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="502ce-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="502ce-104">Permissions</span></span>

<span data-ttu-id="502ce-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="502ce-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="502ce-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="502ce-107">Permission type</span></span>      | <span data-ttu-id="502ce-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="502ce-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="502ce-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="502ce-109">Delegated (work or school account)</span></span> | <span data-ttu-id="502ce-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="502ce-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="502ce-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="502ce-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="502ce-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="502ce-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="502ce-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="502ce-113">Application</span></span> | <span data-ttu-id="502ce-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="502ce-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="list-a-groups-drives"></a><span data-ttu-id="502ce-115">Enumerar las unidades de un grupo</span><span class="sxs-lookup"><span data-stu-id="502ce-115">List a group's drives</span></span>

<span data-ttu-id="502ce-116">Para enumerar las bibliotecas de documentos de un grupo, la aplicación solicita la relación **drives** en el grupo.</span><span class="sxs-lookup"><span data-stu-id="502ce-116">To list the document libraries for a group, your app requests the **drives** relationship on the Group.</span></span>

### <a name="http-request"></a><span data-ttu-id="502ce-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="502ce-117">HTTP request</span></span>

<!-- {"blockType": "request", "name": "group-list-drives", "scopes": "groups.read.all", "tags": "service.graph" } -->

```http
GET /groups/{groupId}/drives
```

## <a name="list-a-sites-drives"></a><span data-ttu-id="502ce-118">Enumerar las unidades de un sitio</span><span class="sxs-lookup"><span data-stu-id="502ce-118">List a site's drives</span></span>

<span data-ttu-id="502ce-119">Para enumerar las bibliotecas de documentos de un sitio, la aplicación solicita la relación **drives** en el sitio.</span><span class="sxs-lookup"><span data-stu-id="502ce-119">To list the document libraries for a site, your app requests the **drives** relationship on the Site.</span></span>

<!-- {"blockType": "request", "name": "site-list-drives", "scopes": "sites.read.all", "tags": "service.graph" } -->

```http
GET /sites/{siteId}/drives
```

## <a name="list-a-users-drives"></a><span data-ttu-id="502ce-120">Enumerar las unidades de un usuario</span><span class="sxs-lookup"><span data-stu-id="502ce-120">List a user's drives</span></span>

<!-- {"blockType": "request", "name": "user-list-drives", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /users/{userId}/drives
```

## <a name="list-the-current-users-drives"></a><span data-ttu-id="502ce-121">Enumerar las unidades del usuario actual</span><span class="sxs-lookup"><span data-stu-id="502ce-121">List the current user's drives</span></span>

<!-- {"blockType": "request", "name": "enum-drives", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drives
```

## <a name="optional-query-parameters"></a><span data-ttu-id="502ce-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="502ce-122">Optional query parameters</span></span>

<span data-ttu-id="502ce-123">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="502ce-123">This method supports the `$expand`, `$select`, `$skipToken`, `$top`, and `$orderby` [OData query parameters](/graph/query-parameters) to customize the response.</span></span>


## <a name="response"></a><span data-ttu-id="502ce-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="502ce-124">Response</span></span>

<span data-ttu-id="502ce-125">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Drive](../resources/drive.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="502ce-125">If successful, this method returns a `200 OK` response code and collection of [Drive](../resources/drive.md) objects in the response body.</span></span>

<!-- { "blockType": "response", 
       "@odata.type": "Collection(microsoft.graph.drive)",
       "name": ["group-list-drives", "site-list-drives", "user-list-drives", "enum-drives"],
       "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "942CAEB0-13AE-491B-85E4-7557CDC0F25F",
      "driveType": "documentLibrary",
      "name": "Shared Documents",
      "owner": {
        "user": {
          "id": "AE2A1EE9-81A7-423C-ABE4-B945F47509BB",
          "displayName": "Ryan Gregg"
        }
      }
    },
    {
      "id": "C1CD3ED9-0E98-4B0B-82D3-C8FB784B9DCC",
      "driveType": "documentLibrary",
      "name": "Contoso Project Files",
      "owner": {
        "user": {
          "id": "406B2281-18E8-4416-9857-38C531B904F1",
          "displayName": "Daron Spektor"
        }
      }
    }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="502ce-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="502ce-126">Remarks</span></span>

<span data-ttu-id="502ce-127">La mayoría de los usuarios solo tendrán un único recurso Drive.</span><span class="sxs-lookup"><span data-stu-id="502ce-127">Most users will only have a single Drive resource.</span></span>

<span data-ttu-id="502ce-128">Puede que los grupos y los sitios tengan varios recursos Drive disponibles.</span><span class="sxs-lookup"><span data-stu-id="502ce-128">Groups and Sites may have multiple Drive resources available.</span></span>

<span data-ttu-id="502ce-129">De manera predeterminada, las unidades con la faceta [system][] están ocultas.</span><span class="sxs-lookup"><span data-stu-id="502ce-129">Drives with the [system][] facet are hidden by default.</span></span>
<span data-ttu-id="502ce-130">Para obtener una lista de ellas, incluya `system` en su `$select` instrucción.</span><span class="sxs-lookup"><span data-stu-id="502ce-130">To list them, include `system` in your `$select` statement.</span></span>

[system]: ../resources/systemfacet.md

<!-- {
  "type": "#page.annotation",
  "description": "List the available drives for a user, group, or site.",
  "keywords": "drive,onedrive.drive,list drives",
  "section": "documentation",
  "tocPath": "Drives/List drives"
} -->

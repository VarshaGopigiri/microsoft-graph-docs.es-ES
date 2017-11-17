---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar unidades
ms.openlocfilehash: 84771e589a65d11fc06707eb01b6211cf90a8581
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="list-available-drives"></a><span data-ttu-id="43bf7-102">List available drives</span><span class="sxs-lookup"><span data-stu-id="43bf7-102">List available drives</span></span>

<span data-ttu-id="43bf7-103">Recupera la lista de recursos [Drive](../resources/drive.md) disponibles para un User, Group o [Site](../resources/site.md) de destino.</span><span class="sxs-lookup"><span data-stu-id="43bf7-103">Retrieve the list of [Drive](../resources/drive.md) resources available for a target User, Group, or [Site](../resources/site.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="43bf7-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="43bf7-104">Permissions</span></span>

<span data-ttu-id="43bf7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="43bf7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="43bf7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43bf7-107">Permission type</span></span>      | <span data-ttu-id="43bf7-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43bf7-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="43bf7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43bf7-109">Delegated (work or school account)</span></span> | <span data-ttu-id="43bf7-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="43bf7-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="43bf7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43bf7-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="43bf7-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="43bf7-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="43bf7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43bf7-113">Application</span></span> | <span data-ttu-id="43bf7-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="43bf7-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="list-a-groups-drives"></a><span data-ttu-id="43bf7-115">Enumerar las unidades de un grupo</span><span class="sxs-lookup"><span data-stu-id="43bf7-115">List a group's drives</span></span>

<span data-ttu-id="43bf7-116">Para enumerar las bibliotecas de documentos de un grupo, la aplicación solicita la relación **drives** en el grupo.</span><span class="sxs-lookup"><span data-stu-id="43bf7-116">To list the document libraries for a group, your app requests the **drives** relationship on the Group.</span></span>

### <a name="http-request"></a><span data-ttu-id="43bf7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43bf7-117">HTTP request</span></span>

<!-- {"blockType": "request", "name": "group-list-drives", "scopes": "groups.read.all" } -->

```http
GET /groups/{groupId}/drives
```

## <a name="list-a-sites-drives"></a><span data-ttu-id="43bf7-118">Enumerar las unidades de un sitio</span><span class="sxs-lookup"><span data-stu-id="43bf7-118">List a site's drives</span></span>

<span data-ttu-id="43bf7-119">Para enumerar las bibliotecas de documentos de un sitio, la aplicación solicita la relación **drives** en el sitio.</span><span class="sxs-lookup"><span data-stu-id="43bf7-119">To list the document libraries for a site, your app requests the **drives** relationship on the Site.</span></span>

<!-- {"blockType": "request", "name": "site-list-drives", "scopes": "sites.read.all" } -->

```http
GET /sites/{siteId}/drives
```

## <a name="list-a-users-drives"></a><span data-ttu-id="43bf7-120">Enumerar las unidades de un usuario</span><span class="sxs-lookup"><span data-stu-id="43bf7-120">List a user's drives</span></span>

<!-- {"blockType": "request", "name": "user-list-drives", "scopes": "files.read.all" } -->

```http
GET /users/{userId}/drives
```

## <a name="list-the-current-users-drives"></a><span data-ttu-id="43bf7-121">Enumerar las unidades del usuario actual</span><span class="sxs-lookup"><span data-stu-id="43bf7-121">List the current user's drives</span></span>

<!-- {"blockType": "request", "name": "enum-drives", "scopes": "files.read" } -->

```http
GET /me/drives
```

## <a name="optional-query-parameters"></a><span data-ttu-id="43bf7-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="43bf7-122">Optional query parameters</span></span>

<span data-ttu-id="43bf7-123">Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43bf7-123">This method supports the `$expand`, `$select`, `$skipToken`, `$top`, and `$orderby` [OData query parameters](../../../concepts/query_parameters.md) to customize the response.</span></span>


## <a name="response"></a><span data-ttu-id="43bf7-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43bf7-124">Response</span></span>

<span data-ttu-id="43bf7-125">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Drive](../resources/drive.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43bf7-125">If successful, this method returns a `200 OK` response code and collection of [Drive](../resources/drive.md) objects in the response body.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="43bf7-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43bf7-126">Remarks</span></span>

<span data-ttu-id="43bf7-127">La mayoría de los usuarios solo tendrán un único recurso Drive.</span><span class="sxs-lookup"><span data-stu-id="43bf7-127">Most users will only have a single Drive resource. Groups and some users may have multiple drive available.</span></span>

<span data-ttu-id="43bf7-128">Puede que los grupos y los sitios tengan varios recursos Drive disponibles.</span><span class="sxs-lookup"><span data-stu-id="43bf7-128">Groups and Sites may have multiple Drive resources available.</span></span>

<span data-ttu-id="43bf7-129">De manera predeterminada, las unidades con la faceta [system][] están ocultas.</span><span class="sxs-lookup"><span data-stu-id="43bf7-129">Drives with the [system][] facet are hidden by default.</span></span>
<span data-ttu-id="43bf7-130">Para obtener una lista de ellas, incluya `system` en su `$select` instrucción.</span><span class="sxs-lookup"><span data-stu-id="43bf7-130">To list them, include `system` in your `$select` statement.</span></span>

[system]: ../resources/systemFacet.md

<!-- {
  "type": "#page.annotation",
  "description": "List the available drives for a user, group, or site.",
  "keywords": "drive,onedrive.drive,list drives",
  "section": "documentation",
  "tocPath": "Drives/List drives"
} -->

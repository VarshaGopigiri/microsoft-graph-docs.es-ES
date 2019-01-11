---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar unidades
localization_priority: Normal
ms.openlocfilehash: 81b5221e9c2823ac9729310d002f755e1c63e061
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843410"
---
# <a name="list-available-drives"></a><span data-ttu-id="4a7b0-102">List available drives</span><span class="sxs-lookup"><span data-stu-id="4a7b0-102">List available drives</span></span>

> <span data-ttu-id="4a7b0-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4a7b0-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4a7b0-105">Recupera la lista de recursos [Drive](../resources/drive.md) disponibles para un User, Group o [Site](../resources/site.md) de destino.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-105">Retrieve the list of [Drive](../resources/drive.md) resources available for a target User, Group, or [Site](../resources/site.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="4a7b0-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a7b0-106">Permissions</span></span>

<span data-ttu-id="4a7b0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4a7b0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4a7b0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a7b0-109">Permission type</span></span>      | <span data-ttu-id="4a7b0-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a7b0-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4a7b0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a7b0-111">Delegated (work or school account)</span></span> | <span data-ttu-id="4a7b0-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a7b0-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="4a7b0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a7b0-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4a7b0-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a7b0-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="4a7b0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a7b0-115">Application</span></span> | <span data-ttu-id="4a7b0-116">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a7b0-116">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="list-a-groups-drives"></a><span data-ttu-id="4a7b0-117">Enumerar las unidades de un grupo</span><span class="sxs-lookup"><span data-stu-id="4a7b0-117">List a group's drives</span></span>

<span data-ttu-id="4a7b0-118">Para enumerar las bibliotecas de documentos de un grupo, la aplicación solicita la relación **drives** en el grupo.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-118">To list the document libraries for a group, your app requests the **drives** relationship on the Group.</span></span>

### <a name="http-request"></a><span data-ttu-id="4a7b0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a7b0-119">HTTP request</span></span>

<!-- {"blockType": "request", "name": "group-list-drives", "scopes": "groups.read.all" } -->

```http
GET /groups/{groupId}/drives
```

## <a name="list-a-sites-drives"></a><span data-ttu-id="4a7b0-120">Enumerar las unidades de un sitio</span><span class="sxs-lookup"><span data-stu-id="4a7b0-120">List a site's drives</span></span>

<span data-ttu-id="4a7b0-121">Para enumerar las bibliotecas de documentos de un sitio, la aplicación solicita la relación **drives** en el sitio.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-121">To list the document libraries for a site, your app requests the **drives** relationship on the Site.</span></span>

<!-- {"blockType": "request", "name": "site-list-drives", "scopes": "sites.read.all" } -->

```http
GET /sites/{siteId}/drives
```

## <a name="list-a-users-drives"></a><span data-ttu-id="4a7b0-122">Enumerar las unidades de un usuario</span><span class="sxs-lookup"><span data-stu-id="4a7b0-122">List a user's drives</span></span>

<!-- {"blockType": "request", "name": "user-list-drives", "scopes": "files.read.all" } -->

```http
GET /users/{userId}/drives
```

## <a name="list-the-current-users-drives"></a><span data-ttu-id="4a7b0-123">Enumerar las unidades del usuario actual</span><span class="sxs-lookup"><span data-stu-id="4a7b0-123">List the current user's drives</span></span>

<!-- {"blockType": "request", "name": "enum-drives", "scopes": "files.read" } -->

```http
GET /me/drives
```

## <a name="optional-query-parameters"></a><span data-ttu-id="4a7b0-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4a7b0-124">Optional query parameters</span></span>

<span data-ttu-id="4a7b0-125">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-125">This method supports the `$expand`, `$select`, `$skipToken`, `$top`, and `$orderby` [OData query parameters](/graph/query-parameters) to customize the response.</span></span>

## <a name="response"></a><span data-ttu-id="4a7b0-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a7b0-126">Response</span></span>

<span data-ttu-id="4a7b0-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Drive](../resources/drive.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-127">If successful, this method returns a `200 OK` response code and collection of [Drive](../resources/drive.md) objects in the response body.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="4a7b0-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a7b0-128">Remarks</span></span>

<span data-ttu-id="4a7b0-129">La mayoría de los usuarios solo tendrán un único recurso Drive.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-129">Most users will only have a single Drive resource.</span></span>

<span data-ttu-id="4a7b0-130">Puede que los grupos y los sitios tengan varios recursos Drive disponibles.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-130">Groups and Sites may have multiple Drive resources available.</span></span>

<span data-ttu-id="4a7b0-131">De manera predeterminada, las unidades con la faceta [system][] están ocultas.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-131">Drives with the [system][] facet are hidden by default.</span></span>
<span data-ttu-id="4a7b0-132">Para obtener una lista de ellas, incluya `system` en su `$select` instrucción.</span><span class="sxs-lookup"><span data-stu-id="4a7b0-132">To list them, include `system` in your `$select` statement.</span></span>

[system]: ../resources/systemfacet.md

<!-- {
  "type": "#page.annotation",
  "description": "List the available drives for a user, group, or site.",
  "keywords": "drive,onedrive.drive,list drives",
  "section": "documentation",
  "tocPath": "Drives/List drives"
} -->

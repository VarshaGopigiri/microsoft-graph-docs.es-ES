---
author: chackman
ms.author: chackman
title: Elementos de lista seguido
ms.openlocfilehash: dfaa727d25b3713d1be2a8d49f87dab8dba3b553
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088052"
---
# <a name="list-followed-items"></a><span data-ttu-id="a58cf-102">Elementos de lista seguido</span><span class="sxs-lookup"><span data-stu-id="a58cf-102">List followed items</span></span>

> <span data-ttu-id="a58cf-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a58cf-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a58cf-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a58cf-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a58cf-105">Lista de los [elementos](../resources/driveitem.md) que se han seguido por el usuario con la sesión.</span><span class="sxs-lookup"><span data-stu-id="a58cf-105">List the [items](../resources/driveitem.md) that have been followed by the signed in user.</span></span>
<span data-ttu-id="a58cf-106">Esta colección incluye los elementos que se encuentran en la unidad del usuario, así como los elementos que tienen acceso a desde otras unidades.</span><span class="sxs-lookup"><span data-stu-id="a58cf-106">This collection includes items that are in the user's drive as well as items they have access to from other drives.</span></span>

## <a name="permissions"></a><span data-ttu-id="a58cf-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a58cf-107">Permissions</span></span>

<span data-ttu-id="a58cf-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a58cf-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a58cf-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a58cf-110">Permission type</span></span>      | <span data-ttu-id="a58cf-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a58cf-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a58cf-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a58cf-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a58cf-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a58cf-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="a58cf-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a58cf-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a58cf-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a58cf-115">Not supported.</span></span>    |
|<span data-ttu-id="a58cf-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a58cf-116">Application</span></span> | <span data-ttu-id="a58cf-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a58cf-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a58cf-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a58cf-118">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-followed-items", "scopes": "files.read" } -->

```http
GET /me/drive/following
```

## <a name="response"></a><span data-ttu-id="a58cf-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a58cf-119">Response</span></span>

<span data-ttu-id="a58cf-120">Este método devuelve una colección de recursos de [driveItem](../resources/driveitem.md) para los elementos que está siguiendo el propietario de la unidad.</span><span class="sxs-lookup"><span data-stu-id="a58cf-120">This method returns a collection of [driveItem](../resources/driveitem.md) resources for items which the owner of the drive is following.</span></span>
<span data-ttu-id="a58cf-121">Si no se encontraron elementos, se devuelve una colección vacía.</span><span class="sxs-lookup"><span data-stu-id="a58cf-121">If no items were found, an empty collection is returned.</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "1312abc!1231",
      "name": "March Proposal.docx",
      "size": 19121,
      "lastModifiedDateTime": "2017-12-12T10:40:59Z"
    },
    {
      "id": "1312def!9943",
      "name": "Vacation.jpg",
      "size": 37810,
      "lastModifiedDateTime": "2016-10-18T10:40:59Z"
    }
  ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "List the items a user is following.",
  "keywords": "drive,onedrive.drive,list followed items",
  "section": "documentation",
  "tocPath": "Drives/List followed items"
} -->

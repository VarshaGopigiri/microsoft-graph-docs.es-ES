---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar archivos recientes
ms.openlocfilehash: 9713803cb639f3eb27e46d087b0e8fec41abb5a7
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267657"
---
# <a name="list-recent-files"></a><span data-ttu-id="8b7d9-102">Enumerar archivos recientes</span><span class="sxs-lookup"><span data-stu-id="8b7d9-102">List recent files</span></span>

<span data-ttu-id="8b7d9-p101">Enumere un conjunto de elementos que ha usado recientemente el usuario que ha iniciado sesión. Esta colección incluye elementos que están en la unidad del usuario, así como elementos de otras unidades a los que tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="8b7d9-p101">List a set of items that have been recently used by the signed in user. This collection includes items that are in the user's drive as well as items they have access to from other drives.</span></span>

## <a name="permissions"></a><span data-ttu-id="8b7d9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="8b7d9-105">Permissions</span></span>

<span data-ttu-id="8b7d9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8b7d9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8b7d9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8b7d9-108">Permission type</span></span>      | <span data-ttu-id="8b7d9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8b7d9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8b7d9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8b7d9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="8b7d9-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8b7d9-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="8b7d9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8b7d9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8b7d9-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8b7d9-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="8b7d9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8b7d9-114">Application</span></span> | <span data-ttu-id="8b7d9-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8b7d9-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8b7d9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8b7d9-116">HTTP request</span></span>

<!-- { "blockType": "request",
       "name": "view-recent-files", 
       "scopes": "files.read",
       "tags": "service.graph",
       "target": "action" } -->

```http
GET /me/drive/recent
```

## <a name="response"></a><span data-ttu-id="8b7d9-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b7d9-117">Response</span></span>

<span data-ttu-id="8b7d9-118">Este método devuelve una colección de recursos [DriveItem](../resources/driveitem.md) para los elementos a los que ha obtenido acceso recientemente el propietario de la unidad.</span><span class="sxs-lookup"><span data-stu-id="8b7d9-118">This method returns a collection of [DriveItem](../resources/driveitem.md) resources for items which the owner of the drive has recently accessed.</span></span>

<!-- { "blockType": "response",
       "@odata.type": "Collection(microsoft.graph.driveItem)",
       "truncated": true} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "1312abc!1231",
      "remoteItem":
      {
        "id": "1991210caf!192",
        "name": "March Proposal.docx",
        "file": { },
        "size": 19121,
        "parentReference": {
          "driveId": "1991210caf",
          "id": "1991210caf!104"
        }
      },
      "fileSystemInfo": {
        "lastAccessedDateTime": "2017-02-20T19:13:00Z"
      }
    },
    {
      "id": "1312def!9943",
      "name": "Vacation.jpg",
      "file": { },
      "size": 37810,
      "parentReference": {
        "driveId": "1312def",
        "id": "1312def!123"
      },
      "fileSystemInfo": {
        "lastAccessedDateTime": "2017-02-20T16:43:21Z"
      }
    }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="8b7d9-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b7d9-119">Remarks</span></span>

<span data-ttu-id="8b7d9-p103">Algunos recursos driveItem devueltos de la acción **recent** incluirán la faceta **remoteItem**, que indica que son elementos de otra unidad. Para acceder al objeto driveItem original, deberá realizar una solicitud con la información proporcionada en **remoteItem** en el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="8b7d9-p103">Some driveItems returned from the **recent** action will include the **remoteItem** facet which indicates they are items from another drive. To access the original driveItem object, you will need to make a request using the information provided in **remoteItem** in the following format:</span></span>

<!-- { "blockType": "ignored", "name": "drives-get-remoteitem" } -->

```http
GET /drives/{remoteItem-driveId}/items/{remoteItem-id}
```

<!-- {
  "type": "#page.annotation",
  "description": "Retrieve a list of recently used files for the owner of the drive.",
  "keywords": "drive,onedrive.drive,default drive",
  "section": "documentation",
  "tocPath": "Drives/Recent files"
} -->

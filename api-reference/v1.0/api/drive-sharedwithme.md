---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar archivos compartidos conmigo
ms.openlocfilehash: bde6908e0d0f8f7950c74963847b1e08b0539004
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029628"
---
# <a name="list-items-shared-with-the-signed-in-user"></a><span data-ttu-id="31701-102">Enumerar elementos compartidos con el usuario que ha iniciado sesión</span><span class="sxs-lookup"><span data-stu-id="31701-102">List items shared with the signed-in user</span></span>

<span data-ttu-id="31701-103">Recupere una colección de recursos [DriveItem](../resources/driveitem.md) que se han compartido con el propietario del [Drive](../resources/drive.md).</span><span class="sxs-lookup"><span data-stu-id="31701-103">Retrieve a collection of [DriveItem](../resources/driveitem.md) resources that have been shared with the owner of the [Drive](../resources/drive.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="31701-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="31701-104">Permissions</span></span>

<span data-ttu-id="31701-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="31701-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="31701-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="31701-107">Permission type</span></span>      | <span data-ttu-id="31701-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="31701-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="31701-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="31701-109">Delegated (work or school account)</span></span> | <span data-ttu-id="31701-110">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="31701-110">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="31701-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="31701-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="31701-112">Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="31701-112">Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="31701-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="31701-113">Application</span></span> | <span data-ttu-id="31701-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="31701-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

<span data-ttu-id="31701-115">**Nota:** Aunque la solicitud de /sharedWithMe será correcta con los permisos Files.Read o Files.ReadWrite, pueden perderse algunas propiedades.</span><span class="sxs-lookup"><span data-stu-id="31701-115">**Note:** while the /sharedWithMe request will succeed with Files.Read or Files.ReadWrite permissions, some properties may be missing.</span></span>
<span data-ttu-id="31701-116">Además, sin uno de los permisos **Todo**, los elementos compartidos devueltos desde esta API no serán accesibles.</span><span class="sxs-lookup"><span data-stu-id="31701-116">Additionally, without one of the  **All** permissions, shared items returned from this API will not be accessible.</span></span>

## <a name="http-request"></a><span data-ttu-id="31701-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31701-117">HTTP request</span></span>

<!-- { "blockType": "request", "name": "shared-with-me", "scopes": "files.read", "tags": "service.graph", "target": "action" } -->

```http
GET /me/drive/sharedWithMe
```

## <a name="response"></a><span data-ttu-id="31701-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31701-118">Response</span></span>

<span data-ttu-id="31701-p103">Devuelve una colección de recursos [DriveItem](../resources/driveitem.md) que contiene los recursos DriveItem compartidos con el propietario de la unidad. En este ejemplo, ya que la unidad es la unidad predeterminada del usuario, devuelve elementos compartidos con el usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="31701-p103">This returns a collection of [DriveItem](../resources/driveitem.md) resources which contain the DriveItem resources shared with the owner of the drive. In this example, since the drive is the user's default drive, this returns items shared with the signed in user.</span></span>

<!-- {"blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "1312abc",
      "remoteItem": {
        "id": "1991210caf!192",
        "name": "March Proposal.docx",
        "file": { },
        "size": 19121,
        "parentReference": {
          "driveId": "1991210caf",
          "id": "1991210caf!104"
        }
      }
    },
    {
      "id": "1312def",
      "remoteItem": {
        "id": "1991210caf!1991",
        "name": "Team Roster.xlsx",
        "file": { },
        "size": 37619,
        "parentReference": {
          "driveId": "1991210caf",
          "id": "1991210caf!104"
        }
      }
    }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="31701-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31701-121">Remarks</span></span>

<span data-ttu-id="31701-p104">Los recursos driveItem devueltos de la acción **sharedWithMe** incluirán siempre la faceta [**remoteItem**](../resources/remoteitem.md) que indica que son elementos de otra unidad. Para acceder al recurso driveItem compartido, deberá realizar una solicitud con la información proporcionada en **remoteItem** en el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="31701-p104">DriveItems returned from the **sharedWithMe** action will always include the [**remoteItem**](../resources/remoteitem.md) facet which indicates they are items from a different drive. To access the shared DriveItem resource, you will need to make a request using the information provided in **remoteItem** in the following format:</span></span>

<!-- { "blockType": "ignored", "name": "drives-get-remoteitem" } -->

```http
GET /drives/{remoteItem-driveId}/items/{remoteItem-id}
```

<!-- {
  "type": "#page.annotation",
  "description": "List the items shared with the owner of a drive.",
  "keywords": "drive,onedrive.drive,default drive",
  "section": "documentation",
  "tocPath": "Sharing/Shared with me"
} -->

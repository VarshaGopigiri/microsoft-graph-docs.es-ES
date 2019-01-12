---
author: chackman
ms.author: chackman
title: Siga el elemento de unidad
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 2323511604937366e9fd69c24f369523e5e6aebc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926193"
---
# <a name="follow-drive-item"></a><span data-ttu-id="6bd3f-102">Siga el elemento de unidad</span><span class="sxs-lookup"><span data-stu-id="6bd3f-102">Follow drive item</span></span>

> <span data-ttu-id="6bd3f-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6bd3f-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6bd3f-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6bd3f-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6bd3f-105">Siga un [driveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="6bd3f-105">Follow a [driveItem](../resources/driveitem.md).</span></span>

><span data-ttu-id="6bd3f-106">**Nota:** Para dejar de seguir un elemento, vea [elemento dejar de seguir](driveitem-unfollow.md).</span><span class="sxs-lookup"><span data-stu-id="6bd3f-106">**Note:** To unfollow an item, see [Unfollow item](driveitem-unfollow.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="6bd3f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6bd3f-107">Permissions</span></span>

<span data-ttu-id="6bd3f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6bd3f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6bd3f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6bd3f-110">Permission type</span></span>      | <span data-ttu-id="6bd3f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6bd3f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6bd3f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6bd3f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6bd3f-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6bd3f-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="6bd3f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6bd3f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6bd3f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6bd3f-115">Not supported.</span></span>    |
|<span data-ttu-id="6bd3f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6bd3f-116">Application</span></span> | <span data-ttu-id="6bd3f-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6bd3f-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6bd3f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6bd3f-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{drive-id}/items/{item-id}/follow
POST /groups/{group-id/drive/items/{item-id}/follow
POST /me/drive/items/{item-id}/follow
POST /sites/{site-id}/drive/items/{item-id}/follow
POST /users/{user-id}/drive/items/{item-id}/follow
```

## <a name="request-body"></a><span data-ttu-id="6bd3f-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="6bd3f-119">Request body</span></span>

<span data-ttu-id="6bd3f-120">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="6bd3f-120">No request body is required.</span></span>

## <a name="response"></a><span data-ttu-id="6bd3f-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6bd3f-121">Response</span></span>

<span data-ttu-id="6bd3f-122">Este método devuelve un [DriveItem](../resources/driveitem.md) para el elemento que se siguen.</span><span class="sxs-lookup"><span data-stu-id="6bd3f-122">This method returns a [DriveItem](../resources/driveitem.md) for the item being followed.</span></span>

## <a name="example"></a><span data-ttu-id="6bd3f-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6bd3f-123">Example</span></span>

<span data-ttu-id="6bd3f-124">En este ejemplo se sigue un elemento identificado por `{item-id}`.</span><span class="sxs-lookup"><span data-stu-id="6bd3f-124">This example follows an item identified by `{item-id}`.</span></span>

<!-- { "blockType": "request", "name": "follow-item", "scopes": "files.read", "target": "action" } -->

```http
POST /me/drive/items/{item-id}/follow
```

<!-- {
  "type": "#page.annotation",
  "description": "Follow an item.",
  "keywords": "follow item",
  "section": "documentation",
  "tocPath": "Items/Follow"
} -->

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "1312abc!1231",
  "name": "March Proposal.docx",
  "size": 19121,
  "lastModifiedDateTime": "2017-12-12T10:40:59Z"
}
```

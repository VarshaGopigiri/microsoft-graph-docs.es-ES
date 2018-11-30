---
author: chackman
ms.author: chackman
title: Dejar de seguir elemento de unidad
ms.openlocfilehash: 871ea9782e62e66adeed743819a265b452e06de3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083351"
---
# <a name="unfollow-drive-item"></a><span data-ttu-id="31179-102">Dejar de seguir elemento de unidad</span><span class="sxs-lookup"><span data-stu-id="31179-102">Unfollow drive item</span></span>

> <span data-ttu-id="31179-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31179-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31179-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31179-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="31179-105">Dejar de seguir un [driveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="31179-105">Unfollow a [driveItem](../resources/driveitem.md).</span></span>

><span data-ttu-id="31179-106">**Nota:** Para seguir un elemento, vea [Elemento siga](driveitem-follow.md).</span><span class="sxs-lookup"><span data-stu-id="31179-106">**Note:** To follow an item, see [Follow Item](driveitem-follow.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="31179-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="31179-107">Permissions</span></span>

<span data-ttu-id="31179-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="31179-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="31179-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="31179-110">Permission type</span></span>      | <span data-ttu-id="31179-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="31179-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="31179-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="31179-112">Delegated (work or school account)</span></span> | <span data-ttu-id="31179-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="31179-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="31179-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="31179-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="31179-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31179-115">Not supported.</span></span>    |
|<span data-ttu-id="31179-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="31179-116">Application</span></span> | <span data-ttu-id="31179-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="31179-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="31179-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31179-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/drive/following/{item-id} 
DELETE /users/{user-id}/drive/following/{item-id}
```

## <a name="request-body"></a><span data-ttu-id="31179-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="31179-119">Request body</span></span>

<span data-ttu-id="31179-120">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="31179-120">No request body is required.</span></span>

## <a name="response"></a><span data-ttu-id="31179-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31179-121">Response</span></span>

<span data-ttu-id="31179-122">Si se realiza correctamente, la llamada API devuelve `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="31179-122">If successful, the API call returns a `204 No Content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

## <a name="example"></a><span data-ttu-id="31179-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31179-123">Example</span></span>

<span data-ttu-id="31179-124">En este ejemplo se unfollows un elemento identificado por `{item-id}`.</span><span class="sxs-lookup"><span data-stu-id="31179-124">This example unfollows an item identified by `{item-id}`.</span></span>

<!-- { "blockType": "request", "name": "unfollow-item", "scopes": "files.read" } -->

```http
DELETE /me/drive/following/{item-id}
```


<!-- {
  "type": "#page.annotation",
  "description": "Unfollow an item that the user is following.",
  "keywords": "unfollow item",
  "section": "documentation",
  "tocPath": "Items/Unfollow"
} -->

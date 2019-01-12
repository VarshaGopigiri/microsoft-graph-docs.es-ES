---
title: Delete directoryObject
description: Elimina un directoryObject.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 3fccafa016dad9892c701e852bc592564661c9cb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926816"
---
# <a name="delete-directoryobject"></a><span data-ttu-id="20190-103">Delete directoryObject</span><span class="sxs-lookup"><span data-stu-id="20190-103">Delete directoryObject</span></span>

<span data-ttu-id="20190-104">Elimina un directoryObject.</span><span class="sxs-lookup"><span data-stu-id="20190-104">Deletes a directoryObject.</span></span>

## <a name="permissions"></a><span data-ttu-id="20190-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="20190-105">Permissions</span></span>
<span data-ttu-id="20190-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="20190-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="20190-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="20190-108">Permission type</span></span>      | <span data-ttu-id="20190-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="20190-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="20190-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="20190-110">Delegated (work or school account)</span></span> | <span data-ttu-id="20190-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="20190-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="20190-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="20190-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="20190-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="20190-113">Not supported.</span></span>    |
|<span data-ttu-id="20190-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="20190-114">Application</span></span> | <span data-ttu-id="20190-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="20190-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="20190-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="20190-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /directoryObjects/{id}

```
## <a name="request-headers"></a><span data-ttu-id="20190-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="20190-117">Request headers</span></span>
| <span data-ttu-id="20190-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="20190-118">Name</span></span>       | <span data-ttu-id="20190-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="20190-119">Type</span></span> | <span data-ttu-id="20190-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="20190-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="20190-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="20190-121">Authorization</span></span>  | <span data-ttu-id="20190-122">string</span><span class="sxs-lookup"><span data-stu-id="20190-122">string</span></span>  | <span data-ttu-id="20190-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="20190-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="20190-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="20190-125">Request body</span></span>
<span data-ttu-id="20190-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="20190-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="20190-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="20190-127">Response</span></span>

<span data-ttu-id="20190-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="20190-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="20190-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="20190-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="20190-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="20190-131">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_directoryobject"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/directoryObjects/{id}
```
##### <a name="response"></a><span data-ttu-id="20190-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="20190-132">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete directoryObject",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

---
title: Delete directoryObject
description: Elimina un directoryObject.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 2c63600ba400041ebf420d5502e14af4a8cd75a9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810853"
---
# <a name="delete-directoryobject"></a><span data-ttu-id="9d4f1-103">Delete directoryObject</span><span class="sxs-lookup"><span data-stu-id="9d4f1-103">Delete directoryObject</span></span>

<span data-ttu-id="9d4f1-104">Elimina un directoryObject.</span><span class="sxs-lookup"><span data-stu-id="9d4f1-104">Deletes a directoryObject.</span></span>

## <a name="permissions"></a><span data-ttu-id="9d4f1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9d4f1-105">Permissions</span></span>
<span data-ttu-id="9d4f1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9d4f1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="9d4f1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9d4f1-108">Permission type</span></span>      | <span data-ttu-id="9d4f1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9d4f1-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9d4f1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9d4f1-110">Delegated (work or school account)</span></span> | <span data-ttu-id="9d4f1-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9d4f1-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="9d4f1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9d4f1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9d4f1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d4f1-113">Not supported.</span></span>    |
|<span data-ttu-id="9d4f1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9d4f1-114">Application</span></span> | <span data-ttu-id="9d4f1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d4f1-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9d4f1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9d4f1-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /directoryObjects/{id}

```
## <a name="request-headers"></a><span data-ttu-id="9d4f1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9d4f1-117">Request headers</span></span>
| <span data-ttu-id="9d4f1-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d4f1-118">Name</span></span>       | <span data-ttu-id="9d4f1-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4f1-119">Type</span></span> | <span data-ttu-id="9d4f1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d4f1-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9d4f1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="9d4f1-121">Authorization</span></span>  | <span data-ttu-id="9d4f1-122">string</span><span class="sxs-lookup"><span data-stu-id="9d4f1-122">string</span></span>  | <span data-ttu-id="9d4f1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d4f1-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9d4f1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9d4f1-125">Request body</span></span>
<span data-ttu-id="9d4f1-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9d4f1-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9d4f1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d4f1-127">Response</span></span>

<span data-ttu-id="9d4f1-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d4f1-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9d4f1-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d4f1-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9d4f1-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9d4f1-131">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_directoryobject"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/directoryObjects/{id}
```
##### <a name="response"></a><span data-ttu-id="9d4f1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d4f1-132">Response</span></span>

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

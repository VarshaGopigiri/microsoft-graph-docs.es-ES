---
title: Eliminación de canal
description: Eliminar el canal.
ms.openlocfilehash: b2756de636f38a14063a345ba2094c1cb628517c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028555"
---
# <a name="delete-channel"></a><span data-ttu-id="3dd9c-103">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="3dd9c-103">Delete channel</span></span>



<span data-ttu-id="3dd9c-104">Eliminar el [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="3dd9c-104">Delete the [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="3dd9c-105">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="3dd9c-105">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="3dd9c-106">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="3dd9c-106">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

> <span data-ttu-id="3dd9c-107">**Nota**: los datos de canales eliminados seguirán almacenarse durante varias semanas permitir que el propietario del equipo de canal de recuperación eliminado.</span><span class="sxs-lookup"><span data-stu-id="3dd9c-107">**Note**: The data in deleted channels will continue to be stored for several weeks to allow team owner to recovery deleted channel.</span></span> <span data-ttu-id="3dd9c-108">Durante este tiempo, no se puede crear un canal nuevo con el mismo displayName.</span><span class="sxs-lookup"><span data-stu-id="3dd9c-108">During that time, a new channel with the same displayName may not be created.</span></span>

## <a name="permissions"></a><span data-ttu-id="3dd9c-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="3dd9c-109">Permissions</span></span>
<span data-ttu-id="3dd9c-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3dd9c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3dd9c-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3dd9c-112">Permission type</span></span>      | <span data-ttu-id="3dd9c-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3dd9c-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3dd9c-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3dd9c-114">Delegated (work or school account)</span></span> | <span data-ttu-id="3dd9c-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3dd9c-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="3dd9c-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3dd9c-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3dd9c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3dd9c-117">Not supported.</span></span>    |
|<span data-ttu-id="3dd9c-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3dd9c-118">Application</span></span> | <span data-ttu-id="3dd9c-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3dd9c-119">Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="3dd9c-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3dd9c-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="3dd9c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3dd9c-121">Request headers</span></span>
| <span data-ttu-id="3dd9c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3dd9c-122">Header</span></span>       | <span data-ttu-id="3dd9c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3dd9c-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3dd9c-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="3dd9c-124">Authorization</span></span>  | <span data-ttu-id="3dd9c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3dd9c-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3dd9c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3dd9c-127">Request body</span></span>
<span data-ttu-id="3dd9c-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3dd9c-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3dd9c-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3dd9c-129">Response</span></span>

<span data-ttu-id="3dd9c-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3dd9c-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3dd9c-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3dd9c-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3dd9c-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3dd9c-133">Request</span></span>
<span data-ttu-id="3dd9c-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3dd9c-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_channel"
}-->

```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```

#### <a name="response"></a><span data-ttu-id="3dd9c-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3dd9c-135">Response</span></span>

<span data-ttu-id="3dd9c-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3dd9c-136">The following is an example of the response.</span></span> 
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
  "description": "Delete channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

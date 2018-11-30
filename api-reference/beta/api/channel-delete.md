---
title: Eliminación de canal
description: Eliminar el canal.
ms.openlocfilehash: 8f34db306ae42493cf23f29117aece6fd4942c2b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083044"
---
# <a name="delete-channel"></a><span data-ttu-id="299a1-103">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="299a1-103">Delete channel</span></span>

> <span data-ttu-id="299a1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="299a1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="299a1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="299a1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="299a1-106">Eliminar el [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="299a1-106">Delete the [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="299a1-107">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="299a1-107">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="299a1-108">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="299a1-108">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

## <a name="permissions"></a><span data-ttu-id="299a1-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="299a1-109">Permissions</span></span>
<span data-ttu-id="299a1-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="299a1-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="299a1-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="299a1-112">Permission type</span></span>      | <span data-ttu-id="299a1-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="299a1-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="299a1-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="299a1-114">Delegated (work or school account)</span></span> | <span data-ttu-id="299a1-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="299a1-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="299a1-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="299a1-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="299a1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="299a1-117">Not supported.</span></span>    |
|<span data-ttu-id="299a1-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="299a1-118">Application</span></span> | <span data-ttu-id="299a1-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="299a1-119">Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="299a1-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="299a1-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="299a1-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="299a1-121">Request headers</span></span>
| <span data-ttu-id="299a1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="299a1-122">Header</span></span>       | <span data-ttu-id="299a1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="299a1-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="299a1-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="299a1-124">Authorization</span></span>  | <span data-ttu-id="299a1-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="299a1-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="299a1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="299a1-127">Request body</span></span>
<span data-ttu-id="299a1-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="299a1-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="299a1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="299a1-129">Response</span></span>

<span data-ttu-id="299a1-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="299a1-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="299a1-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="299a1-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="299a1-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="299a1-133">Request</span></span>
<span data-ttu-id="299a1-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="299a1-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_channel"
}-->

```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```

#### <a name="response"></a><span data-ttu-id="299a1-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="299a1-135">Response</span></span>

<span data-ttu-id="299a1-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="299a1-136">The following is an example of the response.</span></span> 
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

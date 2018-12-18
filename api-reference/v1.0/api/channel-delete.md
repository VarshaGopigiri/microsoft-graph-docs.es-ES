---
title: Eliminación de canal
description: Eliminar el canal.
author: nkramer
ms.openlocfilehash: e3500c536deca45b7444e149477c399cf1609a52
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359559"
---
# <a name="delete-channel"></a><span data-ttu-id="27dce-103">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="27dce-103">Delete channel</span></span>



<span data-ttu-id="27dce-104">Eliminar el [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="27dce-104">Delete the [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="27dce-105">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="27dce-105">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="27dce-106">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="27dce-106">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

> <span data-ttu-id="27dce-107">**Nota**: los datos de canales eliminados seguirán almacenarse durante varias semanas permitir que el propietario del equipo de canal de recuperación eliminado.</span><span class="sxs-lookup"><span data-stu-id="27dce-107">**Note**: The data in deleted channels will continue to be stored for several weeks to allow team owner to recovery deleted channel.</span></span> <span data-ttu-id="27dce-108">Durante este tiempo, no se puede crear un canal nuevo con el mismo displayName.</span><span class="sxs-lookup"><span data-stu-id="27dce-108">During that time, a new channel with the same displayName may not be created.</span></span>

## <a name="permissions"></a><span data-ttu-id="27dce-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="27dce-109">Permissions</span></span>
<span data-ttu-id="27dce-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="27dce-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="27dce-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="27dce-112">Permission type</span></span>      | <span data-ttu-id="27dce-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="27dce-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="27dce-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="27dce-114">Delegated (work or school account)</span></span> | <span data-ttu-id="27dce-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27dce-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="27dce-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="27dce-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="27dce-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27dce-117">Not supported.</span></span>    |
|<span data-ttu-id="27dce-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="27dce-118">Application</span></span> | <span data-ttu-id="27dce-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27dce-119">Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="27dce-120">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="27dce-120">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="27dce-121">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="27dce-121">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="27dce-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27dce-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="27dce-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="27dce-123">Request headers</span></span>
| <span data-ttu-id="27dce-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27dce-124">Header</span></span>       | <span data-ttu-id="27dce-125">Valor</span><span class="sxs-lookup"><span data-stu-id="27dce-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="27dce-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="27dce-126">Authorization</span></span>  | <span data-ttu-id="27dce-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="27dce-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="27dce-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="27dce-129">Request body</span></span>
<span data-ttu-id="27dce-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="27dce-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="27dce-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27dce-131">Response</span></span>

<span data-ttu-id="27dce-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27dce-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="27dce-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27dce-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="27dce-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="27dce-135">Request</span></span>
<span data-ttu-id="27dce-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="27dce-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_channel"
}-->

```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```

#### <a name="response"></a><span data-ttu-id="27dce-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27dce-137">Response</span></span>

<span data-ttu-id="27dce-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27dce-138">The following is an example of the response.</span></span> 
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

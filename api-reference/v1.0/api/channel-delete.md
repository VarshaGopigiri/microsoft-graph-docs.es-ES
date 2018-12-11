---
title: Eliminación de canal
description: Eliminar el canal.
ms.openlocfilehash: f24471a4f93c50d722290feb9093514c34f4cc2f
ms.sourcegitcommit: 72d4da2a6bfaf99fa4edaf6ce3b97b1a6d96d874
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "27222351"
---
# <a name="delete-channel"></a><span data-ttu-id="5608e-103">Eliminación de canal</span><span class="sxs-lookup"><span data-stu-id="5608e-103">Delete channel</span></span>



<span data-ttu-id="5608e-104">Eliminar el [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="5608e-104">Delete the [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="5608e-105">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="5608e-105">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="5608e-106">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="5608e-106">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

> <span data-ttu-id="5608e-107">**Nota**: los datos de canales eliminados seguirán almacenarse durante varias semanas permitir que el propietario del equipo de canal de recuperación eliminado.</span><span class="sxs-lookup"><span data-stu-id="5608e-107">**Note**: The data in deleted channels will continue to be stored for several weeks to allow team owner to recovery deleted channel.</span></span> <span data-ttu-id="5608e-108">Durante este tiempo, no se puede crear un canal nuevo con el mismo displayName.</span><span class="sxs-lookup"><span data-stu-id="5608e-108">During that time, a new channel with the same displayName may not be created.</span></span>

## <a name="permissions"></a><span data-ttu-id="5608e-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="5608e-109">Permissions</span></span>
<span data-ttu-id="5608e-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5608e-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5608e-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5608e-112">Permission type</span></span>      | <span data-ttu-id="5608e-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5608e-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5608e-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5608e-114">Delegated (work or school account)</span></span> | <span data-ttu-id="5608e-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5608e-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="5608e-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5608e-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5608e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5608e-117">Not supported.</span></span>    |
|<span data-ttu-id="5608e-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5608e-118">Application</span></span> | <span data-ttu-id="5608e-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5608e-119">Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="5608e-120">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="5608e-120">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="5608e-121">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="5608e-121">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="5608e-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5608e-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="5608e-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5608e-123">Request headers</span></span>
| <span data-ttu-id="5608e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5608e-124">Header</span></span>       | <span data-ttu-id="5608e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5608e-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5608e-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="5608e-126">Authorization</span></span>  | <span data-ttu-id="5608e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5608e-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5608e-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5608e-129">Request body</span></span>
<span data-ttu-id="5608e-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5608e-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5608e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5608e-131">Response</span></span>

<span data-ttu-id="5608e-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5608e-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5608e-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5608e-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5608e-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5608e-135">Request</span></span>
<span data-ttu-id="5608e-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5608e-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_channel"
}-->

```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```

#### <a name="response"></a><span data-ttu-id="5608e-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5608e-137">Response</span></span>

<span data-ttu-id="5608e-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5608e-138">The following is an example of the response.</span></span> 
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

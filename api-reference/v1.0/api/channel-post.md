---
title: Creación de canal
description: Crear un nuevo canal en un Team Microsoft, tal como se especifica en el cuerpo de la solicitud.
localization_priority: Priority
author: nkramer
ms.prod: microsoft-teams
ms.openlocfilehash: 09d058d9dc64fff053cd0ec507357f2990aeb353
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957343"
---
# <a name="create-channel"></a><span data-ttu-id="ea0a2-103">Creación de canal</span><span class="sxs-lookup"><span data-stu-id="ea0a2-103">Create Channel</span></span>



<span data-ttu-id="ea0a2-104">Crear un nuevo [canal](../resources/channel.md) en un Team Microsoft, tal como se especifica en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea0a2-104">Create a new [channel](../resources/channel.md) in a Microsoft Team, as specified in the request body.</span></span>

> <span data-ttu-id="ea0a2-105">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="ea0a2-105">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="ea0a2-106">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="ea0a2-106">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

## <a name="permissions"></a><span data-ttu-id="ea0a2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ea0a2-107">Permissions</span></span>
<span data-ttu-id="ea0a2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea0a2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="ea0a2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea0a2-110">Permission type</span></span>      | <span data-ttu-id="ea0a2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea0a2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ea0a2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea0a2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ea0a2-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea0a2-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ea0a2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea0a2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea0a2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea0a2-115">Not supported.</span></span>    |
|<span data-ttu-id="ea0a2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea0a2-116">Application</span></span> | <span data-ttu-id="ea0a2-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea0a2-117">Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="ea0a2-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="ea0a2-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="ea0a2-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="ea0a2-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="ea0a2-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea0a2-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/channels
```
## <a name="request-headers"></a><span data-ttu-id="ea0a2-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea0a2-121">Request headers</span></span>
| <span data-ttu-id="ea0a2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea0a2-122">Header</span></span>       | <span data-ttu-id="ea0a2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0a2-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ea0a2-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea0a2-124">Authorization</span></span>  | <span data-ttu-id="ea0a2-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea0a2-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ea0a2-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ea0a2-127">Content-Type</span></span>  | <span data-ttu-id="ea0a2-128">application/json</span><span class="sxs-lookup"><span data-stu-id="ea0a2-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ea0a2-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea0a2-129">Request body</span></span>
<span data-ttu-id="ea0a2-130">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [canal](../resources/channel.md) .</span><span class="sxs-lookup"><span data-stu-id="ea0a2-130">In the request body, supply a JSON representation of [channel](../resources/channel.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="ea0a2-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea0a2-131">Response</span></span>

<span data-ttu-id="ea0a2-132">Si tiene éxito, este método devuelve `201 Created` objeto de [canal](../resources/channel.md) y el código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea0a2-132">If successful, this method returns `201 Created` response code and [channel](../resources/channel.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea0a2-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea0a2-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ea0a2-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea0a2-134">Request</span></span>
<span data-ttu-id="ea0a2-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea0a2-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_channel_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/channels
Content-type: application/json

{
  "displayName": "Architecture Discussion",
  "description": "This channel is where we debate all future architecture plans"
}
```
##### <a name="response"></a><span data-ttu-id="ea0a2-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea0a2-136">Response</span></span>
<span data-ttu-id="ea0a2-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea0a2-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.channel"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
  "id": "id-value",
  "displayName": "Architecture Discussion",
  "description": "This channel is where we debate all future architecture plans"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

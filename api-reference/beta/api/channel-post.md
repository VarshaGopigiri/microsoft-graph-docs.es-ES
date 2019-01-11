---
title: Creación de canal
description: Crear un nuevo canal en un Team Microsoft, tal como se especifica en el cuerpo de la solicitud.
localization_priority: Normal
ms.openlocfilehash: f7192c177d79e48a0a9e55c9edc5dbb394539928
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875050"
---
# <a name="create-channel"></a><span data-ttu-id="e039a-103">Creación de canal</span><span class="sxs-lookup"><span data-stu-id="e039a-103">Create Channel</span></span>

> <span data-ttu-id="e039a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e039a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e039a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e039a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e039a-106">Crear un nuevo [canal](../resources/channel.md) en un Team Microsoft, tal como se especifica en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e039a-106">Create a new [channel](../resources/channel.md) in a Microsoft Team, as specified in the request body.</span></span>

> <span data-ttu-id="e039a-107">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="e039a-107">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="e039a-108">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="e039a-108">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

## <a name="permissions"></a><span data-ttu-id="e039a-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="e039a-109">Permissions</span></span>
<span data-ttu-id="e039a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e039a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="e039a-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e039a-112">Permission type</span></span>      | <span data-ttu-id="e039a-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e039a-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e039a-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e039a-114">Delegated (work or school account)</span></span> | <span data-ttu-id="e039a-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e039a-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="e039a-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e039a-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e039a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e039a-117">Not supported.</span></span>    |
|<span data-ttu-id="e039a-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e039a-118">Application</span></span> | <span data-ttu-id="e039a-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e039a-119">Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="e039a-120">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="e039a-120">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="e039a-121">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="e039a-121">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="e039a-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e039a-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/channels
```
## <a name="request-headers"></a><span data-ttu-id="e039a-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e039a-123">Request headers</span></span>
| <span data-ttu-id="e039a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e039a-124">Header</span></span>       | <span data-ttu-id="e039a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e039a-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e039a-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="e039a-126">Authorization</span></span>  | <span data-ttu-id="e039a-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e039a-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e039a-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e039a-129">Content-Type</span></span>  | <span data-ttu-id="e039a-130">application/json</span><span class="sxs-lookup"><span data-stu-id="e039a-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e039a-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e039a-131">Request body</span></span>
<span data-ttu-id="e039a-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [canal](../resources/channel.md) .</span><span class="sxs-lookup"><span data-stu-id="e039a-132">In the request body, supply a JSON representation of [channel](../resources/channel.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="e039a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e039a-133">Response</span></span>

<span data-ttu-id="e039a-134">Si tiene éxito, este método devuelve `201 Created` objeto de [canal](../resources/channel.md) y el código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e039a-134">If successful, this method returns `201 Created` response code and [channel](../resources/channel.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e039a-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e039a-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e039a-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e039a-136">Request</span></span>
<span data-ttu-id="e039a-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e039a-137">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="e039a-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e039a-138">Response</span></span>
<span data-ttu-id="e039a-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e039a-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

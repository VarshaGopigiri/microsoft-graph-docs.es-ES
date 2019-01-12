---
title: Obtener el canal
description: Recuperar las propiedades y relaciones de un canal.
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
ms.openlocfilehash: 9782bf401f92f6e4654d6d7ab261ad93b753e047
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966044"
---
# <a name="get-channel"></a><span data-ttu-id="364cc-103">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="364cc-103">Get channel</span></span>



<span data-ttu-id="364cc-104">Recuperar las propiedades y relaciones de un [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="364cc-104">Retrieve the properties and relationships of a [channel](../resources/channel.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="364cc-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="364cc-105">Permissions</span></span>
<span data-ttu-id="364cc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="364cc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="364cc-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="364cc-108">Permission type</span></span>      | <span data-ttu-id="364cc-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="364cc-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="364cc-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="364cc-110">Delegated (work or school account)</span></span> | <span data-ttu-id="364cc-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="364cc-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="364cc-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="364cc-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="364cc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="364cc-113">Not supported.</span></span>    |
|<span data-ttu-id="364cc-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="364cc-114">Application</span></span> | <span data-ttu-id="364cc-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="364cc-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="364cc-116">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="364cc-116">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="364cc-117">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="364cc-117">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="364cc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="364cc-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels/{id}

```

## <a name="optional-query-parameters"></a><span data-ttu-id="364cc-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="364cc-119">Optional query parameters</span></span>

<span data-ttu-id="364cc-120">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="364cc-120">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="364cc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="364cc-121">Request headers</span></span>
| <span data-ttu-id="364cc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="364cc-122">Header</span></span>       | <span data-ttu-id="364cc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="364cc-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="364cc-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="364cc-124">Authorization</span></span>  | <span data-ttu-id="364cc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="364cc-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="364cc-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="364cc-127">Request body</span></span>
<span data-ttu-id="364cc-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="364cc-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="364cc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="364cc-129">Response</span></span>

<span data-ttu-id="364cc-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [canal](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="364cc-130">If successful, this method returns a `200 OK` response code and a [channel](../resources/channel.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="364cc-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="364cc-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="364cc-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="364cc-132">Request</span></span>
<span data-ttu-id="364cc-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="364cc-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channel"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="364cc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="364cc-134">Response</span></span>
<span data-ttu-id="364cc-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="364cc-135">Here is an example of the response.</span></span> 

><span data-ttu-id="364cc-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="364cc-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
    "description": "description-value",
    "displayName": "display-name-value",
    "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

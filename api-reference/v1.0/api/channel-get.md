---
title: Obtener el canal
description: Recuperar las propiedades y relaciones de un canal.
author: nkramer
ms.openlocfilehash: 38081fbc23e0f77dc69d1dbb6beba64b8f6d0a82
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324776"
---
# <a name="get-channel"></a><span data-ttu-id="67d70-103">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="67d70-103">Get channel</span></span>



<span data-ttu-id="67d70-104">Recuperar las propiedades y relaciones de un [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="67d70-104">Retrieve the properties and relationships of a [channel](../resources/channel.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="67d70-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="67d70-105">Permissions</span></span>
<span data-ttu-id="67d70-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="67d70-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="67d70-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="67d70-108">Permission type</span></span>      | <span data-ttu-id="67d70-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="67d70-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="67d70-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="67d70-110">Delegated (work or school account)</span></span> | <span data-ttu-id="67d70-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="67d70-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="67d70-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="67d70-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="67d70-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="67d70-113">Not supported.</span></span>    |
|<span data-ttu-id="67d70-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="67d70-114">Application</span></span> | <span data-ttu-id="67d70-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="67d70-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="67d70-116">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="67d70-116">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="67d70-117">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="67d70-117">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="67d70-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="67d70-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels/{id}

```

## <a name="optional-query-parameters"></a><span data-ttu-id="67d70-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="67d70-119">Optional query parameters</span></span>

<span data-ttu-id="67d70-120">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="67d70-120">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="67d70-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="67d70-121">Request headers</span></span>
| <span data-ttu-id="67d70-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67d70-122">Header</span></span>       | <span data-ttu-id="67d70-123">Valor</span><span class="sxs-lookup"><span data-stu-id="67d70-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="67d70-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="67d70-124">Authorization</span></span>  | <span data-ttu-id="67d70-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="67d70-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="67d70-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="67d70-127">Request body</span></span>
<span data-ttu-id="67d70-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="67d70-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="67d70-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67d70-129">Response</span></span>

<span data-ttu-id="67d70-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [canal](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="67d70-130">If successful, this method returns a `200 OK` response code and a [channel](../resources/channel.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="67d70-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67d70-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="67d70-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="67d70-132">Request</span></span>
<span data-ttu-id="67d70-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="67d70-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channel"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="67d70-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67d70-134">Response</span></span>
<span data-ttu-id="67d70-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="67d70-135">Here is an example of the response.</span></span> 

><span data-ttu-id="67d70-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="67d70-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

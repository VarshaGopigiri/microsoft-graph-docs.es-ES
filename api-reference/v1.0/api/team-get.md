---
title: Obtener el equipo
description: Recuperar las propiedades y relaciones del equipo especificado.
author: nkramer
localization_priority: Priority
ms.openlocfilehash: 3efec6e9b767d026d0a7626c2da257feaa20fde3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887083"
---
# <a name="get-team"></a><span data-ttu-id="0663a-103">Obtener el equipo</span><span class="sxs-lookup"><span data-stu-id="0663a-103">Get team</span></span>



<span data-ttu-id="0663a-104">Recuperar las propiedades y relaciones del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="0663a-104">Retrieve the properties and relationships of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="0663a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="0663a-105">Permissions</span></span>
<span data-ttu-id="0663a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0663a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0663a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0663a-108">Permission type</span></span>      | <span data-ttu-id="0663a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0663a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0663a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0663a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="0663a-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0663a-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="0663a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0663a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0663a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0663a-113">Not supported.</span></span>    |
|<span data-ttu-id="0663a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0663a-114">Application</span></span> | <span data-ttu-id="0663a-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0663a-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="0663a-116">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="0663a-116">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="0663a-117">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="0663a-117">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="0663a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0663a-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0663a-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0663a-119">Optional query parameters</span></span>
<span data-ttu-id="0663a-120">Este método admite la $select y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0663a-120">This method supports the $select and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0663a-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0663a-121">Request headers</span></span>
| <span data-ttu-id="0663a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0663a-122">Header</span></span>       | <span data-ttu-id="0663a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0663a-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0663a-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="0663a-124">Authorization</span></span>  | <span data-ttu-id="0663a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0663a-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0663a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0663a-127">Request body</span></span>
<span data-ttu-id="0663a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0663a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0663a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0663a-129">Response</span></span>

<span data-ttu-id="0663a-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [equipo](../resources/team.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0663a-130">If successful, this method returns a `200 OK` response code and a [team](../resources/team.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0663a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0663a-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="0663a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0663a-132">Request</span></span>
<span data-ttu-id="0663a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0663a-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}
```
#### <a name="response"></a><span data-ttu-id="0663a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0663a-134">Response</span></span>
<span data-ttu-id="0663a-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0663a-135">The following is an example of the response.</span></span> 

><span data-ttu-id="0663a-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0663a-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 401

{
  "isArchived" : false,
  "memberSettings": {
    "allowCreateUpdateChannels": true,
    "allowDeleteChannels": true,
    "allowAddRemoveApps": true,
    "allowCreateUpdateRemoveTabs": true,
    "allowCreateUpdateRemoveConnectors": true    
  },
  "guestSettings": {
    "allowCreateUpdateChannels": true,
    "allowDeleteChannels": true 
  },
  "messagingSettings": {
    "allowUserEditMessages": true,
    "allowUserDeleteMessages": true,
    "allowOwnerDeleteMessages": true,
    "allowTeamMentions": true,
    "allowChannelMentions": true    
  },
  "funSettings": {
    "allowGiphy": true,
    "giphyContentRating": "strict",
    "allowStickersAndMemes": true,
    "allowCustomMemes": true
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

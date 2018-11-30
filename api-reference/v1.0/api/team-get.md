---
title: Obtener el equipo
description: Recuperar las propiedades y relaciones del equipo especificado.
ms.openlocfilehash: 790d550024742875b0fb3a5b4383f0ec9ba793bb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031162"
---
# <a name="get-team"></a><span data-ttu-id="3c022-103">Obtener el equipo</span><span class="sxs-lookup"><span data-stu-id="3c022-103">Get team</span></span>



<span data-ttu-id="3c022-104">Recuperar las propiedades y relaciones del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="3c022-104">Retrieve the properties and relationships of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="3c022-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3c022-105">Permissions</span></span>
<span data-ttu-id="3c022-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3c022-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3c022-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3c022-108">Permission type</span></span>      | <span data-ttu-id="3c022-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3c022-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3c022-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3c022-110">Delegated (work or school account)</span></span> | <span data-ttu-id="3c022-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3c022-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="3c022-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3c022-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3c022-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3c022-113">Not supported.</span></span>    |
|<span data-ttu-id="3c022-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3c022-114">Application</span></span> | <span data-ttu-id="3c022-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3c022-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="3c022-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3c022-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3c022-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3c022-117">Optional query parameters</span></span>
<span data-ttu-id="3c022-118">Este método admite la $select y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c022-118">This method supports the $select and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3c022-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3c022-119">Request headers</span></span>
| <span data-ttu-id="3c022-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c022-120">Header</span></span>       | <span data-ttu-id="3c022-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3c022-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3c022-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3c022-122">Authorization</span></span>  | <span data-ttu-id="3c022-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3c022-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3c022-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3c022-125">Request body</span></span>
<span data-ttu-id="3c022-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3c022-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3c022-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c022-127">Response</span></span>

<span data-ttu-id="3c022-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [equipo](../resources/team.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c022-128">If successful, this method returns a `200 OK` response code and a [team](../resources/team.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3c022-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3c022-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="3c022-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3c022-130">Request</span></span>
<span data-ttu-id="3c022-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3c022-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}
```
#### <a name="response"></a><span data-ttu-id="3c022-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c022-132">Response</span></span>
<span data-ttu-id="3c022-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c022-133">The following is an example of the response.</span></span> 

><span data-ttu-id="3c022-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3c022-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

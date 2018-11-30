---
title: Obtener el equipo
description: Recuperar las propiedades y relaciones del equipo especificado.
ms.openlocfilehash: 4ace6ef068eeafffe10af029b3193805abd8a532
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084720"
---
# <a name="get-team"></a><span data-ttu-id="0bfb0-103">Obtener el equipo</span><span class="sxs-lookup"><span data-stu-id="0bfb0-103">Get team</span></span>

> <span data-ttu-id="0bfb0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0bfb0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0bfb0-106">Recuperar las propiedades y relaciones del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-106">Retrieve the properties and relationships of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="0bfb0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0bfb0-107">Permissions</span></span>
<span data-ttu-id="0bfb0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0bfb0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0bfb0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0bfb0-110">Permission type</span></span>      | <span data-ttu-id="0bfb0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0bfb0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0bfb0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0bfb0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0bfb0-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0bfb0-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="0bfb0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0bfb0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0bfb0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-115">Not supported.</span></span>    |
|<span data-ttu-id="0bfb0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0bfb0-116">Application</span></span> | <span data-ttu-id="0bfb0-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0bfb0-117">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="0bfb0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0bfb0-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0bfb0-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0bfb0-119">Optional query parameters</span></span>
<span data-ttu-id="0bfb0-120">Este método admite la $select y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-120">This method supports the $select and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0bfb0-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0bfb0-121">Request headers</span></span>
| <span data-ttu-id="0bfb0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bfb0-122">Header</span></span>       | <span data-ttu-id="0bfb0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0bfb0-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0bfb0-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="0bfb0-124">Authorization</span></span>  | <span data-ttu-id="0bfb0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0bfb0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0bfb0-127">Request body</span></span>
<span data-ttu-id="0bfb0-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0bfb0-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0bfb0-129">Response</span></span>

<span data-ttu-id="0bfb0-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [equipo](../resources/team.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-130">If successful, this method returns a `200 OK` response code and a [team](../resources/team.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0bfb0-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0bfb0-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="0bfb0-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0bfb0-132">Request</span></span>
<span data-ttu-id="0bfb0-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}
```
#### <a name="response"></a><span data-ttu-id="0bfb0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0bfb0-134">Response</span></span>
<span data-ttu-id="0bfb0-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-135">The following is an example of the response.</span></span> 

><span data-ttu-id="0bfb0-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0bfb0-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

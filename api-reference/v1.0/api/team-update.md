---
title: Equipo de actualización
description: Actualizar las propiedades del equipo especificado.
ms.openlocfilehash: 27cbf8f571752a27fb68727fe2695a0250f5dc75
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028921"
---
# <a name="update-team"></a><span data-ttu-id="a4eda-103">Equipo de actualización</span><span class="sxs-lookup"><span data-stu-id="a4eda-103">Update team</span></span>



<span data-ttu-id="a4eda-104">Actualizar las propiedades del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="a4eda-104">Update the properties of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="a4eda-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a4eda-105">Permissions</span></span>
<span data-ttu-id="a4eda-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a4eda-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="a4eda-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4eda-108">Permission type</span></span>      | <span data-ttu-id="a4eda-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4eda-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a4eda-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4eda-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a4eda-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a4eda-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a4eda-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4eda-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a4eda-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4eda-113">Not supported.</span></span>    |
|<span data-ttu-id="a4eda-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4eda-114">Application</span></span> | <span data-ttu-id="a4eda-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a4eda-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="a4eda-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4eda-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}
```
## <a name="request-headers"></a><span data-ttu-id="a4eda-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4eda-117">Request headers</span></span>
| <span data-ttu-id="a4eda-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4eda-118">Header</span></span>       | <span data-ttu-id="a4eda-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a4eda-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a4eda-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="a4eda-120">Authorization</span></span>  | <span data-ttu-id="a4eda-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a4eda-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a4eda-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a4eda-123">Content-Type</span></span>  | <span data-ttu-id="a4eda-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a4eda-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a4eda-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4eda-125">Request body</span></span>
<span data-ttu-id="a4eda-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [equipo](../resources/team.md) .</span><span class="sxs-lookup"><span data-stu-id="a4eda-126">In the request body, supply a JSON representation of [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="a4eda-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4eda-127">Response</span></span>

<span data-ttu-id="a4eda-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a4eda-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="a4eda-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4eda-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="a4eda-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4eda-130">Request</span></span>
<span data-ttu-id="a4eda-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4eda-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_team"
}-->
```http
PATCH https://graph.microsoft.com/beta/teams/{id}
Content-type: application/json
Content-length: 211

{  
  "memberSettings": {
    "allowCreateUpdateChannels": true
  },
  "messagingSettings": {
    "allowUserEditMessages": true,
    "allowUserDeleteMessages": true
  },
  "funSettings": {
    "allowGiphy": true,
    "giphyContentRating": "strict"
  }
}
```
#### <a name="response"></a><span data-ttu-id="a4eda-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4eda-132">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update Team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

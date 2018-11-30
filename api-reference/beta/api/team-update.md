---
title: Equipo de actualización
description: Actualizar las propiedades del equipo especificado.
ms.openlocfilehash: 9d07fd687facc96c1bc4a93c37cb492b321518e6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084412"
---
# <a name="update-team"></a><span data-ttu-id="846b4-103">Equipo de actualización</span><span class="sxs-lookup"><span data-stu-id="846b4-103">Update team</span></span>

> <span data-ttu-id="846b4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="846b4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="846b4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="846b4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="846b4-106">Actualizar las propiedades del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="846b4-106">Update the properties of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="846b4-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="846b4-107">Permissions</span></span>
<span data-ttu-id="846b4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="846b4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="846b4-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="846b4-110">Permission type</span></span>      | <span data-ttu-id="846b4-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="846b4-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="846b4-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="846b4-112">Delegated (work or school account)</span></span> | <span data-ttu-id="846b4-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="846b4-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="846b4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="846b4-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="846b4-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="846b4-115">Not supported.</span></span>    |
|<span data-ttu-id="846b4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="846b4-116">Application</span></span> | <span data-ttu-id="846b4-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="846b4-117">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="846b4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="846b4-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}
```
## <a name="request-headers"></a><span data-ttu-id="846b4-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="846b4-119">Request headers</span></span>
| <span data-ttu-id="846b4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="846b4-120">Header</span></span>       | <span data-ttu-id="846b4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="846b4-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="846b4-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="846b4-122">Authorization</span></span>  | <span data-ttu-id="846b4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="846b4-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="846b4-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="846b4-125">Content-Type</span></span>  | <span data-ttu-id="846b4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="846b4-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="846b4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="846b4-127">Request body</span></span>
<span data-ttu-id="846b4-128">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [equipo](../resources/team.md) .</span><span class="sxs-lookup"><span data-stu-id="846b4-128">In the request body, supply a JSON representation of [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="846b4-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="846b4-129">Response</span></span>

<span data-ttu-id="846b4-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="846b4-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="846b4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="846b4-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="846b4-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="846b4-132">Request</span></span>
<span data-ttu-id="846b4-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="846b4-133">The following is an example of the request.</span></span>
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
#### <a name="response"></a><span data-ttu-id="846b4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="846b4-134">Response</span></span>
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

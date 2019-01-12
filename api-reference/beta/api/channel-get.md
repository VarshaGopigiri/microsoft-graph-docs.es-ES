---
title: Obtener el canal
description: Recuperar las propiedades y relaciones de un canal.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: bd02ce2e46dc176ee9c94f0f20c880e278efe5f7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966366"
---
# <a name="get-channel"></a><span data-ttu-id="71f75-103">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="71f75-103">Get channel</span></span>

> <span data-ttu-id="71f75-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="71f75-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="71f75-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="71f75-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="71f75-106">Recuperar las propiedades y relaciones de un [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="71f75-106">Retrieve the properties and relationships of a [channel](../resources/channel.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="71f75-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="71f75-107">Permissions</span></span>
<span data-ttu-id="71f75-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="71f75-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="71f75-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71f75-110">Permission type</span></span>      | <span data-ttu-id="71f75-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71f75-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="71f75-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71f75-112">Delegated (work or school account)</span></span> | <span data-ttu-id="71f75-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71f75-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="71f75-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71f75-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="71f75-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71f75-115">Not supported.</span></span>    |
|<span data-ttu-id="71f75-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71f75-116">Application</span></span> | <span data-ttu-id="71f75-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71f75-117">Group.Read.All, Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="71f75-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="71f75-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="71f75-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="71f75-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="71f75-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71f75-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels/{id}

```

## <a name="optional-query-parameters"></a><span data-ttu-id="71f75-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="71f75-121">Optional query parameters</span></span>

<span data-ttu-id="71f75-122">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71f75-122">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="71f75-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71f75-123">Request headers</span></span>
| <span data-ttu-id="71f75-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71f75-124">Header</span></span>       | <span data-ttu-id="71f75-125">Valor</span><span class="sxs-lookup"><span data-stu-id="71f75-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="71f75-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="71f75-126">Authorization</span></span>  | <span data-ttu-id="71f75-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71f75-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="71f75-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71f75-129">Request body</span></span>
<span data-ttu-id="71f75-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71f75-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71f75-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71f75-131">Response</span></span>

<span data-ttu-id="71f75-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [canal](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71f75-132">If successful, this method returns a `200 OK` response code and a [channel](../resources/channel.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="71f75-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71f75-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="71f75-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71f75-134">Request</span></span>
<span data-ttu-id="71f75-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71f75-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channel"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="71f75-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71f75-136">Response</span></span>
<span data-ttu-id="71f75-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71f75-137">Here is an example of the response.</span></span> 

><span data-ttu-id="71f75-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71f75-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

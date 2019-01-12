---
title: Obtener la ficha
description: 'Recuperar las propiedades y relaciones de la ficha especificada seleccionada. '
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 70782682e2e87de50459384d782a56ccb7e6cfe8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945604"
---
# <a name="get-tab"></a><span data-ttu-id="24719-103">Obtener la ficha</span><span class="sxs-lookup"><span data-stu-id="24719-103">Get tab</span></span>



<span data-ttu-id="24719-104">Recuperar las propiedades y relaciones de la [ficha](../resources/teamstab.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="24719-104">Retrieve the properties and relationships of the specified [tab](../resources/teamstab.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="24719-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="24719-105">Permissions</span></span>
<span data-ttu-id="24719-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="24719-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="24719-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="24719-108">Permission type</span></span>      | <span data-ttu-id="24719-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="24719-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="24719-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="24719-110">Delegated (work or school account)</span></span> | <span data-ttu-id="24719-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="24719-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="24719-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="24719-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="24719-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="24719-113">Not supported.</span></span>    |
|<span data-ttu-id="24719-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="24719-114">Application</span></span> | <span data-ttu-id="24719-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="24719-115">Group.Read.All, Group.ReadWrite.All</span></span> |

> <span data-ttu-id="24719-116">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="24719-116">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="24719-117">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="24719-117">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="24719-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="24719-118">HTTP request</span></span>
```http
GET /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="24719-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="24719-119">Optional query parameters</span></span>

<span data-ttu-id="24719-120">Este método admite la $select y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="24719-120">This method supports the $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="24719-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="24719-121">Request headers</span></span>
| <span data-ttu-id="24719-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24719-122">Header</span></span>       | <span data-ttu-id="24719-123">Valor</span><span class="sxs-lookup"><span data-stu-id="24719-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="24719-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="24719-124">Authorization</span></span>  | <span data-ttu-id="24719-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="24719-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="24719-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="24719-127">Request body</span></span>
<span data-ttu-id="24719-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="24719-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="24719-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24719-129">Response</span></span>

<span data-ttu-id="24719-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [tab](../resources/teamstab.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="24719-130">If successful, this method returns a `200 OK` response code and a [tab](../resources/teamstab.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="24719-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="24719-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="24719-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="24719-132">Request</span></span>
<span data-ttu-id="24719-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="24719-133">The following is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="24719-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24719-134">Response</span></span>
<span data-ttu-id="24719-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="24719-135">The following is an example of the response.</span></span> 

><span data-ttu-id="24719-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="24719-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 401

{
  "id": "tabId",
  "name": "My Contoso Tab - updated",
  "teamsAppId": "06805b9e-77e3-4b93-ac81-525eb87513b8",
  "configuration": {
    "entityId": "2DCA2E6C7A10415CAF6B8AB6661B3154",
    "contentUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/tabView",
    "websiteUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154",
    "removeUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/uninstallTab"
  },
  "sortOrderIndex": 20,
  "webUrl": "https://teams.microsoft.com/l/channel/19%3ac2e36757ee744c569e70b385e6dd79b6%40thread.skype/tab%3a%3afd736d46-51ed-4c0b-9b23-e67ca354bb24?label=my%20%contoso%to%tab"
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get a channel tab",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

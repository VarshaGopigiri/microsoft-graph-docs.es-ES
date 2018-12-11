---
title: Obtener la ficha
description: 'Recuperar las propiedades y relaciones de la ficha especificada seleccionada. '
ms.openlocfilehash: 6dcc850bb42487cd8ca7f9cc9f7330b59fa965cc
ms.sourcegitcommit: 72d4da2a6bfaf99fa4edaf6ce3b97b1a6d96d874
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "27222621"
---
# <a name="get-tab"></a><span data-ttu-id="d420e-103">Obtener la ficha</span><span class="sxs-lookup"><span data-stu-id="d420e-103">Get tab</span></span>



<span data-ttu-id="d420e-104">Recuperar las propiedades y relaciones de la [ficha](../resources/teamstab.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="d420e-104">Retrieve the properties and relationships of the specified [tab](../resources/teamstab.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="d420e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d420e-105">Permissions</span></span>
<span data-ttu-id="d420e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d420e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d420e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d420e-108">Permission type</span></span>      | <span data-ttu-id="d420e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d420e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d420e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d420e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d420e-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d420e-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="d420e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d420e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d420e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d420e-113">Not supported.</span></span>    |
|<span data-ttu-id="d420e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d420e-114">Application</span></span> | <span data-ttu-id="d420e-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d420e-115">Group.Read.All, Group.ReadWrite.All</span></span> |

> <span data-ttu-id="d420e-116">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="d420e-116">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="d420e-117">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="d420e-117">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="d420e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d420e-118">HTTP request</span></span>
```http
GET /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="d420e-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d420e-119">Optional query parameters</span></span>

<span data-ttu-id="d420e-120">Este método admite la $select y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d420e-120">This method supports the $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d420e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d420e-121">Request headers</span></span>
| <span data-ttu-id="d420e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d420e-122">Header</span></span>       | <span data-ttu-id="d420e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d420e-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d420e-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="d420e-124">Authorization</span></span>  | <span data-ttu-id="d420e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d420e-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d420e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d420e-127">Request body</span></span>
<span data-ttu-id="d420e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d420e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d420e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d420e-129">Response</span></span>

<span data-ttu-id="d420e-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [tab](../resources/teamstab.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d420e-130">If successful, this method returns a `200 OK` response code and a [tab](../resources/teamstab.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d420e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d420e-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="d420e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d420e-132">Request</span></span>
<span data-ttu-id="d420e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d420e-133">The following is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="d420e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d420e-134">Response</span></span>
<span data-ttu-id="d420e-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d420e-135">The following is an example of the response.</span></span> 

><span data-ttu-id="d420e-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d420e-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

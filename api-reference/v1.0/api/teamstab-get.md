---
title: Obtener la ficha
description: 'Recuperar las propiedades y relaciones de la ficha especificada seleccionada. '
ms.openlocfilehash: 0a183d9bd55e0002a40335849549285d45fe9f69
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028824"
---
# <a name="get-tab"></a><span data-ttu-id="7b62a-103">Obtener la ficha</span><span class="sxs-lookup"><span data-stu-id="7b62a-103">Get tab</span></span>



<span data-ttu-id="7b62a-104">Recuperar las propiedades y relaciones de la [ficha](../resources/teamstab.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="7b62a-104">Retrieve the properties and relationships of the specified [tab](../resources/teamstab.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="7b62a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b62a-105">Permissions</span></span>
<span data-ttu-id="7b62a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b62a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7b62a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b62a-108">Permission type</span></span>      | <span data-ttu-id="7b62a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b62a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7b62a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b62a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="7b62a-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b62a-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7b62a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b62a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b62a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b62a-113">Not supported.</span></span>    |
|<span data-ttu-id="7b62a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b62a-114">Application</span></span> | <span data-ttu-id="7b62a-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b62a-115">Group.Read.All, Group.ReadWrite.All</span></span> |

> <span data-ttu-id="7b62a-116">Actualmente, se admiten sólo [delegar permisos](/graph/permissions-reference) para esta operación.</span><span class="sxs-lookup"><span data-stu-id="7b62a-116">Currently, only [delegated permissions](/graph/permissions-reference) are supported for this operation.</span></span>

## <a name="http-request"></a><span data-ttu-id="7b62a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b62a-117">HTTP request</span></span>
```http
GET /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="7b62a-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7b62a-118">Optional query parameters</span></span>

<span data-ttu-id="7b62a-119">Este método admite la $select y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b62a-119">This method supports the $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7b62a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b62a-120">Request headers</span></span>
| <span data-ttu-id="7b62a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b62a-121">Header</span></span>       | <span data-ttu-id="7b62a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7b62a-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7b62a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7b62a-123">Authorization</span></span>  | <span data-ttu-id="7b62a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b62a-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7b62a-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b62a-126">Request body</span></span>
<span data-ttu-id="7b62a-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7b62a-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7b62a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b62a-128">Response</span></span>

<span data-ttu-id="7b62a-129">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [tab](../resources/teamstab.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b62a-129">If successful, this method returns a `200 OK` response code and a [tab](../resources/teamstab.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7b62a-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b62a-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="7b62a-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b62a-131">Request</span></span>
<span data-ttu-id="7b62a-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b62a-132">The following is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="7b62a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b62a-133">Response</span></span>
<span data-ttu-id="7b62a-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b62a-134">The following is an example of the response.</span></span> 

><span data-ttu-id="7b62a-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b62a-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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

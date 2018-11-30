---
title: Obtener la ficha
description: 'Recuperar las propiedades y relaciones de la ficha especificada seleccionada. '
ms.openlocfilehash: 57bd7d8b11b0bf20d54bf8da16cdd41220320fcd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083419"
---
# <a name="get-tab"></a><span data-ttu-id="625cb-103">Obtener la ficha</span><span class="sxs-lookup"><span data-stu-id="625cb-103">Get tab</span></span>

> <span data-ttu-id="625cb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="625cb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="625cb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="625cb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="625cb-106">Recuperar las propiedades y relaciones de la [ficha](../resources/teamstab.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="625cb-106">Retrieve the properties and relationships of the specified [tab](../resources/teamstab.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="625cb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="625cb-107">Permissions</span></span>
<span data-ttu-id="625cb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="625cb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="625cb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="625cb-110">Permission type</span></span>      | <span data-ttu-id="625cb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="625cb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="625cb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="625cb-112">Delegated (work or school account)</span></span> | <span data-ttu-id="625cb-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="625cb-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="625cb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="625cb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="625cb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="625cb-115">Not supported.</span></span>    |
|<span data-ttu-id="625cb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="625cb-116">Application</span></span> | <span data-ttu-id="625cb-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="625cb-117">Group.Read.All, Group.ReadWrite.All</span></span> |

> <span data-ttu-id="625cb-118">Actualmente, se admiten sólo [delegar permisos](/graph/permissions-reference) para esta operación.</span><span class="sxs-lookup"><span data-stu-id="625cb-118">Currently, only [delegated permissions](/graph/permissions-reference) are supported for this operation.</span></span>

## <a name="http-request"></a><span data-ttu-id="625cb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="625cb-119">HTTP request</span></span>
```http
GET /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="625cb-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="625cb-120">Optional query parameters</span></span>

<span data-ttu-id="625cb-121">Este método admite la $select y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="625cb-121">This method supports the $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="625cb-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="625cb-122">Request headers</span></span>
| <span data-ttu-id="625cb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="625cb-123">Header</span></span>       | <span data-ttu-id="625cb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="625cb-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="625cb-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="625cb-125">Authorization</span></span>  | <span data-ttu-id="625cb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="625cb-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="625cb-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="625cb-128">Request body</span></span>
<span data-ttu-id="625cb-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="625cb-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="625cb-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="625cb-130">Response</span></span>

<span data-ttu-id="625cb-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [tab](../resources/teamstab.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="625cb-131">If successful, this method returns a `200 OK` response code and a [tab](../resources/teamstab.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="625cb-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="625cb-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="625cb-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="625cb-133">Request</span></span>
<span data-ttu-id="625cb-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="625cb-134">The following is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="625cb-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="625cb-135">Response</span></span>
<span data-ttu-id="625cb-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="625cb-136">The following is an example of the response.</span></span> 

><span data-ttu-id="625cb-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="625cb-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
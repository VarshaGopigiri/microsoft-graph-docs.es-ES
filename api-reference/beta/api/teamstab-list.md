---
title: Fichas de lista de canal
description: 'Recuperar la lista de fichas en el canal especificado dentro de un equipo. '
author: nkramer
ms.openlocfilehash: 12d2c0c1abe85d1e2fa93cee0bdab12d8880eed9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346861"
---
# <a name="list-tabs-in-channel"></a><span data-ttu-id="a73ef-103">Fichas de lista de canal</span><span class="sxs-lookup"><span data-stu-id="a73ef-103">List tabs in channel</span></span>

> <span data-ttu-id="a73ef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a73ef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a73ef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a73ef-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a73ef-106">Recuperar la lista de [fichas](../resources/teamstab.md) en el [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="a73ef-106">Retrieve the list of [tabs](../resources/teamstab.md) in the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="a73ef-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a73ef-107">Permissions</span></span>
<span data-ttu-id="a73ef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a73ef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a73ef-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a73ef-110">Permission type</span></span>      | <span data-ttu-id="a73ef-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a73ef-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a73ef-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a73ef-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a73ef-113">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a73ef-113">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="a73ef-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a73ef-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a73ef-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a73ef-115">Not supported.</span></span>    |
| <span data-ttu-id="a73ef-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a73ef-116">Application</span></span>                            | <span data-ttu-id="a73ef-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a73ef-117">Group.Read.All, Group.ReadWrite.All</span></span>         |

> <span data-ttu-id="a73ef-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="a73ef-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="a73ef-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="a73ef-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="a73ef-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a73ef-120">HTTP request</span></span>

```http
GET /teams/{id}/channels/{id}/tabs
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a73ef-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a73ef-121">Optional query parameters</span></span>

<span data-ttu-id="a73ef-122">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a73ef-122">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a73ef-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a73ef-123">Request headers</span></span>
| <span data-ttu-id="a73ef-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a73ef-124">Header</span></span>       | <span data-ttu-id="a73ef-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a73ef-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a73ef-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="a73ef-126">Authorization</span></span>  | <span data-ttu-id="a73ef-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a73ef-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a73ef-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a73ef-129">Request body</span></span>
<span data-ttu-id="a73ef-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a73ef-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a73ef-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a73ef-131">Response</span></span>
<span data-ttu-id="a73ef-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [las fichas](../resources/teamstab.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a73ef-132">If successful, this method returns a `200 OK` response code and collection of [tabs](../resources/teamstab.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a73ef-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a73ef-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="a73ef-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a73ef-134">Request</span></span>
<span data-ttu-id="a73ef-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a73ef-135">The following is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs
```

#### <a name="response"></a><span data-ttu-id="a73ef-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a73ef-136">Response</span></span>
<span data-ttu-id="a73ef-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a73ef-137">The following is an example of the response.</span></span>
><span data-ttu-id="a73ef-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a73ef-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
```http
HTTP/1.1 200 Success
Content-type: application/json

{
  "value": [
    {
      "id": "794f0e4e-4d10-4bb5-9079-3a465a629eff",
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
    },
    {
      "id": "b5d5f001-0471-49a5-aac4-04ef96683be0",
      "name": "My Trello Tab",
      "teamsAppId": "23134c6b-5e4b-439c-8f70-3ded1df20805",
      "configuration": null,
      "sortOrderIndex": 21,
      "webUrl": "https://teams.microsoft.com/l/channel/19%3ac2e36757ee744c569e70b385e6dd79b6%40thread.skype/tab%3a%3a3709b35c-a0ba-467c-8001-0f66895fb9d3?label=My%20Trello%Tab"
    }
  ]
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List all tabs in channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

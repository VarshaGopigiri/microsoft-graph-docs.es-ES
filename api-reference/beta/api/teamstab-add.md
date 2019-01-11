---
title: Agregar una ficha a canal
description: '(PIN) se agrega una ficha al canal especificado dentro de un equipo. '
author: nkramer
localization_priority: Normal
ms.openlocfilehash: fc8ff6d56e5aa91b6d24401e2a5466cf259c7ac6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845426"
---
# <a name="add-tab-to-channel"></a><span data-ttu-id="badb9-103">Agregar una ficha a canal</span><span class="sxs-lookup"><span data-stu-id="badb9-103">Add tab to channel</span></span>

> <span data-ttu-id="badb9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="badb9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="badb9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="badb9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="badb9-106">(PIN) se agrega una [ficha](../resources/teamstab.md) al [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="badb9-106">Adds (pins) a [tab](../resources/teamstab.md) to the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> <span data-ttu-id="badb9-107">La aplicación correspondiente ya debe estar [instalado en el equipo](../api/teamsappinstallation-add.md).</span><span class="sxs-lookup"><span data-stu-id="badb9-107">The corresponding app must already be [installed in the team](../api/teamsappinstallation-add.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="badb9-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="badb9-108">Permissions</span></span>
<span data-ttu-id="badb9-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="badb9-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="badb9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="badb9-111">Permission type</span></span>      | <span data-ttu-id="badb9-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="badb9-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="badb9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="badb9-113">Delegated (work or school account)</span></span> | <span data-ttu-id="badb9-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="badb9-114">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="badb9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="badb9-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="badb9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="badb9-116">Not supported.</span></span>    |
| <span data-ttu-id="badb9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="badb9-117">Application</span></span>                            | <span data-ttu-id="badb9-118">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="badb9-118">Group.ReadWrite.All</span></span>                         |

> <span data-ttu-id="badb9-119">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="badb9-119">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="badb9-120">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="badb9-120">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="badb9-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="badb9-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/channels/{id}/tabs
```

## <a name="request-headers"></a><span data-ttu-id="badb9-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="badb9-122">Request headers</span></span>
| <span data-ttu-id="badb9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="badb9-123">Header</span></span>       | <span data-ttu-id="badb9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="badb9-124">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="badb9-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="badb9-125">Authorization</span></span>  | <span data-ttu-id="badb9-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="badb9-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="badb9-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="badb9-128">Request body</span></span>

<span data-ttu-id="badb9-129">Un [teamsTab](../resources/teamstab.md).</span><span class="sxs-lookup"><span data-stu-id="badb9-129">A [teamsTab](../resources/teamstab.md).</span></span>

## <a name="response"></a><span data-ttu-id="badb9-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="badb9-130">Response</span></span>

<span data-ttu-id="badb9-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 OK`.</span><span class="sxs-lookup"><span data-stu-id="badb9-131">If successful, this method returns a `201 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="badb9-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="badb9-132">Example</span></span>

#### <a name="request"></a><span data-ttu-id="badb9-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="badb9-133">Request</span></span>

<span data-ttu-id="badb9-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="badb9-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs
{
  "name": "My Contoso Tab",
  "teamsApp@odata.bind" : "https://graph.microsoft.com/beta/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8",
  "configuration": {
    "entityId": "2DCA2E6C7A10415CAF6B8AB6661B3154",
    "contentUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/tabView",
    "websiteUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154",
    "removeUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/uninstallTab"
  }
}
```

#### <a name="response"></a><span data-ttu-id="badb9-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="badb9-135">Response</span></span>

<span data-ttu-id="badb9-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="badb9-136">The following is an example of the response.</span></span> <span data-ttu-id="badb9-137">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="badb9-137">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="badb9-138">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="badb9-138">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "794f0e4e-4d10-4bb5-9079-3a465a629eff",
  "name": "My Contoso Tab",
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

## <a name="see-also"></a><span data-ttu-id="badb9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="badb9-139">See also</span></span>

[<span data-ttu-id="badb9-140">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="badb9-140">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Add tab to channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

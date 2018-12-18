---
title: Agregar una ficha a canal
description: '(PIN) se agrega una ficha al canal especificado dentro de un equipo. '
author: nkramer
ms.openlocfilehash: 2e99e2297fd21f651b9461798c1a2236f9ffb321
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337509"
---
# <a name="add-tab-to-channel"></a><span data-ttu-id="a979d-103">Agregar una ficha a canal</span><span class="sxs-lookup"><span data-stu-id="a979d-103">Add tab to channel</span></span>



<span data-ttu-id="a979d-104">(PIN) se agrega una [ficha](../resources/teamstab.md) al [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="a979d-104">Adds (pins) a [tab](../resources/teamstab.md) to the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> <span data-ttu-id="a979d-105">La aplicación correspondiente ya debe estar [instalado en el equipo](../api/teamsappinstallation-add.md).</span><span class="sxs-lookup"><span data-stu-id="a979d-105">The corresponding app must already be [installed in the team](../api/teamsappinstallation-add.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="a979d-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="a979d-106">Permissions</span></span>
<span data-ttu-id="a979d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a979d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a979d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a979d-109">Permission type</span></span>      | <span data-ttu-id="a979d-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a979d-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a979d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a979d-111">Delegated (work or school account)</span></span> | <span data-ttu-id="a979d-112">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a979d-112">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a979d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a979d-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a979d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a979d-114">Not supported.</span></span>    |
| <span data-ttu-id="a979d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a979d-115">Application</span></span>                            | <span data-ttu-id="a979d-116">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a979d-116">Group.ReadWrite.All</span></span>                         |

> <span data-ttu-id="a979d-117">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="a979d-117">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="a979d-118">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="a979d-118">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="a979d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a979d-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/channels/{id}/tabs
```

## <a name="request-headers"></a><span data-ttu-id="a979d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a979d-120">Request headers</span></span>
| <span data-ttu-id="a979d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a979d-121">Header</span></span>       | <span data-ttu-id="a979d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a979d-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a979d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a979d-123">Authorization</span></span>  | <span data-ttu-id="a979d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a979d-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a979d-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a979d-126">Request body</span></span>

<span data-ttu-id="a979d-127">Un [teamsTab](../resources/teamstab.md).</span><span class="sxs-lookup"><span data-stu-id="a979d-127">A [teamsTab](../resources/teamstab.md).</span></span>

## <a name="response"></a><span data-ttu-id="a979d-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a979d-128">Response</span></span>

<span data-ttu-id="a979d-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 OK`.</span><span class="sxs-lookup"><span data-stu-id="a979d-129">If successful, this method returns a `201 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="a979d-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a979d-130">Example</span></span>

#### <a name="request"></a><span data-ttu-id="a979d-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a979d-131">Request</span></span>

<span data-ttu-id="a979d-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a979d-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs
{
  "name": "My Contoso Tab",
  "teamsApp@odata.bind" : "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8",
  "configuration": {
    "entityId": "2DCA2E6C7A10415CAF6B8AB6661B3154",
    "contentUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/tabView",
    "websiteUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154",
    "removeUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/uninstallTab"
  }
}
```

#### <a name="response"></a><span data-ttu-id="a979d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a979d-133">Response</span></span>

<span data-ttu-id="a979d-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a979d-134">The following is an example of the response.</span></span> <span data-ttu-id="a979d-135">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="a979d-135">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="a979d-136">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a979d-136">All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="a979d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a979d-137">See also</span></span>

[<span data-ttu-id="a979d-138">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="a979d-138">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Add tab to channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

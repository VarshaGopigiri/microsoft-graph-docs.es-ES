---
title: Agregar una ficha a canal
description: '(PIN) se agrega una ficha al canal especificado dentro de un equipo. '
ms.openlocfilehash: 1bf2021438cc9c0c74a2a4133e54a4fbc42fdf4d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030674"
---
# <a name="add-tab-to-channel"></a><span data-ttu-id="3c3d8-103">Agregar una ficha a canal</span><span class="sxs-lookup"><span data-stu-id="3c3d8-103">Add tab to channel</span></span>



<span data-ttu-id="3c3d8-104">(PIN) se agrega una [ficha](../resources/teamstab.md) al [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="3c3d8-104">Adds (pins) a [tab](../resources/teamstab.md) to the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> <span data-ttu-id="3c3d8-105">La aplicación correspondiente ya debe estar [instalado en el equipo](../api/teamsappinstallation-add.md).</span><span class="sxs-lookup"><span data-stu-id="3c3d8-105">The corresponding app must already be [installed in the team](../api/teamsappinstallation-add.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="3c3d8-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="3c3d8-106">Permissions</span></span>
<span data-ttu-id="3c3d8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3c3d8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3c3d8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3c3d8-109">Permission type</span></span>      | <span data-ttu-id="3c3d8-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3c3d8-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3c3d8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3c3d8-111">Delegated (work or school account)</span></span> | <span data-ttu-id="3c3d8-112">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3c3d8-112">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="3c3d8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3c3d8-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3c3d8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3c3d8-114">Not supported.</span></span>    |
| <span data-ttu-id="3c3d8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3c3d8-115">Application</span></span>                            | <span data-ttu-id="3c3d8-116">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3c3d8-116">Group.ReadWrite.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="3c3d8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3c3d8-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/channels/{id}/tabs
```

## <a name="request-headers"></a><span data-ttu-id="3c3d8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3c3d8-118">Request headers</span></span>
| <span data-ttu-id="3c3d8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c3d8-119">Header</span></span>       | <span data-ttu-id="3c3d8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3c3d8-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3c3d8-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="3c3d8-121">Authorization</span></span>  | <span data-ttu-id="3c3d8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3c3d8-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3c3d8-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3c3d8-124">Request body</span></span>

<span data-ttu-id="3c3d8-125">Un [teamsTab](../resources/teamstab.md).</span><span class="sxs-lookup"><span data-stu-id="3c3d8-125">A [teamsTab](../resources/teamstab.md).</span></span>

## <a name="response"></a><span data-ttu-id="3c3d8-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c3d8-126">Response</span></span>

<span data-ttu-id="3c3d8-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 OK`.</span><span class="sxs-lookup"><span data-stu-id="3c3d8-127">If successful, this method returns a `201 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="3c3d8-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3c3d8-128">Example</span></span>

#### <a name="request"></a><span data-ttu-id="3c3d8-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3c3d8-129">Request</span></span>

<span data-ttu-id="3c3d8-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3c3d8-130">The following is an example of the request.</span></span>
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

#### <a name="response"></a><span data-ttu-id="3c3d8-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c3d8-131">Response</span></span>

<span data-ttu-id="3c3d8-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c3d8-132">The following is an example of the response.</span></span> <span data-ttu-id="3c3d8-133">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="3c3d8-133">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="3c3d8-134">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3c3d8-134">All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="3c3d8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c3d8-135">See also</span></span>

[<span data-ttu-id="3c3d8-136">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="3c3d8-136">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Add tab to channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

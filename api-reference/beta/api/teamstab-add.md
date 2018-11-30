---
title: Agregar una ficha a canal
description: '(PIN) se agrega una ficha al canal especificado dentro de un equipo. '
ms.openlocfilehash: be246b0308be83e0b411fa89fe16034018756829
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084725"
---
# <a name="add-tab-to-channel"></a><span data-ttu-id="18b30-103">Agregar una ficha a canal</span><span class="sxs-lookup"><span data-stu-id="18b30-103">Add tab to channel</span></span>

> <span data-ttu-id="18b30-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="18b30-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="18b30-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="18b30-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="18b30-106">(PIN) se agrega una [ficha](../resources/teamstab.md) al [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="18b30-106">Adds (pins) a [tab](../resources/teamstab.md) to the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> <span data-ttu-id="18b30-107">La aplicación correspondiente ya debe estar [instalado en el equipo](../api/teamsappinstallation-add.md).</span><span class="sxs-lookup"><span data-stu-id="18b30-107">The corresponding app must already be [installed in the team](../api/teamsappinstallation-add.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="18b30-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="18b30-108">Permissions</span></span>
<span data-ttu-id="18b30-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="18b30-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="18b30-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="18b30-111">Permission type</span></span>      | <span data-ttu-id="18b30-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="18b30-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="18b30-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="18b30-113">Delegated (work or school account)</span></span> | <span data-ttu-id="18b30-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="18b30-114">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="18b30-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18b30-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="18b30-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18b30-116">Not supported.</span></span>    |
| <span data-ttu-id="18b30-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="18b30-117">Application</span></span>                            | <span data-ttu-id="18b30-118">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="18b30-118">Group.ReadWrite.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="18b30-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18b30-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/channels/{id}/tabs
```

## <a name="request-headers"></a><span data-ttu-id="18b30-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18b30-120">Request headers</span></span>
| <span data-ttu-id="18b30-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18b30-121">Header</span></span>       | <span data-ttu-id="18b30-122">Valor</span><span class="sxs-lookup"><span data-stu-id="18b30-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="18b30-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="18b30-123">Authorization</span></span>  | <span data-ttu-id="18b30-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18b30-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="18b30-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="18b30-126">Request body</span></span>

<span data-ttu-id="18b30-127">Un [teamsTab](../resources/teamstab.md).</span><span class="sxs-lookup"><span data-stu-id="18b30-127">A [teamsTab](../resources/teamstab.md).</span></span>

## <a name="response"></a><span data-ttu-id="18b30-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18b30-128">Response</span></span>

<span data-ttu-id="18b30-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 OK`.</span><span class="sxs-lookup"><span data-stu-id="18b30-129">If successful, this method returns a `201 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="18b30-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18b30-130">Example</span></span>

#### <a name="request"></a><span data-ttu-id="18b30-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18b30-131">Request</span></span>

<span data-ttu-id="18b30-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18b30-132">The following is an example of the request.</span></span>
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

#### <a name="response"></a><span data-ttu-id="18b30-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18b30-133">Response</span></span>

<span data-ttu-id="18b30-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18b30-134">The following is an example of the response.</span></span> <span data-ttu-id="18b30-135">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="18b30-135">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="18b30-136">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="18b30-136">All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="18b30-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="18b30-137">See also</span></span>

[<span data-ttu-id="18b30-138">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="18b30-138">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Add tab to channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

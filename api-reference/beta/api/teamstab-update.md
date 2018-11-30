---
title: Ficha de actualización
description: Actualizar las propiedades de la ficha especificada seleccionada.
ms.openlocfilehash: 6943e9ea4ff602b3fcd4dc8ac899d55cee120ecc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084729"
---
# <a name="update-tab"></a><span data-ttu-id="c4282-103">Ficha de actualización</span><span class="sxs-lookup"><span data-stu-id="c4282-103">Update tab</span></span>

> <span data-ttu-id="c4282-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c4282-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c4282-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c4282-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c4282-106">Actualizar las propiedades de la [ficha](../resources/teamstab.md)de especificado. Esto se puede usar para configurar el contenido de la ficha.</span><span class="sxs-lookup"><span data-stu-id="c4282-106">Update the properties of the specified [tab](../resources/teamstab.md). This can be used to configure the content of the tab.</span></span>

## <a name="permissions"></a><span data-ttu-id="c4282-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c4282-107">Permissions</span></span>
<span data-ttu-id="c4282-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c4282-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c4282-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c4282-110">Permission type</span></span>      | <span data-ttu-id="c4282-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c4282-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c4282-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c4282-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c4282-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c4282-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c4282-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c4282-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c4282-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4282-115">Not supported.</span></span>    |
|<span data-ttu-id="c4282-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c4282-116">Application</span></span>                            | <span data-ttu-id="c4282-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c4282-117">Group.ReadWrite.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="c4282-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c4282-118">HTTP request</span></span>
```http
PATCH /teams/{id}/channels/{id}/tabs/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c4282-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c4282-119">Request headers</span></span>
| <span data-ttu-id="c4282-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4282-120">Header</span></span>       | <span data-ttu-id="c4282-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c4282-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c4282-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c4282-122">Authorization</span></span>  | <span data-ttu-id="c4282-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c4282-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c4282-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c4282-125">Content-Type</span></span>  | <span data-ttu-id="c4282-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c4282-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c4282-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c4282-127">Request body</span></span>
<span data-ttu-id="c4282-128">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [tab](../resources/teamstab.md) .</span><span class="sxs-lookup"><span data-stu-id="c4282-128">In the request body, supply a JSON representation of [tab](../resources/teamstab.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="c4282-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4282-129">Response</span></span>

<span data-ttu-id="c4282-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="c4282-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="c4282-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c4282-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="c4282-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c4282-132">Request</span></span>
<span data-ttu-id="c4282-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4282-133">The following is an example of the request.</span></span>
```http
PATCH https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
Content-type: application/json
Content-length: 211

{
  "name": "My Contoso Tab - updated"
}
```
#### <a name="response"></a><span data-ttu-id="c4282-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4282-134">Response</span></span>
```http
HTTP/1.1 200 Success
Content-type: application/json

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

## <a name="see-also"></a><span data-ttu-id="c4282-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4282-135">See also</span></span>

[<span data-ttu-id="c4282-136">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="c4282-136">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update tab in channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
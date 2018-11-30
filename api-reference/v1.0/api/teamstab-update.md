---
title: Ficha de actualización
description: Actualizar las propiedades de la ficha especificada seleccionada.
ms.openlocfilehash: fb2346fbadcb9794e05f8bb583596536a5710052
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031769"
---
# <a name="update-tab"></a><span data-ttu-id="c3eb6-103">Ficha de actualización</span><span class="sxs-lookup"><span data-stu-id="c3eb6-103">Update tab</span></span>



<span data-ttu-id="c3eb6-104">Actualizar las propiedades de la [ficha](../resources/teamstab.md)de especificado. Esto se puede usar para configurar el contenido de la ficha.</span><span class="sxs-lookup"><span data-stu-id="c3eb6-104">Update the properties of the specified [tab](../resources/teamstab.md). This can be used to configure the content of the tab.</span></span>

## <a name="permissions"></a><span data-ttu-id="c3eb6-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c3eb6-105">Permissions</span></span>
<span data-ttu-id="c3eb6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c3eb6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c3eb6-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c3eb6-108">Permission type</span></span>      | <span data-ttu-id="c3eb6-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c3eb6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c3eb6-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c3eb6-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c3eb6-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3eb6-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c3eb6-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c3eb6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c3eb6-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3eb6-113">Not supported.</span></span>    |
|<span data-ttu-id="c3eb6-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c3eb6-114">Application</span></span>                            | <span data-ttu-id="c3eb6-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3eb6-115">Group.ReadWrite.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="c3eb6-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3eb6-116">HTTP request</span></span>
```http
PATCH /teams/{id}/channels/{id}/tabs/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c3eb6-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c3eb6-117">Request headers</span></span>
| <span data-ttu-id="c3eb6-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3eb6-118">Header</span></span>       | <span data-ttu-id="c3eb6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c3eb6-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c3eb6-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c3eb6-120">Authorization</span></span>  | <span data-ttu-id="c3eb6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3eb6-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c3eb6-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c3eb6-123">Content-Type</span></span>  | <span data-ttu-id="c3eb6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c3eb6-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c3eb6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c3eb6-125">Request body</span></span>
<span data-ttu-id="c3eb6-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [tab](../resources/teamstab.md) .</span><span class="sxs-lookup"><span data-stu-id="c3eb6-126">In the request body, supply a JSON representation of [tab](../resources/teamstab.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="c3eb6-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3eb6-127">Response</span></span>

<span data-ttu-id="c3eb6-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="c3eb6-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="c3eb6-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3eb6-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="c3eb6-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c3eb6-130">Request</span></span>
<span data-ttu-id="c3eb6-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c3eb6-131">The following is an example of the request.</span></span>
```http
PATCH https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
Content-type: application/json
Content-length: 211

{
  "name": "My Contoso Tab - updated"
}
```
#### <a name="response"></a><span data-ttu-id="c3eb6-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3eb6-132">Response</span></span>
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

## <a name="see-also"></a><span data-ttu-id="c3eb6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3eb6-133">See also</span></span>

[<span data-ttu-id="c3eb6-134">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="c3eb6-134">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update tab in channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

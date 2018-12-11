---
title: Ficha de actualización
description: Actualizar las propiedades de la ficha especificada seleccionada.
ms.openlocfilehash: bc25830411f93ed1644b86c1228f987c091db32a
ms.sourcegitcommit: 72d4da2a6bfaf99fa4edaf6ce3b97b1a6d96d874
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "27222565"
---
# <a name="update-tab"></a><span data-ttu-id="0e3e8-103">Ficha de actualización</span><span class="sxs-lookup"><span data-stu-id="0e3e8-103">Update tab</span></span>

> <span data-ttu-id="0e3e8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0e3e8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0e3e8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0e3e8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0e3e8-106">Actualizar las propiedades de la [ficha](../resources/teamstab.md)de especificado. Esto se puede usar para configurar el contenido de la ficha.</span><span class="sxs-lookup"><span data-stu-id="0e3e8-106">Update the properties of the specified [tab](../resources/teamstab.md). This can be used to configure the content of the tab.</span></span>

## <a name="permissions"></a><span data-ttu-id="0e3e8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0e3e8-107">Permissions</span></span>
<span data-ttu-id="0e3e8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e3e8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="0e3e8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e3e8-110">Permission type</span></span>      | <span data-ttu-id="0e3e8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e3e8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0e3e8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e3e8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0e3e8-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e3e8-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="0e3e8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e3e8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0e3e8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e3e8-115">Not supported.</span></span>    |
|<span data-ttu-id="0e3e8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e3e8-116">Application</span></span>                            | <span data-ttu-id="0e3e8-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e3e8-117">Group.ReadWrite.All</span></span>                         |

> <span data-ttu-id="0e3e8-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="0e3e8-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="0e3e8-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="0e3e8-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="0e3e8-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e3e8-120">HTTP request</span></span>
```http
PATCH /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="request-headers"></a><span data-ttu-id="0e3e8-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e3e8-121">Request headers</span></span>
| <span data-ttu-id="0e3e8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e3e8-122">Header</span></span>       | <span data-ttu-id="0e3e8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0e3e8-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0e3e8-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e3e8-124">Authorization</span></span>  | <span data-ttu-id="0e3e8-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e3e8-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="0e3e8-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="0e3e8-127">Content-Type</span></span>  | <span data-ttu-id="0e3e8-128">application/json</span><span class="sxs-lookup"><span data-stu-id="0e3e8-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0e3e8-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e3e8-129">Request body</span></span>
<span data-ttu-id="0e3e8-130">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [tab](../resources/teamstab.md) .</span><span class="sxs-lookup"><span data-stu-id="0e3e8-130">In the request body, supply a JSON representation of [tab](../resources/teamstab.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="0e3e8-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e3e8-131">Response</span></span>

<span data-ttu-id="0e3e8-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="0e3e8-132">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="0e3e8-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e3e8-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="0e3e8-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e3e8-134">Request</span></span>
<span data-ttu-id="0e3e8-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e3e8-135">The following is an example of the request.</span></span>
```http
PATCH https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
Content-type: application/json
Content-length: 211

{
  "name": "My Contoso Tab - updated"
}
```
#### <a name="response"></a><span data-ttu-id="0e3e8-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e3e8-136">Response</span></span>
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

## <a name="see-also"></a><span data-ttu-id="0e3e8-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e3e8-137">See also</span></span>

[<span data-ttu-id="0e3e8-138">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="0e3e8-138">Configuring the built-in tab types</span></span>](/graph/teams-configuring-builtin-tabs)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update tab in channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

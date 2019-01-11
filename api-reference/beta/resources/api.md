---
title: tipo de recurso de API
description: Especifica la configuración para una aplicación Web API.
localization_priority: Normal
ms.openlocfilehash: 50c21c31fec7434514408e1a214c6edf2b838c98
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845213"
---
# <a name="api-resource-type"></a><span data-ttu-id="c9319-103">tipo de recurso de API</span><span class="sxs-lookup"><span data-stu-id="c9319-103">api resource type</span></span>

> <span data-ttu-id="c9319-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c9319-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c9319-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c9319-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c9319-106">Especifica la configuración para una aplicación Web API.</span><span class="sxs-lookup"><span data-stu-id="c9319-106">Specifies settings for a Web API application.</span></span>

## <a name="properties"></a><span data-ttu-id="c9319-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9319-107">Properties</span></span>

| <span data-ttu-id="c9319-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c9319-108">Property</span></span> | <span data-ttu-id="c9319-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9319-109">Type</span></span> | <span data-ttu-id="c9319-110">Description</span><span class="sxs-lookup"><span data-stu-id="c9319-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="c9319-111">requestedAccessTokenVersion</span><span class="sxs-lookup"><span data-stu-id="c9319-111">requestedAccessTokenVersion</span></span>|<span data-ttu-id="c9319-112">Int32</span><span class="sxs-lookup"><span data-stu-id="c9319-112">Int32</span></span>| <span data-ttu-id="c9319-113">Especifica la versión de token de acceso aceptados para el recurso de API actual.</span><span class="sxs-lookup"><span data-stu-id="c9319-113">Specifies the accepted access token version for the current API resource.</span></span> <span data-ttu-id="c9319-114">Los valores posibles son 1 ó 2.</span><span class="sxs-lookup"><span data-stu-id="c9319-114">Possible values are 1 or 2.</span></span>  |
|<span data-ttu-id="c9319-115">oauth2PermissionScopes</span><span class="sxs-lookup"><span data-stu-id="c9319-115">oauth2PermissionScopes</span></span>|<span data-ttu-id="c9319-116">colección de [permissionScope](permissionscope.md)</span><span class="sxs-lookup"><span data-stu-id="c9319-116">[permissionScope](permissionscope.md) collection</span></span>| <span data-ttu-id="c9319-117">La colección de los ámbitos de permiso de OAuth 2.0 que expone la web de aplicación de la API (recurso) a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="c9319-117">The collection of OAuth 2.0 permission scopes that the web API (resource) application exposes to client applications.</span></span> <span data-ttu-id="c9319-118">Estos ámbitos de permisos pueden concederse a las aplicaciones cliente durante su consentimiento.</span><span class="sxs-lookup"><span data-stu-id="c9319-118">These permission scopes may be granted to client applications during consent.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="c9319-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c9319-119">JSON representation</span></span>
<span data-ttu-id="c9319-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c9319-120">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.api"
}-->

```json
{
  "requestedAccessTokenVersion": 1,
  "oauth2PermissionScopes": [{"@odata.type": "microsoft.graph.permissionScope"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "api resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

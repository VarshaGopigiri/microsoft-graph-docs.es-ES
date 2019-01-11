---
title: tipo de recurso requiredResourceAccess
description: Especifica el conjunto de OAuth 2.0 ámbitos de permisos y roles de la aplicación en el recurso especificado que una aplicación necesita tener acceso a. Los ámbitos de permisos especificados OAuth 2.0 pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** ) cuando una llamada a una aplicación de recursos. La propiedad **requiredResourceAccess** de la entidad de la aplicación es una colección de **ReqiredResourceAccess**.
localization_priority: Normal
ms.openlocfilehash: 473126365a7f0b3ba3ab0371322ff90bd36318e3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856171"
---
# <a name="requiredresourceaccess-resource-type"></a><span data-ttu-id="f737a-105">tipo de recurso requiredResourceAccess</span><span class="sxs-lookup"><span data-stu-id="f737a-105">requiredResourceAccess resource type</span></span>

> <span data-ttu-id="f737a-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f737a-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f737a-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f737a-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f737a-108">Especifica el conjunto de OAuth 2.0 ámbitos de permisos y roles de la aplicación en el recurso especificado que una aplicación necesita tener acceso a.</span><span class="sxs-lookup"><span data-stu-id="f737a-108">Specifies the set of OAuth 2.0 permission scopes and app roles under the specified resource that an application requires access to.</span></span> <span data-ttu-id="f737a-109">Los ámbitos de permisos especificados OAuth 2.0 pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** ) cuando una llamada a una aplicación de recursos.</span><span class="sxs-lookup"><span data-stu-id="f737a-109">The specified OAuth 2.0 permission scopes may be requested by client applications (through the **requiredResourceAccess** collection) when calling a resource application.</span></span> <span data-ttu-id="f737a-110">La propiedad **requiredResourceAccess** de la entidad de la [aplicación](application.md) es una colección de **ReqiredResourceAccess**.</span><span class="sxs-lookup"><span data-stu-id="f737a-110">The **requiredResourceAccess** property of the [application](application.md) entity is a collection of **ReqiredResourceAccess**.</span></span>


## <a name="json-representation"></a><span data-ttu-id="f737a-111">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f737a-111">JSON representation</span></span>

<span data-ttu-id="f737a-112">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f737a-112">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.requiredResourceAccess"
}-->

```json
{
  "resourceAccess": [{"@odata.type": "microsoft.graph.resourceAccess"}],
  "resourceAppId": "string"
}

```
## <a name="properties"></a><span data-ttu-id="f737a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f737a-113">Properties</span></span>
| <span data-ttu-id="f737a-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f737a-114">Property</span></span>     | <span data-ttu-id="f737a-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="f737a-115">Type</span></span>   |<span data-ttu-id="f737a-116">Description</span><span class="sxs-lookup"><span data-stu-id="f737a-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f737a-117">resourceAccess</span><span class="sxs-lookup"><span data-stu-id="f737a-117">resourceAccess</span></span>|<span data-ttu-id="f737a-118">Colección de [ResourceAccess](resourceaccess.md)</span><span class="sxs-lookup"><span data-stu-id="f737a-118">[ResourceAccess](resourceaccess.md) collection</span></span>|<span data-ttu-id="f737a-119">La lista de ámbitos de OAuth2.0 de permisos y roles de la aplicación que requiere la aplicación desde el recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="f737a-119">The list of OAuth2.0 permission scopes and app roles that the application requires from the specified resource.</span></span>|
|<span data-ttu-id="f737a-120">resourceAppId</span><span class="sxs-lookup"><span data-stu-id="f737a-120">resourceAppId</span></span>|<span data-ttu-id="f737a-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="f737a-121">String</span></span>|<span data-ttu-id="f737a-122">El identificador único para el recurso que la aplicación necesita tener acceso a.</span><span class="sxs-lookup"><span data-stu-id="f737a-122">The unique identifier for the resource that the application requires access to.</span></span>  <span data-ttu-id="f737a-123">Debe ser igual que el **appId** declaradas en la aplicación de destino de recursos.</span><span class="sxs-lookup"><span data-stu-id="f737a-123">This should be equal to the **appId** declared on the target resource application.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "requiredResourceAccess resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

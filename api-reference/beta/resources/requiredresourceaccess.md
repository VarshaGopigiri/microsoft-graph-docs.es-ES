---
title: tipo de recurso requiredResourceAccess
description: Especifica el conjunto de OAuth 2.0 ámbitos de permisos y roles de la aplicación en el recurso especificado que una aplicación necesita tener acceso a. Los ámbitos de permisos especificados OAuth 2.0 pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** ) cuando una llamada a una aplicación de recursos. La propiedad **requiredResourceAccess** de la entidad de la aplicación es una colección de **ReqiredResourceAccess**.
ms.openlocfilehash: 937557f2f078ade1b336cfd00cd128d428d59cbb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089191"
---
# <a name="requiredresourceaccess-resource-type"></a><span data-ttu-id="5daba-105">tipo de recurso requiredResourceAccess</span><span class="sxs-lookup"><span data-stu-id="5daba-105">requiredResourceAccess resource type</span></span>

> <span data-ttu-id="5daba-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5daba-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5daba-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5daba-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5daba-108">Especifica el conjunto de OAuth 2.0 ámbitos de permisos y roles de la aplicación en el recurso especificado que una aplicación necesita tener acceso a.</span><span class="sxs-lookup"><span data-stu-id="5daba-108">Specifies the set of OAuth 2.0 permission scopes and app roles under the specified resource that an application requires access to.</span></span> <span data-ttu-id="5daba-109">Los ámbitos de permisos especificados OAuth 2.0 pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** ) cuando una llamada a una aplicación de recursos.</span><span class="sxs-lookup"><span data-stu-id="5daba-109">The specified OAuth 2.0 permission scopes may be requested by client applications (through the **requiredResourceAccess** collection) when calling a resource application.</span></span> <span data-ttu-id="5daba-110">La propiedad **requiredResourceAccess** de la entidad de la [aplicación](application.md) es una colección de **ReqiredResourceAccess**.</span><span class="sxs-lookup"><span data-stu-id="5daba-110">The **requiredResourceAccess** property of the [application](application.md) entity is a collection of **ReqiredResourceAccess**.</span></span>


## <a name="json-representation"></a><span data-ttu-id="5daba-111">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5daba-111">JSON representation</span></span>

<span data-ttu-id="5daba-112">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5daba-112">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="5daba-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5daba-113">Properties</span></span>
| <span data-ttu-id="5daba-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5daba-114">Property</span></span>     | <span data-ttu-id="5daba-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="5daba-115">Type</span></span>   |<span data-ttu-id="5daba-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5daba-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5daba-117">resourceAccess</span><span class="sxs-lookup"><span data-stu-id="5daba-117">resourceAccess</span></span>|<span data-ttu-id="5daba-118">Colección de [ResourceAccess](resourceaccess.md)</span><span class="sxs-lookup"><span data-stu-id="5daba-118">[ResourceAccess](resourceaccess.md) collection</span></span>|<span data-ttu-id="5daba-119">La lista de ámbitos de OAuth2.0 de permisos y roles de la aplicación que requiere la aplicación desde el recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="5daba-119">The list of OAuth2.0 permission scopes and app roles that the application requires from the specified resource.</span></span>|
|<span data-ttu-id="5daba-120">resourceAppId</span><span class="sxs-lookup"><span data-stu-id="5daba-120">resourceAppId</span></span>|<span data-ttu-id="5daba-121">String</span><span class="sxs-lookup"><span data-stu-id="5daba-121">String</span></span>|<span data-ttu-id="5daba-122">El identificador único para el recurso que la aplicación necesita tener acceso a.</span><span class="sxs-lookup"><span data-stu-id="5daba-122">The unique identifier for the resource that the application requires access to.</span></span>  <span data-ttu-id="5daba-123">Debe ser igual que el **appId** declaradas en la aplicación de destino de recursos.</span><span class="sxs-lookup"><span data-stu-id="5daba-123">This should be equal to the **appId** declared on the target resource application.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "requiredResourceAccess resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

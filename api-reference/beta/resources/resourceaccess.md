---
title: tipo de recurso resourceAccess
description: Especifica un ámbito de permiso OAuth 2.0 o una función de aplicación que requiere una aplicación. La propiedad **resourceAccess** del tipo requiredResourceAccess es una colección de **ResourceAccess**.
ms.openlocfilehash: 56e9b2b006d63d2a9abebc9e9585744b08438800
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088535"
---
# <a name="resourceaccess-resource-type"></a><span data-ttu-id="74d97-104">tipo de recurso resourceAccess</span><span class="sxs-lookup"><span data-stu-id="74d97-104">resourceAccess resource type</span></span>

> <span data-ttu-id="74d97-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="74d97-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="74d97-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="74d97-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="74d97-107">Especifica un ámbito de permiso OAuth 2.0 o una función de aplicación que requiere una aplicación.</span><span class="sxs-lookup"><span data-stu-id="74d97-107">Specifies an OAuth 2.0 permission scope or an app role that an application requires.</span></span> <span data-ttu-id="74d97-108">La propiedad **resourceAccess** del tipo [requiredResourceAccess](requiredresourceaccess.md) es una colección de **ResourceAccess**.</span><span class="sxs-lookup"><span data-stu-id="74d97-108">The **resourceAccess** property of the [requiredResourceAccess](requiredresourceaccess.md) type is a collection of **ResourceAccess**.</span></span>


## <a name="json-representation"></a><span data-ttu-id="74d97-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="74d97-109">JSON representation</span></span>

<span data-ttu-id="74d97-110">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="74d97-110">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.resourceAccess"
}-->

```json
{
  "id": "guid",
  "type": "string"
}

```
## <a name="properties"></a><span data-ttu-id="74d97-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="74d97-111">Properties</span></span>
| <span data-ttu-id="74d97-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="74d97-112">Property</span></span>     | <span data-ttu-id="74d97-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d97-113">Type</span></span>   |<span data-ttu-id="74d97-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="74d97-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="74d97-115">id</span><span class="sxs-lookup"><span data-stu-id="74d97-115">id</span></span>|<span data-ttu-id="74d97-116">Guid</span><span class="sxs-lookup"><span data-stu-id="74d97-116">Guid</span></span>|<span data-ttu-id="74d97-117">El identificador único para una de las instancias de [oAuth2Permission](oauth2permission.md) o [función de aplicación](approle.md) que expone la aplicación de recursos.</span><span class="sxs-lookup"><span data-stu-id="74d97-117">The unique identifier for one of the [oAuth2Permission](oauth2permission.md) or [appRole](approle.md) instances that the resource application exposes.</span></span>|
|<span data-ttu-id="74d97-118">type</span><span class="sxs-lookup"><span data-stu-id="74d97-118">type</span></span>|<span data-ttu-id="74d97-119">String</span><span class="sxs-lookup"><span data-stu-id="74d97-119">String</span></span>|<span data-ttu-id="74d97-120">Especifica si la propiedad **id** hace referencia a un [oAuth2Permission](oauth2permission.md) o una [función de aplicación](approle.md).</span><span class="sxs-lookup"><span data-stu-id="74d97-120">Specifies whether the **id** property references an [oAuth2Permission](oauth2permission.md) or an [appRole](approle.md).</span></span> <span data-ttu-id="74d97-121">Los valores posibles son "ámbito" o "role".</span><span class="sxs-lookup"><span data-stu-id="74d97-121">Possible values are "scope" or "role".</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resourceAccess resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

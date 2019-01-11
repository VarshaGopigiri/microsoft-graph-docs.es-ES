---
title: tipo de recurso appIdentity
description: Indica la identidad de la aplicación que realiza la acción o se ha cambiado. Incluye el identificador de aplicación, el nombre, el identificador de entidad de seguridad de servicio y el nombre. Se llama a este recurso por la API de directoryAudit
localization_priority: Normal
ms.openlocfilehash: ec61782fca0ab4004fab5a55bd4774c0d64afb3a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855786"
---
# <a name="appidentity-resource-type"></a><span data-ttu-id="a44e5-105">tipo de recurso appIdentity</span><span class="sxs-lookup"><span data-stu-id="a44e5-105">appIdentity resource type</span></span>
<span data-ttu-id="a44e5-106">Indica la identidad de la aplicación que realiza la acción o se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a44e5-106">Indicates the identity of the application that performed the action or was changed.</span></span> <span data-ttu-id="a44e5-107">Incluye el identificador de aplicación, el nombre, el identificador de entidad de seguridad de servicio y el nombre.</span><span class="sxs-lookup"><span data-stu-id="a44e5-107">Includes Application Id, Name, Service Principal ID and Name.</span></span> <span data-ttu-id="a44e5-108">Se llama a este recurso por la API [directoryAudit](../api/directoryaudit-get.md)</span><span class="sxs-lookup"><span data-stu-id="a44e5-108">This resource is called by the [directoryAudit](../api/directoryaudit-get.md) API</span></span>


## <a name="properties"></a><span data-ttu-id="a44e5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a44e5-109">Properties</span></span>
| <span data-ttu-id="a44e5-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a44e5-110">Property</span></span>     | <span data-ttu-id="a44e5-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a44e5-111">Type</span></span>   |<span data-ttu-id="a44e5-112">Description</span><span class="sxs-lookup"><span data-stu-id="a44e5-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a44e5-113">appId</span><span class="sxs-lookup"><span data-stu-id="a44e5-113">appId</span></span>|<span data-ttu-id="a44e5-114">cadena</span><span class="sxs-lookup"><span data-stu-id="a44e5-114">String</span></span>|<span data-ttu-id="a44e5-115">Hace referencia a los GUID único que representa el identificador de aplicación en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a44e5-115">Refers to the Unique GUID representing Application Id in the Azure Active Directory.</span></span>|
|<span data-ttu-id="a44e5-116">displayName</span><span class="sxs-lookup"><span data-stu-id="a44e5-116">displayName</span></span>|<span data-ttu-id="a44e5-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="a44e5-117">String</span></span>|<span data-ttu-id="a44e5-118">Hace referencia al nombre de la aplicación que se muestra en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="a44e5-118">Refers to the Application Name displayed in the Azure Portal.</span></span>|
|<span data-ttu-id="a44e5-119">servicePrincipalId</span><span class="sxs-lookup"><span data-stu-id="a44e5-119">servicePrincipalId</span></span>|<span data-ttu-id="a44e5-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="a44e5-120">String</span></span>|<span data-ttu-id="a44e5-121">Hace referencia a los GUID único que indica el identificador de entidad de seguridad de servicio en Azure Active Directory para la aplicación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a44e5-121">Refers to the Unique GUID indicating Service Principal Id in Azure Active Directory for the corresponding App.</span></span>|
|<span data-ttu-id="a44e5-122">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a44e5-122">servicePrincipalName</span></span>|<span data-ttu-id="a44e5-123">cadena</span><span class="sxs-lookup"><span data-stu-id="a44e5-123">String</span></span>|<span data-ttu-id="a44e5-124">Hace referencia al nombre Principal de servicio es el nombre de la aplicación en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="a44e5-124">Refers to the Service Principal Name is the Application name in the tenant.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a44e5-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a44e5-125">JSON representation</span></span>

<span data-ttu-id="a44e5-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a44e5-126">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.appIdentity"
}-->

```json
{
  "appId": "String",
  "displayName": "String",
  "servicePrincipalId": "String",
  "servicePrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "appIdentity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

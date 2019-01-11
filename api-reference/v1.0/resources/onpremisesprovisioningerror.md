---
title: tipo de recurso onPremisesProvisioningError
description: Representa los errores de sincronización de Active directory para las entidades de usuario y de grupo cuando la sincronización de directorios local para Azure Active Directory.
localization_priority: Normal
ms.openlocfilehash: c8989a78dfb60a6c7c25a66a9f1e619dcbdca15d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830670"
---
# <a name="onpremisesprovisioningerror-resource-type"></a><span data-ttu-id="1440b-103">tipo de recurso onPremisesProvisioningError</span><span class="sxs-lookup"><span data-stu-id="1440b-103">onPremisesProvisioningError resource type</span></span>

<span data-ttu-id="1440b-104">Representa los errores de sincronización de Active directory para las entidades de [usuario](user.md) y de [grupo](group.md) cuando sincronización local de directorios en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1440b-104">Represents directory synchronization errors for the [user](user.md) and [group](group.md) entities when synchronizing on-premises directories to Azure Active Directory.</span></span>

## <a name="properties"></a><span data-ttu-id="1440b-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1440b-105">Properties</span></span>

| <span data-ttu-id="1440b-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1440b-106">Property</span></span> | <span data-ttu-id="1440b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1440b-107">Type</span></span> | <span data-ttu-id="1440b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1440b-108">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="1440b-109">categoría</span><span class="sxs-lookup"><span data-stu-id="1440b-109">category</span></span>|<span data-ttu-id="1440b-110">String</span><span class="sxs-lookup"><span data-stu-id="1440b-110">String</span></span>| <span data-ttu-id="1440b-111">Categoría del error de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="1440b-111">Category of the provisioning error.</span></span> <span data-ttu-id="1440b-112">Nota: Actualmente, hay un único valor posible.</span><span class="sxs-lookup"><span data-stu-id="1440b-112">Note: Currently, there is only one possible value.</span></span> <span data-ttu-id="1440b-113">Valor posible: *PropertyConflict* - indica un valor de propiedad no es único.</span><span class="sxs-lookup"><span data-stu-id="1440b-113">Possible value: *PropertyConflict* - indicates a property value is not unique.</span></span> <span data-ttu-id="1440b-114">Otros objetos contienen el mismo valor para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1440b-114">Other objects contain the same value for the property.</span></span> |
|<span data-ttu-id="1440b-115">occurredDateTime</span><span class="sxs-lookup"><span data-stu-id="1440b-115">occurredDateTime</span></span>|<span data-ttu-id="1440b-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1440b-116">DateTimeOffset</span></span>| <span data-ttu-id="1440b-117">La fecha y la hora a la que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="1440b-117">The date and time at which the error occurred.</span></span> |
|<span data-ttu-id="1440b-118">propertyCausingError</span><span class="sxs-lookup"><span data-stu-id="1440b-118">propertyCausingError</span></span>|<span data-ttu-id="1440b-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="1440b-119">String</span></span>| <span data-ttu-id="1440b-120">Nombre de la propiedad de Active directory que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="1440b-120">Name of the directory property causing the error.</span></span> <span data-ttu-id="1440b-121">Los valores posibles actuales: *UserPrincipalName* o *ProxyAddress*</span><span class="sxs-lookup"><span data-stu-id="1440b-121">Current possible values: *UserPrincipalName* or *ProxyAddress*</span></span> |
|<span data-ttu-id="1440b-122">valor</span><span class="sxs-lookup"><span data-stu-id="1440b-122">value</span></span>|<span data-ttu-id="1440b-123">String</span><span class="sxs-lookup"><span data-stu-id="1440b-123">String</span></span>| <span data-ttu-id="1440b-124">Valor de la propiedad que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="1440b-124">Value of the property causing the error.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="1440b-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1440b-125">JSON representation</span></span>
<span data-ttu-id="1440b-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1440b-126">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesProvisioningError"
}-->

```json
{
  "category": "String",
  "occurredDateTime": "String (timestamp)",
  "propertyCausingError": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesProvisioningError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

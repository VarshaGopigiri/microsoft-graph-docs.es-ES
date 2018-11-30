---
title: tipo de recurso onPremisesProvisioningError
description: Representa los errores de sincronización de Active directory para el usuario, grupo o entidades organizativas de contacto cuando sincronización local de directorios en Azure Active Directory.
ms.openlocfilehash: 9fa7850d39c9f7a490135a127938fc7fae30b6f3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085790"
---
# <a name="onpremisesprovisioningerror-resource-type"></a><span data-ttu-id="6d0f1-103">tipo de recurso onPremisesProvisioningError</span><span class="sxs-lookup"><span data-stu-id="6d0f1-103">onPremisesProvisioningError resource type</span></span>

> <span data-ttu-id="6d0f1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6d0f1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6d0f1-106">Representa los errores de sincronización de Active directory para las entidades de [usuario](user.md), [grupo](group.md)o [contacto organizativa](orgcontact.md) cuando sincronización local de directorios en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-106">Represents directory synchronization errors for the [user](user.md), [group](group.md), or [organizational contact](orgcontact.md) entities when synchronizing on-premises directories to Azure Active Directory.</span></span>

## <a name="properties"></a><span data-ttu-id="6d0f1-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6d0f1-107">Properties</span></span>

| <span data-ttu-id="6d0f1-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6d0f1-108">Property</span></span> | <span data-ttu-id="6d0f1-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d0f1-109">Type</span></span> | <span data-ttu-id="6d0f1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d0f1-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="6d0f1-111">categoría</span><span class="sxs-lookup"><span data-stu-id="6d0f1-111">category</span></span>|<span data-ttu-id="6d0f1-112">String</span><span class="sxs-lookup"><span data-stu-id="6d0f1-112">String</span></span>| <span data-ttu-id="6d0f1-113">Categoría del error de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-113">Category of the provisioning error.</span></span> <span data-ttu-id="6d0f1-114">Nota: Actualmente, hay un único valor posible.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-114">Note: Currently, there is only one possible value.</span></span> <span data-ttu-id="6d0f1-115">Valor posible: *PropertyConflict* - indica un valor de propiedad no es único.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-115">Possible value: *PropertyConflict* - indicates a property value is not unique.</span></span> <span data-ttu-id="6d0f1-116">Otros objetos contienen el mismo valor para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-116">Other objects contain the same value for the property.</span></span> |
|<span data-ttu-id="6d0f1-117">occurredDateTime</span><span class="sxs-lookup"><span data-stu-id="6d0f1-117">occurredDateTime</span></span>|<span data-ttu-id="6d0f1-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6d0f1-118">DateTimeOffset</span></span>| <span data-ttu-id="6d0f1-119">La fecha y la hora a la que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-119">The date and time at which the error occurred.</span></span> |
|<span data-ttu-id="6d0f1-120">propertyCausingError</span><span class="sxs-lookup"><span data-stu-id="6d0f1-120">propertyCausingError</span></span>|<span data-ttu-id="6d0f1-121">String</span><span class="sxs-lookup"><span data-stu-id="6d0f1-121">String</span></span>| <span data-ttu-id="6d0f1-122">Nombre de la propiedad de Active directory que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-122">Name of the directory property causing the error.</span></span> <span data-ttu-id="6d0f1-123">Los valores posibles actuales: *UserPrincipalName* o *ProxyAddress*</span><span class="sxs-lookup"><span data-stu-id="6d0f1-123">Current possible values: *UserPrincipalName* or *ProxyAddress*</span></span> |
|<span data-ttu-id="6d0f1-124">valor</span><span class="sxs-lookup"><span data-stu-id="6d0f1-124">value</span></span>|<span data-ttu-id="6d0f1-125">String</span><span class="sxs-lookup"><span data-stu-id="6d0f1-125">String</span></span>| <span data-ttu-id="6d0f1-126">Valor de la propiedad que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-126">Value of the property causing the error.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="6d0f1-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6d0f1-127">JSON representation</span></span>
<span data-ttu-id="6d0f1-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-128">Here is a JSON representation of the resource.</span></span>

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
---
title: tipo de recurso educationIdentityMatchingOptions
description: Proporciona una asignación entre una propiedad de origen y una propiedad de destino para que coincidan con las cuentas de usuario. La propiedad source debe existir en el origen de datos. La propiedad de destino debe ser una propiedad válida en Azure Active Directory (AD Azure).
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 624e2717387c5cc8994596fd83d5a6856ac6082b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978259"
---
# <a name="educationidentitymatchingoptions-resource-type"></a><span data-ttu-id="8ffc4-105">tipo de recurso educationIdentityMatchingOptions</span><span class="sxs-lookup"><span data-stu-id="8ffc4-105">educationIdentityMatchingOptions resource type</span></span>

> <span data-ttu-id="8ffc4-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8ffc4-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8ffc4-108">Proporciona una asignación entre una propiedad de origen y una propiedad de destino para que coincidan con las cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-108">Provides a mapping between a source property and a target property for matching user accounts.</span></span> <span data-ttu-id="8ffc4-109">La propiedad source debe existir en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-109">The source property should exist in the source data.</span></span> <span data-ttu-id="8ffc4-110">La propiedad de destino debe ser una propiedad válida en Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="8ffc4-110">The target property should be a valid property in Azure Active Directory (Azure AD).</span></span>

## <a name="properties"></a><span data-ttu-id="8ffc4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ffc4-111">Properties</span></span>

| <span data-ttu-id="8ffc4-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ffc4-112">Property</span></span> | <span data-ttu-id="8ffc4-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ffc4-113">Type</span></span> | <span data-ttu-id="8ffc4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ffc4-114">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="8ffc4-115">**appliesTo**</span><span class="sxs-lookup"><span data-stu-id="8ffc4-115">**appliesTo**</span></span> | <span data-ttu-id="8ffc4-116">string</span><span class="sxs-lookup"><span data-stu-id="8ffc4-116">string</span></span> |  <span data-ttu-id="8ffc4-117">El tipo de función de usuario para asignar a la licencia.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-117">The user role type to assign to the license.</span></span> <span data-ttu-id="8ffc4-118">Los valores posibles son: `student` y `teacher`.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-118">Possible values are: `student`, `teacher`.</span></span>      |
| <span data-ttu-id="8ffc4-119">**sourcePropertyName**</span><span class="sxs-lookup"><span data-stu-id="8ffc4-119">**sourcePropertyName**</span></span> | <span data-ttu-id="8ffc4-120">string</span><span class="sxs-lookup"><span data-stu-id="8ffc4-120">string</span></span> |  <span data-ttu-id="8ffc4-121">El nombre de la propiedad source, que debe ser un nombre de campo en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-121">The name of the source property, which should be a field name in the source data.</span></span> <span data-ttu-id="8ffc4-122">Esta propiedad distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-122">This property is case-sensitive.</span></span>        |
| <span data-ttu-id="8ffc4-123">**targetPropertyName**</span><span class="sxs-lookup"><span data-stu-id="8ffc4-123">**targetPropertyName**</span></span> | <span data-ttu-id="8ffc4-124">string</span><span class="sxs-lookup"><span data-stu-id="8ffc4-124">string</span></span> |  <span data-ttu-id="8ffc4-125">El nombre de la propiedad de destino, que debe ser una propiedad válida en Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-125">The name of the target property, which should be a valid property in Azure AD.</span></span> <span data-ttu-id="8ffc4-126">Esta propiedad distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-126">This property is case-sensitive.</span></span>     |
| <span data-ttu-id="8ffc4-127">**targetDomain**</span><span class="sxs-lookup"><span data-stu-id="8ffc4-127">**targetDomain**</span></span> | <span data-ttu-id="8ffc4-128">string</span><span class="sxs-lookup"><span data-stu-id="8ffc4-128">string</span></span> |  <span data-ttu-id="8ffc4-129">El dominio en sufijo con la propiedad de origen para que coincidan en el destino.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-129">The domain to suffix with the source property to match on the target.</span></span> <span data-ttu-id="8ffc4-130">Si se proporciona como null, la propiedad source se usará para hacer coincidir con la propiedad de destino.</span><span class="sxs-lookup"><span data-stu-id="8ffc4-130">If provided as null,  the source property will be used to match with the target property.</span></span>        |

## <a name="json-representation"></a><span data-ttu-id="8ffc4-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8ffc4-131">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationIdentityMatchingOptions"
}-->

```json
{
    "appliesTo": {"@odata.type": "#microsoft.graph.educationUserRole"},
    "sourcePropertyName": "String",
    "targetPropertyName": "String",
    "targetDomain": "String"
}
```

---
title: tipo de recurso educationIdentityMatchingOptions
description: Proporciona una asignación entre una propiedad de origen y una propiedad de destino para que coincidan con las cuentas de usuario. La propiedad source debe existir en el origen de datos. La propiedad de destino debe ser una propiedad válida en Azure Active Directory (AD Azure).
ms.openlocfilehash: 2cabb255648f4089d437912a97bb7d29ff286779
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088550"
---
# <a name="educationidentitymatchingoptions-resource-type"></a><span data-ttu-id="4374a-105">tipo de recurso educationIdentityMatchingOptions</span><span class="sxs-lookup"><span data-stu-id="4374a-105">educationIdentityMatchingOptions resource type</span></span>

> <span data-ttu-id="4374a-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4374a-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4374a-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4374a-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4374a-108">Proporciona una asignación entre una propiedad de origen y una propiedad de destino para que coincidan con las cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="4374a-108">Provides a mapping between a source property and a target property for matching user accounts.</span></span> <span data-ttu-id="4374a-109">La propiedad source debe existir en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="4374a-109">The source property should exist in the source data.</span></span> <span data-ttu-id="4374a-110">La propiedad de destino debe ser una propiedad válida en Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="4374a-110">The target property should be a valid property in Azure Active Directory (Azure AD).</span></span>

## <a name="properties"></a><span data-ttu-id="4374a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4374a-111">Properties</span></span>

| <span data-ttu-id="4374a-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4374a-112">Property</span></span> | <span data-ttu-id="4374a-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="4374a-113">Type</span></span> | <span data-ttu-id="4374a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4374a-114">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="4374a-115">**appliesTo**</span><span class="sxs-lookup"><span data-stu-id="4374a-115">**appliesTo**</span></span> | <span data-ttu-id="4374a-116">string</span><span class="sxs-lookup"><span data-stu-id="4374a-116">string</span></span> |  <span data-ttu-id="4374a-117">El tipo de función de usuario para asignar a la licencia.</span><span class="sxs-lookup"><span data-stu-id="4374a-117">The user role type to assign to the license.</span></span> <span data-ttu-id="4374a-118">Los valores posibles son: `student` y `teacher`.</span><span class="sxs-lookup"><span data-stu-id="4374a-118">Possible values are: `student`, `teacher`.</span></span>      |
| <span data-ttu-id="4374a-119">**sourcePropertyName**</span><span class="sxs-lookup"><span data-stu-id="4374a-119">**sourcePropertyName**</span></span> | <span data-ttu-id="4374a-120">string</span><span class="sxs-lookup"><span data-stu-id="4374a-120">string</span></span> |  <span data-ttu-id="4374a-121">El nombre de la propiedad source, que debe ser un nombre de campo en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="4374a-121">The name of the source property, which should be a field name in the source data.</span></span> <span data-ttu-id="4374a-122">Esta propiedad distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4374a-122">This property is case-sensitive.</span></span>        |
| <span data-ttu-id="4374a-123">**targetPropertyName**</span><span class="sxs-lookup"><span data-stu-id="4374a-123">**targetPropertyName**</span></span> | <span data-ttu-id="4374a-124">string</span><span class="sxs-lookup"><span data-stu-id="4374a-124">string</span></span> |  <span data-ttu-id="4374a-125">El nombre de la propiedad de destino, que debe ser una propiedad válida en Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4374a-125">The name of the target property, which should be a valid property in Azure AD.</span></span> <span data-ttu-id="4374a-126">Esta propiedad distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4374a-126">This property is case-sensitive.</span></span>     |
| <span data-ttu-id="4374a-127">**targetDomain**</span><span class="sxs-lookup"><span data-stu-id="4374a-127">**targetDomain**</span></span> | <span data-ttu-id="4374a-128">string</span><span class="sxs-lookup"><span data-stu-id="4374a-128">string</span></span> |  <span data-ttu-id="4374a-129">El dominio en sufijo con la propiedad de origen para que coincidan en el destino.</span><span class="sxs-lookup"><span data-stu-id="4374a-129">The domain to suffix with the source property to match on the target.</span></span> <span data-ttu-id="4374a-130">Si se proporciona como null, la propiedad source se usará para hacer coincidir con la propiedad de destino.</span><span class="sxs-lookup"><span data-stu-id="4374a-130">If provided as null,  the source property will be used to match with the target property.</span></span>        |

## <a name="json-representation"></a><span data-ttu-id="4374a-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4374a-131">JSON representation</span></span>
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

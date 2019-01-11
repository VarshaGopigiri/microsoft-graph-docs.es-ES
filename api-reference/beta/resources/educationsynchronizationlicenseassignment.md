---
title: tipo de recurso educationSynchronizationLicenseAssignment
description: Representa la información de licencia para asignar a las cuentas de usuario. El recurso se usará para configurar asignaciones de licencias al crear nuevas cuentas de usuario.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 9100ba799c8981d5defdd74d6346a66859b2d53e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804911"
---
# <a name="educationsynchronizationlicenseassignment-resource-type"></a><span data-ttu-id="eb238-104">tipo de recurso educationSynchronizationLicenseAssignment</span><span class="sxs-lookup"><span data-stu-id="eb238-104">educationSynchronizationLicenseAssignment resource type</span></span>

> <span data-ttu-id="eb238-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eb238-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eb238-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eb238-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eb238-107">Representa la información de licencia para asignar a las cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="eb238-107">Represents the license information to assign to user accounts.</span></span> <span data-ttu-id="eb238-108">El recurso se usará para configurar asignaciones de licencias al crear nuevas cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="eb238-108">The resource will be used to set up license assignments when creating new user accounts.</span></span>

## <a name="properties"></a><span data-ttu-id="eb238-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb238-109">Properties</span></span>

| <span data-ttu-id="eb238-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eb238-110">Property</span></span> | <span data-ttu-id="eb238-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb238-111">Type</span></span> | <span data-ttu-id="eb238-112">Description</span><span class="sxs-lookup"><span data-stu-id="eb238-112">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="eb238-113">**appliesTo**</span><span class="sxs-lookup"><span data-stu-id="eb238-113">**appliesTo**</span></span> | <span data-ttu-id="eb238-114">string</span><span class="sxs-lookup"><span data-stu-id="eb238-114">string</span></span> | <span data-ttu-id="eb238-115">El tipo de función de usuario para asignar a la licencia.</span><span class="sxs-lookup"><span data-stu-id="eb238-115">The user role type to assign to license.</span></span> <span data-ttu-id="eb238-116">Los valores posibles son: `student` y `teacher`.</span><span class="sxs-lookup"><span data-stu-id="eb238-116">Possible values are: `student`, `teacher`.</span></span>         |
| <span data-ttu-id="eb238-117">**skuIds**</span><span class="sxs-lookup"><span data-stu-id="eb238-117">**skuIds**</span></span> | <span data-ttu-id="eb238-118">colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="eb238-118">collection of strings</span></span> |  <span data-ttu-id="eb238-119">Representa los identificadores SKU de las licencias para asignar.</span><span class="sxs-lookup"><span data-stu-id="eb238-119">Represents the SKU identifiers of the licenses to assign.</span></span>        |

## <a name="json-representation"></a><span data-ttu-id="eb238-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eb238-120">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationLicenseAssignment"
}-->

```json
{
    "appliesTo": {"@odata.type": "#microsoft.graph.educationUserRole"},
    "skuIds": ["String"]
}
```

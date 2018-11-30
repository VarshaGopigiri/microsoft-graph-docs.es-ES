---
title: insightIdentity
description: " tipo de recurso"
ms.openlocfilehash: e13d08eb111844896c96b02ab22c52d2f598ce58
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087751"
---
# <a name="insightidentity"></a><span data-ttu-id="b051d-103">insightIdentity</span><span class="sxs-lookup"><span data-stu-id="b051d-103">insightIdentity</span></span>

> <span data-ttu-id="b051d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b051d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b051d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b051d-105">Use of these APIs in production applications is not supported.</span></span>

 <span data-ttu-id="b051d-106">tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="b051d-106">resource type</span></span>

<span data-ttu-id="b051d-107">Tipo complejo que contiene las propiedades de los elementos [compartidos](insights-shared.md) .</span><span class="sxs-lookup"><span data-stu-id="b051d-107">Complex type containing properties of [Shared](insights-shared.md) items.</span></span> 

## <a name="json-representation"></a><span data-ttu-id="b051d-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b051d-108">JSON representation</span></span>
<span data-ttu-id="b051d-109">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b051d-109">Here is a JSON representation of the resource</span></span>

```json
{
  "displayName": "string",
  "id": "string",
  "address": "string"
}
```

## <a name="properties"></a><span data-ttu-id="b051d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b051d-110">Properties</span></span>

| <span data-ttu-id="b051d-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b051d-111">Property</span></span>              | <span data-ttu-id="b051d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="b051d-112">Type</span></span>          | <span data-ttu-id="b051d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b051d-113">Description</span></span>  |
| -------------         |-----------    | -------------|
| <span data-ttu-id="b051d-114">displayName</span><span class="sxs-lookup"><span data-stu-id="b051d-114">displayName</span></span>       | <span data-ttu-id="b051d-115">String</span><span class="sxs-lookup"><span data-stu-id="b051d-115">String</span></span>          | <span data-ttu-id="b051d-116">El nombre para mostrar del usuario que comparte el elemento.</span><span class="sxs-lookup"><span data-stu-id="b051d-116">The display name of the user who shared the item.</span></span> |
| <span data-ttu-id="b051d-117">id</span><span class="sxs-lookup"><span data-stu-id="b051d-117">id</span></span>              | <span data-ttu-id="b051d-118">String</span><span class="sxs-lookup"><span data-stu-id="b051d-118">String</span></span>        | <span data-ttu-id="b051d-119">El identificador del usuario que comparte el elemento.</span><span class="sxs-lookup"><span data-stu-id="b051d-119">The id of the user who shared the item.</span></span>     |
| <span data-ttu-id="b051d-120">address</span><span class="sxs-lookup"><span data-stu-id="b051d-120">address</span></span>             | <span data-ttu-id="b051d-121">String</span><span class="sxs-lookup"><span data-stu-id="b051d-121">String</span></span>      | <span data-ttu-id="b051d-122">La dirección de correo electrónico del usuario que comparte el elemento.</span><span class="sxs-lookup"><span data-stu-id="b051d-122">The email address of the user who shared the item.</span></span>  |
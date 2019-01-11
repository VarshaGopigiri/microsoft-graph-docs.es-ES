---
title: tipo de recurso governancePermission
description: 'Representa el permiso de acceso que tiene un governanceSubject para un governanceResource específica.  '
localization_priority: Normal
ms.openlocfilehash: e082ca50e5642e865b3e30859eea607df63a03b4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882877"
---
# <a name="governancepermission-resource-type"></a><span data-ttu-id="d7d75-103">tipo de recurso governancePermission</span><span class="sxs-lookup"><span data-stu-id="d7d75-103">governancePermission resource type</span></span>

> <span data-ttu-id="d7d75-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7d75-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7d75-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7d75-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d7d75-106">Representa el permiso de acceso que tiene un [governanceSubject](../resources/governancesubject.md) para un específico [governanceResource](../resources/governanceresource.md).</span><span class="sxs-lookup"><span data-stu-id="d7d75-106">Represents the access permission that a [governanceSubject](../resources/governancesubject.md) has to a specific [governanceResource](../resources/governanceresource.md).</span></span>  


## <a name="properties"></a><span data-ttu-id="d7d75-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d7d75-107">Properties</span></span>
| <span data-ttu-id="d7d75-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7d75-108">Property</span></span>     | <span data-ttu-id="d7d75-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7d75-109">Type</span></span>   |<span data-ttu-id="d7d75-110">Description</span><span class="sxs-lookup"><span data-stu-id="d7d75-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d7d75-111">accessLevel</span><span class="sxs-lookup"><span data-stu-id="d7d75-111">accessLevel</span></span>|<span data-ttu-id="d7d75-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7d75-112">String</span></span>|<span data-ttu-id="d7d75-113">El nivel de acceso.</span><span class="sxs-lookup"><span data-stu-id="d7d75-113">The access level.</span></span> <span data-ttu-id="d7d75-114">Valores válidos: ``None``, ``UserRead``, ``AdminRead``, y ``AdminReadWrite``.</span><span class="sxs-lookup"><span data-stu-id="d7d75-114">Valid values: ``None``, ``UserRead``, ``AdminRead``, and ``AdminReadWrite``.</span></span>|
|<span data-ttu-id="d7d75-115">isActive</span><span class="sxs-lookup"><span data-stu-id="d7d75-115">isActive</span></span>|<span data-ttu-id="d7d75-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="d7d75-116">Boolean</span></span>|<span data-ttu-id="d7d75-117">Indicar si el solicitante tiene cualquier asignación de rol activo para el nivel de acceso.</span><span class="sxs-lookup"><span data-stu-id="d7d75-117">Indicate if the the requestor has any active role assignment for the access level.</span></span>|
|<span data-ttu-id="d7d75-118">isEligible</span><span class="sxs-lookup"><span data-stu-id="d7d75-118">isEligible</span></span>|<span data-ttu-id="d7d75-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="d7d75-119">Boolean</span></span>|<span data-ttu-id="d7d75-120">Indicar si el solicitante no tiene ninguna asignación de roles aptos para el nivel de acceso.</span><span class="sxs-lookup"><span data-stu-id="d7d75-120">Indicate if the requestor has any eligible role assignment for the access level.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d7d75-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d7d75-121">JSON representation</span></span>

<span data-ttu-id="d7d75-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d7d75-122">Here is a JSON representation of the resource.</span></span>

```json
{
  "accessLevel": "String",
  "isActive": true,
  "isEligible": true
}

```

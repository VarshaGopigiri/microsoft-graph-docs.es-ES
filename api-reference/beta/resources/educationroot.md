---
title: Tipo de recurso educationRoot
description: 'El espacio de nombres `/education` expone funcionalidad específica del sector educativo. '
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: e610ca79dcef29d85a9190c9d3d9429cbf3b363d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949657"
---
# <a name="educationroot-resource-type"></a><span data-ttu-id="2e7eb-103">Tipo de recurso educationRoot</span><span class="sxs-lookup"><span data-stu-id="2e7eb-103">educationRoot resource type</span></span>

> <span data-ttu-id="2e7eb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2e7eb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2e7eb-106">El espacio de nombres `/education` expone funcionalidad específica del sector educativo.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-106">The `/education` namespace exposes functionality that is specific to the education sector.</span></span> <span data-ttu-id="2e7eb-107">Algunos objetos del espacio de nombres `/education` pueden encontrarse en otras partes de Microsoft Graph (por ejemplo, [users](user.md)).</span><span class="sxs-lookup"><span data-stu-id="2e7eb-107">Some objects in the `/education` namespace can be found in other parts of Microsoft Graph (for example, [users](user.md)).</span></span> <span data-ttu-id="2e7eb-108">El espacio de nombres de educación ofrece características y propiedades específicas del ámbito educativo en esos objetos.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-108">The education namespace provides education-specific properties and features on these objects.</span></span>

## <a name="methods"></a><span data-ttu-id="2e7eb-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e7eb-109">Methods</span></span>

| <span data-ttu-id="2e7eb-110">Método</span><span class="sxs-lookup"><span data-stu-id="2e7eb-110">Method</span></span>           | <span data-ttu-id="2e7eb-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e7eb-111">Return Type</span></span>    |<span data-ttu-id="2e7eb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e7eb-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="2e7eb-113">Crear educationClass</span><span class="sxs-lookup"><span data-stu-id="2e7eb-113">Create educationClass</span></span>](../api/educationroot-post-classes.md) |[<span data-ttu-id="2e7eb-114">educationClass</span><span class="sxs-lookup"><span data-stu-id="2e7eb-114">educationClass</span></span>](educationclass.md)| <span data-ttu-id="2e7eb-115">Cree un objeto **educationClass** publicando en la colección de clases.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-115">Create a new **educationClass** by posting to the classes collection.</span></span>|
|[<span data-ttu-id="2e7eb-116">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="2e7eb-116">List classes</span></span>](../api/educationroot-list-classes.md) |<span data-ttu-id="2e7eb-117">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="2e7eb-117">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="2e7eb-118">Obtenga una colección de objetos **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-118">Get an **educationClass** object collection.</span></span>|
|[<span data-ttu-id="2e7eb-119">Crear educationSchool</span><span class="sxs-lookup"><span data-stu-id="2e7eb-119">Create educationSchool</span></span>](../api/educationroot-post-schools.md) |[<span data-ttu-id="2e7eb-120">educationSchool</span><span class="sxs-lookup"><span data-stu-id="2e7eb-120">educationSchool</span></span>](educationschool.md)| <span data-ttu-id="2e7eb-121">Cree un objeto **educationSchool** publicando en la colección de centros educativos.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-121">Create a new **educationSchool** by posting to the schools collection.</span></span>|
|[<span data-ttu-id="2e7eb-122">Enumerar centros educativos</span><span class="sxs-lookup"><span data-stu-id="2e7eb-122">List schools</span></span>](../api/educationroot-list-schools.md) |<span data-ttu-id="2e7eb-123">Colección [educationSchool](educationschool.md)</span><span class="sxs-lookup"><span data-stu-id="2e7eb-123">[educationSchool](educationschool.md) collection</span></span>| <span data-ttu-id="2e7eb-124">Obtenga una colección de objetos **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-124">Get an **educationSchool** object collection.</span></span>|
|[<span data-ttu-id="2e7eb-125">Crear educationUser</span><span class="sxs-lookup"><span data-stu-id="2e7eb-125">Create educationUser</span></span>](../api/educationroot-post-users.md) |[<span data-ttu-id="2e7eb-126">educationUser</span><span class="sxs-lookup"><span data-stu-id="2e7eb-126">educationUser</span></span>](educationuser.md)| <span data-ttu-id="2e7eb-127">Cree un objeto **educationUser** publicando en la colección de usuarios.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-127">Create a new **educationUser** by posting to the users collection.</span></span>|
|[<span data-ttu-id="2e7eb-128">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="2e7eb-128">List users</span></span>](../api/educationroot-list-users.md) |<span data-ttu-id="2e7eb-129">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="2e7eb-129">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="2e7eb-130">Obtenga una colección de objetos **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-130">Get an **educationUser** object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="2e7eb-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2e7eb-131">Properties</span></span>
<span data-ttu-id="2e7eb-132">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-132">None.</span></span>

## <a name="relationships"></a><span data-ttu-id="2e7eb-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2e7eb-133">Relationships</span></span>
| <span data-ttu-id="2e7eb-134">Relación</span><span class="sxs-lookup"><span data-stu-id="2e7eb-134">Relationship</span></span> | <span data-ttu-id="2e7eb-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="2e7eb-135">Type</span></span>   |<span data-ttu-id="2e7eb-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e7eb-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2e7eb-137">classes</span><span class="sxs-lookup"><span data-stu-id="2e7eb-137">classes</span></span>|<span data-ttu-id="2e7eb-138">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="2e7eb-138">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="2e7eb-p103">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-p103">Read-only. Nullable.</span></span>|
|<span data-ttu-id="2e7eb-141">me</span><span class="sxs-lookup"><span data-stu-id="2e7eb-141">me</span></span>|[<span data-ttu-id="2e7eb-142">educationUser</span><span class="sxs-lookup"><span data-stu-id="2e7eb-142">educationUser</span></span>](educationuser.md)| <span data-ttu-id="2e7eb-p104">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-p104">Read-only. Nullable.</span></span>|
|<span data-ttu-id="2e7eb-145">schools</span><span class="sxs-lookup"><span data-stu-id="2e7eb-145">schools</span></span>|<span data-ttu-id="2e7eb-146">Colección [educationSchool](educationschool.md)</span><span class="sxs-lookup"><span data-stu-id="2e7eb-146">[educationSchool](educationschool.md) collection</span></span>| <span data-ttu-id="2e7eb-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-p105">Read-only. Nullable.</span></span>|
|<span data-ttu-id="2e7eb-149">users</span><span class="sxs-lookup"><span data-stu-id="2e7eb-149">users</span></span>|<span data-ttu-id="2e7eb-150">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="2e7eb-150">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="2e7eb-p106">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2e7eb-p106">Read-only. Nullable.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationRoot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

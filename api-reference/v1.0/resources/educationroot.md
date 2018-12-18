---
title: Tipo de recurso educationRoot
description: 'El espacio de nombres `/education` expone funcionalidad específica del sector educativo. '
author: mmast-msft
ms.openlocfilehash: 11aaaec20ccd688b16b74224d1a8c6937e52c5cd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27342472"
---
# <a name="educationroot-resource-type"></a><span data-ttu-id="25beb-103">Tipo de recurso educationRoot</span><span class="sxs-lookup"><span data-stu-id="25beb-103">educationRoot resource type</span></span>

<span data-ttu-id="25beb-104">El espacio de nombres `/education` expone funcionalidad específica del sector educativo.</span><span class="sxs-lookup"><span data-stu-id="25beb-104">The `/education` namespace exposes functionality that is specific to the education sector.</span></span> <span data-ttu-id="25beb-105">Algunos objetos del espacio de nombres `/education` pueden encontrarse en otras partes de Microsoft Graph (por ejemplo, [users](user.md)).</span><span class="sxs-lookup"><span data-stu-id="25beb-105">Some objects in the `/education` namespace can be found in other parts of Microsoft Graph (for example, [users](user.md)).</span></span> <span data-ttu-id="25beb-106">El espacio de nombres de educación ofrece características y propiedades específicas del ámbito educativo en esos objetos.</span><span class="sxs-lookup"><span data-stu-id="25beb-106">The education namespace provides education-specific properties and features on these objects.</span></span>

## <a name="methods"></a><span data-ttu-id="25beb-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="25beb-107">Methods</span></span>

| <span data-ttu-id="25beb-108">Método</span><span class="sxs-lookup"><span data-stu-id="25beb-108">Method</span></span>           | <span data-ttu-id="25beb-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25beb-109">Return Type</span></span>    |<span data-ttu-id="25beb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="25beb-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="25beb-111">Crear educationClass</span><span class="sxs-lookup"><span data-stu-id="25beb-111">Create educationClass</span></span>](../api/educationroot-post-classes.md) |[<span data-ttu-id="25beb-112">educationClass</span><span class="sxs-lookup"><span data-stu-id="25beb-112">educationClass</span></span>](educationclass.md)| <span data-ttu-id="25beb-113">Cree un objeto **educationClass** publicando en la colección de clases.</span><span class="sxs-lookup"><span data-stu-id="25beb-113">Create a new **educationClass** by posting to the classes collection.</span></span>|
|[<span data-ttu-id="25beb-114">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="25beb-114">List classes</span></span>](../api/educationroot-list-classes.md) |<span data-ttu-id="25beb-115">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="25beb-115">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="25beb-116">Obtenga una colección de objetos **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="25beb-116">Get an **educationClass** object collection.</span></span>|
|[<span data-ttu-id="25beb-117">Crear educationSchool</span><span class="sxs-lookup"><span data-stu-id="25beb-117">Create educationSchool</span></span>](../api/educationroot-post-schools.md) |[<span data-ttu-id="25beb-118">educationSchool</span><span class="sxs-lookup"><span data-stu-id="25beb-118">educationSchool</span></span>](educationschool.md)| <span data-ttu-id="25beb-119">Cree un objeto **educationSchool** publicando en la colección de centros educativos.</span><span class="sxs-lookup"><span data-stu-id="25beb-119">Create a new **educationSchool** by posting to the schools collection.</span></span>|
|[<span data-ttu-id="25beb-120">Enumerar centros educativos</span><span class="sxs-lookup"><span data-stu-id="25beb-120">List schools</span></span>](../api/educationroot-list-schools.md) |<span data-ttu-id="25beb-121">Colección [educationSchool](educationschool.md)</span><span class="sxs-lookup"><span data-stu-id="25beb-121">[educationSchool](educationschool.md) collection</span></span>| <span data-ttu-id="25beb-122">Obtenga una colección de objetos **educationSchool**.</span><span class="sxs-lookup"><span data-stu-id="25beb-122">Get an **educationSchool** object collection.</span></span>|
|[<span data-ttu-id="25beb-123">Crear educationUser</span><span class="sxs-lookup"><span data-stu-id="25beb-123">Create educationUser</span></span>](../api/educationroot-post-users.md) |[<span data-ttu-id="25beb-124">educationUser</span><span class="sxs-lookup"><span data-stu-id="25beb-124">educationUser</span></span>](educationuser.md)| <span data-ttu-id="25beb-125">Cree un objeto **educationUser** publicando en la colección de usuarios.</span><span class="sxs-lookup"><span data-stu-id="25beb-125">Create a new **educationUser** by posting to the users collection.</span></span>|
|[<span data-ttu-id="25beb-126">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="25beb-126">List users</span></span>](../api/educationroot-list-users.md) |<span data-ttu-id="25beb-127">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="25beb-127">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="25beb-128">Obtenga una colección de objetos **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="25beb-128">Get an **educationUser** object collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="25beb-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25beb-129">Properties</span></span>
<span data-ttu-id="25beb-130">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="25beb-130">None.</span></span>

## <a name="relationships"></a><span data-ttu-id="25beb-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="25beb-131">Relationships</span></span>
| <span data-ttu-id="25beb-132">Relación</span><span class="sxs-lookup"><span data-stu-id="25beb-132">Relationship</span></span> | <span data-ttu-id="25beb-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="25beb-133">Type</span></span>   |<span data-ttu-id="25beb-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="25beb-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="25beb-135">classes</span><span class="sxs-lookup"><span data-stu-id="25beb-135">classes</span></span>|<span data-ttu-id="25beb-136">Colección [educationClass](educationclass.md)</span><span class="sxs-lookup"><span data-stu-id="25beb-136">[educationClass](educationclass.md) collection</span></span>| <span data-ttu-id="25beb-p102">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="25beb-p102">Read-only. Nullable.</span></span>|
|<span data-ttu-id="25beb-139">me</span><span class="sxs-lookup"><span data-stu-id="25beb-139">me</span></span>|[<span data-ttu-id="25beb-140">educationUser</span><span class="sxs-lookup"><span data-stu-id="25beb-140">educationUser</span></span>](educationuser.md)| <span data-ttu-id="25beb-p103">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="25beb-p103">Read-only. Nullable.</span></span>|
|<span data-ttu-id="25beb-143">schools</span><span class="sxs-lookup"><span data-stu-id="25beb-143">schools</span></span>|<span data-ttu-id="25beb-144">Colección [educationSchool](educationschool.md)</span><span class="sxs-lookup"><span data-stu-id="25beb-144">[educationSchool](educationschool.md) collection</span></span>| <span data-ttu-id="25beb-p104">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="25beb-p104">Read-only. Nullable.</span></span>|
|<span data-ttu-id="25beb-147">users</span><span class="sxs-lookup"><span data-stu-id="25beb-147">users</span></span>|<span data-ttu-id="25beb-148">Colección [educationUser](educationuser.md)</span><span class="sxs-lookup"><span data-stu-id="25beb-148">[educationUser](educationuser.md) collection</span></span>| <span data-ttu-id="25beb-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="25beb-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="25beb-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25beb-151">JSON representation</span></span>
<span data-ttu-id="25beb-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="25beb-152">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.educationRoot"
}-->

```json
{
}
```

<!-- {
  "blockType": "request",
  "name": "get_education"
}-->
```http
GET https://graph.microsoft.com/v1.0/education
```

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationRoot"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationRoot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
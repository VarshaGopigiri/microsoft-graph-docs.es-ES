---
title: tipo de recurso governanceSubject
description: Representa los usuarios, grupos y entidades de seguridad de servicio que se administra en la administración de identidad con privilegios (PIM).
ms.openlocfilehash: c2129a0da488d4e7f425d6ef3596a955269e0da8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083771"
---
# <a name="governancesubject-resource-type"></a><span data-ttu-id="6a1ad-103">tipo de recurso governanceSubject</span><span class="sxs-lookup"><span data-stu-id="6a1ad-103">governanceSubject resource type</span></span>

> <span data-ttu-id="6a1ad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6a1ad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6a1ad-106">Representa los usuarios, grupos y entidades de seguridad de servicio que se administra en la administración de identidad con privilegios (PIM).</span><span class="sxs-lookup"><span data-stu-id="6a1ad-106">Represents users, groups, and service principals being managed in Privileged Identity Management (PIM).</span></span>


## <a name="properties"></a><span data-ttu-id="6a1ad-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a1ad-107">Properties</span></span>
| <span data-ttu-id="6a1ad-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6a1ad-108">Property</span></span>  | <span data-ttu-id="6a1ad-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a1ad-109">Type</span></span>       |<span data-ttu-id="6a1ad-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a1ad-110">Description</span></span>|
|:----------|:----------|:----------|
|<span data-ttu-id="6a1ad-111">id</span><span class="sxs-lookup"><span data-stu-id="6a1ad-111">id</span></span>         |<span data-ttu-id="6a1ad-112">String</span><span class="sxs-lookup"><span data-stu-id="6a1ad-112">String</span></span>     | <span data-ttu-id="6a1ad-113">El identificador del tema.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-113">The id of the subject.</span></span>|
|<span data-ttu-id="6a1ad-114">type</span><span class="sxs-lookup"><span data-stu-id="6a1ad-114">type</span></span>       |<span data-ttu-id="6a1ad-115">String</span><span class="sxs-lookup"><span data-stu-id="6a1ad-115">String</span></span>     |<span data-ttu-id="6a1ad-116">El tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-116">The type of the subject.</span></span> <span data-ttu-id="6a1ad-117">El valor puede ser ``User``, ``Group``, y ``ServicePrincipal``.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-117">The value can be ``User``, ``Group``, and ``ServicePrincipal``.</span></span>|
|<span data-ttu-id="6a1ad-118">displayName</span><span class="sxs-lookup"><span data-stu-id="6a1ad-118">displayName</span></span>|<span data-ttu-id="6a1ad-119">String</span><span class="sxs-lookup"><span data-stu-id="6a1ad-119">String</span></span>     |<span data-ttu-id="6a1ad-120">El nombre para mostrar del asunto.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-120">The display name of the subject.</span></span>|
|<span data-ttu-id="6a1ad-121">email</span><span class="sxs-lookup"><span data-stu-id="6a1ad-121">email</span></span>      |<span data-ttu-id="6a1ad-122">String</span><span class="sxs-lookup"><span data-stu-id="6a1ad-122">String</span></span>     |<span data-ttu-id="6a1ad-123">La dirección de correo electrónico del sujeto del usuario.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-123">The email address of the user subject.</span></span> <span data-ttu-id="6a1ad-124">Si el asunto es en otros tipos, está vacío.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-124">If the subject is in other types, it is empty.</span></span>|
|<span data-ttu-id="6a1ad-125">principalName</span><span class="sxs-lookup"><span data-stu-id="6a1ad-125">principalName</span></span>|<span data-ttu-id="6a1ad-126">String</span><span class="sxs-lookup"><span data-stu-id="6a1ad-126">String</span></span>   |<span data-ttu-id="6a1ad-127">El nombre principal del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-127">The principal name of the user subject.</span></span> <span data-ttu-id="6a1ad-128">Si el asunto es en otros tipos, está vacío.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-128">If the subject is in other types, it is empty.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6a1ad-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6a1ad-129">Relationships</span></span>
<span data-ttu-id="6a1ad-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6a1ad-130">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="6a1ad-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6a1ad-131">JSON representation</span></span>

<span data-ttu-id="6a1ad-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6a1ad-132">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceSubject"
}-->

```json
{
  "id": "String",  
  "displayName": "String",
  "email": "String",
  "principalName": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceSubject",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
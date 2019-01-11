---
title: tipo de recurso governanceSubject
description: Representa los usuarios, grupos y entidades de seguridad de servicio que se administra en la administración de identidad con privilegios (PIM).
localization_priority: Normal
ms.openlocfilehash: f3f8762c9136a3ae92269f6c06f52000fb73f710
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832595"
---
# <a name="governancesubject-resource-type"></a><span data-ttu-id="580fa-103">tipo de recurso governanceSubject</span><span class="sxs-lookup"><span data-stu-id="580fa-103">governanceSubject resource type</span></span>

> <span data-ttu-id="580fa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="580fa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="580fa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="580fa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="580fa-106">Representa los usuarios, grupos y entidades de seguridad de servicio que se administra en la administración de identidad con privilegios (PIM).</span><span class="sxs-lookup"><span data-stu-id="580fa-106">Represents users, groups, and service principals being managed in Privileged Identity Management (PIM).</span></span>


## <a name="properties"></a><span data-ttu-id="580fa-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="580fa-107">Properties</span></span>
| <span data-ttu-id="580fa-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="580fa-108">Property</span></span>  | <span data-ttu-id="580fa-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="580fa-109">Type</span></span>       |<span data-ttu-id="580fa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="580fa-110">Description</span></span>|
|:----------|:----------|:----------|
|<span data-ttu-id="580fa-111">id</span><span class="sxs-lookup"><span data-stu-id="580fa-111">id</span></span>         |<span data-ttu-id="580fa-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="580fa-112">String</span></span>     | <span data-ttu-id="580fa-113">El identificador del tema.</span><span class="sxs-lookup"><span data-stu-id="580fa-113">The id of the subject.</span></span>|
|<span data-ttu-id="580fa-114">type</span><span class="sxs-lookup"><span data-stu-id="580fa-114">type</span></span>       |<span data-ttu-id="580fa-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="580fa-115">String</span></span>     |<span data-ttu-id="580fa-116">El tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="580fa-116">The type of the subject.</span></span> <span data-ttu-id="580fa-117">El valor puede ser ``User``, ``Group``, y ``ServicePrincipal``.</span><span class="sxs-lookup"><span data-stu-id="580fa-117">The value can be ``User``, ``Group``, and ``ServicePrincipal``.</span></span>|
|<span data-ttu-id="580fa-118">displayName</span><span class="sxs-lookup"><span data-stu-id="580fa-118">displayName</span></span>|<span data-ttu-id="580fa-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="580fa-119">String</span></span>     |<span data-ttu-id="580fa-120">El nombre para mostrar del asunto.</span><span class="sxs-lookup"><span data-stu-id="580fa-120">The display name of the subject.</span></span>|
|<span data-ttu-id="580fa-121">email</span><span class="sxs-lookup"><span data-stu-id="580fa-121">email</span></span>      |<span data-ttu-id="580fa-122">String</span><span class="sxs-lookup"><span data-stu-id="580fa-122">String</span></span>     |<span data-ttu-id="580fa-123">La dirección de correo electrónico del sujeto del usuario.</span><span class="sxs-lookup"><span data-stu-id="580fa-123">The email address of the user subject.</span></span> <span data-ttu-id="580fa-124">Si el asunto es en otros tipos, está vacío.</span><span class="sxs-lookup"><span data-stu-id="580fa-124">If the subject is in other types, it is empty.</span></span>|
|<span data-ttu-id="580fa-125">principalName</span><span class="sxs-lookup"><span data-stu-id="580fa-125">principalName</span></span>|<span data-ttu-id="580fa-126">String</span><span class="sxs-lookup"><span data-stu-id="580fa-126">String</span></span>   |<span data-ttu-id="580fa-127">El nombre principal del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="580fa-127">The principal name of the user subject.</span></span> <span data-ttu-id="580fa-128">Si el asunto es en otros tipos, está vacío.</span><span class="sxs-lookup"><span data-stu-id="580fa-128">If the subject is in other types, it is empty.</span></span>|

## <a name="relationships"></a><span data-ttu-id="580fa-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="580fa-129">Relationships</span></span>
<span data-ttu-id="580fa-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="580fa-130">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="580fa-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="580fa-131">JSON representation</span></span>

<span data-ttu-id="580fa-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="580fa-132">Here is a JSON representation of the resource.</span></span>

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

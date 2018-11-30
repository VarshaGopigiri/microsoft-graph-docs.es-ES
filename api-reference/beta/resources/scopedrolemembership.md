---
title: tipo de recurso scopedRoleMembership
description: Una pertenencia a una función con ámbito describe la pertenencia de un usuario de un rol de Active directory, que es aún más el ámbito a una unidad administrativa (AU).  Esto proporciona un mecanismo para permitir que un adminsistrator del inquilino de toda la empresa delegar privilegios administrativos a un usuario para administrar usuarios y grupos en un subconjunto de la organización (el subconjunto está definido por un AU).
ms.openlocfilehash: bd635a5b1b06b98657ba24c397e2f67afb76fa8f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086464"
---
# <a name="scopedrolemembership-resource-type"></a><span data-ttu-id="a84d8-104">tipo de recurso scopedRoleMembership</span><span class="sxs-lookup"><span data-stu-id="a84d8-104">scopedRoleMembership resource type</span></span>

> <span data-ttu-id="a84d8-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a84d8-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a84d8-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a84d8-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a84d8-107">Una pertenencia a una función con ámbito describe la pertenencia de un usuario de un rol de Active directory, que es aún más el ámbito a una unidad administrativa (AU).</span><span class="sxs-lookup"><span data-stu-id="a84d8-107">A scoped-role membership describes a user's membership of a directory role, that is further scoped to an Administrative Unit (AU).</span></span>  <span data-ttu-id="a84d8-108">Esto proporciona un mecanismo para permitir que un adminsistrator del inquilino de toda la empresa delegar privilegios administrativos a un usuario para administrar usuarios y grupos en un subconjunto de la organización (el subconjunto está definido por un AU).</span><span class="sxs-lookup"><span data-stu-id="a84d8-108">This provides a mechanism to allow a tenant-wide company adminsistrator to delegate administrative privileges to a user to manage users and groups in a subset of the organization (the subset being defined by an AU).</span></span>

## <a name="methods"></a><span data-ttu-id="a84d8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a84d8-109">Methods</span></span>
<span data-ttu-id="a84d8-110">No se admiten las consultas directas a este recurso.</span><span class="sxs-lookup"><span data-stu-id="a84d8-110">Direct queries to this resource are not supported.</span></span>  <span data-ttu-id="a84d8-111">Vea el tema de [unidades administrativas](administrativeunit.md) para ver información acerca de la consulta para las pertenencias a funciones con ámbito, así como agregar y quitar pertenencias de rol con ámbito.</span><span class="sxs-lookup"><span data-stu-id="a84d8-111">Please see the [adminstrative units](administrativeunit.md) topic to see information on how to query for scoped-role memberships, as well as adding and removing scoped-role memberships.</span></span> 

## <a name="properties"></a><span data-ttu-id="a84d8-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a84d8-112">Properties</span></span>
| <span data-ttu-id="a84d8-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a84d8-113">Property</span></span>   | <span data-ttu-id="a84d8-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="a84d8-114">Type</span></span> | <span data-ttu-id="a84d8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a84d8-115">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="a84d8-116">administrativeUnitId</span><span class="sxs-lookup"><span data-stu-id="a84d8-116">administrativeUnitId</span></span>|<span data-ttu-id="a84d8-117">string</span><span class="sxs-lookup"><span data-stu-id="a84d8-117">string</span></span>|<span data-ttu-id="a84d8-118">Identificador único para la unidad administrativa que el rol de Active directory se limita a</span><span class="sxs-lookup"><span data-stu-id="a84d8-118">Unique identifier for the administrative unit that the directory role is scoped to</span></span>|
|<span data-ttu-id="a84d8-119">id</span><span class="sxs-lookup"><span data-stu-id="a84d8-119">id</span></span>|<span data-ttu-id="a84d8-120">string</span><span class="sxs-lookup"><span data-stu-id="a84d8-120">string</span></span>| <span data-ttu-id="a84d8-121">Identificador único para la pertenencia a una función con ámbito.</span><span class="sxs-lookup"><span data-stu-id="a84d8-121">Unique identifier for the scoped-role membership.</span></span> <span data-ttu-id="a84d8-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a84d8-122">Read-only.</span></span>|
|<span data-ttu-id="a84d8-123">identificador de función</span><span class="sxs-lookup"><span data-stu-id="a84d8-123">roleId</span></span>|<span data-ttu-id="a84d8-124">string</span><span class="sxs-lookup"><span data-stu-id="a84d8-124">string</span></span>| <span data-ttu-id="a84d8-125">Identificador único para el rol de Active directory que se encuentra en el miembro.</span><span class="sxs-lookup"><span data-stu-id="a84d8-125">Unique identifier for the directory role that the member is in.</span></span>|
|<span data-ttu-id="a84d8-126">roleMemberInfo</span><span class="sxs-lookup"><span data-stu-id="a84d8-126">roleMemberInfo</span></span>|[<span data-ttu-id="a84d8-127">identity</span><span class="sxs-lookup"><span data-stu-id="a84d8-127">identity</span></span>](identity.md)| <span data-ttu-id="a84d8-128">Información de identidad del miembro de función.</span><span class="sxs-lookup"><span data-stu-id="a84d8-128">Role member identity information.</span></span> <span data-ttu-id="a84d8-129">Representa el usuario que sea miembro de esta función con ámbito.</span><span class="sxs-lookup"><span data-stu-id="a84d8-129">Represents the user that is a member of this scoped-role.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a84d8-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a84d8-130">Relationships</span></span>
<span data-ttu-id="a84d8-131">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a84d8-131">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="a84d8-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a84d8-132">JSON representation</span></span>

<span data-ttu-id="a84d8-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a84d8-133">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scopedrolemembership"
}-->

```json
{
  "administrativeUnitId": "string",
  "id": "string (identifier)",
  "roleId": "string",
  "roleMemberInfo": {"@odata.type": "microsoft.graph.identity"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scopedRoleMembership resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
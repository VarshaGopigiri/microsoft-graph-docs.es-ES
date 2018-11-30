---
title: tipo de recurso de la función de aplicación
description: Representa una función de aplicación que pueden solicitarse por una aplicación de cliente al llamar a otra aplicación o que se puede usar para asignar una aplicación a usuarios o grupos en una función de la aplicación especificada. La propiedad **appRoles** de la entidad servicePrincipal y de la entidad de la aplicación es una colección de **función de aplicación**.
ms.openlocfilehash: f87ef6f40fbeb18ec4b3a2373fb2a19e14da84a4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084591"
---
# <a name="approle-resource-type"></a><span data-ttu-id="d7dda-104">tipo de recurso de la función de aplicación</span><span class="sxs-lookup"><span data-stu-id="d7dda-104">appRole resource type</span></span>

> <span data-ttu-id="d7dda-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7dda-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7dda-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7dda-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d7dda-107">Representa una función de aplicación que pueden solicitarse por una aplicación de cliente al llamar a otra aplicación o que se puede usar para asignar una aplicación a usuarios o grupos en una función de la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="d7dda-107">Represents an application role that may be requested by a client application calling another application or that may be used to assign an application to users or groups in a specified application role.</span></span> <span data-ttu-id="d7dda-108">La propiedad **appRoles** de la entidad [servicePrincipal](serviceprincipal.md) y de la entidad de la [aplicación](application.md) es una colección de **función de aplicación**.</span><span class="sxs-lookup"><span data-stu-id="d7dda-108">The **appRoles** property of the [servicePrincipal](serviceprincipal.md) entity and of the [application](application.md) entity is a collection of **appRole**.</span></span>

> <span data-ttu-id="d7dda-109">Importante: Esta funcionalidad está deshabilitada en la versión actual.</span><span class="sxs-lookup"><span data-stu-id="d7dda-109">Important: This functionality is disabled in the current release.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d7dda-110">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d7dda-110">JSON representation</span></span>

<span data-ttu-id="d7dda-111">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d7dda-111">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.approle"
}-->

```json
{
  "allowedMemberTypes": ["string"],
  "description": "string",
  "displayName": "string",
  "id": "guid",
  "isEnabled": true,
  "origin": "string",
  "value": "string"
}

```
## <a name="properties"></a><span data-ttu-id="d7dda-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d7dda-112">Properties</span></span>
| <span data-ttu-id="d7dda-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7dda-113">Property</span></span>     | <span data-ttu-id="d7dda-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7dda-114">Type</span></span>   |<span data-ttu-id="d7dda-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7dda-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d7dda-116">allowedMemberTypes</span><span class="sxs-lookup"><span data-stu-id="d7dda-116">allowedMemberTypes</span></span>|<span data-ttu-id="d7dda-117">Colección String</span><span class="sxs-lookup"><span data-stu-id="d7dda-117">String collection</span></span>|<span data-ttu-id="d7dda-118">Especifica si esta definición de rol de aplicación se puede asignar a usuarios y grupos por valor a "User", o a otras aplicaciones (que tienen acceso a esta aplicación en escenarios de servicio de demonio) estableciendo a "Aplicación", o a ambos.</span><span class="sxs-lookup"><span data-stu-id="d7dda-118">Specifies whether this app role definition can be assigned to users and groups by setting to “User”, or to other applications (that are accessing this application in daemon service scenarios) by setting to “Application”, or to both.</span></span>|
|<span data-ttu-id="d7dda-119">descripción</span><span class="sxs-lookup"><span data-stu-id="d7dda-119">description</span></span>|<span data-ttu-id="d7dda-120">String</span><span class="sxs-lookup"><span data-stu-id="d7dda-120">String</span></span>|<span data-ttu-id="d7dda-121">Texto de ayuda que aparece en la asignación de la aplicación de administración de permisos y experiencias de consentimiento.</span><span class="sxs-lookup"><span data-stu-id="d7dda-121">Permission help text that appears in the admin app assignment and consent experiences.</span></span>|
|<span data-ttu-id="d7dda-122">displayName</span><span class="sxs-lookup"><span data-stu-id="d7dda-122">displayName</span></span>|<span data-ttu-id="d7dda-123">String</span><span class="sxs-lookup"><span data-stu-id="d7dda-123">String</span></span>|<span data-ttu-id="d7dda-124">Nombre para mostrar para el permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="d7dda-124">Display name for the permission that appears in the admin consent and app assignment experiences.</span></span>|
|<span data-ttu-id="d7dda-125">id</span><span class="sxs-lookup"><span data-stu-id="d7dda-125">id</span></span>|<span data-ttu-id="d7dda-126">Guid</span><span class="sxs-lookup"><span data-stu-id="d7dda-126">Guid</span></span>|<span data-ttu-id="d7dda-127">Identificador único de la función dentro de la colección **appRoles** .</span><span class="sxs-lookup"><span data-stu-id="d7dda-127">Unique role identifier inside the **appRoles** collection.</span></span>|
|<span data-ttu-id="d7dda-128">isEnabled</span><span class="sxs-lookup"><span data-stu-id="d7dda-128">isEnabled</span></span>|<span data-ttu-id="d7dda-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="d7dda-129">Boolean</span></span>|<span data-ttu-id="d7dda-130">Al crear o actualizar una definición de rol, esto se debe establecer en **true** (que es el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="d7dda-130">When creating or updating a role definition, this must be set to **true** (which is the default).</span></span> <span data-ttu-id="d7dda-131">Para eliminar un rol, esto en primer lugar se debe establecer en **false**.</span><span class="sxs-lookup"><span data-stu-id="d7dda-131">To delete a role, this must first be set to **false**.</span></span>  <span data-ttu-id="d7dda-132">En ese momento, en una llamada posterior, se puede quitar este rol.</span><span class="sxs-lookup"><span data-stu-id="d7dda-132">At that point, in a subsequent call, this role may be removed.</span></span>|
|<span data-ttu-id="d7dda-133">valor</span><span class="sxs-lookup"><span data-stu-id="d7dda-133">value</span></span>|<span data-ttu-id="d7dda-134">String</span><span class="sxs-lookup"><span data-stu-id="d7dda-134">String</span></span>|<span data-ttu-id="d7dda-135">Especifica el valor de la notificación de roles que se debe esperar la aplicación en los tokens de autenticación y acceso.</span><span class="sxs-lookup"><span data-stu-id="d7dda-135">Specifies the value of the roles claim that the application should expect in the authentication and access tokens.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "appRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
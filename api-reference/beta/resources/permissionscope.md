---
title: tipo de recurso permissionScope
description: Representa una OAuth 2.0 habían delegada ámbito de permisos. La versión 2.0 de OAuth especificado ámbitos de permisos delegado pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** en el objeto Application) cuando se llama a una aplicación de recursos. La propiedad **oauth2Permissions** de la entidad ServicePrincipal y de la entidad de la aplicación es una colección de **OAuth2Permission**.
localization_priority: Normal
ms.openlocfilehash: a294316f5c6255d0873ce0dbe809c33dad89ae08
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818154"
---
# <a name="permissionscope-resource-type"></a><span data-ttu-id="8017f-105">tipo de recurso permissionScope</span><span class="sxs-lookup"><span data-stu-id="8017f-105">permissionScope resource type</span></span>

> <span data-ttu-id="8017f-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8017f-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8017f-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8017f-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8017f-108">Representa una OAuth 2.0 habían delegada ámbito de permisos.</span><span class="sxs-lookup"><span data-stu-id="8017f-108">Represents an OAuth 2.0 delegated permission scope.</span></span> <span data-ttu-id="8017f-109">La versión 2.0 de OAuth especificado ámbitos de permisos delegado pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** en el objeto [Application](application.md) ) cuando se llama a una aplicación de recursos.</span><span class="sxs-lookup"><span data-stu-id="8017f-109">The specified OAuth 2.0 delegated permission scopes may be requested by client applications (through the **requiredResourceAccess** collection on the [Application](application.md) object) when calling a resource application.</span></span> <span data-ttu-id="8017f-110">La propiedad **oauth2Permissions** de la entidad [ServicePrincipal](serviceprincipal.md) y de la entidad de la [aplicación](application.md) es una colección de **OAuth2Permission**.</span><span class="sxs-lookup"><span data-stu-id="8017f-110">The **oauth2Permissions** property of the [ServicePrincipal](serviceprincipal.md) entity and of the [Application](application.md) entity is a collection of **OAuth2Permission**.</span></span>

## <a name="properties"></a><span data-ttu-id="8017f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8017f-111">Properties</span></span>

| <span data-ttu-id="8017f-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8017f-112">Property</span></span> | <span data-ttu-id="8017f-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="8017f-113">Type</span></span> | <span data-ttu-id="8017f-114">Description</span><span class="sxs-lookup"><span data-stu-id="8017f-114">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="8017f-115">adminConsentDescription</span><span class="sxs-lookup"><span data-stu-id="8017f-115">adminConsentDescription</span></span>|<span data-ttu-id="8017f-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="8017f-116">String</span></span>| <span data-ttu-id="8017f-117">Texto de Ayuda de permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="8017f-117">Permission help text that appears in the admin consent and app assignment experiences.</span></span> |
|<span data-ttu-id="8017f-118">adminConsentDisplayName</span><span class="sxs-lookup"><span data-stu-id="8017f-118">adminConsentDisplayName</span></span>|<span data-ttu-id="8017f-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="8017f-119">String</span></span>| <span data-ttu-id="8017f-120">Nombre para mostrar para el permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="8017f-120">Display name for the permission that appears in the admin consent and app assignment experiences.</span></span> |
|<span data-ttu-id="8017f-121">id</span><span class="sxs-lookup"><span data-stu-id="8017f-121">id</span></span>|<span data-ttu-id="8017f-122">Guid</span><span class="sxs-lookup"><span data-stu-id="8017f-122">Guid</span></span>| <span data-ttu-id="8017f-123">Identificador de permiso de ámbito único dentro de la colección oauth2Permissions.</span><span class="sxs-lookup"><span data-stu-id="8017f-123">Unique scope permission identifier inside the oauth2Permissions collection.</span></span> |
|<span data-ttu-id="8017f-124">isEnabled</span><span class="sxs-lookup"><span data-stu-id="8017f-124">isEnabled</span></span>|<span data-ttu-id="8017f-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="8017f-125">Boolean</span></span>| <span data-ttu-id="8017f-126">Al crear o actualizar un permiso, se debe establecer esta propiedad en **true** (que es el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="8017f-126">When creating or updating a permission, this property must be set to **true** (which is the default).</span></span> <span data-ttu-id="8017f-127">Para eliminar un permiso, primero se debe establecer esta propiedad en **false**.</span><span class="sxs-lookup"><span data-stu-id="8017f-127">To delete a permission, this property must first be set to **false**.</span></span> <span data-ttu-id="8017f-128">En ese momento, en una llamada posterior, se puede quitar el permiso.</span><span class="sxs-lookup"><span data-stu-id="8017f-128">At that point, in a subsequent call, the permission may be removed.</span></span> |
|<span data-ttu-id="8017f-129">origen</span><span class="sxs-lookup"><span data-stu-id="8017f-129">origin</span></span>|<span data-ttu-id="8017f-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="8017f-130">String</span></span>| <span data-ttu-id="8017f-131">Para uso interno.</span><span class="sxs-lookup"><span data-stu-id="8017f-131">For internal use.</span></span> |
|<span data-ttu-id="8017f-132">type</span><span class="sxs-lookup"><span data-stu-id="8017f-132">type</span></span>|<span data-ttu-id="8017f-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="8017f-133">String</span></span>| <span data-ttu-id="8017f-134">Especifica si se puede aceptado este permiso ámbito por un usuario final, o si es un permiso de todo el inquilino que debe ser aceptado por un administrador de la compañía.</span><span class="sxs-lookup"><span data-stu-id="8017f-134">Specifies whether this scope permission can be consented to by an end user, or whether it is a tenant-wide permission that must be consented to by a company administrator.</span></span> <span data-ttu-id="8017f-135">Los valores posibles son el *usuario* o *Administrador*.</span><span class="sxs-lookup"><span data-stu-id="8017f-135">Possible values are *User* or *Admin*.</span></span> |
|<span data-ttu-id="8017f-136">userConsentDescription</span><span class="sxs-lookup"><span data-stu-id="8017f-136">userConsentDescription</span></span>|<span data-ttu-id="8017f-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="8017f-137">String</span></span>| <span data-ttu-id="8017f-138">Texto de Ayuda de permiso que aparece en la experiencia de consentimiento de usuario final.</span><span class="sxs-lookup"><span data-stu-id="8017f-138">Permission help text that appears in the end-user consent experience.</span></span> |
|<span data-ttu-id="8017f-139">userConsentDisplayName</span><span class="sxs-lookup"><span data-stu-id="8017f-139">userConsentDisplayName</span></span>|<span data-ttu-id="8017f-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="8017f-140">String</span></span>| <span data-ttu-id="8017f-141">Nombre para mostrar para el permiso que aparece en la experiencia de consentimiento de usuario final.</span><span class="sxs-lookup"><span data-stu-id="8017f-141">Display name for the permission that appears in the end-user consent experience.</span></span> |
|<span data-ttu-id="8017f-142">valor</span><span class="sxs-lookup"><span data-stu-id="8017f-142">value</span></span>|<span data-ttu-id="8017f-143">String</span><span class="sxs-lookup"><span data-stu-id="8017f-143">String</span></span>| <span data-ttu-id="8017f-144">El valor de la notificación de ámbito que se debe esperar la aplicación de recursos en el token de acceso de OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="8017f-144">The value of the scope claim that the resource application should expect in the OAuth 2.0 access token.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="8017f-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8017f-145">JSON representation</span></span>
<span data-ttu-id="8017f-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8017f-146">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.permissionScope"
}-->

```json
{
  "adminConsentDescription": "String",
  "adminConsentDisplayName": "String",
  "id": "Guid",
  "isEnabled": true,
  "origin": "String",
  "type": "String",
  "userConsentDescription": "String",
  "userConsentDisplayName": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "permissionScope resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

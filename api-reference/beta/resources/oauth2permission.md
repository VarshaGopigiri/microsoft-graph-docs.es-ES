---
title: tipo de recurso oAuth2Permission
description: Representa una OAuth 2.0 habían delegada ámbito de permisos. La versión 2.0 de OAuth especificado ámbitos de permisos delegado pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** en el objeto application) cuando se llama a una aplicación de recursos. La propiedad **appRoles** de la entidad servicePrincipal y de la entidad de la aplicación es una colección de **oAuth2Permission**.
ms.openlocfilehash: 4a790c935dd84fb7bd4e1422ca59914d9a319ae9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088635"
---
# <a name="oauth2permission-resource-type"></a><span data-ttu-id="377e7-105">tipo de recurso oAuth2Permission</span><span class="sxs-lookup"><span data-stu-id="377e7-105">oAuth2Permission resource type</span></span>

> <span data-ttu-id="377e7-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="377e7-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="377e7-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="377e7-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="377e7-108">Representa una OAuth 2.0 habían delegada ámbito de permisos.</span><span class="sxs-lookup"><span data-stu-id="377e7-108">Represents an OAuth 2.0 delegated permission scope.</span></span> <span data-ttu-id="377e7-109">La versión 2.0 de OAuth especificado ámbitos de permisos delegado pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** en el objeto [application](application.md) ) cuando se llama a una aplicación de recursos.</span><span class="sxs-lookup"><span data-stu-id="377e7-109">The specified OAuth 2.0 delegated permission scopes may be requested by client applications (through the **requiredResourceAccess** collection on the [application](application.md) object) when calling a resource application.</span></span> <span data-ttu-id="377e7-110">La propiedad **appRoles** de la entidad [servicePrincipal](serviceprincipal.md) y de la entidad de la [aplicación](application.md) es una colección de **oAuth2Permission**.</span><span class="sxs-lookup"><span data-stu-id="377e7-110">The **appRoles** property of the [servicePrincipal](serviceprincipal.md) entity and of the [application](application.md) entity is a collection of **oAuth2Permission**.</span></span>


## <a name="json-representation"></a><span data-ttu-id="377e7-111">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="377e7-111">JSON representation</span></span>

<span data-ttu-id="377e7-112">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="377e7-112">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.oAuth2Permission"
}-->

```json
{
  "adminConsentDescription": "string",
  "adminConsentDisplayName": "string",
  "id": "guid",
  "isEnabled": true,
  "origin": "string",
  "type": "string",
  "userConsentDescription": "string",
  "userConsentDisplayName": "string",
  "value": "string"
}

```
## <a name="properties"></a><span data-ttu-id="377e7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="377e7-113">Properties</span></span>
| <span data-ttu-id="377e7-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="377e7-114">Property</span></span>     | <span data-ttu-id="377e7-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="377e7-115">Type</span></span>   |<span data-ttu-id="377e7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="377e7-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="377e7-117">adminConsentDescription</span><span class="sxs-lookup"><span data-stu-id="377e7-117">adminConsentDescription</span></span>|<span data-ttu-id="377e7-118">String</span><span class="sxs-lookup"><span data-stu-id="377e7-118">String</span></span>|<span data-ttu-id="377e7-119">Texto de Ayuda de permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="377e7-119">Permission help text that appears in the admin consent and app assignment experiences.</span></span>|
|<span data-ttu-id="377e7-120">adminConsentDisplayName</span><span class="sxs-lookup"><span data-stu-id="377e7-120">adminConsentDisplayName</span></span>|<span data-ttu-id="377e7-121">String</span><span class="sxs-lookup"><span data-stu-id="377e7-121">String</span></span>|<span data-ttu-id="377e7-122">Nombre para mostrar para el permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="377e7-122">Display name for the permission that appears in the admin consent and app assignment experiences.</span></span>|
|<span data-ttu-id="377e7-123">id</span><span class="sxs-lookup"><span data-stu-id="377e7-123">id</span></span>|<span data-ttu-id="377e7-124">Guid</span><span class="sxs-lookup"><span data-stu-id="377e7-124">Guid</span></span>|<span data-ttu-id="377e7-125">Identificador de permiso de ámbito único dentro de la colección oauth2Permissions.</span><span class="sxs-lookup"><span data-stu-id="377e7-125">Unique scope permission identifier inside the oauth2Permissions collection.</span></span>|
|<span data-ttu-id="377e7-126">isEnabled</span><span class="sxs-lookup"><span data-stu-id="377e7-126">isEnabled</span></span>|<span data-ttu-id="377e7-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="377e7-127">Boolean</span></span>|<span data-ttu-id="377e7-128">Al crear o actualizar un permiso, se debe establecer esta propiedad en **true** (que es el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="377e7-128">When creating or updating a permission, this property must be set to **true** (which is the default).</span></span> <span data-ttu-id="377e7-129">Para eliminar un permiso, primero se debe establecer esta propiedad en **false**.</span><span class="sxs-lookup"><span data-stu-id="377e7-129">To delete a permission, this property must first be set to **false**.</span></span>  <span data-ttu-id="377e7-130">En ese momento, en una llamada posterior, se puede quitar el permiso.</span><span class="sxs-lookup"><span data-stu-id="377e7-130">At that point, in a subsequent call, the permission may be removed.</span></span>|
|<span data-ttu-id="377e7-131">type</span><span class="sxs-lookup"><span data-stu-id="377e7-131">type</span></span>|<span data-ttu-id="377e7-132">String</span><span class="sxs-lookup"><span data-stu-id="377e7-132">String</span></span>|<span data-ttu-id="377e7-133">Especifica si se puede aceptado este permiso ámbito por un usuario final, o si es un permiso de todo el inquilino que debe ser aceptado por un administrador de la compañía.</span><span class="sxs-lookup"><span data-stu-id="377e7-133">Specifies whether this scope permission can be consented to by an end user, or whether it is a tenant-wide permission that must be consented to by a Company Administrator.</span></span>  <span data-ttu-id="377e7-134">Los valores posibles son "Usuario" o "Administrador".</span><span class="sxs-lookup"><span data-stu-id="377e7-134">Possible values are "User" or "Admin".</span></span>|
|<span data-ttu-id="377e7-135">userConsentDescription</span><span class="sxs-lookup"><span data-stu-id="377e7-135">userConsentDescription</span></span>|<span data-ttu-id="377e7-136">String</span><span class="sxs-lookup"><span data-stu-id="377e7-136">String</span></span>|<span data-ttu-id="377e7-137">Texto de Ayuda de permiso que aparece en la experiencia de consentimiento de usuario final.</span><span class="sxs-lookup"><span data-stu-id="377e7-137">Permission help text that appears in the end user consent experience.</span></span>|
|<span data-ttu-id="377e7-138">userConsentDisplayName</span><span class="sxs-lookup"><span data-stu-id="377e7-138">userConsentDisplayName</span></span>|<span data-ttu-id="377e7-139">String</span><span class="sxs-lookup"><span data-stu-id="377e7-139">String</span></span>|<span data-ttu-id="377e7-140">Nombre para mostrar para el permiso que aparece en la experiencia de consentimiento de usuario final.</span><span class="sxs-lookup"><span data-stu-id="377e7-140">Display name for the permission that appears in the end user consent experience.</span></span>|
|<span data-ttu-id="377e7-141">valor</span><span class="sxs-lookup"><span data-stu-id="377e7-141">value</span></span>|<span data-ttu-id="377e7-142">String</span><span class="sxs-lookup"><span data-stu-id="377e7-142">String</span></span>|<span data-ttu-id="377e7-143">El valor de la notificación de ámbito que se debe esperar la aplicación de recursos en el token de acceso de OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="377e7-143">The value of the scope claim that the resource application should expect in the OAuth 2.0 access token.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "oAuth2Permission resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
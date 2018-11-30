---
title: tipo de recurso oAuth2PermissionGrant
description: Representa los ámbitos de OAuth 2.0 (delegado permisos) que se hayan concedido a una aplicación (representada por una entidad de seguridad de servicio) como parte del proceso de consentimiento de usuario o un administrador.
ms.openlocfilehash: 8fc5154ddba1b78976dc3e24c6712f9fc8944f43
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084348"
---
# <a name="oauth2permissiongrant-resource-type"></a><span data-ttu-id="b5b6f-103">tipo de recurso oAuth2PermissionGrant</span><span class="sxs-lookup"><span data-stu-id="b5b6f-103">oAuth2PermissionGrant resource type</span></span>

> <span data-ttu-id="b5b6f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b5b6f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b5b6f-106">Representa los ámbitos de OAuth 2.0 (delegado permisos) que se hayan concedido a una aplicación (representada por una entidad de seguridad de servicio) como parte del proceso de consentimiento de usuario o un administrador.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-106">Represents the OAuth 2.0 scopes (delegated permissions) that have been granted to an application (represented by a service principal) as part of the user or admin consent process.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b5b6f-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b5b6f-107">JSON representation</span></span>

<span data-ttu-id="b5b6f-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b5b6f-108">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.oAuth2Permissiongrant"
}-->

```json
{
  "clientId": "string",
  "consentType": "string",
  "expiryTime": "String (timestamp)",
  "id": "string (identifier)",
  "principalId": "string",
  "resourceId": "string",
  "scope": "string",
  "startTime": "String (timestamp)"
}

```
## <a name="properties"></a><span data-ttu-id="b5b6f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5b6f-109">Properties</span></span>
| <span data-ttu-id="b5b6f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b5b6f-110">Property</span></span>     | <span data-ttu-id="b5b6f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5b6f-111">Type</span></span>   |<span data-ttu-id="b5b6f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5b6f-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b5b6f-113">clientId</span><span class="sxs-lookup"><span data-stu-id="b5b6f-113">clientId</span></span>|<span data-ttu-id="b5b6f-114">String</span><span class="sxs-lookup"><span data-stu-id="b5b6f-114">String</span></span>| <span data-ttu-id="b5b6f-115">El identificador de la entidad de seguridad de servicio concedido da su consentimiento para suplantar al usuario al obtener acceso a los recursos (representado por la propiedad resourceId).</span><span class="sxs-lookup"><span data-stu-id="b5b6f-115">The id of the service principal granted consent to impersonate the user when accessing the resource (represented by the resourceId property).</span></span> |
|<span data-ttu-id="b5b6f-116">consentType</span><span class="sxs-lookup"><span data-stu-id="b5b6f-116">consentType</span></span>|<span data-ttu-id="b5b6f-117">String</span><span class="sxs-lookup"><span data-stu-id="b5b6f-117">String</span></span>| <span data-ttu-id="b5b6f-118">Indica si su consentimiento le ha proporcionado por el administrador (en nombre de la organización) o de forma individual.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-118">Indicates if consent was provided by the administrator (on behalf of the organization) or by an individual.</span></span> <span data-ttu-id="b5b6f-119">Los valores posibles son *AllPrincipals* o *entidad de seguridad*.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-119">The possible values are *AllPrincipals* or *Principal*.</span></span> |
|<span data-ttu-id="b5b6f-120">expiryTime</span><span class="sxs-lookup"><span data-stu-id="b5b6f-120">expiryTime</span></span>|<span data-ttu-id="b5b6f-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b5b6f-121">DateTimeOffset</span></span>| <span data-ttu-id="b5b6f-122">Actualmente, se ignora el valor de tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-122">Currently, the expiry time value is ignored.</span></span> |
|<span data-ttu-id="b5b6f-123">id</span><span class="sxs-lookup"><span data-stu-id="b5b6f-123">id</span></span>|<span data-ttu-id="b5b6f-124">String</span><span class="sxs-lookup"><span data-stu-id="b5b6f-124">String</span></span>| <span data-ttu-id="b5b6f-125">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-125">Unique identifier.</span></span> <span data-ttu-id="b5b6f-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-126">Read-only.</span></span>|
|<span data-ttu-id="b5b6f-127">principalId</span><span class="sxs-lookup"><span data-stu-id="b5b6f-127">principalId</span></span>|<span data-ttu-id="b5b6f-128">String</span><span class="sxs-lookup"><span data-stu-id="b5b6f-128">String</span></span>| <span data-ttu-id="b5b6f-129">Si consentType es *AllPrincipals* este valor es null, y el consentimiento se aplica a todos los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-129">If consentType is *AllPrincipals* this value is null, and the consent applies to all users in the organization.</span></span> <span data-ttu-id="b5b6f-130">Si consentType es *Principal*, esta propiedad especifica el identificador del usuario que concede el consentimiento y se aplica únicamente para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-130">If consentType is *Principal*, then this property specifies the id of the user that granted consent and applies only for that user.</span></span> |
|<span data-ttu-id="b5b6f-131">resourceId</span><span class="sxs-lookup"><span data-stu-id="b5b6f-131">resourceId</span></span>|<span data-ttu-id="b5b6f-132">cadena</span><span class="sxs-lookup"><span data-stu-id="b5b6f-132">String</span></span>| <span data-ttu-id="b5b6f-133">Especifica el identificador de la entidad de seguridad de servicio de recurso al que se ha concedido acceso.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-133">Specifies the id of the resource service principal to which access has been granted.</span></span> |
|<span data-ttu-id="b5b6f-134">scope</span><span class="sxs-lookup"><span data-stu-id="b5b6f-134">scope</span></span>|<span data-ttu-id="b5b6f-135">String</span><span class="sxs-lookup"><span data-stu-id="b5b6f-135">String</span></span>| <span data-ttu-id="b5b6f-136">Especifica el valor de la notificación de [ámbito](/graph/permissions-reference) que se debe esperar a que la aplicación de recursos en el token de acceso de OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-136">Specifies the value of the [scope](/graph/permissions-reference) claim that the resource application should expect in the OAuth 2.0 access token.</span></span> <span data-ttu-id="b5b6f-137">Por ejemplo, *User.Read*</span><span class="sxs-lookup"><span data-stu-id="b5b6f-137">For example, *User.Read*</span></span> |
|<span data-ttu-id="b5b6f-138">startTime</span><span class="sxs-lookup"><span data-stu-id="b5b6f-138">startTime</span></span>|<span data-ttu-id="b5b6f-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b5b6f-139">DateTimeOffset</span></span>| <span data-ttu-id="b5b6f-140">Actualmente, se ignora el valor de tiempo de inicio.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-140">Currently, the start time value is ignored.</span></span> |

## <a name="relationships"></a><span data-ttu-id="b5b6f-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b5b6f-141">Relationships</span></span>
<span data-ttu-id="b5b6f-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b5b6f-142">None</span></span>


## <a name="methods"></a><span data-ttu-id="b5b6f-143">Métodos</span><span class="sxs-lookup"><span data-stu-id="b5b6f-143">Methods</span></span>

| <span data-ttu-id="b5b6f-144">Método</span><span class="sxs-lookup"><span data-stu-id="b5b6f-144">Method</span></span>           | <span data-ttu-id="b5b6f-145">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5b6f-145">Return Type</span></span>    |<span data-ttu-id="b5b6f-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5b6f-146">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b5b6f-147">Obtener oAuth2PermissionGrant</span><span class="sxs-lookup"><span data-stu-id="b5b6f-147">Get oAuth2PermissionGrant</span></span>](../api/oauth2permissiongrant-get.md) | [<span data-ttu-id="b5b6f-148">oAuth2PermissionGrant</span><span class="sxs-lookup"><span data-stu-id="b5b6f-148">oAuth2PermissionGrant</span></span>](oauth2permissiongrant.md) |<span data-ttu-id="b5b6f-149">Leer las propiedades y las relaciones del objeto oAuth2PermissionGrant.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-149">Read properties and relationships of oAuth2PermissionGrant object.</span></span>|
|[<span data-ttu-id="b5b6f-150">Lista oAuth2PermissionGrants</span><span class="sxs-lookup"><span data-stu-id="b5b6f-150">List oAuth2PermissionGrants</span></span>](../api/oauth2permissiongrant-list.md) | <span data-ttu-id="b5b6f-151">colección de [oAuth2PermissionGrant](oauth2permissiongrant.md)</span><span class="sxs-lookup"><span data-stu-id="b5b6f-151">[oAuth2PermissionGrant](oauth2permissiongrant.md) collection</span></span> | <span data-ttu-id="b5b6f-152">Recuperar una lista de objetos de oauth2PermissionGrant.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-152">Retrieve a list of oauth2PermissionGrant objects.</span></span> |
|[<span data-ttu-id="b5b6f-153">Actualizar oAuth2PermissionGrant</span><span class="sxs-lookup"><span data-stu-id="b5b6f-153">Update oAuth2PermissionGrant</span></span>](../api/oauth2permissiongrant-update.md) | [<span data-ttu-id="b5b6f-154">oAuth2PermissionGrant</span><span class="sxs-lookup"><span data-stu-id="b5b6f-154">oAuth2PermissionGrant</span></span>](oauth2permissiongrant.md) |<span data-ttu-id="b5b6f-155">Actualizar el objeto oAuth2PermissionGrant.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-155">Update oAuth2PermissionGrant object.</span></span> |
|[<span data-ttu-id="b5b6f-156">Eliminar oAuth2PermissionGrant</span><span class="sxs-lookup"><span data-stu-id="b5b6f-156">Delete oAuth2PermissionGrant</span></span>](../api/oauth2permissiongrant-delete.md) | <span data-ttu-id="b5b6f-157">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b5b6f-157">None</span></span> |<span data-ttu-id="b5b6f-158">Eliminar el objeto oAuth2PermissionGrant.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-158">Delete oAuth2PermissionGrant object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "oAuth2PermissionGrant resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
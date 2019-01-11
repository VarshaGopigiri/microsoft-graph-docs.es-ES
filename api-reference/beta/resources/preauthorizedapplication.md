---
title: tipo de recurso preAuthorizedApplication
description: Representa una aplicación y los permisos solicitados para consentimiento implícito. Requiere un administrador que se ha proporcionado el consentimiento a la aplicación. preAuthorizedApplications no requieren el usuario da su consentimiento a los permisos solicitados. Los permisos enumerados en preAuthorizedApplications no requieren el consentimiento de usuario. Sin embargo, los permisos solicitados adicionales no aparece en preAuthorizedApplications requieren el consentimiento de usuario.
localization_priority: Normal
ms.openlocfilehash: fa26b8046b81db70300b8ff40abcbd2b84f3f0c8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832798"
---
# <a name="preauthorizedapplication-resource-type"></a><span data-ttu-id="4e027-107">tipo de recurso preAuthorizedApplication</span><span class="sxs-lookup"><span data-stu-id="4e027-107">preAuthorizedApplication resource type</span></span>

> <span data-ttu-id="4e027-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4e027-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4e027-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4e027-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4e027-110">Representa una aplicación y los permisos solicitados para consentimiento implícito.</span><span class="sxs-lookup"><span data-stu-id="4e027-110">Represents an application and requested permissions for implicit consent.</span></span> <span data-ttu-id="4e027-111">Requiere un administrador que se ha proporcionado el consentimiento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e027-111">Requires an admin to have provided consent to the application.</span></span> <span data-ttu-id="4e027-112">preAuthorizedApplications no requieren el usuario da su consentimiento a los permisos solicitados.</span><span class="sxs-lookup"><span data-stu-id="4e027-112">preAuthorizedApplications do not require the user to consent to the requested permissions.</span></span> <span data-ttu-id="4e027-113">Los permisos enumerados en preAuthorizedApplications no requieren el consentimiento de usuario.</span><span class="sxs-lookup"><span data-stu-id="4e027-113">Permissions listed in preAuthorizedApplications do not require user consent.</span></span> <span data-ttu-id="4e027-114">Sin embargo, los permisos solicitados adicionales no aparece en preAuthorizedApplications requieren el consentimiento de usuario.</span><span class="sxs-lookup"><span data-stu-id="4e027-114">However, any additional requested permissions not listed in preAuthorizedApplications require user consent.</span></span>

## <a name="properties"></a><span data-ttu-id="4e027-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e027-115">Properties</span></span>

| <span data-ttu-id="4e027-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4e027-116">Property</span></span> | <span data-ttu-id="4e027-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e027-117">Type</span></span> | <span data-ttu-id="4e027-118">Description</span><span class="sxs-lookup"><span data-stu-id="4e027-118">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="4e027-119">appId</span><span class="sxs-lookup"><span data-stu-id="4e027-119">appId</span></span>|<span data-ttu-id="4e027-120">cadena</span><span class="sxs-lookup"><span data-stu-id="4e027-120">String</span></span>| <span data-ttu-id="4e027-121">El identificador único para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e027-121">The unique identifier for the application.</span></span> |
|<span data-ttu-id="4e027-122">permissionIds</span><span class="sxs-lookup"><span data-stu-id="4e027-122">permissionIds</span></span>|<span data-ttu-id="4e027-123">Colección String</span><span class="sxs-lookup"><span data-stu-id="4e027-123">String collection</span></span>| <span data-ttu-id="4e027-124">Se requiere el identificador único para el [publishedPermissionScope](permissionscope.md) o la [función de aplicación](approle.md) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e027-124">The unique identifier for either the [publishedPermissionScope](permissionscope.md) or [appRole](approle.md) the application requires.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="4e027-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4e027-125">JSON representation</span></span>
<span data-ttu-id="4e027-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4e027-126">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.preAuthorizedApplication"
}-->

```json
{
  "appId": "String",
  "permissionIds": ["String"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "preAuthorizedApplication resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

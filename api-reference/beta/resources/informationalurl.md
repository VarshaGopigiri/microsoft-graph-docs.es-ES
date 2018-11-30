---
title: tipo de recurso informationalUrl
description: Información de perfil básico de la aplicación.
ms.openlocfilehash: c8a13f4f686fe3b6ffd460ab05342b7da9b4a808
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088200"
---
# <a name="informationalurl-resource-type"></a><span data-ttu-id="90b93-103">tipo de recurso informationalUrl</span><span class="sxs-lookup"><span data-stu-id="90b93-103">informationalUrl resource type</span></span>

> <span data-ttu-id="90b93-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90b93-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90b93-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90b93-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="90b93-106">Información de perfil básico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="90b93-106">Basic profile information of the application.</span></span>

## <a name="properties"></a><span data-ttu-id="90b93-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90b93-107">Properties</span></span>

| <span data-ttu-id="90b93-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90b93-108">Property</span></span> | <span data-ttu-id="90b93-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="90b93-109">Type</span></span> | <span data-ttu-id="90b93-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="90b93-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="90b93-111">de marketing</span><span class="sxs-lookup"><span data-stu-id="90b93-111">marketing</span></span>|<span data-ttu-id="90b93-112">String</span><span class="sxs-lookup"><span data-stu-id="90b93-112">String</span></span>| <span data-ttu-id="90b93-113">Vínculo a la aplicación de la página de marketing.</span><span class="sxs-lookup"><span data-stu-id="90b93-113">Link to the application's marketing page.</span></span> <span data-ttu-id="90b93-114">Por ejemplo: https://www.contoso.com/app/marketing</span><span class="sxs-lookup"><span data-stu-id="90b93-114">For example, https://www.contoso.com/app/marketing</span></span> |
|<span data-ttu-id="90b93-115">privacidad</span><span class="sxs-lookup"><span data-stu-id="90b93-115">privacy</span></span>|<span data-ttu-id="90b93-116">String</span><span class="sxs-lookup"><span data-stu-id="90b93-116">String</span></span>| <span data-ttu-id="90b93-117">Vínculo a la declaración de privacidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="90b93-117">Link to the application's privacy statement.</span></span> <span data-ttu-id="90b93-118">Por ejemplo: https://www.contoso.com/app/privacy</span><span class="sxs-lookup"><span data-stu-id="90b93-118">For example, https://www.contoso.com/app/privacy</span></span> |
|<span data-ttu-id="90b93-119">soporte técnico</span><span class="sxs-lookup"><span data-stu-id="90b93-119">support</span></span>|<span data-ttu-id="90b93-120">String</span><span class="sxs-lookup"><span data-stu-id="90b93-120">String</span></span>| <span data-ttu-id="90b93-121">Vínculo a la página de soporte técnico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="90b93-121">Link to the application's support page.</span></span> <span data-ttu-id="90b93-122">Por ejemplo: https://www.contoso.com/app/support</span><span class="sxs-lookup"><span data-stu-id="90b93-122">For example, https://www.contoso.com/app/support</span></span> |
|<span data-ttu-id="90b93-123">termsOfService</span><span class="sxs-lookup"><span data-stu-id="90b93-123">termsOfService</span></span>|<span data-ttu-id="90b93-124">String</span><span class="sxs-lookup"><span data-stu-id="90b93-124">String</span></span>| <span data-ttu-id="90b93-125">Vínculo a los términos de la aplicación de instrucción de servicio.</span><span class="sxs-lookup"><span data-stu-id="90b93-125">Link to the application's terms of service statement.</span></span> <span data-ttu-id="90b93-126">Por ejemplo: https://www.contoso.com/app/termsofservice</span><span class="sxs-lookup"><span data-stu-id="90b93-126">For example, https://www.contoso.com/app/termsofservice</span></span> |

## <a name="json-representation"></a><span data-ttu-id="90b93-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="90b93-127">JSON representation</span></span>
<span data-ttu-id="90b93-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="90b93-128">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.informationalUrl"
}-->

```json
{
  "marketing": "String",
  "privacy": "String",
  "support": "String",
  "termsOfService": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "informationalUrl resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
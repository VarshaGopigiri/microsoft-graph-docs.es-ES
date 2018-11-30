---
title: Tipo de recurso localeInfo
description: Información sobre la configuración regional, como el idioma preferido y el país o región del usuario que inició sesión.
ms.openlocfilehash: 5dae464a4931fb094ae47cce600a95d55c6c3f93
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089467"
---
# <a name="localeinfo-resource-type"></a><span data-ttu-id="d9b2b-103">Tipo de recurso localeInfo</span><span class="sxs-lookup"><span data-stu-id="d9b2b-103">localeInfo resource type</span></span>

> <span data-ttu-id="d9b2b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9b2b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d9b2b-106">Información sobre la configuración regional, como el idioma preferido y el país o región del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-106">Information about the locale, including the preferred language and country/region, of the signed-in user.</span></span>


## <a name="properties"></a><span data-ttu-id="d9b2b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9b2b-107">Properties</span></span>
| <span data-ttu-id="d9b2b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9b2b-108">Property</span></span>     | <span data-ttu-id="d9b2b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9b2b-109">Type</span></span>   |<span data-ttu-id="d9b2b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9b2b-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d9b2b-111">configuración regional</span><span class="sxs-lookup"><span data-stu-id="d9b2b-111">locale</span></span>|<span data-ttu-id="d9b2b-112">string</span><span class="sxs-lookup"><span data-stu-id="d9b2b-112">string</span></span>|<span data-ttu-id="d9b2b-p102">Representación de la configuración regional del usuario, que incluye el idioma preferido y el país o región del usuario. Por ejemplo, "es-es". El componente de idioma sigue códigos de dos letras, tal y como se define en [ISO 639-1](https://www.iso.org/iso/home/standards/language_codes.htm), y el componente de país sigue códigos de dos letras, tal y como se define en [ISO 3166-1 alpha-2](https://www.iso.org/iso/country_codes.htm).</span><span class="sxs-lookup"><span data-stu-id="d9b2b-p102">A locale representation for the user, which includes the user's preferred language and country/region. For example, "en-us". The language component follows 2-letter codes as defined in [ISO 639-1](https://www.iso.org/iso/home/standards/language_codes.htm), and the country component follows 2-letter codes as defined in [ISO 3166-1 alpha-2](https://www.iso.org/iso/country_codes.htm).</span></span>|
|<span data-ttu-id="d9b2b-116">displayName</span><span class="sxs-lookup"><span data-stu-id="d9b2b-116">displayName</span></span>|<span data-ttu-id="d9b2b-117">string</span><span class="sxs-lookup"><span data-stu-id="d9b2b-117">string</span></span>|<span data-ttu-id="d9b2b-118">Nombre que representa la configuración regional del usuario en lenguaje natural, por ejemplo, "Inglés (Estados Unidos)".</span><span class="sxs-lookup"><span data-stu-id="d9b2b-118">A name representing the user's locale in natural language, for example, "English (United States)".</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d9b2b-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d9b2b-119">JSON representation</span></span>

<span data-ttu-id="d9b2b-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d9b2b-120">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.localeInfo"
}-->

```json
{
  "locale": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "localeInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
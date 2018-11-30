---
title: Tipo de recurso privacyProfile
description: Representa el perfil de privacidad de una compañía; incluye la dirección URL de una declaración de privacidad y una persona de contacto para las preguntas sobre la declaración de privacidad.
ms.openlocfilehash: fb9d5f929f1c9ae28687b80e987dc0909387f5d6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090768"
---
# <a name="privacyprofile-resource-type"></a><span data-ttu-id="f9c54-103">Tipo de recurso privacyProfile</span><span class="sxs-lookup"><span data-stu-id="f9c54-103">privacyProfile resource type</span></span>

> <span data-ttu-id="f9c54-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f9c54-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f9c54-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f9c54-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f9c54-106">Representa el perfil de privacidad de una compañía; incluye la dirección URL de una declaración de privacidad y una persona de contacto para las preguntas sobre la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="f9c54-106">Represents a company's privacy profile, which includes a privacy statement URL and a contact person for questions regarding the privacy statement.</span></span>

## <a name="properties"></a><span data-ttu-id="f9c54-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9c54-107">Properties</span></span>
| <span data-ttu-id="f9c54-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9c54-108">Property</span></span>   | <span data-ttu-id="f9c54-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9c54-109">Type</span></span>|<span data-ttu-id="f9c54-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9c54-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f9c54-111">contactEmail</span><span class="sxs-lookup"><span data-stu-id="f9c54-111">contactEmail</span></span>|<span data-ttu-id="f9c54-112">String</span><span class="sxs-lookup"><span data-stu-id="f9c54-112">String</span></span>| <span data-ttu-id="f9c54-113">Dirección de correo electrónico smtp válida para el contacto de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="f9c54-113">A valid smtp email address for the privacy statement contact.</span></span> <span data-ttu-id="f9c54-114">No se requiere.</span><span class="sxs-lookup"><span data-stu-id="f9c54-114">Not required.</span></span>|
|<span data-ttu-id="f9c54-115">statementUrl</span><span class="sxs-lookup"><span data-stu-id="f9c54-115">statementUrl</span></span>|<span data-ttu-id="f9c54-116">String</span><span class="sxs-lookup"><span data-stu-id="f9c54-116">String</span></span>| <span data-ttu-id="f9c54-117">Formato de URL válido que empiece por http:// o https://.</span><span class="sxs-lookup"><span data-stu-id="f9c54-117">A valid URL format that begins with http:// or https://.</span></span> <span data-ttu-id="f9c54-118">La longitud máxima es de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f9c54-118">Maximum length is 255 characters.</span></span> <span data-ttu-id="f9c54-119">Dirección URL que se dirige a la declaración de privacidad de la compañía.</span><span class="sxs-lookup"><span data-stu-id="f9c54-119">The URL that directs to the company's privacy statement.</span></span> <span data-ttu-id="f9c54-120">No se requiere.</span><span class="sxs-lookup"><span data-stu-id="f9c54-120">Not required.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f9c54-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f9c54-121">JSON representation</span></span>

<span data-ttu-id="f9c54-122">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f9c54-122">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privacyProfile"
}-->

```json
{
  "contactEmail": "string",
  "statementUrl": "string"
}
```
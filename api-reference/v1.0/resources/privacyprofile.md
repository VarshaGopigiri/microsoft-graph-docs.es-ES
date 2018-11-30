---
title: Tipo de recurso privacyProfile
description: Representa el perfil de privacidad de una compañía; incluye la dirección URL de una declaración de privacidad y una persona de contacto para las preguntas sobre la declaración de privacidad.
ms.openlocfilehash: 5d1a8e48a2d8310f45c71fbc73485e8ec4fe8697
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032081"
---
# <a name="privacyprofile-resource-type"></a><span data-ttu-id="1106b-103">Tipo de recurso privacyProfile</span><span class="sxs-lookup"><span data-stu-id="1106b-103">privacyProfile resource type</span></span>

<span data-ttu-id="1106b-104">Representa el perfil de privacidad de una compañía; incluye la dirección URL de una declaración de privacidad y una persona de contacto para las preguntas sobre la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="1106b-104">Represents a company's privacy profile, which includes a privacy statement URL and a contact person for questions regarding the privacy statement.</span></span>

## <a name="properties"></a><span data-ttu-id="1106b-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1106b-105">Properties</span></span>
| <span data-ttu-id="1106b-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1106b-106">Property</span></span>   | <span data-ttu-id="1106b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1106b-107">Type</span></span>|<span data-ttu-id="1106b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1106b-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1106b-109">contactEmail</span><span class="sxs-lookup"><span data-stu-id="1106b-109">contactEmail</span></span>|<span data-ttu-id="1106b-110">String</span><span class="sxs-lookup"><span data-stu-id="1106b-110">String</span></span>| <span data-ttu-id="1106b-111">Dirección de correo electrónico smtp válida para el contacto de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="1106b-111">A valid smtp email address for the privacy statement contact.</span></span> <span data-ttu-id="1106b-112">No se requiere.</span><span class="sxs-lookup"><span data-stu-id="1106b-112">Not required.</span></span>|
|<span data-ttu-id="1106b-113">statementUrl</span><span class="sxs-lookup"><span data-stu-id="1106b-113">statementUrl</span></span>|<span data-ttu-id="1106b-114">String</span><span class="sxs-lookup"><span data-stu-id="1106b-114">String</span></span>| <span data-ttu-id="1106b-115">Formato de URL válido que empiece por http:// o https://.</span><span class="sxs-lookup"><span data-stu-id="1106b-115">A valid URL format that begins with http:// or https://.</span></span> <span data-ttu-id="1106b-116">La longitud máxima es de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1106b-116">Maximum length is 255 characters.</span></span> <span data-ttu-id="1106b-117">Dirección URL que se dirige a la declaración de privacidad de la compañía.</span><span class="sxs-lookup"><span data-stu-id="1106b-117">The URL that directs to the company's privacy statement.</span></span> <span data-ttu-id="1106b-118">No se requiere.</span><span class="sxs-lookup"><span data-stu-id="1106b-118">Not required.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1106b-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1106b-119">JSON representation</span></span>

<span data-ttu-id="1106b-120">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1106b-120">Here is a JSON representation of the resource</span></span>

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
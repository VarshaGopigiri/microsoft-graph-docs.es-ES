---
title: tipo de recurso passwordCredential
description: Contiene una credencial de contraseña asociada con una aplicación o un servicio de entidad de seguridad. La propiedad **passwordCredentials** de la entidad servicePrincipal y de la entidad de la aplicación es una colección de **passwordCredential**.
ms.openlocfilehash: 79d3f76606533cf639f52ed22cd93f353e18e977
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083229"
---
# <a name="passwordcredential-resource-type"></a><span data-ttu-id="4286d-104">tipo de recurso passwordCredential</span><span class="sxs-lookup"><span data-stu-id="4286d-104">passwordCredential resource type</span></span>

> <span data-ttu-id="4286d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4286d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4286d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4286d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4286d-107">Contiene una credencial de contraseña asociada con una aplicación o un servicio de entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4286d-107">Contains a password credential associated with an application or a service principal.</span></span> <span data-ttu-id="4286d-108">La propiedad **passwordCredentials** de la entidad [servicePrincipal](serviceprincipal.md) y de la entidad de la [aplicación](application.md) es una colección de **passwordCredential**.</span><span class="sxs-lookup"><span data-stu-id="4286d-108">The **passwordCredentials** property of the [servicePrincipal](serviceprincipal.md) entity and of the [application](application.md) entity is a collection of **passwordCredential**.</span></span>


## <a name="json-representation"></a><span data-ttu-id="4286d-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4286d-109">JSON representation</span></span>

<span data-ttu-id="4286d-110">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4286d-110">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.passwordCredential"
}-->

```json
{
  "customKeyIdentifier": "binary",
  "endDateTime": "String (timestamp)",
  "keyId": "guid",
  "startDateTime": "String (timestamp)",
  "secretText": "string",
  "hint": "string"
}

```
## <a name="properties"></a><span data-ttu-id="4286d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4286d-111">Properties</span></span>
| <span data-ttu-id="4286d-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4286d-112">Property</span></span>     | <span data-ttu-id="4286d-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="4286d-113">Type</span></span>   |<span data-ttu-id="4286d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4286d-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4286d-115">customKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="4286d-115">customKeyIdentifier</span></span>|<span data-ttu-id="4286d-116">Binario</span><span class="sxs-lookup"><span data-stu-id="4286d-116">Binary</span></span>|            |
|<span data-ttu-id="4286d-117">endDateTime</span><span class="sxs-lookup"><span data-stu-id="4286d-117">endDateTime</span></span>|<span data-ttu-id="4286d-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4286d-118">DateTimeOffset</span></span>|<span data-ttu-id="4286d-119">La fecha y hora de caducidad de la contraseña. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="4286d-119">The date and time at which the password expires.The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="4286d-120">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="4286d-120">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="4286d-121">Id</span><span class="sxs-lookup"><span data-stu-id="4286d-121">keyId</span></span>|<span data-ttu-id="4286d-122">Guid</span><span class="sxs-lookup"><span data-stu-id="4286d-122">Guid</span></span>|            |
|<span data-ttu-id="4286d-123">startDateTime</span><span class="sxs-lookup"><span data-stu-id="4286d-123">startDateTime</span></span>|<span data-ttu-id="4286d-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4286d-124">DateTimeOffset</span></span>|<span data-ttu-id="4286d-125">La fecha y la hora en que la contraseña es válida. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="4286d-125">The date and time at which the password becomes valid.The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="4286d-126">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="4286d-126">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="4286d-127">secretText</span><span class="sxs-lookup"><span data-stu-id="4286d-127">secretText</span></span>|<span data-ttu-id="4286d-128">String</span><span class="sxs-lookup"><span data-stu-id="4286d-128">String</span></span>| <span data-ttu-id="4286d-129">Las contraseñas deben ser 16-64 caracteres de longitud</span><span class="sxs-lookup"><span data-stu-id="4286d-129">The passwords must be 16-64 characters in length</span></span> |
|<span data-ttu-id="4286d-130">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="4286d-130">hint</span></span>|<span data-ttu-id="4286d-131">String</span><span class="sxs-lookup"><span data-stu-id="4286d-131">String</span></span>|  |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordCredential resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

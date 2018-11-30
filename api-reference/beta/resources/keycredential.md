---
title: tipo de recurso keyCredential
description: Contiene una credencial de clave asociada con una aplicación o una entidad de seguridad de servicio. La propiedad **keyCredentials** de las entidades de la aplicación y servicePrincipal es una colección de **keyCredential**.
ms.openlocfilehash: d4509360c0425c255566b9f77b9ecd96cf349dec
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083462"
---
# <a name="keycredential-resource-type"></a><span data-ttu-id="3df99-104">tipo de recurso keyCredential</span><span class="sxs-lookup"><span data-stu-id="3df99-104">keyCredential resource type</span></span>

> <span data-ttu-id="3df99-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3df99-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3df99-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3df99-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3df99-107">Contiene una credencial de clave asociada con una aplicación o una entidad de seguridad de servicio.</span><span class="sxs-lookup"><span data-stu-id="3df99-107">Contains a key credential associated with an application or a service principal.</span></span> <span data-ttu-id="3df99-108">La propiedad **keyCredentials** de las entidades de la [aplicación](application.md) y [servicePrincipal](serviceprincipal.md) es una colección de **keyCredential**.</span><span class="sxs-lookup"><span data-stu-id="3df99-108">The **keyCredentials** property of the [application](application.md) and [servicePrincipal](serviceprincipal.md) entities is a collection of **keyCredential**.</span></span>


## <a name="json-representation"></a><span data-ttu-id="3df99-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3df99-109">JSON representation</span></span>

<span data-ttu-id="3df99-110">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3df99-110">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.keyCredential"
}-->

```json
{
  "customKeyIdentifier": "binary",
  "endDateTime": "String (timestamp)",
  "keyId": "guid",
  "startDateTime": "String (timestamp)",
  "type": "string",
  "usage": "string",
  "key": "binary"
}

```
## <a name="properties"></a><span data-ttu-id="3df99-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3df99-111">Properties</span></span>
| <span data-ttu-id="3df99-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3df99-112">Property</span></span>     | <span data-ttu-id="3df99-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="3df99-113">Type</span></span>   |<span data-ttu-id="3df99-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3df99-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3df99-115">customKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="3df99-115">customKeyIdentifier</span></span>|<span data-ttu-id="3df99-116">Binario</span><span class="sxs-lookup"><span data-stu-id="3df99-116">Binary</span></span>| <span data-ttu-id="3df99-117">Identificador de clave personalizado</span><span class="sxs-lookup"><span data-stu-id="3df99-117">Custom key identifier</span></span> |
|<span data-ttu-id="3df99-118">endDateTime</span><span class="sxs-lookup"><span data-stu-id="3df99-118">endDateTime</span></span>|<span data-ttu-id="3df99-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3df99-119">DateTimeOffset</span></span>|<span data-ttu-id="3df99-120">La fecha y hora de caducidad de la credencial. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="3df99-120">The date and time at which the credential expires.The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="3df99-121">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="3df99-121">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="3df99-122">Id</span><span class="sxs-lookup"><span data-stu-id="3df99-122">keyId</span></span>|<span data-ttu-id="3df99-123">Guid</span><span class="sxs-lookup"><span data-stu-id="3df99-123">Guid</span></span>|<span data-ttu-id="3df99-124">Identificador único (GUID) de la clave.</span><span class="sxs-lookup"><span data-stu-id="3df99-124">The unique identifier (GUID) for the key.</span></span>|
|<span data-ttu-id="3df99-125">startDateTime</span><span class="sxs-lookup"><span data-stu-id="3df99-125">startDateTime</span></span>|<span data-ttu-id="3df99-126">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3df99-126">DateTimeOffset</span></span>|<span data-ttu-id="3df99-127">La fecha y la hora en que la credencial es válida. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="3df99-127">The date and time at which the credential becomes valid.The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="3df99-128">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="3df99-128">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="3df99-129">type</span><span class="sxs-lookup"><span data-stu-id="3df99-129">type</span></span>|<span data-ttu-id="3df99-130">String</span><span class="sxs-lookup"><span data-stu-id="3df99-130">String</span></span>|<span data-ttu-id="3df99-131">El tipo de credencial clave; Por ejemplo, "Simétrico".</span><span class="sxs-lookup"><span data-stu-id="3df99-131">The type of key credential; for example, “Symmetric”.</span></span>|
|<span data-ttu-id="3df99-132">uso</span><span class="sxs-lookup"><span data-stu-id="3df99-132">usage</span></span>|<span data-ttu-id="3df99-133">String</span><span class="sxs-lookup"><span data-stu-id="3df99-133">String</span></span>|<span data-ttu-id="3df99-134">Una cadena que describa el objetivo para el que se puede usar la clave; Por ejemplo, "comprobar".</span><span class="sxs-lookup"><span data-stu-id="3df99-134">A string that describes the purpose for which the key can be used; for example, “Verify”.</span></span>|
|<span data-ttu-id="3df99-135">key</span><span class="sxs-lookup"><span data-stu-id="3df99-135">key</span></span>|<span data-ttu-id="3df99-136">Binary</span><span class="sxs-lookup"><span data-stu-id="3df99-136">Binary</span></span>|            |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "keyCredential resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
---
title: tipo de recurso fileSecurityState
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 9d18021591b24d26577e41897111b90310746d18
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869506"
---
# <a name="filesecuritystate-resource-type"></a><span data-ttu-id="45618-104">tipo de recurso fileSecurityState</span><span class="sxs-lookup"><span data-stu-id="45618-104">fileSecurityState resource type</span></span>

 > <span data-ttu-id="45618-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="45618-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="45618-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="45618-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="45618-107">Contiene información sobre el archivo (no process) relacionados con la alerta.</span><span class="sxs-lookup"><span data-stu-id="45618-107">Contains information about the file (not process) related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="45618-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45618-108">Properties</span></span>

| <span data-ttu-id="45618-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="45618-109">Property</span></span>   | <span data-ttu-id="45618-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="45618-110">Type</span></span>|<span data-ttu-id="45618-111">Description</span><span class="sxs-lookup"><span data-stu-id="45618-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="45618-112">fileHash</span><span class="sxs-lookup"><span data-stu-id="45618-112">fileHash</span></span>|[<span data-ttu-id="45618-113">fileHash</span><span class="sxs-lookup"><span data-stu-id="45618-113">fileHash</span></span>](filehash.md)|<span data-ttu-id="45618-114">Tipo complejo que contiene los valores de hash de archivo (criptográficas y la ubicación).</span><span class="sxs-lookup"><span data-stu-id="45618-114">Complex type containing file hashes (cryptographic and location-sensitive).</span></span>|
|<span data-ttu-id="45618-115">name</span><span class="sxs-lookup"><span data-stu-id="45618-115">name</span></span>|<span data-ttu-id="45618-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="45618-116">String</span></span>|<span data-ttu-id="45618-117">Nombre de archivo (sin ruta de acceso).</span><span class="sxs-lookup"><span data-stu-id="45618-117">File name (without path).</span></span>|
|<span data-ttu-id="45618-118">ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="45618-118">path</span></span>|<span data-ttu-id="45618-119">String</span><span class="sxs-lookup"><span data-stu-id="45618-119">String</span></span>|<span data-ttu-id="45618-120">Ruta de acceso completa al archivo del archivo/imageFile.</span><span class="sxs-lookup"><span data-stu-id="45618-120">Full file path of the file/imageFile.</span></span>|
|<span data-ttu-id="45618-121">riskScore</span><span class="sxs-lookup"><span data-stu-id="45618-121">riskScore</span></span>|<span data-ttu-id="45618-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="45618-122">String</span></span>|<span data-ttu-id="45618-123">Proveedor generado/calcula el riesgo de puntuación del archivo alerta.</span><span class="sxs-lookup"><span data-stu-id="45618-123">Provider generated/calculated risk score of the alert file.</span></span> <span data-ttu-id="45618-124">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="45618-124">Recommended value range of 0-1, which equates to a percentage.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="45618-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="45618-125">JSON representation</span></span>

<span data-ttu-id="45618-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="45618-126">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileSecurityState"
}-->

```json
{
  "fileHash": {"@odata.type": "microsoft.graph.fileHash"},
  "name": "String",
  "path": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

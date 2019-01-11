---
title: tipo de recurso fileSecurityState
description: Contiene información sobre el archivo (no process) relacionados con la alerta.
localization_priority: Normal
ms.openlocfilehash: 14ffa41b395bde04972f0af0436297aa4d038524
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894099"
---
# <a name="filesecuritystate-resource-type"></a><span data-ttu-id="4d11f-103">tipo de recurso fileSecurityState</span><span class="sxs-lookup"><span data-stu-id="4d11f-103">fileSecurityState resource type</span></span>

<span data-ttu-id="4d11f-104">Contiene información sobre el archivo (no process) relacionados con la alerta.</span><span class="sxs-lookup"><span data-stu-id="4d11f-104">Contains information about the file (not process) related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="4d11f-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d11f-105">Properties</span></span>

| <span data-ttu-id="4d11f-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d11f-106">Property</span></span>   | <span data-ttu-id="4d11f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d11f-107">Type</span></span>|<span data-ttu-id="4d11f-108">Description</span><span class="sxs-lookup"><span data-stu-id="4d11f-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4d11f-109">fileHash</span><span class="sxs-lookup"><span data-stu-id="4d11f-109">fileHash</span></span>|[<span data-ttu-id="4d11f-110">fileHash</span><span class="sxs-lookup"><span data-stu-id="4d11f-110">fileHash</span></span>](filehash.md)|<span data-ttu-id="4d11f-111">Tipo complejo que contiene los valores de hash de archivo (criptográficas y la ubicación).</span><span class="sxs-lookup"><span data-stu-id="4d11f-111">Complex type containing file hashes (cryptographic and location-sensitive).</span></span>|
|<span data-ttu-id="4d11f-112">name</span><span class="sxs-lookup"><span data-stu-id="4d11f-112">name</span></span>|<span data-ttu-id="4d11f-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="4d11f-113">String</span></span>|<span data-ttu-id="4d11f-114">Nombre de archivo (sin ruta de acceso).</span><span class="sxs-lookup"><span data-stu-id="4d11f-114">File name (without path).</span></span>|
|<span data-ttu-id="4d11f-115">ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="4d11f-115">path</span></span>|<span data-ttu-id="4d11f-116">String</span><span class="sxs-lookup"><span data-stu-id="4d11f-116">String</span></span>|<span data-ttu-id="4d11f-117">Ruta de acceso completa al archivo del archivo/imageFile.</span><span class="sxs-lookup"><span data-stu-id="4d11f-117">Full file path of the file/imageFile.</span></span>|
|<span data-ttu-id="4d11f-118">riskScore</span><span class="sxs-lookup"><span data-stu-id="4d11f-118">riskScore</span></span>|<span data-ttu-id="4d11f-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="4d11f-119">String</span></span>|<span data-ttu-id="4d11f-120">Proveedor generado/calcula el riesgo de puntuación del archivo alerta.</span><span class="sxs-lookup"><span data-stu-id="4d11f-120">Provider generated/calculated risk score of the alert file.</span></span> <span data-ttu-id="4d11f-121">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="4d11f-121">Recommended value range of 0-1, which equates to a percentage.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4d11f-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4d11f-122">JSON representation</span></span>

<span data-ttu-id="4d11f-123">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4d11f-123">The following is a JSON representation of the resource.</span></span>

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

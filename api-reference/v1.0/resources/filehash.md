---
title: tipo de recurso fileHash
description: Contiene información de estado acerca de los valores de hash de archivo (criptográficas y la ubicación).
localization_priority: Normal
ms.openlocfilehash: 9d72812d1ad43999ea3ed5b28251d629b9380d47
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876772"
---
# <a name="filehash-resource-type"></a><span data-ttu-id="b327f-103">tipo de recurso fileHash</span><span class="sxs-lookup"><span data-stu-id="b327f-103">fileHash resource type</span></span>

<span data-ttu-id="b327f-104">Contiene información de estado acerca de los valores de hash de archivo (criptográficas y la ubicación).</span><span class="sxs-lookup"><span data-stu-id="b327f-104">Contains stateful information about file hashes (cryptographic and location-sensitive).</span></span>

## <a name="properties"></a><span data-ttu-id="b327f-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b327f-105">Properties</span></span>

| <span data-ttu-id="b327f-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b327f-106">Property</span></span>     | <span data-ttu-id="b327f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b327f-107">Type</span></span>        | <span data-ttu-id="b327f-108">Description</span><span class="sxs-lookup"><span data-stu-id="b327f-108">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="b327f-109">hashType</span><span class="sxs-lookup"><span data-stu-id="b327f-109">hashType</span></span>|<span data-ttu-id="b327f-110">fileHashType</span><span class="sxs-lookup"><span data-stu-id="b327f-110">fileHashType</span></span>|<span data-ttu-id="b327f-111">Tipo de hash de archivo.</span><span class="sxs-lookup"><span data-stu-id="b327f-111">File hash type.</span></span> <span data-ttu-id="b327f-112">Los valores posibles son: `unknown`, `sha1`, `sha256`, `md5`, `authenticodeHash256`, `lsHash`, `ctph`, `peSha1` y `peSha256`.</span><span class="sxs-lookup"><span data-stu-id="b327f-112">Possible values are: `unknown`, `sha1`, `sha256`, `md5`, `authenticodeHash256`, `lsHash`, `ctph`, `peSha1`, `peSha256`.</span></span>|
|<span data-ttu-id="b327f-113">hashValue</span><span class="sxs-lookup"><span data-stu-id="b327f-113">hashValue</span></span>|<span data-ttu-id="b327f-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="b327f-114">String</span></span>|<span data-ttu-id="b327f-115">Valor de hash de archivo.</span><span class="sxs-lookup"><span data-stu-id="b327f-115">Value of the file hash.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b327f-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b327f-116">JSON representation</span></span>

<span data-ttu-id="b327f-117">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b327f-117">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileHash"
}-->

```json
{
  "hashType": "@odata.type: microsoft.graph.fileHashType",
  "hashValue": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileHash resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

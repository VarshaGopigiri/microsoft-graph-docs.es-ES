---
title: tipo de recurso fileHash
description: Contiene información de estado acerca de los valores de hash de archivo (criptográficas y la ubicación).
ms.openlocfilehash: 8f283046efc9b4af181cb33fb4e9ca63e4892b67
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087398"
---
# <a name="filehash-resource-type"></a><span data-ttu-id="55010-103">tipo de recurso fileHash</span><span class="sxs-lookup"><span data-stu-id="55010-103">fileHash resource type</span></span>

<span data-ttu-id="55010-104">Contiene información de estado acerca de los valores de hash de archivo (criptográficas y la ubicación).</span><span class="sxs-lookup"><span data-stu-id="55010-104">Contains stateful information about file hashes (cryptographic and location-sensitive).</span></span>

## <a name="properties"></a><span data-ttu-id="55010-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55010-105">Properties</span></span>

| <span data-ttu-id="55010-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55010-106">Property</span></span>     | <span data-ttu-id="55010-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="55010-107">Type</span></span>        | <span data-ttu-id="55010-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="55010-108">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="55010-109">hashType</span><span class="sxs-lookup"><span data-stu-id="55010-109">hashType</span></span>|<span data-ttu-id="55010-110">enumeración [fileHashType](filehashtypeenumtype.md)</span><span class="sxs-lookup"><span data-stu-id="55010-110">[fileHashType](filehashtypeenumtype.md) enum</span></span>|<span data-ttu-id="55010-111">Tipo de hash de archivo.</span><span class="sxs-lookup"><span data-stu-id="55010-111">File hash type.</span></span> <span data-ttu-id="55010-112">Los valores posibles son: `unknown`, `sha1`, `sha256`, `md5`, `authenticodeHash256`, `lsHash`, `ctph`, `peSha1` y `peSha256`.</span><span class="sxs-lookup"><span data-stu-id="55010-112">Possible values are: `unknown`, `sha1`, `sha256`, `md5`, `authenticodeHash256`, `lsHash`, `ctph`, `peSha1`, `peSha256`.</span></span>|
|<span data-ttu-id="55010-113">hashValue</span><span class="sxs-lookup"><span data-stu-id="55010-113">hashValue</span></span>|<span data-ttu-id="55010-114">String</span><span class="sxs-lookup"><span data-stu-id="55010-114">String</span></span>|<span data-ttu-id="55010-115">Valor de hash de archivo.</span><span class="sxs-lookup"><span data-stu-id="55010-115">Value of the file hash.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="55010-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="55010-116">JSON representation</span></span>

<span data-ttu-id="55010-117">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="55010-117">The following is a JSON representation of the resource.</span></span>

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
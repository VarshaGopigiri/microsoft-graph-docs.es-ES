---
title: tipo de recurso agreementFileData
description: Representa el blob de Azure Active Directory términos (Azure AD) de utilizar el archivo de contrato.
localization_priority: Normal
ms.openlocfilehash: 64de3a72ad648225f24429987f5729f76ed8a2e7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815221"
---
# <a name="agreementfiledata-resource-type"></a><span data-ttu-id="7a32e-103">tipo de recurso agreementFileData</span><span class="sxs-lookup"><span data-stu-id="7a32e-103">agreementFileData resource type</span></span>

> <span data-ttu-id="7a32e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7a32e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7a32e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7a32e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7a32e-106">Representa el blob de Azure Active Directory términos (Azure AD) de utilizar el archivo de contrato.</span><span class="sxs-lookup"><span data-stu-id="7a32e-106">Represents the blob of an Azure Active Directory (Azure AD) terms of use agreement file.</span></span>

## <a name="properties"></a><span data-ttu-id="7a32e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a32e-107">Properties</span></span>
| <span data-ttu-id="7a32e-108">Método</span><span class="sxs-lookup"><span data-stu-id="7a32e-108">Method</span></span>       | <span data-ttu-id="7a32e-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a32e-109">Return Type</span></span> | <span data-ttu-id="7a32e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a32e-110">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="7a32e-111">data</span><span class="sxs-lookup"><span data-stu-id="7a32e-111">data</span></span>|<span data-ttu-id="7a32e-112">Binario</span><span class="sxs-lookup"><span data-stu-id="7a32e-112">Binary</span></span>|<span data-ttu-id="7a32e-113">Datos que representan las condiciones de usar un documento PDF.</span><span class="sxs-lookup"><span data-stu-id="7a32e-113">Data representing the terms of use PDF document.</span></span> <span data-ttu-id="7a32e-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7a32e-114">Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7a32e-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7a32e-115">JSON representation</span></span>

<span data-ttu-id="7a32e-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7a32e-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreementFileData"
}-->

```json
{
  "data": "Binary"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "agreementFileData resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

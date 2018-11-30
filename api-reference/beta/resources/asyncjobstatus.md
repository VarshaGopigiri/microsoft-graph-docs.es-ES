---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: AsyncJobStatus
ms.openlocfilehash: 9e0f95802f9f75930384ab1534bf4c519fd9cfeb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083476"
---
# <a name="asyncjobstatus-resource"></a><span data-ttu-id="a39c4-102">Recurso AsyncJobStatus</span><span class="sxs-lookup"><span data-stu-id="a39c4-102">AsyncJobStatus resource</span></span>

> <span data-ttu-id="a39c4-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a39c4-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a39c4-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a39c4-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a39c4-105">Este recurso proporciona información sobre el estado del progreso de un trabajo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="a39c4-105">This resource provides information on the status of a asynchronous job progress.</span></span>

<span data-ttu-id="a39c4-106">La API siguiente llama a los recursos **AsyncJobStatus** de devolución:</span><span class="sxs-lookup"><span data-stu-id="a39c4-106">The following API calls return **AsyncJobStatus** resources:</span></span>

* [<span data-ttu-id="a39c4-107">Copiar elemento</span><span class="sxs-lookup"><span data-stu-id="a39c4-107">Copy Item</span></span>](../api/driveitem-copy.md)

## <a name="json-representation"></a><span data-ttu-id="a39c4-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a39c4-108">JSON representation</span></span>

<!-- { "blockType": "resource", "@type": "microsoft.graph.asyncJobStatus", "@type.aka": "oneDrive.asyncOperationStatus" } -->

```json
{
  "percentageComplete": 100.0,
  "status": "notStarted | inProgress | completed | updating | failed | deletePending | deleteFailed | waiting"
}
```

## <a name="properties"></a><span data-ttu-id="a39c4-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a39c4-109">Properties</span></span>

| <span data-ttu-id="a39c4-110">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="a39c4-110">Property name</span></span>          | <span data-ttu-id="a39c4-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a39c4-111">Type</span></span>   | <span data-ttu-id="a39c4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a39c4-112">Description</span></span>                                                                                |
|:-----------------------|:-------|:-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a39c4-113">**percentageComplete**</span><span class="sxs-lookup"><span data-stu-id="a39c4-113">**percentageComplete**</span></span> | <span data-ttu-id="a39c4-114">Double</span><span class="sxs-lookup"><span data-stu-id="a39c4-114">Double</span></span> | <span data-ttu-id="a39c4-115">Un valor entre 0 y 100 que indica el porcentaje completado.</span><span class="sxs-lookup"><span data-stu-id="a39c4-115">A value between 0 and 100 that indicates the percentage complete.</span></span>                          |
| <span data-ttu-id="a39c4-116">**status**</span><span class="sxs-lookup"><span data-stu-id="a39c4-116">**status**</span></span>             | <span data-ttu-id="a39c4-117">String</span><span class="sxs-lookup"><span data-stu-id="a39c4-117">String</span></span> | <span data-ttu-id="a39c4-118">Un valor de cadena que se asigna a una enumeración de posibles valores sobre el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="a39c4-118">A string value that maps to an enumeration of possible values about the status of the job.</span></span> |

<!-- {
  "type": "#page.annotation",
  "description": "AsyncJobResource provides details about how to poll for an async completion.",
  "keywords": "async,job status,async status,copy,upload from url",
  "section": "documentation"
} -->

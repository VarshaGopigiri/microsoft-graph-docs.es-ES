---
title: tipo de recurso educationSynchronizationProfileStatus
description: 'Representa el estado de sincronización de un perfil de sincronización de datos de school. '
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: d16619b0cf1e2c09358cf585b896b0c7c7d4f318
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928930"
---
# <a name="educationsynchronizationprofilestatus-resource-type"></a><span data-ttu-id="88962-103">tipo de recurso educationSynchronizationProfileStatus</span><span class="sxs-lookup"><span data-stu-id="88962-103">educationSynchronizationProfileStatus resource type</span></span>

> <span data-ttu-id="88962-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="88962-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="88962-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="88962-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="88962-106">Representa el estado de sincronización del school datos [perfil de sincronización](educationsynchronizationprofile.md).</span><span class="sxs-lookup"><span data-stu-id="88962-106">Represents the synchronization status of a school data [synchronization profile](educationsynchronizationprofile.md).</span></span> 

> <span data-ttu-id="88962-107">**Nota:** Se pueden retrasar las actualizaciones de la **educationSynchronizationProfileStatus** debido a la naturaleza asincrónica de procesamiento de sincronización en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="88962-107">**Note:** Updates to the **educationSynchronizationProfileStatus** might be delayed due to the asynchronous nature of background sync processing.</span></span>

## <a name="methods"></a><span data-ttu-id="88962-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="88962-108">Methods</span></span>

| <span data-ttu-id="88962-109">Método</span><span class="sxs-lookup"><span data-stu-id="88962-109">Method</span></span> | <span data-ttu-id="88962-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88962-110">Return Type</span></span> | <span data-ttu-id="88962-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="88962-111">Description</span></span> |
|:-|:-|:-|
| [<span data-ttu-id="88962-112">Obtener el estado de una sincronización</span><span class="sxs-lookup"><span data-stu-id="88962-112">Get status of a sync</span></span>](../api/educationsynchronizationprofilestatus-get.md) | <span data-ttu-id="88962-113">**educationSynchronizationProfileStatus**</span><span class="sxs-lookup"><span data-stu-id="88962-113">**educationSynchronizationProfileStatus**</span></span> | <span data-ttu-id="88962-114">Devolver el estado de un perfil de sincronización específica.</span><span class="sxs-lookup"><span data-stu-id="88962-114">Return the status of a specific synchronization profile.</span></span> |

## <a name="properties"></a><span data-ttu-id="88962-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88962-115">Properties</span></span>

| <span data-ttu-id="88962-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="88962-116">Property</span></span> | <span data-ttu-id="88962-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="88962-117">Type</span></span> | <span data-ttu-id="88962-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="88962-118">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="88962-119">**status**</span><span class="sxs-lookup"><span data-stu-id="88962-119">**status**</span></span> | <span data-ttu-id="88962-120">string</span><span class="sxs-lookup"><span data-stu-id="88962-120">string</span></span> | <span data-ttu-id="88962-121">El estado de una sincronización. Los valores posibles son: `paused`, `inProgress`, `success`, `error`, `quarantined`, `validationError`.</span><span class="sxs-lookup"><span data-stu-id="88962-121">The status of a sync. Possible values are: `paused`, `inProgress`, `success`, `error`, `quarantined`, `validationError`.</span></span> |
| <span data-ttu-id="88962-122">**lastSynchronizationDateTime**</span><span class="sxs-lookup"><span data-stu-id="88962-122">**lastSynchronizationDateTime**</span></span> | <span data-ttu-id="88962-123">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88962-123">DateTimeOffset</span></span> | <span data-ttu-id="88962-124">Representa el tiempo cuando se han observado cambios más recientes en el directorio.</span><span class="sxs-lookup"><span data-stu-id="88962-124">Represents the time when most recent changes have been observed in the directory.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="88962-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="88962-125">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationProfileStatus"
}-->

```json
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#education/synchronizationProfiles('{id}')/profileStatus/$entity",
    "status": {"@odata.type":"microsoft.graph.educationSynchronizationStatus"},
    "lastSynchronizationDateTime": "DateTimeOffset"
}
```

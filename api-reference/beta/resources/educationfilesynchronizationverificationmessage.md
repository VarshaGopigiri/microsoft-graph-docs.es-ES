---
title: tipo de recurso educationFileSynchronizationVerificationMessage
description: Representa un error devuelto al cliente en respuesta a una solicitud para iniciar la sincronización de perfiles de datos de school basada en CSV. El recurso va a contener errores derivados de la comprobación. Los usuarios deben corregir los datos de origen antes de reiniciar la solicitud para sincronizar con Azure Active Directory (AD Azure).
author: mmast-msft
ms.openlocfilehash: f2826f779aac3ba41146b6677f3d1e0364be92a1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336067"
---
# <a name="educationfilesynchronizationverificationmessage-resource-type"></a><span data-ttu-id="24f94-105">tipo de recurso educationFileSynchronizationVerificationMessage</span><span class="sxs-lookup"><span data-stu-id="24f94-105">educationFileSynchronizationVerificationMessage resource type</span></span>

> <span data-ttu-id="24f94-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="24f94-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="24f94-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="24f94-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="24f94-108">Representa un error devuelto al cliente en respuesta a una solicitud para [iniciar la sincronización](../api/educationsynchronizationprofile-start.md) para los perfiles de datos basada en CSV school.</span><span class="sxs-lookup"><span data-stu-id="24f94-108">Represents an error returned to the client in response to a request to [start synchronization](../api/educationsynchronizationprofile-start.md) for CSV-based school data profiles.</span></span> <span data-ttu-id="24f94-109">El recurso va a contener errores derivados de la comprobación.</span><span class="sxs-lookup"><span data-stu-id="24f94-109">The resource will contain errors that result from the verification.</span></span> <span data-ttu-id="24f94-110">Los usuarios deben corregir los datos de origen antes de reiniciar la solicitud para sincronizar con Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="24f94-110">Users must fix the source data before you restart the request to synchronize with Azure Active Directory (Azure AD).</span></span>

## <a name="properties"></a><span data-ttu-id="24f94-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24f94-111">Properties</span></span>

| <span data-ttu-id="24f94-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="24f94-112">Property</span></span> | <span data-ttu-id="24f94-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="24f94-113">Type</span></span> | <span data-ttu-id="24f94-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="24f94-114">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="24f94-115">**type**</span><span class="sxs-lookup"><span data-stu-id="24f94-115">**type**</span></span> | <span data-ttu-id="24f94-116">string</span><span class="sxs-lookup"><span data-stu-id="24f94-116">string</span></span> | <span data-ttu-id="24f94-117">Tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="24f94-117">Type of the message.</span></span> <span data-ttu-id="24f94-118">Los valores posibles son: `error`, `warning` y `information`.</span><span class="sxs-lookup"><span data-stu-id="24f94-118">Possible values are: `error`, `warning`, `information`.</span></span> | 
| <span data-ttu-id="24f94-119">**nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="24f94-119">**filename**</span></span> | <span data-ttu-id="24f94-120">string</span><span class="sxs-lookup"><span data-stu-id="24f94-120">string</span></span> | <span data-ttu-id="24f94-121">Archivo de origen que contiene el error.</span><span class="sxs-lookup"><span data-stu-id="24f94-121">Source file that contains the error.</span></span> |
| <span data-ttu-id="24f94-122">**description**</span><span class="sxs-lookup"><span data-stu-id="24f94-122">**description**</span></span> | <span data-ttu-id="24f94-123">string</span><span class="sxs-lookup"><span data-stu-id="24f94-123">string</span></span> | <span data-ttu-id="24f94-124">Obtener información detallada sobre el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="24f94-124">Detailed information about the message type.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="24f94-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="24f94-125">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationFileSynchronizationVerificationMessage"
}-->

```json
{
    "type": "String",
    "fileName": "String",
    "description": "String"
}
```
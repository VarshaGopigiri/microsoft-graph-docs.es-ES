---
title: tipo de recurso educationFileSynchronizationVerificationMessage
description: Representa un error devuelto al cliente en respuesta a una solicitud para iniciar la sincronización de perfiles de datos de school basada en CSV. El recurso va a contener errores derivados de la comprobación. Los usuarios deben corregir los datos de origen antes de reiniciar la solicitud para sincronizar con Azure Active Directory (AD Azure).
ms.openlocfilehash: cf685e0619c5600340df68ba86ecaef11a8a435d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083529"
---
# <a name="educationfilesynchronizationverificationmessage-resource-type"></a><span data-ttu-id="fbd1c-105">tipo de recurso educationFileSynchronizationVerificationMessage</span><span class="sxs-lookup"><span data-stu-id="fbd1c-105">educationFileSynchronizationVerificationMessage resource type</span></span>

> <span data-ttu-id="fbd1c-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fbd1c-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fbd1c-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fbd1c-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fbd1c-108">Representa un error devuelto al cliente en respuesta a una solicitud para [iniciar la sincronización](../api/educationsynchronizationprofile-start.md) para los perfiles de datos basada en CSV school.</span><span class="sxs-lookup"><span data-stu-id="fbd1c-108">Represents an error returned to the client in response to a request to [start synchronization](../api/educationsynchronizationprofile-start.md) for CSV-based school data profiles.</span></span> <span data-ttu-id="fbd1c-109">El recurso va a contener errores derivados de la comprobación.</span><span class="sxs-lookup"><span data-stu-id="fbd1c-109">The resource will contain errors that result from the verification.</span></span> <span data-ttu-id="fbd1c-110">Los usuarios deben corregir los datos de origen antes de reiniciar la solicitud para sincronizar con Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="fbd1c-110">Users must fix the source data before you restart the request to synchronize with Azure Active Directory (Azure AD).</span></span>

## <a name="properties"></a><span data-ttu-id="fbd1c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbd1c-111">Properties</span></span>

| <span data-ttu-id="fbd1c-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbd1c-112">Property</span></span> | <span data-ttu-id="fbd1c-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbd1c-113">Type</span></span> | <span data-ttu-id="fbd1c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbd1c-114">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="fbd1c-115">**type**</span><span class="sxs-lookup"><span data-stu-id="fbd1c-115">**type**</span></span> | <span data-ttu-id="fbd1c-116">string</span><span class="sxs-lookup"><span data-stu-id="fbd1c-116">string</span></span> | <span data-ttu-id="fbd1c-117">Tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fbd1c-117">Type of the message.</span></span> <span data-ttu-id="fbd1c-118">Los valores posibles son: `error`, `warning` y `information`.</span><span class="sxs-lookup"><span data-stu-id="fbd1c-118">Possible values are: `error`, `warning`, `information`.</span></span> | 
| <span data-ttu-id="fbd1c-119">**nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="fbd1c-119">**filename**</span></span> | <span data-ttu-id="fbd1c-120">string</span><span class="sxs-lookup"><span data-stu-id="fbd1c-120">string</span></span> | <span data-ttu-id="fbd1c-121">Archivo de origen que contiene el error.</span><span class="sxs-lookup"><span data-stu-id="fbd1c-121">Source file that contains the error.</span></span> |
| <span data-ttu-id="fbd1c-122">**description**</span><span class="sxs-lookup"><span data-stu-id="fbd1c-122">**description**</span></span> | <span data-ttu-id="fbd1c-123">string</span><span class="sxs-lookup"><span data-stu-id="fbd1c-123">string</span></span> | <span data-ttu-id="fbd1c-124">Obtener información detallada sobre el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fbd1c-124">Detailed information about the message type.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="fbd1c-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fbd1c-125">JSON representation</span></span>

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
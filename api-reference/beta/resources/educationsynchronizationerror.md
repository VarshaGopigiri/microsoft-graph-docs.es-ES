---
title: tipo de recurso educationSynchronizationError
description: Representa un error durante la validación de perfiles de datos de escuela o sincronización. Se genera un error único para cada entrada que se produce un error al validar y sincronizar con Azure Active Directory (AD Azure).
ms.openlocfilehash: 91a633ab4056e8e86854a0e2d45ae13e22da19a8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083769"
---
# <a name="educationsynchronizationerror-resource-type"></a><span data-ttu-id="5411e-103">tipo de recurso educationSynchronizationError</span><span class="sxs-lookup"><span data-stu-id="5411e-103">educationSynchronizationError resource type</span></span>

> <span data-ttu-id="5411e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5411e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5411e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5411e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5411e-106">Representa un error durante la validación de perfiles de datos de escuela o sincronización. Se genera un error único para cada entrada que se produce un error al validar y sincronizar con Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="5411e-106">Represents an error during school data profile validation and/or sync. A unique error is generated for every entry that fails to validate and/or synchronize with Azure Active Directory (Azure AD).</span></span>

## <a name="methods"></a><span data-ttu-id="5411e-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="5411e-107">Methods</span></span>

| <span data-ttu-id="5411e-108">Método</span><span class="sxs-lookup"><span data-stu-id="5411e-108">Method</span></span> | <span data-ttu-id="5411e-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5411e-109">Return Type</span></span> | <span data-ttu-id="5411e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5411e-110">Description</span></span> |
|:-|:-|:-|
| [<span data-ttu-id="5411e-111">Obtener errores de sincronización</span><span class="sxs-lookup"><span data-stu-id="5411e-111">Get synchronization errors</span></span>](../api/educationsynchronizationerrors-get.md) | <span data-ttu-id="5411e-112">colección de **educationSynchronizationError**</span><span class="sxs-lookup"><span data-stu-id="5411e-112">**educationSynchronizationError** collection</span></span>| <span data-ttu-id="5411e-113">Devuelve la lista de errores de sincronización asociado con un perfil.</span><span class="sxs-lookup"><span data-stu-id="5411e-113">Returns the list of synchronization errors associated with a profile.</span></span> |

## <a name="properties"></a><span data-ttu-id="5411e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5411e-114">Properties</span></span>

| <span data-ttu-id="5411e-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5411e-115">Property</span></span> | <span data-ttu-id="5411e-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="5411e-116">Type</span></span> | <span data-ttu-id="5411e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5411e-117">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="5411e-118">**entryType**</span><span class="sxs-lookup"><span data-stu-id="5411e-118">**entryType**</span></span> | <span data-ttu-id="5411e-119">string</span><span class="sxs-lookup"><span data-stu-id="5411e-119">string</span></span> |  <span data-ttu-id="5411e-120">Representa la entidad de sincronización (escuela, sección, estudiantes, profesor).</span><span class="sxs-lookup"><span data-stu-id="5411e-120">Represents the sync entity (school, section, student, teacher).</span></span>       |
| <span data-ttu-id="5411e-121">**errorCode**</span><span class="sxs-lookup"><span data-stu-id="5411e-121">**errorCode**</span></span> | <span data-ttu-id="5411e-122">string</span><span class="sxs-lookup"><span data-stu-id="5411e-122">string</span></span> |  <span data-ttu-id="5411e-123">Representa el código de error de este error.</span><span class="sxs-lookup"><span data-stu-id="5411e-123">Represents the error code for this error.</span></span>         |
| <span data-ttu-id="5411e-124">**errorMessage**</span><span class="sxs-lookup"><span data-stu-id="5411e-124">**errorMessage**</span></span> | <span data-ttu-id="5411e-125">string</span><span class="sxs-lookup"><span data-stu-id="5411e-125">string</span></span> |  <span data-ttu-id="5411e-126">Contiene una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="5411e-126">Contains a description of the error.</span></span>        |
| <span data-ttu-id="5411e-127">**joiningValue**</span><span class="sxs-lookup"><span data-stu-id="5411e-127">**joiningValue**</span></span> | <span data-ttu-id="5411e-128">string</span><span class="sxs-lookup"><span data-stu-id="5411e-128">string</span></span> |  <span data-ttu-id="5411e-129">El identificador único para la entrada.</span><span class="sxs-lookup"><span data-stu-id="5411e-129">The unique identifier for the entry.</span></span>         |
| <span data-ttu-id="5411e-130">**recordedDateTime**</span><span class="sxs-lookup"><span data-stu-id="5411e-130">**recordedDateTime**</span></span> | <span data-ttu-id="5411e-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5411e-131">DateTimeOffset</span></span> | <span data-ttu-id="5411e-132">El momento de la aparición de este error.</span><span class="sxs-lookup"><span data-stu-id="5411e-132">The time of occurrence of this error.</span></span>         |
| <span data-ttu-id="5411e-133">**reportableIdentifier**</span><span class="sxs-lookup"><span data-stu-id="5411e-133">**reportableIdentifier**</span></span> | <span data-ttu-id="5411e-134">string</span><span class="sxs-lookup"><span data-stu-id="5411e-134">string</span></span> | <span data-ttu-id="5411e-135">El identificador de entrada de este error.</span><span class="sxs-lookup"><span data-stu-id="5411e-135">The identifier of this error entry.</span></span>       |

## <a name="json-representation"></a><span data-ttu-id="5411e-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5411e-136">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationError"
}-->

```json
{
    "entryType": "String",
    "errorCode": "String",
    "errorMessage": "String",
    "joiningValue": "String",
    "recordedDateTime": "DateTimeOffset",
    "reportableIdentifier": "String"
}
```

---
title: Tipo de recurso reportRoot
description: El recurso que representa una instancia de un dispositivo o del informe para solucionar problemas, según el contexto.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: efb8950b9956901161c822df8b467b0182a4cc75
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959590"
---
# <a name="reportroot-resource-type"></a><span data-ttu-id="46831-103">Tipo de recurso reportRoot</span><span class="sxs-lookup"><span data-stu-id="46831-103">reportRoot resource type</span></span>

> <span data-ttu-id="46831-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46831-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46831-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46831-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="46831-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46831-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46831-107">El recurso que representa una instancia de un dispositivo o del informe para solucionar problemas, según el contexto.</span><span class="sxs-lookup"><span data-stu-id="46831-107">The resource that represents an instance of a device or troubleshooting report, depending on context.</span></span>

## <a name="methods"></a><span data-ttu-id="46831-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="46831-108">Methods</span></span>
|<span data-ttu-id="46831-109">Método</span><span class="sxs-lookup"><span data-stu-id="46831-109">Method</span></span>|<span data-ttu-id="46831-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46831-110">Return Type</span></span>|<span data-ttu-id="46831-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="46831-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="46831-112">Obtener reportRoot</span><span class="sxs-lookup"><span data-stu-id="46831-112">Get reportRoot</span></span>](../api/intune-shared-reportroot-get.md)|<span data-ttu-id="46831-113">Lea las propiedades y las relaciones del objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="46831-113">Read properties and relationships of the [reportRoot](../resources/intune-shared-reportroot.md) object.</span></span>|
|[<span data-ttu-id="46831-114">Actualizar reportRoot</span><span class="sxs-lookup"><span data-stu-id="46831-114">Update reportRoot</span></span>](../api/intune-shared-reportroot-update.md)|<span data-ttu-id="46831-115">Actualice las propiedades de un objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="46831-115">Update the properties of a [reportRoot](../resources/intune-shared-reportroot.md) object.</span></span>|
|<span data-ttu-id="46831-116">**Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="46831-116">**Device configuration**</span></span>|
|[<span data-ttu-id="46831-117">Función deviceConfigurationUserActivity</span><span class="sxs-lookup"><span data-stu-id="46831-117">deviceConfigurationUserActivity function</span></span>](../api/intune-shared-reportroot-deviceconfigurationuseractivity.md)|<span data-ttu-id="46831-118">Metadatos para el informe de actividad de usuario de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="46831-118">Metadata for the device configuration user activity report</span></span>|
|[<span data-ttu-id="46831-119">Función deviceConfigurationDeviceActivity</span><span class="sxs-lookup"><span data-stu-id="46831-119">deviceConfigurationDeviceActivity function</span></span>](../api/intune-shared-reportroot-deviceconfigurationdeviceactivity.md)|<span data-ttu-id="46831-120">Metadatos para el informe de actividad de dispositivo de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="46831-120">Metadata for the device configuration device activity report</span></span>|
|<span data-ttu-id="46831-121">**Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="46831-121">**Troubleshooting**</span></span>|
|[<span data-ttu-id="46831-122">managedDeviceEnrollmentAbandonmentDetails (función)</span><span class="sxs-lookup"><span data-stu-id="46831-122">managedDeviceEnrollmentAbandonmentDetails function</span></span>](../api/intune-shared-reportroot-manageddeviceenrollmentabandonmentdetails.md)|[<span data-ttu-id="46831-123">report</span><span class="sxs-lookup"><span data-stu-id="46831-123">report</span></span>](../resources/intune-shared-report.md)|<span data-ttu-id="46831-124">Informe detallan de metadatos por abandono de inscripción</span><span class="sxs-lookup"><span data-stu-id="46831-124">Metadata for Enrollment abandonment details report</span></span>|
|[<span data-ttu-id="46831-125">managedDeviceEnrollmentAbandonmentSummary (función)</span><span class="sxs-lookup"><span data-stu-id="46831-125">managedDeviceEnrollmentAbandonmentSummary function</span></span>](../api/intune-shared-reportroot-manageddeviceenrollmentabandonmentsummary.md)|[<span data-ttu-id="46831-126">report</span><span class="sxs-lookup"><span data-stu-id="46831-126">report</span></span>](../resources/intune-shared-report.md)|<span data-ttu-id="46831-127">Metadatos para el informe de resumen de abandono de inscripción</span><span class="sxs-lookup"><span data-stu-id="46831-127">Metadata for Enrollment abandonment summary report</span></span>|
|[<span data-ttu-id="46831-128">managedDeviceEnrollmentFailureDetails (función)</span><span class="sxs-lookup"><span data-stu-id="46831-128">managedDeviceEnrollmentFailureDetails function</span></span>](../api/intune-shared-reportroot-manageddeviceenrollmentfailuredetails.md)|<span data-ttu-id="46831-129">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="46831-129">Not yet documented</span></span>|
|[<span data-ttu-id="46831-130">managedDeviceEnrollmentFailureTrends (función)</span><span class="sxs-lookup"><span data-stu-id="46831-130">managedDeviceEnrollmentFailureTrends function</span></span>](../api/intune-shared-reportroot-manageddeviceenrollmentfailuretrends.md)|<span data-ttu-id="46831-131">Metadatos para el informe de tendencias de errores de inscripción</span><span class="sxs-lookup"><span data-stu-id="46831-131">Metadata for the enrollment failure trends report</span></span>|
|[<span data-ttu-id="46831-132">managedDeviceEnrollmentTopFailures (función)</span><span class="sxs-lookup"><span data-stu-id="46831-132">managedDeviceEnrollmentTopFailures function</span></span>](../api/intune-shared-reportroot-manageddeviceenrollmenttopfailures.md)|<span data-ttu-id="46831-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="46831-133">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="46831-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46831-134">Properties</span></span>
|<span data-ttu-id="46831-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46831-135">Property</span></span>|<span data-ttu-id="46831-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="46831-136">Type</span></span>|<span data-ttu-id="46831-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="46831-137">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46831-138">id</span><span class="sxs-lookup"><span data-stu-id="46831-138">id</span></span>|<span data-ttu-id="46831-139">String</span><span class="sxs-lookup"><span data-stu-id="46831-139">String</span></span>|<span data-ttu-id="46831-140">El identificador único de esta entidad.</span><span class="sxs-lookup"><span data-stu-id="46831-140">The unique identifier for this entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="46831-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="46831-141">Relationships</span></span>
<span data-ttu-id="46831-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="46831-142">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="46831-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="46831-143">JSON Representation</span></span>
<span data-ttu-id="46831-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="46831-144">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.reportRoot"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.reportRoot",
  "id": "String (identifier)"
}
```




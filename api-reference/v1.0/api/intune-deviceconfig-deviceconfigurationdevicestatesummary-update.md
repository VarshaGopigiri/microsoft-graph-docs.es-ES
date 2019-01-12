---
title: Actualizar deviceConfigurationDeviceStateSummary
description: Actualice las propiedades de un objeto deviceConfigurationDeviceStateSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fd1d2fc9c9838e3a2252161b909dc2b401fd3e7d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930197"
---
# <a name="update-deviceconfigurationdevicestatesummary"></a><span data-ttu-id="6233f-103">Actualizar deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="6233f-103">Update deviceConfigurationDeviceStateSummary</span></span>

> <span data-ttu-id="6233f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6233f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6233f-105">Actualice las propiedades de un objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="6233f-105">Update the properties of a [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6233f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6233f-106">Prerequisites</span></span>
<span data-ttu-id="6233f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6233f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6233f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6233f-109">Permission type</span></span>|<span data-ttu-id="6233f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6233f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6233f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6233f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6233f-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6233f-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6233f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6233f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6233f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6233f-114">Not supported.</span></span>|
|<span data-ttu-id="6233f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6233f-115">Application</span></span>|<span data-ttu-id="6233f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6233f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6233f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6233f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurationDeviceStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="6233f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6233f-118">Request headers</span></span>
|<span data-ttu-id="6233f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6233f-119">Header</span></span>|<span data-ttu-id="6233f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6233f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6233f-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6233f-121">Authorization</span></span>|<span data-ttu-id="6233f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6233f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6233f-123">Accept</span><span class="sxs-lookup"><span data-stu-id="6233f-123">Accept</span></span>|<span data-ttu-id="6233f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6233f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6233f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6233f-125">Request body</span></span>
<span data-ttu-id="6233f-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="6233f-126">In the request body, supply a JSON representation for the [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object.</span></span>

<span data-ttu-id="6233f-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="6233f-127">The following table shows the properties that are required when you create the [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span></span>

|<span data-ttu-id="6233f-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6233f-128">Property</span></span>|<span data-ttu-id="6233f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6233f-129">Type</span></span>|<span data-ttu-id="6233f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6233f-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6233f-131">id</span><span class="sxs-lookup"><span data-stu-id="6233f-131">id</span></span>|<span data-ttu-id="6233f-132">String</span><span class="sxs-lookup"><span data-stu-id="6233f-132">String</span></span>|<span data-ttu-id="6233f-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6233f-133">Key of the entity.</span></span>|
|<span data-ttu-id="6233f-134">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6233f-134">unknownDeviceCount</span></span>|<span data-ttu-id="6233f-135">Int32</span><span class="sxs-lookup"><span data-stu-id="6233f-135">Int32</span></span>|<span data-ttu-id="6233f-136">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="6233f-136">Number of unknown devices</span></span>|
|<span data-ttu-id="6233f-137">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6233f-137">notApplicableDeviceCount</span></span>|<span data-ttu-id="6233f-138">Int32</span><span class="sxs-lookup"><span data-stu-id="6233f-138">Int32</span></span>|<span data-ttu-id="6233f-139">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="6233f-139">Number of not applicable devices</span></span>|
|<span data-ttu-id="6233f-140">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6233f-140">compliantDeviceCount</span></span>|<span data-ttu-id="6233f-141">Int32</span><span class="sxs-lookup"><span data-stu-id="6233f-141">Int32</span></span>|<span data-ttu-id="6233f-142">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="6233f-142">Number of compliant devices</span></span>|
|<span data-ttu-id="6233f-143">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6233f-143">remediatedDeviceCount</span></span>|<span data-ttu-id="6233f-144">Int32</span><span class="sxs-lookup"><span data-stu-id="6233f-144">Int32</span></span>|<span data-ttu-id="6233f-145">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="6233f-145">Number of remediated devices</span></span>|
|<span data-ttu-id="6233f-146">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6233f-146">nonCompliantDeviceCount</span></span>|<span data-ttu-id="6233f-147">Int32</span><span class="sxs-lookup"><span data-stu-id="6233f-147">Int32</span></span>|<span data-ttu-id="6233f-148">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="6233f-148">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="6233f-149">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6233f-149">errorDeviceCount</span></span>|<span data-ttu-id="6233f-150">Int32</span><span class="sxs-lookup"><span data-stu-id="6233f-150">Int32</span></span>|<span data-ttu-id="6233f-151">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="6233f-151">Number of error devices</span></span>|
|<span data-ttu-id="6233f-152">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6233f-152">conflictDeviceCount</span></span>|<span data-ttu-id="6233f-153">Int32</span><span class="sxs-lookup"><span data-stu-id="6233f-153">Int32</span></span>|<span data-ttu-id="6233f-154">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="6233f-154">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="6233f-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6233f-155">Response</span></span>
<span data-ttu-id="6233f-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6233f-156">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6233f-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6233f-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="6233f-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6233f-158">Request</span></span>
<span data-ttu-id="6233f-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6233f-159">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurationDeviceStateSummaries
Content-type: application/json
Content-length: 290

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStateSummary",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="6233f-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6233f-160">Response</span></span>
<span data-ttu-id="6233f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6233f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 339

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStateSummary",
  "id": "5db26f5a-6f5a-5db2-5a6f-b25d5a6fb25d",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```




---
title: Actualizar deviceConfigurationDeviceStateSummary
description: Actualice las propiedades de un objeto deviceConfigurationDeviceStateSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1c11471cbf86806e914e939f2385f92440046c05
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849836"
---
# <a name="update-deviceconfigurationdevicestatesummary"></a><span data-ttu-id="f35af-103">Actualizar deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="f35af-103">Update deviceConfigurationDeviceStateSummary</span></span>

> <span data-ttu-id="f35af-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f35af-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f35af-105">Actualice las propiedades de un objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="f35af-105">Update the properties of a [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f35af-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f35af-106">Prerequisites</span></span>
<span data-ttu-id="f35af-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f35af-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f35af-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f35af-109">Permission type</span></span>|<span data-ttu-id="f35af-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f35af-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f35af-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f35af-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f35af-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f35af-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f35af-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f35af-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f35af-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f35af-114">Not supported.</span></span>|
|<span data-ttu-id="f35af-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f35af-115">Application</span></span>|<span data-ttu-id="f35af-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f35af-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f35af-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f35af-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurationDeviceStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="f35af-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f35af-118">Request headers</span></span>
|<span data-ttu-id="f35af-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f35af-119">Header</span></span>|<span data-ttu-id="f35af-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f35af-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f35af-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f35af-121">Authorization</span></span>|<span data-ttu-id="f35af-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f35af-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f35af-123">Accept</span><span class="sxs-lookup"><span data-stu-id="f35af-123">Accept</span></span>|<span data-ttu-id="f35af-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f35af-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f35af-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f35af-125">Request body</span></span>
<span data-ttu-id="f35af-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="f35af-126">In the request body, supply a JSON representation for the [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object.</span></span>

<span data-ttu-id="f35af-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="f35af-127">The following table shows the properties that are required when you create the [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span></span>

|<span data-ttu-id="f35af-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f35af-128">Property</span></span>|<span data-ttu-id="f35af-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f35af-129">Type</span></span>|<span data-ttu-id="f35af-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f35af-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f35af-131">id</span><span class="sxs-lookup"><span data-stu-id="f35af-131">id</span></span>|<span data-ttu-id="f35af-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="f35af-132">String</span></span>|<span data-ttu-id="f35af-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f35af-133">Key of the entity.</span></span>|
|<span data-ttu-id="f35af-134">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f35af-134">unknownDeviceCount</span></span>|<span data-ttu-id="f35af-135">Int32</span><span class="sxs-lookup"><span data-stu-id="f35af-135">Int32</span></span>|<span data-ttu-id="f35af-136">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="f35af-136">Number of unknown devices</span></span>|
|<span data-ttu-id="f35af-137">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f35af-137">notApplicableDeviceCount</span></span>|<span data-ttu-id="f35af-138">Int32</span><span class="sxs-lookup"><span data-stu-id="f35af-138">Int32</span></span>|<span data-ttu-id="f35af-139">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="f35af-139">Number of not applicable devices</span></span>|
|<span data-ttu-id="f35af-140">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f35af-140">compliantDeviceCount</span></span>|<span data-ttu-id="f35af-141">Int32</span><span class="sxs-lookup"><span data-stu-id="f35af-141">Int32</span></span>|<span data-ttu-id="f35af-142">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="f35af-142">Number of compliant devices</span></span>|
|<span data-ttu-id="f35af-143">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f35af-143">remediatedDeviceCount</span></span>|<span data-ttu-id="f35af-144">Int32</span><span class="sxs-lookup"><span data-stu-id="f35af-144">Int32</span></span>|<span data-ttu-id="f35af-145">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="f35af-145">Number of remediated devices</span></span>|
|<span data-ttu-id="f35af-146">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f35af-146">nonCompliantDeviceCount</span></span>|<span data-ttu-id="f35af-147">Int32</span><span class="sxs-lookup"><span data-stu-id="f35af-147">Int32</span></span>|<span data-ttu-id="f35af-148">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="f35af-148">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="f35af-149">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f35af-149">errorDeviceCount</span></span>|<span data-ttu-id="f35af-150">Int32</span><span class="sxs-lookup"><span data-stu-id="f35af-150">Int32</span></span>|<span data-ttu-id="f35af-151">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="f35af-151">Number of error devices</span></span>|
|<span data-ttu-id="f35af-152">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f35af-152">conflictDeviceCount</span></span>|<span data-ttu-id="f35af-153">Int32</span><span class="sxs-lookup"><span data-stu-id="f35af-153">Int32</span></span>|<span data-ttu-id="f35af-154">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="f35af-154">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="f35af-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f35af-155">Response</span></span>
<span data-ttu-id="f35af-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f35af-156">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f35af-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f35af-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="f35af-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f35af-158">Request</span></span>
<span data-ttu-id="f35af-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f35af-159">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="f35af-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f35af-160">Response</span></span>
<span data-ttu-id="f35af-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f35af-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




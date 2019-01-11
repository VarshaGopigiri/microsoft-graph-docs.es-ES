---
title: Actualizar deviceConfigurationDeviceOverview
description: Actualice las propiedades de un objeto deviceConfigurationDeviceOverview.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 60eab56cad999974eb9635cc76c8b4bb4d0e50aa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844999"
---
# <a name="update-deviceconfigurationdeviceoverview"></a><span data-ttu-id="0295b-103">Actualizar deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="0295b-103">Update deviceConfigurationDeviceOverview</span></span>

> <span data-ttu-id="0295b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0295b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0295b-105">Actualice las propiedades de un objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0295b-105">Update the properties of a [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0295b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0295b-106">Prerequisites</span></span>
<span data-ttu-id="0295b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0295b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0295b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0295b-109">Permission type</span></span>|<span data-ttu-id="0295b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0295b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0295b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0295b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="0295b-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0295b-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0295b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0295b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0295b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0295b-114">Not supported.</span></span>|
|<span data-ttu-id="0295b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0295b-115">Application</span></span>|<span data-ttu-id="0295b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0295b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0295b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0295b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatusOverview
```

## <a name="request-headers"></a><span data-ttu-id="0295b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0295b-118">Request headers</span></span>
|<span data-ttu-id="0295b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0295b-119">Header</span></span>|<span data-ttu-id="0295b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0295b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0295b-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="0295b-121">Authorization</span></span>|<span data-ttu-id="0295b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0295b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0295b-123">Accept</span><span class="sxs-lookup"><span data-stu-id="0295b-123">Accept</span></span>|<span data-ttu-id="0295b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="0295b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0295b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0295b-125">Request body</span></span>
<span data-ttu-id="0295b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0295b-126">In the request body, supply a JSON representation for the [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) object.</span></span>

<span data-ttu-id="0295b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="0295b-127">The following table shows the properties that are required when you create the [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).</span></span>

|<span data-ttu-id="0295b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0295b-128">Property</span></span>|<span data-ttu-id="0295b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="0295b-129">Type</span></span>|<span data-ttu-id="0295b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="0295b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0295b-131">id</span><span class="sxs-lookup"><span data-stu-id="0295b-131">id</span></span>|<span data-ttu-id="0295b-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="0295b-132">String</span></span>|<span data-ttu-id="0295b-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0295b-133">Key of the entity.</span></span>|
|<span data-ttu-id="0295b-134">pendingCount</span><span class="sxs-lookup"><span data-stu-id="0295b-134">pendingCount</span></span>|<span data-ttu-id="0295b-135">Int32</span><span class="sxs-lookup"><span data-stu-id="0295b-135">Int32</span></span>|<span data-ttu-id="0295b-136">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="0295b-136">Number of pending devices</span></span>|
|<span data-ttu-id="0295b-137">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="0295b-137">notApplicableCount</span></span>|<span data-ttu-id="0295b-138">Int32</span><span class="sxs-lookup"><span data-stu-id="0295b-138">Int32</span></span>|<span data-ttu-id="0295b-139">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="0295b-139">Number of not applicable devices</span></span>|
|<span data-ttu-id="0295b-140">successCount</span><span class="sxs-lookup"><span data-stu-id="0295b-140">successCount</span></span>|<span data-ttu-id="0295b-141">Int32</span><span class="sxs-lookup"><span data-stu-id="0295b-141">Int32</span></span>|<span data-ttu-id="0295b-142">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="0295b-142">Number of succeeded devices</span></span>|
|<span data-ttu-id="0295b-143">errorCount</span><span class="sxs-lookup"><span data-stu-id="0295b-143">errorCount</span></span>|<span data-ttu-id="0295b-144">Int32</span><span class="sxs-lookup"><span data-stu-id="0295b-144">Int32</span></span>|<span data-ttu-id="0295b-145">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="0295b-145">Number of error devices</span></span>|
|<span data-ttu-id="0295b-146">failedCount</span><span class="sxs-lookup"><span data-stu-id="0295b-146">failedCount</span></span>|<span data-ttu-id="0295b-147">Int32</span><span class="sxs-lookup"><span data-stu-id="0295b-147">Int32</span></span>|<span data-ttu-id="0295b-148">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="0295b-148">Number of failed devices</span></span>|
|<span data-ttu-id="0295b-149">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="0295b-149">lastUpdateDateTime</span></span>|<span data-ttu-id="0295b-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0295b-150">DateTimeOffset</span></span>|<span data-ttu-id="0295b-151">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="0295b-151">Last update time</span></span>|
|<span data-ttu-id="0295b-152">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="0295b-152">configurationVersion</span></span>|<span data-ttu-id="0295b-153">Int32</span><span class="sxs-lookup"><span data-stu-id="0295b-153">Int32</span></span>|<span data-ttu-id="0295b-154">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="0295b-154">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="0295b-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0295b-155">Response</span></span>
<span data-ttu-id="0295b-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0295b-156">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0295b-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0295b-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="0295b-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0295b-158">Request</span></span>
<span data-ttu-id="0295b-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0295b-159">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatusOverview
Content-type: application/json
Content-length: 284

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceOverview",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="0295b-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0295b-160">Response</span></span>
<span data-ttu-id="0295b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0295b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 333

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceOverview",
  "id": "62d48e3a-8e3a-62d4-3a8e-d4623a8ed462",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```




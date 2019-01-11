---
title: Actualizar managedDeviceOverview
description: Actualice las propiedades de un objeto managedDeviceOverview.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: be6b7260b6613ef4396e84670b0c83869804b43c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824937"
---
# <a name="update-manageddeviceoverview"></a><span data-ttu-id="59b11-103">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="59b11-103">Update managedDeviceOverview</span></span>

> <span data-ttu-id="59b11-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="59b11-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="59b11-105">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="59b11-105">Update the properties of a [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="59b11-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="59b11-106">Prerequisites</span></span>
<span data-ttu-id="59b11-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="59b11-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="59b11-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59b11-109">Permission type</span></span>|<span data-ttu-id="59b11-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59b11-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="59b11-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59b11-111">Delegated (work or school account)</span></span>|<span data-ttu-id="59b11-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59b11-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="59b11-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59b11-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="59b11-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59b11-114">Not supported.</span></span>|
|<span data-ttu-id="59b11-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59b11-115">Application</span></span>|<span data-ttu-id="59b11-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59b11-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="59b11-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59b11-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/managedDeviceOverview
```

## <a name="request-headers"></a><span data-ttu-id="59b11-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59b11-118">Request headers</span></span>
|<span data-ttu-id="59b11-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59b11-119">Header</span></span>|<span data-ttu-id="59b11-120">Valor</span><span class="sxs-lookup"><span data-stu-id="59b11-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="59b11-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="59b11-121">Authorization</span></span>|<span data-ttu-id="59b11-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="59b11-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="59b11-123">Accept</span><span class="sxs-lookup"><span data-stu-id="59b11-123">Accept</span></span>|<span data-ttu-id="59b11-124">application/json</span><span class="sxs-lookup"><span data-stu-id="59b11-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="59b11-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59b11-125">Request body</span></span>
<span data-ttu-id="59b11-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="59b11-126">In the request body, supply a JSON representation for the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>

<span data-ttu-id="59b11-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="59b11-127">The following table shows the properties that are required when you create the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span></span>

|<span data-ttu-id="59b11-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59b11-128">Property</span></span>|<span data-ttu-id="59b11-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="59b11-129">Type</span></span>|<span data-ttu-id="59b11-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="59b11-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="59b11-131">id</span><span class="sxs-lookup"><span data-stu-id="59b11-131">id</span></span>|<span data-ttu-id="59b11-132">String</span><span class="sxs-lookup"><span data-stu-id="59b11-132">String</span></span>|<span data-ttu-id="59b11-133">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="59b11-133">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="59b11-134">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="59b11-134">enrolledDeviceCount</span></span>|<span data-ttu-id="59b11-135">Int32</span><span class="sxs-lookup"><span data-stu-id="59b11-135">Int32</span></span>|<span data-ttu-id="59b11-136">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="59b11-136">Total enrolled device count.</span></span> <span data-ttu-id="59b11-137">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="59b11-137">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="59b11-138">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="59b11-138">mdmEnrolledCount</span></span>|<span data-ttu-id="59b11-139">Int32</span><span class="sxs-lookup"><span data-stu-id="59b11-139">Int32</span></span>|<span data-ttu-id="59b11-140">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="59b11-140">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="59b11-141">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="59b11-141">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="59b11-142">Int32</span><span class="sxs-lookup"><span data-stu-id="59b11-142">Int32</span></span>|<span data-ttu-id="59b11-143">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="59b11-143">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="59b11-144">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="59b11-144">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="59b11-145">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="59b11-145">deviceOperatingSystemSummary</span></span>](../resources/intune-devices-deviceoperatingsystemsummary.md)|<span data-ttu-id="59b11-146">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="59b11-146">Device operating system summary.</span></span>|
|<span data-ttu-id="59b11-147">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="59b11-147">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="59b11-148">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="59b11-148">deviceExchangeAccessStateSummary</span></span>](../resources/intune-devices-deviceexchangeaccessstatesummary.md)|<span data-ttu-id="59b11-149">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="59b11-149">Distribution of Exchange Access State in Intune</span></span>|



## <a name="response"></a><span data-ttu-id="59b11-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59b11-150">Response</span></span>
<span data-ttu-id="59b11-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59b11-151">If successful, this method returns a `200 OK` response code and an updated [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="59b11-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59b11-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="59b11-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59b11-153">Request</span></span>
<span data-ttu-id="59b11-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59b11-154">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/managedDeviceOverview
Content-type: application/json
Content-length: 685

{
  "@odata.type": "#microsoft.graph.managedDeviceOverview",
  "enrolledDeviceCount": 3,
  "mdmEnrolledCount": 0,
  "dualEnrolledDeviceCount": 7,
  "deviceOperatingSystemSummary": {
    "@odata.type": "microsoft.graph.deviceOperatingSystemSummary",
    "androidCount": 12,
    "iosCount": 8,
    "macOSCount": 10,
    "windowsMobileCount": 2,
    "windowsCount": 12,
    "unknownCount": 12
  },
  "deviceExchangeAccessStateSummary": {
    "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary",
    "allowedDeviceCount": 2,
    "blockedDeviceCount": 2,
    "quarantinedDeviceCount": 6,
    "unknownDeviceCount": 2,
    "unavailableDeviceCount": 6
  }
}
```

### <a name="response"></a><span data-ttu-id="59b11-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59b11-155">Response</span></span>
<span data-ttu-id="59b11-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="59b11-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 734

{
  "@odata.type": "#microsoft.graph.managedDeviceOverview",
  "id": "42a91653-1653-42a9-5316-a9425316a942",
  "enrolledDeviceCount": 3,
  "mdmEnrolledCount": 0,
  "dualEnrolledDeviceCount": 7,
  "deviceOperatingSystemSummary": {
    "@odata.type": "microsoft.graph.deviceOperatingSystemSummary",
    "androidCount": 12,
    "iosCount": 8,
    "macOSCount": 10,
    "windowsMobileCount": 2,
    "windowsCount": 12,
    "unknownCount": 12
  },
  "deviceExchangeAccessStateSummary": {
    "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary",
    "allowedDeviceCount": 2,
    "blockedDeviceCount": 2,
    "quarantinedDeviceCount": 6,
    "unknownDeviceCount": 2,
    "unavailableDeviceCount": 6
  }
}
```




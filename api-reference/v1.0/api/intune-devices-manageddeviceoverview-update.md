---
title: Actualizar managedDeviceOverview
description: Actualice las propiedades de un objeto managedDeviceOverview.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a4545fb198dcb4c9433a1988392f6388020e37d4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959877"
---
# <a name="update-manageddeviceoverview"></a><span data-ttu-id="ee830-103">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="ee830-103">Update managedDeviceOverview</span></span>

> <span data-ttu-id="ee830-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ee830-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ee830-105">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ee830-105">Update the properties of a [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ee830-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ee830-106">Prerequisites</span></span>
<span data-ttu-id="ee830-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ee830-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ee830-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee830-109">Permission type</span></span>|<span data-ttu-id="ee830-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee830-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ee830-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee830-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ee830-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ee830-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="ee830-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee830-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ee830-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ee830-114">Not supported.</span></span>|
|<span data-ttu-id="ee830-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee830-115">Application</span></span>|<span data-ttu-id="ee830-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ee830-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ee830-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee830-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/managedDeviceOverview
```

## <a name="request-headers"></a><span data-ttu-id="ee830-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee830-118">Request headers</span></span>
|<span data-ttu-id="ee830-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee830-119">Header</span></span>|<span data-ttu-id="ee830-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ee830-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ee830-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ee830-121">Authorization</span></span>|<span data-ttu-id="ee830-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ee830-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ee830-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ee830-123">Accept</span></span>|<span data-ttu-id="ee830-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ee830-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ee830-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ee830-125">Request body</span></span>
<span data-ttu-id="ee830-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ee830-126">In the request body, supply a JSON representation for the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>

<span data-ttu-id="ee830-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ee830-127">The following table shows the properties that are required when you create the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span></span>

|<span data-ttu-id="ee830-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee830-128">Property</span></span>|<span data-ttu-id="ee830-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee830-129">Type</span></span>|<span data-ttu-id="ee830-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee830-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ee830-131">id</span><span class="sxs-lookup"><span data-stu-id="ee830-131">id</span></span>|<span data-ttu-id="ee830-132">String</span><span class="sxs-lookup"><span data-stu-id="ee830-132">String</span></span>|<span data-ttu-id="ee830-133">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="ee830-133">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="ee830-134">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ee830-134">enrolledDeviceCount</span></span>|<span data-ttu-id="ee830-135">Int32</span><span class="sxs-lookup"><span data-stu-id="ee830-135">Int32</span></span>|<span data-ttu-id="ee830-136">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="ee830-136">Total enrolled device count.</span></span> <span data-ttu-id="ee830-137">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="ee830-137">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="ee830-138">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="ee830-138">mdmEnrolledCount</span></span>|<span data-ttu-id="ee830-139">Int32</span><span class="sxs-lookup"><span data-stu-id="ee830-139">Int32</span></span>|<span data-ttu-id="ee830-140">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="ee830-140">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="ee830-141">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ee830-141">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="ee830-142">Int32</span><span class="sxs-lookup"><span data-stu-id="ee830-142">Int32</span></span>|<span data-ttu-id="ee830-143">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="ee830-143">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="ee830-144">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="ee830-144">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="ee830-145">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="ee830-145">deviceOperatingSystemSummary</span></span>](../resources/intune-devices-deviceoperatingsystemsummary.md)|<span data-ttu-id="ee830-146">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ee830-146">Device operating system summary.</span></span>|
|<span data-ttu-id="ee830-147">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="ee830-147">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="ee830-148">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="ee830-148">deviceExchangeAccessStateSummary</span></span>](../resources/intune-devices-deviceexchangeaccessstatesummary.md)|<span data-ttu-id="ee830-149">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="ee830-149">Distribution of Exchange Access State in Intune</span></span>|



## <a name="response"></a><span data-ttu-id="ee830-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee830-150">Response</span></span>
<span data-ttu-id="ee830-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee830-151">If successful, this method returns a `200 OK` response code and an updated [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ee830-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee830-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="ee830-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee830-153">Request</span></span>
<span data-ttu-id="ee830-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ee830-154">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ee830-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee830-155">Response</span></span>
<span data-ttu-id="ee830-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ee830-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




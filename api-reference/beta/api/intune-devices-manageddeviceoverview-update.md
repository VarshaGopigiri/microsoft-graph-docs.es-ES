---
title: Actualizar managedDeviceOverview
description: Actualice las propiedades de un objeto managedDeviceOverview.
author: tfitzmac
ms.openlocfilehash: 004ebc370c0223b807c722bd40ce53021379e00d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349584"
---
# <a name="update-manageddeviceoverview"></a><span data-ttu-id="6947b-103">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="6947b-103">Update managedDeviceOverview</span></span>

> <span data-ttu-id="6947b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6947b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6947b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6947b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6947b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6947b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6947b-107">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6947b-107">Update the properties of a [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6947b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6947b-108">Prerequisites</span></span>
<span data-ttu-id="6947b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6947b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6947b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6947b-111">Permission type</span></span>|<span data-ttu-id="6947b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6947b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6947b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6947b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6947b-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6947b-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="6947b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6947b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6947b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6947b-116">Not supported.</span></span>|
|<span data-ttu-id="6947b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6947b-117">Application</span></span>|<span data-ttu-id="6947b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6947b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6947b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6947b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/managedDeviceOverview
```

## <a name="request-headers"></a><span data-ttu-id="6947b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6947b-120">Request headers</span></span>
|<span data-ttu-id="6947b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6947b-121">Header</span></span>|<span data-ttu-id="6947b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6947b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6947b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6947b-123">Authorization</span></span>|<span data-ttu-id="6947b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6947b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6947b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6947b-125">Accept</span></span>|<span data-ttu-id="6947b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6947b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6947b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6947b-127">Request body</span></span>
<span data-ttu-id="6947b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6947b-128">In the request body, supply a JSON representation for the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>

<span data-ttu-id="6947b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6947b-129">The following table shows the properties that are required when you create the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span></span>

|<span data-ttu-id="6947b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6947b-130">Property</span></span>|<span data-ttu-id="6947b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6947b-131">Type</span></span>|<span data-ttu-id="6947b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6947b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6947b-133">id</span><span class="sxs-lookup"><span data-stu-id="6947b-133">id</span></span>|<span data-ttu-id="6947b-134">String</span><span class="sxs-lookup"><span data-stu-id="6947b-134">String</span></span>|<span data-ttu-id="6947b-135">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="6947b-135">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="6947b-136">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6947b-136">enrolledDeviceCount</span></span>|<span data-ttu-id="6947b-137">Int32</span><span class="sxs-lookup"><span data-stu-id="6947b-137">Int32</span></span>|<span data-ttu-id="6947b-138">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="6947b-138">Total enrolled device count.</span></span> <span data-ttu-id="6947b-139">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="6947b-139">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="6947b-140">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="6947b-140">mdmEnrolledCount</span></span>|<span data-ttu-id="6947b-141">Int32</span><span class="sxs-lookup"><span data-stu-id="6947b-141">Int32</span></span>|<span data-ttu-id="6947b-142">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="6947b-142">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="6947b-143">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6947b-143">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="6947b-144">Int32</span><span class="sxs-lookup"><span data-stu-id="6947b-144">Int32</span></span>|<span data-ttu-id="6947b-145">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="6947b-145">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="6947b-146">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="6947b-146">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="6947b-147">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="6947b-147">deviceOperatingSystemSummary</span></span>](../resources/intune-devices-deviceoperatingsystemsummary.md)|<span data-ttu-id="6947b-148">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6947b-148">Device operating system summary.</span></span>|
|<span data-ttu-id="6947b-149">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="6947b-149">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="6947b-150">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="6947b-150">deviceExchangeAccessStateSummary</span></span>](../resources/intune-devices-deviceexchangeaccessstatesummary.md)|<span data-ttu-id="6947b-151">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="6947b-151">Distribution of Exchange Access State in Intune</span></span>|
|<span data-ttu-id="6947b-152">managedDeviceModelsAndManufacturers</span><span class="sxs-lookup"><span data-stu-id="6947b-152">managedDeviceModelsAndManufacturers</span></span>|[<span data-ttu-id="6947b-153">managedDeviceModelsAndManufacturers</span><span class="sxs-lookup"><span data-stu-id="6947b-153">managedDeviceModelsAndManufacturers</span></span>](../resources/intune-devices-manageddevicemodelsandmanufacturers.md)|<span data-ttu-id="6947b-154">Modelos y fabricantes meatadata para los dispositivos administrados en la cuenta</span><span class="sxs-lookup"><span data-stu-id="6947b-154">Models and Manufactures meatadata for managed devices in the account</span></span>|
|<span data-ttu-id="6947b-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6947b-155">lastModifiedDateTime</span></span>|<span data-ttu-id="6947b-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6947b-156">DateTimeOffset</span></span>|<span data-ttu-id="6947b-157">Hora última fecha de modificación de información general de dispositivos</span><span class="sxs-lookup"><span data-stu-id="6947b-157">Last modified date time of device overview</span></span>|



## <a name="response"></a><span data-ttu-id="6947b-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6947b-158">Response</span></span>
<span data-ttu-id="6947b-159">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6947b-159">If successful, this method returns a `200 OK` response code and an updated [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6947b-160">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6947b-160">Example</span></span>
### <a name="request"></a><span data-ttu-id="6947b-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6947b-161">Request</span></span>
<span data-ttu-id="6947b-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6947b-162">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/managedDeviceOverview
Content-type: application/json
Content-length: 947

{
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
  },
  "managedDeviceModelsAndManufacturers": {
    "@odata.type": "microsoft.graph.managedDeviceModelsAndManufacturers",
    "deviceModels": [
      "Device Models value"
    ],
    "deviceManufacturers": [
      "Device Manufacturers value"
    ]
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```

### <a name="response"></a><span data-ttu-id="6947b-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6947b-163">Response</span></span>
<span data-ttu-id="6947b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6947b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1056

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
  },
  "managedDeviceModelsAndManufacturers": {
    "@odata.type": "microsoft.graph.managedDeviceModelsAndManufacturers",
    "deviceModels": [
      "Device Models value"
    ],
    "deviceManufacturers": [
      "Device Manufacturers value"
    ]
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```






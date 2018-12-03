---
title: Actualizar managedDeviceMobileAppConfigurationDeviceSummary
description: Actualice las propiedades y las relaciones de un objeto managedDeviceMobileAppConfigurationDeviceSummary.
ms.openlocfilehash: cb1f021ad5c41ac513c5e70ae9053c50a8f9b821
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029358"
---
# <a name="update-manageddevicemobileappconfigurationdevicesummary"></a><span data-ttu-id="9d4aa-103">Actualizar managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="9d4aa-103">Update managedDeviceMobileAppConfigurationDeviceSummary</span></span>

> <span data-ttu-id="9d4aa-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9d4aa-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9d4aa-105">Actualice las propiedades y las relaciones de un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="9d4aa-105">Update the properties of a [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9d4aa-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9d4aa-106">Prerequisites</span></span>
<span data-ttu-id="9d4aa-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9d4aa-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9d4aa-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9d4aa-109">Permission type</span></span>|<span data-ttu-id="9d4aa-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9d4aa-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9d4aa-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9d4aa-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9d4aa-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d4aa-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9d4aa-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9d4aa-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9d4aa-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d4aa-114">Not supported.</span></span>|
|<span data-ttu-id="9d4aa-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9d4aa-115">Application</span></span>|<span data-ttu-id="9d4aa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d4aa-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9d4aa-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9d4aa-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatusSummary
```

## <a name="request-headers"></a><span data-ttu-id="9d4aa-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9d4aa-118">Request headers</span></span>
|<span data-ttu-id="9d4aa-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d4aa-119">Header</span></span>|<span data-ttu-id="9d4aa-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9d4aa-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9d4aa-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="9d4aa-121">Authorization</span></span>|<span data-ttu-id="9d4aa-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9d4aa-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9d4aa-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9d4aa-123">Accept</span></span>|<span data-ttu-id="9d4aa-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9d4aa-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9d4aa-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9d4aa-125">Request body</span></span>
<span data-ttu-id="9d4aa-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="9d4aa-126">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>

<span data-ttu-id="9d4aa-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="9d4aa-127">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span></span>

|<span data-ttu-id="9d4aa-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9d4aa-128">Property</span></span>|<span data-ttu-id="9d4aa-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d4aa-129">Type</span></span>|<span data-ttu-id="9d4aa-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d4aa-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9d4aa-131">id</span><span class="sxs-lookup"><span data-stu-id="9d4aa-131">id</span></span>|<span data-ttu-id="9d4aa-132">String</span><span class="sxs-lookup"><span data-stu-id="9d4aa-132">String</span></span>|<span data-ttu-id="9d4aa-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9d4aa-133">Key of the entity.</span></span>|
|<span data-ttu-id="9d4aa-134">pendingCount</span><span class="sxs-lookup"><span data-stu-id="9d4aa-134">pendingCount</span></span>|<span data-ttu-id="9d4aa-135">Int32</span><span class="sxs-lookup"><span data-stu-id="9d4aa-135">Int32</span></span>|<span data-ttu-id="9d4aa-136">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="9d4aa-136">Number of pending devices</span></span>|
|<span data-ttu-id="9d4aa-137">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="9d4aa-137">notApplicableCount</span></span>|<span data-ttu-id="9d4aa-138">Int32</span><span class="sxs-lookup"><span data-stu-id="9d4aa-138">Int32</span></span>|<span data-ttu-id="9d4aa-139">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="9d4aa-139">Number of not applicable devices</span></span>|
|<span data-ttu-id="9d4aa-140">successCount</span><span class="sxs-lookup"><span data-stu-id="9d4aa-140">successCount</span></span>|<span data-ttu-id="9d4aa-141">Int32</span><span class="sxs-lookup"><span data-stu-id="9d4aa-141">Int32</span></span>|<span data-ttu-id="9d4aa-142">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="9d4aa-142">Number of succeeded devices</span></span>|
|<span data-ttu-id="9d4aa-143">errorCount</span><span class="sxs-lookup"><span data-stu-id="9d4aa-143">errorCount</span></span>|<span data-ttu-id="9d4aa-144">Int32</span><span class="sxs-lookup"><span data-stu-id="9d4aa-144">Int32</span></span>|<span data-ttu-id="9d4aa-145">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="9d4aa-145">Number of error devices</span></span>|
|<span data-ttu-id="9d4aa-146">failedCount</span><span class="sxs-lookup"><span data-stu-id="9d4aa-146">failedCount</span></span>|<span data-ttu-id="9d4aa-147">Int32</span><span class="sxs-lookup"><span data-stu-id="9d4aa-147">Int32</span></span>|<span data-ttu-id="9d4aa-148">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="9d4aa-148">Number of failed devices</span></span>|
|<span data-ttu-id="9d4aa-149">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="9d4aa-149">lastUpdateDateTime</span></span>|<span data-ttu-id="9d4aa-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9d4aa-150">DateTimeOffset</span></span>|<span data-ttu-id="9d4aa-151">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="9d4aa-151">Last update time</span></span>|
|<span data-ttu-id="9d4aa-152">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="9d4aa-152">configurationVersion</span></span>|<span data-ttu-id="9d4aa-153">Int32</span><span class="sxs-lookup"><span data-stu-id="9d4aa-153">Int32</span></span>|<span data-ttu-id="9d4aa-154">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="9d4aa-154">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="9d4aa-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d4aa-155">Response</span></span>
<span data-ttu-id="9d4aa-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d4aa-156">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9d4aa-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d4aa-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="9d4aa-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9d4aa-158">Request</span></span>
<span data-ttu-id="9d4aa-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d4aa-159">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatusSummary
Content-type: application/json
Content-length: 299

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceSummary",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="9d4aa-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d4aa-160">Response</span></span>
<span data-ttu-id="9d4aa-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9d4aa-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 348

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceSummary",
  "id": "9997c455-c455-9997-55c4-979955c49799",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```



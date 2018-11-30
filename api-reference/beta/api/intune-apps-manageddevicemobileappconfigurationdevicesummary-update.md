---
title: Actualizar managedDeviceMobileAppConfigurationDeviceSummary
description: Actualice las propiedades y las relaciones de un objeto managedDeviceMobileAppConfigurationDeviceSummary.
ms.openlocfilehash: bc5c7642daa408186e05dd06c7630a8c8431df1f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084896"
---
# <a name="update-manageddevicemobileappconfigurationdevicesummary"></a><span data-ttu-id="6d733-103">Actualizar managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="6d733-103">Update managedDeviceMobileAppConfigurationDeviceSummary</span></span>

> <span data-ttu-id="6d733-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6d733-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6d733-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6d733-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6d733-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6d733-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6d733-107">Actualice las propiedades y las relaciones de un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="6d733-107">Update the properties of a [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6d733-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6d733-108">Prerequisites</span></span>
<span data-ttu-id="6d733-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6d733-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6d733-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d733-111">Permission type</span></span>|<span data-ttu-id="6d733-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d733-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6d733-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d733-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6d733-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6d733-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6d733-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d733-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6d733-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d733-116">Not supported.</span></span>|
|<span data-ttu-id="6d733-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d733-117">Application</span></span>|<span data-ttu-id="6d733-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d733-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6d733-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d733-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatusSummary
```

## <a name="request-headers"></a><span data-ttu-id="6d733-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d733-120">Request headers</span></span>
|<span data-ttu-id="6d733-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d733-121">Header</span></span>|<span data-ttu-id="6d733-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6d733-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6d733-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6d733-123">Authorization</span></span>|<span data-ttu-id="6d733-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6d733-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6d733-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6d733-125">Accept</span></span>|<span data-ttu-id="6d733-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6d733-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6d733-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d733-127">Request body</span></span>
<span data-ttu-id="6d733-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="6d733-128">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>

<span data-ttu-id="6d733-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="6d733-129">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span></span>

|<span data-ttu-id="6d733-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6d733-130">Property</span></span>|<span data-ttu-id="6d733-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d733-131">Type</span></span>|<span data-ttu-id="6d733-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d733-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6d733-133">id</span><span class="sxs-lookup"><span data-stu-id="6d733-133">id</span></span>|<span data-ttu-id="6d733-134">String</span><span class="sxs-lookup"><span data-stu-id="6d733-134">String</span></span>|<span data-ttu-id="6d733-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6d733-135">Key of the entity.</span></span>|
|<span data-ttu-id="6d733-136">pendingCount</span><span class="sxs-lookup"><span data-stu-id="6d733-136">pendingCount</span></span>|<span data-ttu-id="6d733-137">Int32</span><span class="sxs-lookup"><span data-stu-id="6d733-137">Int32</span></span>|<span data-ttu-id="6d733-138">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="6d733-138">Number of pending devices</span></span>|
|<span data-ttu-id="6d733-139">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="6d733-139">notApplicableCount</span></span>|<span data-ttu-id="6d733-140">Int32</span><span class="sxs-lookup"><span data-stu-id="6d733-140">Int32</span></span>|<span data-ttu-id="6d733-141">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="6d733-141">Number of not applicable devices</span></span>|
|<span data-ttu-id="6d733-142">notApplicablePlatformCount</span><span class="sxs-lookup"><span data-stu-id="6d733-142">notApplicablePlatformCount</span></span>|<span data-ttu-id="6d733-143">Int32</span><span class="sxs-lookup"><span data-stu-id="6d733-143">Int32</span></span>|<span data-ttu-id="6d733-144">Número de dispositivos no aplicables debido a la plataforma de error de coincidencia y la directiva</span><span class="sxs-lookup"><span data-stu-id="6d733-144">Number of not applicable devices due to mismatch platform and policy</span></span>|
|<span data-ttu-id="6d733-145">successCount</span><span class="sxs-lookup"><span data-stu-id="6d733-145">successCount</span></span>|<span data-ttu-id="6d733-146">Int32</span><span class="sxs-lookup"><span data-stu-id="6d733-146">Int32</span></span>|<span data-ttu-id="6d733-147">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="6d733-147">Number of succeeded devices</span></span>|
|<span data-ttu-id="6d733-148">errorCount</span><span class="sxs-lookup"><span data-stu-id="6d733-148">errorCount</span></span>|<span data-ttu-id="6d733-149">Int32</span><span class="sxs-lookup"><span data-stu-id="6d733-149">Int32</span></span>|<span data-ttu-id="6d733-150">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="6d733-150">Number of error devices</span></span>|
|<span data-ttu-id="6d733-151">failedCount</span><span class="sxs-lookup"><span data-stu-id="6d733-151">failedCount</span></span>|<span data-ttu-id="6d733-152">Int32</span><span class="sxs-lookup"><span data-stu-id="6d733-152">Int32</span></span>|<span data-ttu-id="6d733-153">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="6d733-153">Number of failed devices</span></span>|
|<span data-ttu-id="6d733-154">conflictCount</span><span class="sxs-lookup"><span data-stu-id="6d733-154">conflictCount</span></span>|<span data-ttu-id="6d733-155">Int32</span><span class="sxs-lookup"><span data-stu-id="6d733-155">Int32</span></span>|<span data-ttu-id="6d733-156">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="6d733-156">Number of devices in conflict</span></span>|
|<span data-ttu-id="6d733-157">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="6d733-157">lastUpdateDateTime</span></span>|<span data-ttu-id="6d733-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6d733-158">DateTimeOffset</span></span>|<span data-ttu-id="6d733-159">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="6d733-159">Last update time</span></span>|
|<span data-ttu-id="6d733-160">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="6d733-160">configurationVersion</span></span>|<span data-ttu-id="6d733-161">Int32</span><span class="sxs-lookup"><span data-stu-id="6d733-161">Int32</span></span>|<span data-ttu-id="6d733-162">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="6d733-162">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="6d733-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d733-163">Response</span></span>
<span data-ttu-id="6d733-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d733-164">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6d733-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d733-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="6d733-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d733-166">Request</span></span>
<span data-ttu-id="6d733-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d733-167">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatusSummary
Content-type: application/json
Content-length: 273

{
  "pendingCount": 12,
  "notApplicableCount": 2,
  "notApplicablePlatformCount": 10,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "conflictCount": 13,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="6d733-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d733-168">Response</span></span>
<span data-ttu-id="6d733-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6d733-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 409

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceSummary",
  "id": "9997c455-c455-9997-55c4-979955c49799",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "notApplicablePlatformCount": 10,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "conflictCount": 13,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```






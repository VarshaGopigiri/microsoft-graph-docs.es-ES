---
title: Actualizar deviceManagement
description: Actualice las propiedades de un objeto deviceManagement.
ms.openlocfilehash: f63e9b717f912e255abccedf809772590eb44d1f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029790"
---
# <a name="update-devicemanagement"></a><span data-ttu-id="0d75c-103">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="0d75c-103">Update deviceManagement</span></span>

> <span data-ttu-id="0d75c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0d75c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0d75c-105">Actualice las propiedades de un objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="0d75c-105">Update the properties of a [deviceManagement](../resources/intune-shared-devicemanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0d75c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0d75c-106">Prerequisites</span></span>
<span data-ttu-id="0d75c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0d75c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0d75c-109">Permisos&nbsp;tipo&nbsp;(por&nbsp;flujo de trabajo)</span><span class="sxs-lookup"><span data-stu-id="0d75c-109">Permission&nbsp;type&nbsp;(by&nbsp;workflow)</span></span> | <span data-ttu-id="0d75c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0d75c-110">Permissions (from most to least privileged)</span></span> |
|:---|:---|
| <span data-ttu-id="0d75c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0d75c-111">Delegated (work or school account)</span></span> |
| <span data-ttu-id="0d75c-112">&nbsp;&nbsp; Auditoría</span><span class="sxs-lookup"><span data-stu-id="0d75c-112">&nbsp; &nbsp; Auditing</span></span> | <span data-ttu-id="0d75c-113">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-113">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-114">&nbsp;&nbsp; Los términos de la empresa</span><span class="sxs-lookup"><span data-stu-id="0d75c-114">&nbsp; &nbsp; Company terms</span></span> | <span data-ttu-id="0d75c-115">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-115">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-116">&nbsp;&nbsp; Inscripción corporativa</span><span class="sxs-lookup"><span data-stu-id="0d75c-116">&nbsp; &nbsp; Corporate enrollment</span></span> | <span data-ttu-id="0d75c-117">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-117">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
| <span data-ttu-id="0d75c-118">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0d75c-118">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="0d75c-119">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-119">DeviceManagementConfiguration.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-120">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="0d75c-120">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="0d75c-121">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-121">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-122">&nbsp;&nbsp; Protección de extremo</span><span class="sxs-lookup"><span data-stu-id="0d75c-122">&nbsp; &nbsp; Endpoint protection</span></span> | <span data-ttu-id="0d75c-123">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-123">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-124">&nbsp;&nbsp; Notificación</span><span class="sxs-lookup"><span data-stu-id="0d75c-124">&nbsp; &nbsp; Notification</span></span> | <span data-ttu-id="0d75c-125">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-125">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-126">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="0d75c-126">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="0d75c-127">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-127">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-128">&nbsp;&nbsp; Control de acceso basado en roles</span><span class="sxs-lookup"><span data-stu-id="0d75c-128">&nbsp; &nbsp; Role-based access control</span></span> | <span data-ttu-id="0d75c-129">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-129">DeviceManagementRBAC.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-130">&nbsp;&nbsp; Asistencia remota</span><span class="sxs-lookup"><span data-stu-id="0d75c-130">&nbsp; &nbsp; Remote assistance</span></span> | <span data-ttu-id="0d75c-131">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-131">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-132">&nbsp;&nbsp; Gestión de gastos de telecomunicaciones</span><span class="sxs-lookup"><span data-stu-id="0d75c-132">&nbsp; &nbsp; Telecom expense management</span></span> | <span data-ttu-id="0d75c-133">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-133">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-134">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="0d75c-134">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="0d75c-135">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-135">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-136">&nbsp;&nbsp; Protección de la información de Windows</span><span class="sxs-lookup"><span data-stu-id="0d75c-136">&nbsp; &nbsp; Windows Information Protection</span></span> | <span data-ttu-id="0d75c-137">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d75c-137">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="0d75c-138">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0d75c-138">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0d75c-139">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0d75c-139">Not supported.</span></span>|
| <span data-ttu-id="0d75c-140">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0d75c-140">Application</span></span> | <span data-ttu-id="0d75c-141">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0d75c-141">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0d75c-142">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0d75c-142">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement
```

## <a name="request-headers"></a><span data-ttu-id="0d75c-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0d75c-143">Request headers</span></span>
|<span data-ttu-id="0d75c-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d75c-144">Header</span></span>|<span data-ttu-id="0d75c-145">Valor</span><span class="sxs-lookup"><span data-stu-id="0d75c-145">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0d75c-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="0d75c-146">Authorization</span></span>|<span data-ttu-id="0d75c-147">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0d75c-147">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0d75c-148">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0d75c-148">Accept</span></span>|<span data-ttu-id="0d75c-149">application/json</span><span class="sxs-lookup"><span data-stu-id="0d75c-149">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0d75c-150">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0d75c-150">Request body</span></span>
<span data-ttu-id="0d75c-151">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="0d75c-151">In the request body, supply a JSON representation for the [deviceManagement](../resources/intune-shared-devicemanagement.md) object.</span></span>

<span data-ttu-id="0d75c-152">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="0d75c-152">The following table shows the properties that are required when you create the [deviceManagement](../resources/intune-shared-devicemanagement.md).</span></span>

|<span data-ttu-id="0d75c-153">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0d75c-153">Property</span></span>|<span data-ttu-id="0d75c-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d75c-154">Type</span></span>|<span data-ttu-id="0d75c-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d75c-155">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0d75c-156">id</span><span class="sxs-lookup"><span data-stu-id="0d75c-156">id</span></span>|<span data-ttu-id="0d75c-157">String</span><span class="sxs-lookup"><span data-stu-id="0d75c-157">String</span></span>|<span data-ttu-id="0d75c-158">Identificador único del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d75c-158">Unique Identifier for the device</span></span>|
|<span data-ttu-id="0d75c-159">**Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="0d75c-159">**Device configuration**</span></span>|
|<span data-ttu-id="0d75c-160">configuración</span><span class="sxs-lookup"><span data-stu-id="0d75c-160">settings</span></span>|[<span data-ttu-id="0d75c-161">deviceManagementSettings</span><span class="sxs-lookup"><span data-stu-id="0d75c-161">deviceManagementSettings</span></span>](../resources/intune-deviceconfig-devicemanagementsettings.md)|<span data-ttu-id="0d75c-162">Configuración de niveles de cuenta.</span><span class="sxs-lookup"><span data-stu-id="0d75c-162">Account level settings.</span></span>|
|<span data-ttu-id="0d75c-163">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="0d75c-163">**Device management**</span></span>|
|<span data-ttu-id="0d75c-164">subscriptionState</span><span class="sxs-lookup"><span data-stu-id="0d75c-164">subscriptionState</span></span>|[<span data-ttu-id="0d75c-165">deviceManagementSubscriptionState</span><span class="sxs-lookup"><span data-stu-id="0d75c-165">deviceManagementSubscriptionState</span></span>](../resources/intune-devices-devicemanagementsubscriptionstate.md)|<span data-ttu-id="0d75c-166">Estado de suscripción de administración de dispositivos móviles del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="0d75c-166">Tenant mobile device management subscription state.</span></span> <span data-ttu-id="0d75c-167">Los valores posibles son: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked`, `lockedOut`.</span><span class="sxs-lookup"><span data-stu-id="0d75c-167">The possible values are: `pending`, `active`, `warning`, `disabled`, `deleted`, `blocked`, `lockedOut`.</span></span>|
|<span data-ttu-id="0d75c-168">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="0d75c-168">**Onboarding**</span></span>|
|<span data-ttu-id="0d75c-169">intuneBrand</span><span class="sxs-lookup"><span data-stu-id="0d75c-169">intuneBrand</span></span>|[<span data-ttu-id="0d75c-170">intuneBrand</span><span class="sxs-lookup"><span data-stu-id="0d75c-170">intuneBrand</span></span>](../resources/intune-onboarding-intunebrand.md)|<span data-ttu-id="0d75c-171">intuneBrand contiene datos que se usan para personalizar las aplicaciones del Portal de empresa, así como el portal web del usuario final.</span><span class="sxs-lookup"><span data-stu-id="0d75c-171">intuneBrand contains data which is used in customizing the appearance of the Company Portal applications as well as the end user web portal.</span></span>|

<span data-ttu-id="0d75c-172">Compatibilidad con propiedades de cuerpo de solicitud varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0d75c-172">Request body property support varies according to workflow.</span></span>

## <a name="response"></a><span data-ttu-id="0d75c-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d75c-173">Response</span></span>
<span data-ttu-id="0d75c-174">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagement](../resources/intune-shared-devicemanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d75c-174">If successful, this method returns a `200 OK` response code and an updated [deviceManagement](../resources/intune-shared-devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0d75c-175">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d75c-175">Example</span></span>

### <a name="request"></a><span data-ttu-id="0d75c-176">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0d75c-176">Request</span></span>
<span data-ttu-id="0d75c-177">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0d75c-177">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement
Content-type: application/json
Content-length: 751

{
  "subscriptionState": "active",
  "subscriptions": "intune",
  "adminConsent": {
    "@odata.type": "microsoft.graph.adminConsent",
    "shareAPNSData": "granted"
  },
  "deviceProtectionOverview": {
    "@odata.type": "microsoft.graph.deviceProtectionOverview",
    "totalReportedDeviceCount": 8,
    "inactiveThreatAgentDeviceCount": 14,
    "unknownStateThreatAgentDeviceCount": 2,
    "pendingSignatureUpdateDeviceCount": 1,
    "cleanDeviceCount": 0,
    "pendingFullScanDeviceCount": 10,
    "pendingRestartDeviceCount": 9,
    "pendingManualStepsDeviceCount": 13,
    "pendingOfflineScanDeviceCount": 13,
    "criticalFailuresDeviceCount": 11
  },
  "accountMoveCompletionDateTime": "2017-01-01T00:01:17.9006709-08:00"
}
```

### <a name="response"></a><span data-ttu-id="0d75c-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d75c-178">Response</span></span>

<span data-ttu-id="0d75c-179">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d75c-179">Here is an example of the response.</span></span> <span data-ttu-id="0d75c-180">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="0d75c-180">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="0d75c-181">Propiedades devueltas varían según el flujo de trabajo y el contexto.</span><span class="sxs-lookup"><span data-stu-id="0d75c-181">Returned properties vary according to workflow and context.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 855

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "0b283420-3420-0b28-2034-280b2034280b",
  "subscriptionState": "active",
  "subscriptions": "intune",
  "adminConsent": {
    "@odata.type": "microsoft.graph.adminConsent",
    "shareAPNSData": "granted"
  },
  "deviceProtectionOverview": {
    "@odata.type": "microsoft.graph.deviceProtectionOverview",
    "totalReportedDeviceCount": 8,
    "inactiveThreatAgentDeviceCount": 14,
    "unknownStateThreatAgentDeviceCount": 2,
    "pendingSignatureUpdateDeviceCount": 1,
    "cleanDeviceCount": 0,
    "pendingFullScanDeviceCount": 10,
    "pendingRestartDeviceCount": 9,
    "pendingManualStepsDeviceCount": 13,
    "pendingOfflineScanDeviceCount": 13,
    "criticalFailuresDeviceCount": 11
  },
  "accountMoveCompletionDateTime": "2017-01-01T00:01:17.9006709-08:00"
}
```




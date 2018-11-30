---
title: Obtener deviceManagement
description: Lea las propiedades y las relaciones del objeto deviceManagement.
ms.openlocfilehash: a268a44d37f405bc5ee31c8d2f9a02df9085e5ce
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030658"
---
# <a name="get-devicemanagement"></a><span data-ttu-id="4d466-103">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="4d466-103">Get deviceManagement</span></span>

> <span data-ttu-id="4d466-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4d466-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4d466-105">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="4d466-105">Read properties and relationships of the [deviceManagement](../resources/intune-shared-devicemanagement.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4d466-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4d466-106">Prerequisites</span></span>
<span data-ttu-id="4d466-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d466-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="4d466-109">Permisos&nbsp;tipo&nbsp;(por&nbsp;flujo de trabajo)</span><span class="sxs-lookup"><span data-stu-id="4d466-109">Permission&nbsp;type&nbsp;(by&nbsp;workflow)</span></span> | <span data-ttu-id="4d466-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d466-110">Permissions (from most to least privileged)</span></span> |
|:---|:---|
| <span data-ttu-id="4d466-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d466-111">Delegated (work or school account)</span></span> | |
| <span data-ttu-id="4d466-112">&nbsp;&nbsp; Auditoría</span><span class="sxs-lookup"><span data-stu-id="4d466-112">&nbsp; &nbsp; Auditing</span></span> | <span data-ttu-id="4d466-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="4d466-114">&nbsp;&nbsp; Los términos de la empresa</span><span class="sxs-lookup"><span data-stu-id="4d466-114">&nbsp; &nbsp; Company terms</span></span> | <span data-ttu-id="4d466-115">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-115">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="4d466-116">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4d466-116">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="4d466-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="4d466-118">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="4d466-118">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="4d466-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="4d466-120">&nbsp;&nbsp; Inscripción</span><span class="sxs-lookup"><span data-stu-id="4d466-120">&nbsp; &nbsp; Enrollment</span></span> | <span data-ttu-id="4d466-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="4d466-122">&nbsp;&nbsp; Notificación</span><span class="sxs-lookup"><span data-stu-id="4d466-122">&nbsp; &nbsp; Notification</span></span> | <span data-ttu-id="4d466-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="4d466-124">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="4d466-124">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="4d466-125">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-125">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="4d466-126">&nbsp;&nbsp; RBAC</span><span class="sxs-lookup"><span data-stu-id="4d466-126">&nbsp; &nbsp; RBAC</span></span> | <span data-ttu-id="4d466-127">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-127">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span> |
| <span data-ttu-id="4d466-128">&nbsp;&nbsp; Asistencia remota</span><span class="sxs-lookup"><span data-stu-id="4d466-128">&nbsp; &nbsp; Remote assistance</span></span> | <span data-ttu-id="4d466-129">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-129">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="4d466-130">&nbsp;&nbsp; Gestión de gastos de telecomunicaciones</span><span class="sxs-lookup"><span data-stu-id="4d466-130">&nbsp; &nbsp; Telecom expense management</span></span> | <span data-ttu-id="4d466-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="4d466-132">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="4d466-132">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="4d466-133">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-133">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
| <span data-ttu-id="4d466-134">&nbsp;&nbsp; Protección de la información de Windows</span><span class="sxs-lookup"><span data-stu-id="4d466-134">&nbsp; &nbsp; Windows Information Protection</span></span> | <span data-ttu-id="4d466-135">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="4d466-135">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
| <span data-ttu-id="4d466-136">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d466-136">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d466-137">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d466-137">Not supported.</span></span>|
| <span data-ttu-id="4d466-138">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d466-138">Application</span></span> | <span data-ttu-id="4d466-139">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d466-139">Not supported.</span></span> |



## <a name="http-request"></a><span data-ttu-id="4d466-140">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d466-140">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="4d466-141">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4d466-141">Optional query parameters</span></span>
<span data-ttu-id="4d466-142">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d466-142">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4d466-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d466-143">Request headers</span></span>
|<span data-ttu-id="4d466-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d466-144">Header</span></span>|<span data-ttu-id="4d466-145">Valor</span><span class="sxs-lookup"><span data-stu-id="4d466-145">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4d466-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d466-146">Authorization</span></span>|<span data-ttu-id="4d466-147">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4d466-147">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4d466-148">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4d466-148">Accept</span></span>|<span data-ttu-id="4d466-149">application/json</span><span class="sxs-lookup"><span data-stu-id="4d466-149">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4d466-150">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d466-150">Request body</span></span>
<span data-ttu-id="4d466-151">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4d466-151">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4d466-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d466-152">Response</span></span>
<span data-ttu-id="4d466-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagement](../resources/intune-shared-devicemanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d466-153">If successful, this method returns a `200 OK` response code and [deviceManagement](../resources/intune-shared-devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4d466-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d466-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="4d466-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d466-155">Request</span></span>
<span data-ttu-id="4d466-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d466-156">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement
```

### <a name="response"></a><span data-ttu-id="4d466-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d466-157">Response</span></span>
<span data-ttu-id="4d466-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d466-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 918

{
  "value": {
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
}
```




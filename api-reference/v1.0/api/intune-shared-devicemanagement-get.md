---
title: Obtener deviceManagement
description: Lea las propiedades y las relaciones del objeto deviceManagement.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: af4dc08832b09387774ad3ad1642b0103b3b7db9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936931"
---
# <a name="get-devicemanagement"></a><span data-ttu-id="b0f9f-103">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="b0f9f-103">Get deviceManagement</span></span>

> <span data-ttu-id="b0f9f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b0f9f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b0f9f-105">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="b0f9f-105">Read properties and relationships of the [deviceManagement](../resources/intune-shared-devicemanagement.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b0f9f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b0f9f-106">Prerequisites</span></span>
<span data-ttu-id="b0f9f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b0f9f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b0f9f-109">Permisos&nbsp;tipo&nbsp;(por&nbsp;flujo de trabajo)</span><span class="sxs-lookup"><span data-stu-id="b0f9f-109">Permission&nbsp;type&nbsp;(by&nbsp;workflow)</span></span> | <span data-ttu-id="b0f9f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b0f9f-110">Permissions (from most to least privileged)</span></span> |
|:---|:---|
| <span data-ttu-id="b0f9f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b0f9f-111">Delegated (work or school account)</span></span> | |
| <span data-ttu-id="b0f9f-112">&nbsp;&nbsp; Auditoría</span><span class="sxs-lookup"><span data-stu-id="b0f9f-112">&nbsp; &nbsp; Auditing</span></span> | <span data-ttu-id="b0f9f-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="b0f9f-114">&nbsp;&nbsp; Los términos de la empresa</span><span class="sxs-lookup"><span data-stu-id="b0f9f-114">&nbsp; &nbsp; Company terms</span></span> | <span data-ttu-id="b0f9f-115">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-115">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="b0f9f-116">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b0f9f-116">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="b0f9f-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="b0f9f-118">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="b0f9f-118">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="b0f9f-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="b0f9f-120">&nbsp;&nbsp; Inscripción</span><span class="sxs-lookup"><span data-stu-id="b0f9f-120">&nbsp; &nbsp; Enrollment</span></span> | <span data-ttu-id="b0f9f-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="b0f9f-122">&nbsp;&nbsp; Notificación</span><span class="sxs-lookup"><span data-stu-id="b0f9f-122">&nbsp; &nbsp; Notification</span></span> | <span data-ttu-id="b0f9f-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="b0f9f-124">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="b0f9f-124">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="b0f9f-125">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-125">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="b0f9f-126">&nbsp;&nbsp; RBAC</span><span class="sxs-lookup"><span data-stu-id="b0f9f-126">&nbsp; &nbsp; RBAC</span></span> | <span data-ttu-id="b0f9f-127">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-127">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span> |
| <span data-ttu-id="b0f9f-128">&nbsp;&nbsp; Asistencia remota</span><span class="sxs-lookup"><span data-stu-id="b0f9f-128">&nbsp; &nbsp; Remote assistance</span></span> | <span data-ttu-id="b0f9f-129">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-129">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="b0f9f-130">&nbsp;&nbsp; Gestión de gastos de telecomunicaciones</span><span class="sxs-lookup"><span data-stu-id="b0f9f-130">&nbsp; &nbsp; Telecom expense management</span></span> | <span data-ttu-id="b0f9f-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="b0f9f-132">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="b0f9f-132">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="b0f9f-133">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-133">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
| <span data-ttu-id="b0f9f-134">&nbsp;&nbsp; Protección de la información de Windows</span><span class="sxs-lookup"><span data-stu-id="b0f9f-134">&nbsp; &nbsp; Windows Information Protection</span></span> | <span data-ttu-id="b0f9f-135">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="b0f9f-135">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
| <span data-ttu-id="b0f9f-136">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b0f9f-136">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b0f9f-137">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b0f9f-137">Not supported.</span></span>|
| <span data-ttu-id="b0f9f-138">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b0f9f-138">Application</span></span> | <span data-ttu-id="b0f9f-139">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b0f9f-139">Not supported.</span></span> |



## <a name="http-request"></a><span data-ttu-id="b0f9f-140">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b0f9f-140">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b0f9f-141">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b0f9f-141">Optional query parameters</span></span>
<span data-ttu-id="b0f9f-142">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b0f9f-142">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b0f9f-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b0f9f-143">Request headers</span></span>
|<span data-ttu-id="b0f9f-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0f9f-144">Header</span></span>|<span data-ttu-id="b0f9f-145">Valor</span><span class="sxs-lookup"><span data-stu-id="b0f9f-145">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b0f9f-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="b0f9f-146">Authorization</span></span>|<span data-ttu-id="b0f9f-147">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b0f9f-147">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b0f9f-148">Accept</span><span class="sxs-lookup"><span data-stu-id="b0f9f-148">Accept</span></span>|<span data-ttu-id="b0f9f-149">application/json</span><span class="sxs-lookup"><span data-stu-id="b0f9f-149">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b0f9f-150">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b0f9f-150">Request body</span></span>
<span data-ttu-id="b0f9f-151">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b0f9f-151">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b0f9f-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b0f9f-152">Response</span></span>
<span data-ttu-id="b0f9f-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagement](../resources/intune-shared-devicemanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b0f9f-153">If successful, this method returns a `200 OK` response code and [deviceManagement](../resources/intune-shared-devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b0f9f-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b0f9f-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="b0f9f-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b0f9f-155">Request</span></span>
<span data-ttu-id="b0f9f-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b0f9f-156">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement
```

### <a name="response"></a><span data-ttu-id="b0f9f-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b0f9f-157">Response</span></span>
<span data-ttu-id="b0f9f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b0f9f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




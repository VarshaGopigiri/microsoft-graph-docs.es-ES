---
title: Obtener deviceManagement
description: Lea las propiedades y las relaciones del objeto deviceManagement.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 89156113d0b357bc0d7a76cadad8c2ab7e2e4b91
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816271"
---
# <a name="get-devicemanagement"></a><span data-ttu-id="bbb5b-103">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="bbb5b-103">Get deviceManagement</span></span>

> <span data-ttu-id="bbb5b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bbb5b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bbb5b-105">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="bbb5b-105">Read properties and relationships of the [deviceManagement](../resources/intune-shared-devicemanagement.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bbb5b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bbb5b-106">Prerequisites</span></span>
<span data-ttu-id="bbb5b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bbb5b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="bbb5b-109">Permisos&nbsp;tipo&nbsp;(por&nbsp;flujo de trabajo)</span><span class="sxs-lookup"><span data-stu-id="bbb5b-109">Permission&nbsp;type&nbsp;(by&nbsp;workflow)</span></span> | <span data-ttu-id="bbb5b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bbb5b-110">Permissions (from most to least privileged)</span></span> |
|:---|:---|
| <span data-ttu-id="bbb5b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bbb5b-111">Delegated (work or school account)</span></span> | |
| <span data-ttu-id="bbb5b-112">&nbsp;&nbsp; Auditoría</span><span class="sxs-lookup"><span data-stu-id="bbb5b-112">&nbsp; &nbsp; Auditing</span></span> | <span data-ttu-id="bbb5b-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="bbb5b-114">&nbsp;&nbsp; Los términos de la empresa</span><span class="sxs-lookup"><span data-stu-id="bbb5b-114">&nbsp; &nbsp; Company terms</span></span> | <span data-ttu-id="bbb5b-115">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-115">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="bbb5b-116">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="bbb5b-116">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="bbb5b-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="bbb5b-118">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="bbb5b-118">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="bbb5b-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="bbb5b-120">&nbsp;&nbsp; Inscripción</span><span class="sxs-lookup"><span data-stu-id="bbb5b-120">&nbsp; &nbsp; Enrollment</span></span> | <span data-ttu-id="bbb5b-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="bbb5b-122">&nbsp;&nbsp; Notificación</span><span class="sxs-lookup"><span data-stu-id="bbb5b-122">&nbsp; &nbsp; Notification</span></span> | <span data-ttu-id="bbb5b-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="bbb5b-124">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="bbb5b-124">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="bbb5b-125">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-125">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="bbb5b-126">&nbsp;&nbsp; RBAC</span><span class="sxs-lookup"><span data-stu-id="bbb5b-126">&nbsp; &nbsp; RBAC</span></span> | <span data-ttu-id="bbb5b-127">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-127">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span> |
| <span data-ttu-id="bbb5b-128">&nbsp;&nbsp; Asistencia remota</span><span class="sxs-lookup"><span data-stu-id="bbb5b-128">&nbsp; &nbsp; Remote assistance</span></span> | <span data-ttu-id="bbb5b-129">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-129">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="bbb5b-130">&nbsp;&nbsp; Gestión de gastos de telecomunicaciones</span><span class="sxs-lookup"><span data-stu-id="bbb5b-130">&nbsp; &nbsp; Telecom expense management</span></span> | <span data-ttu-id="bbb5b-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="bbb5b-132">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="bbb5b-132">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="bbb5b-133">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-133">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
| <span data-ttu-id="bbb5b-134">&nbsp;&nbsp; Protección de la información de Windows</span><span class="sxs-lookup"><span data-stu-id="bbb5b-134">&nbsp; &nbsp; Windows Information Protection</span></span> | <span data-ttu-id="bbb5b-135">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="bbb5b-135">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
| <span data-ttu-id="bbb5b-136">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bbb5b-136">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bbb5b-137">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bbb5b-137">Not supported.</span></span>|
| <span data-ttu-id="bbb5b-138">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bbb5b-138">Application</span></span> | <span data-ttu-id="bbb5b-139">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bbb5b-139">Not supported.</span></span> |



## <a name="http-request"></a><span data-ttu-id="bbb5b-140">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bbb5b-140">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="bbb5b-141">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bbb5b-141">Optional query parameters</span></span>
<span data-ttu-id="bbb5b-142">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bbb5b-142">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bbb5b-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bbb5b-143">Request headers</span></span>
|<span data-ttu-id="bbb5b-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbb5b-144">Header</span></span>|<span data-ttu-id="bbb5b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="bbb5b-145">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bbb5b-146">Autorización</span><span class="sxs-lookup"><span data-stu-id="bbb5b-146">Authorization</span></span>|<span data-ttu-id="bbb5b-147">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bbb5b-147">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bbb5b-148">Accept</span><span class="sxs-lookup"><span data-stu-id="bbb5b-148">Accept</span></span>|<span data-ttu-id="bbb5b-149">application/json</span><span class="sxs-lookup"><span data-stu-id="bbb5b-149">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bbb5b-150">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bbb5b-150">Request body</span></span>
<span data-ttu-id="bbb5b-151">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bbb5b-151">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bbb5b-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbb5b-152">Response</span></span>
<span data-ttu-id="bbb5b-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagement](../resources/intune-shared-devicemanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bbb5b-153">If successful, this method returns a `200 OK` response code and [deviceManagement](../resources/intune-shared-devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bbb5b-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bbb5b-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="bbb5b-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bbb5b-155">Request</span></span>
<span data-ttu-id="bbb5b-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bbb5b-156">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement
```

### <a name="response"></a><span data-ttu-id="bbb5b-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbb5b-157">Response</span></span>
<span data-ttu-id="bbb5b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bbb5b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




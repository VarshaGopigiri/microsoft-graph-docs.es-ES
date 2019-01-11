---
title: Obtener deviceManagement
description: Lea las propiedades y las relaciones del objeto deviceManagement.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1c00b60793209904ce184de25f12f1f4ad14fad1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862639"
---
# <a name="get-devicemanagement"></a><span data-ttu-id="930e6-103">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="930e6-103">Get deviceManagement</span></span>

> <span data-ttu-id="930e6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="930e6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="930e6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="930e6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="930e6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="930e6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="930e6-107">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune-shared-devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="930e6-107">Read properties and relationships of the [deviceManagement](../resources/intune-shared-devicemanagement.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="930e6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="930e6-108">Prerequisites</span></span>

<span data-ttu-id="930e6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="930e6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="930e6-111">Permisos&nbsp;tipo&nbsp;(por&nbsp;flujo de trabajo)</span><span class="sxs-lookup"><span data-stu-id="930e6-111">Permission&nbsp;type&nbsp;(by&nbsp;workflow)</span></span> | <span data-ttu-id="930e6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="930e6-112">Permissions (from most to least privileged)</span></span> |
|:---|:---|
| <span data-ttu-id="930e6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="930e6-113">Delegated (work or school account)</span></span> | |
| <span data-ttu-id="930e6-114">&nbsp;&nbsp; **Android para el trabajo**</span><span class="sxs-lookup"><span data-stu-id="930e6-114">&nbsp; &nbsp; **Android for Work**</span></span> | <span data-ttu-id="930e6-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="930e6-116">&nbsp; &nbsp; **Auditoría**</span><span class="sxs-lookup"><span data-stu-id="930e6-116">&nbsp; &nbsp; **Auditing**</span></span> | <span data-ttu-id="930e6-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="930e6-118">&nbsp;&nbsp; **Los términos de la compañía**</span><span class="sxs-lookup"><span data-stu-id="930e6-118">&nbsp; &nbsp; **Company terms**</span></span> | <span data-ttu-id="930e6-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="930e6-120">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="930e6-120">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="930e6-121">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-121">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="930e6-122">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="930e6-122">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="930e6-123">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-123">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="930e6-124">&nbsp;&nbsp; **SIM electrónica**</span><span class="sxs-lookup"><span data-stu-id="930e6-124">&nbsp; &nbsp; **Electronic SIM**</span></span> | <span data-ttu-id="930e6-125">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-125">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="930e6-126">&nbsp; &nbsp; **Inscripción**</span><span class="sxs-lookup"><span data-stu-id="930e6-126">&nbsp; &nbsp; **Enrollment**</span></span> | <span data-ttu-id="930e6-127">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-127">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="930e6-128">&nbsp;&nbsp; **De barrera**</span><span class="sxs-lookup"><span data-stu-id="930e6-128">&nbsp; &nbsp; **Fencing**</span></span> | <span data-ttu-id="930e6-129">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-129">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="930e6-130">&nbsp;&nbsp; **Notificación**</span><span class="sxs-lookup"><span data-stu-id="930e6-130">&nbsp; &nbsp; **Notification**</span></span> | <span data-ttu-id="930e6-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="930e6-132">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="930e6-132">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="930e6-133">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-133">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="930e6-134">&nbsp;&nbsp; **RBAC**</span><span class="sxs-lookup"><span data-stu-id="930e6-134">&nbsp; &nbsp; **RBAC**</span></span> | <span data-ttu-id="930e6-135">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-135">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span> |
| <span data-ttu-id="930e6-136">&nbsp;&nbsp; **El acceso remoto**</span><span class="sxs-lookup"><span data-stu-id="930e6-136">&nbsp; &nbsp; **Remote access**</span></span> | <span data-ttu-id="930e6-137">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-137">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="930e6-138">&nbsp;&nbsp; **Asistencia remota**</span><span class="sxs-lookup"><span data-stu-id="930e6-138">&nbsp; &nbsp; **Remote assistance**</span></span> | <span data-ttu-id="930e6-139">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-139">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="930e6-140">&nbsp;&nbsp; **Gestión de gastos de telecomunicaciones**</span><span class="sxs-lookup"><span data-stu-id="930e6-140">&nbsp; &nbsp; **Telecom expense management**</span></span> | <span data-ttu-id="930e6-141">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-141">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="930e6-142">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="930e6-142">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="930e6-143">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-143">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="930e6-144">&nbsp;&nbsp; **Protección de la información de Windows**</span><span class="sxs-lookup"><span data-stu-id="930e6-144">&nbsp; &nbsp; **Windows Information Protection**</span></span> | <span data-ttu-id="930e6-145">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="930e6-145">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="930e6-146">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="930e6-146">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="930e6-147">No admitida.</span><span class="sxs-lookup"><span data-stu-id="930e6-147">Not supported.</span></span>|
| <span data-ttu-id="930e6-148">Aplicación</span><span class="sxs-lookup"><span data-stu-id="930e6-148">Application</span></span> | <span data-ttu-id="930e6-149">No admitida.</span><span class="sxs-lookup"><span data-stu-id="930e6-149">Not supported.</span></span> |



## <a name="http-request"></a><span data-ttu-id="930e6-150">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="930e6-150">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="930e6-151">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="930e6-151">Optional query parameters</span></span>

<span data-ttu-id="930e6-152">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="930e6-152">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="930e6-153">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="930e6-153">Request headers</span></span>
|<span data-ttu-id="930e6-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="930e6-154">Header</span></span>|<span data-ttu-id="930e6-155">Valor</span><span class="sxs-lookup"><span data-stu-id="930e6-155">Value</span></span>|
|:---|:---|
|<span data-ttu-id="930e6-156">Autorización</span><span class="sxs-lookup"><span data-stu-id="930e6-156">Authorization</span></span>|<span data-ttu-id="930e6-157">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="930e6-157">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="930e6-158">Accept</span><span class="sxs-lookup"><span data-stu-id="930e6-158">Accept</span></span>|<span data-ttu-id="930e6-159">application/json</span><span class="sxs-lookup"><span data-stu-id="930e6-159">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="930e6-160">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="930e6-160">Request body</span></span>

<span data-ttu-id="930e6-161">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="930e6-161">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="930e6-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="930e6-162">Response</span></span>

<span data-ttu-id="930e6-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagement](../resources/intune-shared-devicemanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="930e6-163">If successful, this method returns a `200 OK` response code and [deviceManagement](../resources/intune-shared-devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="930e6-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="930e6-164">Example</span></span>

### <a name="request"></a><span data-ttu-id="930e6-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="930e6-165">Request</span></span>

<span data-ttu-id="930e6-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="930e6-166">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement
```

### <a name="response"></a><span data-ttu-id="930e6-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="930e6-167">Response</span></span>

<span data-ttu-id="930e6-168">Éstos son ejemplos de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="930e6-168">Here are example of the response.</span></span> 

<span data-ttu-id="930e6-169">Nota: Los objetos de respuesta que se muestra aquí es posible que esté truncados por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="930e6-169">Note: The response objects shown here may be truncated for brevity.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 130

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceManagement",
    "id": "0b283420-3420-0b28-2034-280b2034280b"
  }
}
```

<span data-ttu-id="930e6-170">Se devuelven las propiedades apropiadas para el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="930e6-170">Properties appropriate for the workflow are returned.</span></span>

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




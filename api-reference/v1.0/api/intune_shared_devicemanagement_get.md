# <a name="get-devicemanagement"></a><span data-ttu-id="13744-101">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="13744-101">Get deviceManagement</span></span>

> <span data-ttu-id="13744-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="13744-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="13744-103">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="13744-103">Read properties and relationships of the [deviceManagement](../resources/intune_shared_devicemanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="13744-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="13744-104">Prerequisites</span></span>
<span data-ttu-id="13744-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="13744-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="13744-107">Tipo de&nbsp;permiso&nbsp;(por&nbsp;flujo de trabajo)</span><span class="sxs-lookup"><span data-stu-id="13744-107">Permission&nbsp;type&nbsp;(by&nbsp;workflow)</span></span> | <span data-ttu-id="13744-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="13744-108">Permissions (from most to least privileged)</span></span> |
|:---|:---|
| <span data-ttu-id="13744-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="13744-109">Delegated (work or school account)</span></span> | |
| <span data-ttu-id="13744-110">&nbsp; &nbsp; Auditoría</span><span class="sxs-lookup"><span data-stu-id="13744-110">&nbsp; &nbsp;Auditing</span></span> | <span data-ttu-id="13744-111">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-111">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="13744-112">&nbsp; &nbsp; Condiciones de la compañía</span><span class="sxs-lookup"><span data-stu-id="13744-112">&nbsp; &nbsp; Company terms</span></span> | <span data-ttu-id="13744-113">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-113">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="13744-114">&nbsp; &nbsp; Inscripción corporativa</span><span class="sxs-lookup"><span data-stu-id="13744-114">&nbsp; &nbsp; Corporate enrollment</span></span> | <span data-ttu-id="13744-115">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-115">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="13744-116">&nbsp; &nbsp; Configuración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="13744-116">&nbsp; &nbsp;Device configuration</span></span> | <span data-ttu-id="13744-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-117">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="13744-118">&nbsp; &nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="13744-118">&nbsp; &nbsp;Device management</span></span> | <span data-ttu-id="13744-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-119">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="13744-120">&nbsp; &nbsp; Protección de extremo</span><span class="sxs-lookup"><span data-stu-id="13744-120">&nbsp; &nbsp;Endpoint Protection</span></span> | <span data-ttu-id="13744-121">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-121">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="13744-122">&nbsp; &nbsp; Inscripción</span><span class="sxs-lookup"><span data-stu-id="13744-122">&nbsp; &nbsp;Enrollment</span></span> | <span data-ttu-id="13744-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="13744-124">&nbsp; &nbsp; Notificación</span><span class="sxs-lookup"><span data-stu-id="13744-124">&nbsp; &nbsp;Notification</span></span> | <span data-ttu-id="13744-125">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-125">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="13744-126">&nbsp; &nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="13744-126">&nbsp; &nbsp; On-boarding</span></span> | <span data-ttu-id="13744-127">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-127">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="13744-128">&nbsp; &nbsp; RBAC</span><span class="sxs-lookup"><span data-stu-id="13744-128">&nbsp; &nbsp;RBAC</span></span> | <span data-ttu-id="13744-129">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-129">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span> |
| <span data-ttu-id="13744-130">&nbsp; &nbsp; Asistencia remota</span><span class="sxs-lookup"><span data-stu-id="13744-130">remote assistance,</span></span> | <span data-ttu-id="13744-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-131">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="13744-132">&nbsp; &nbsp; Gestión de gastos de telecomunicaciones</span><span class="sxs-lookup"><span data-stu-id="13744-132">&nbsp; &nbsp;Telecom expense management partner</span></span> | <span data-ttu-id="13744-133">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-133">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="13744-134">&nbsp; &nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="13744-134">&nbsp; &nbsp;Troubleshooting</span></span> | <span data-ttu-id="13744-135">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-135">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
| <span data-ttu-id="13744-136">&nbsp; &nbsp; Protección de la información de Windows</span><span class="sxs-lookup"><span data-stu-id="13744-136">Windows information protection</span></span> | <span data-ttu-id="13744-137">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="13744-137">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
| <span data-ttu-id="13744-138">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="13744-138">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="13744-139">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13744-139">Not supported.</span></span>|
| <span data-ttu-id="13744-140">Aplicación</span><span class="sxs-lookup"><span data-stu-id="13744-140">Application</span></span> | <span data-ttu-id="13744-141">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13744-141">Not supported.</span></span> |



## <a name="http-request"></a><span data-ttu-id="13744-142">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="13744-142">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="13744-143">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="13744-143">Optional query parameters</span></span>
<span data-ttu-id="13744-144">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13744-144">This method supports the [OData Query Parameters](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="13744-145">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="13744-145">Request headers</span></span>
|<span data-ttu-id="13744-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13744-146">Header</span></span>|<span data-ttu-id="13744-147">Valor</span><span class="sxs-lookup"><span data-stu-id="13744-147">Value</span></span>|
|:---|:---|
|<span data-ttu-id="13744-148">Authorization</span><span class="sxs-lookup"><span data-stu-id="13744-148">Authorization</span></span>|<span data-ttu-id="13744-149">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="13744-149">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="13744-150">Aceptar</span><span class="sxs-lookup"><span data-stu-id="13744-150">Accept</span></span>|<span data-ttu-id="13744-151">application/json</span><span class="sxs-lookup"><span data-stu-id="13744-151">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="13744-152">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="13744-152">Request body</span></span>
<span data-ttu-id="13744-153">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="13744-153">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="13744-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13744-154">Response</span></span>
<span data-ttu-id="13744-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagement](../resources/intune_shared_devicemanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13744-155">If successful, this method returns a `200 OK` response code and [deviceManagement](../resources/intune_shared_devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="13744-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13744-156">Example</span></span>
### <a name="request"></a><span data-ttu-id="13744-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="13744-157">Request</span></span>
<span data-ttu-id="13744-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13744-158">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement
```

### <a name="response"></a><span data-ttu-id="13744-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13744-159">Response</span></span>
<span data-ttu-id="13744-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="13744-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




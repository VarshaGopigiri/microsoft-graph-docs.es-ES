# <a name="get-devicemanagement"></a><span data-ttu-id="89399-101">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="89399-101">Get deviceManagement</span></span>

> <span data-ttu-id="89399-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="89399-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="89399-103">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_shared_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="89399-103">Read properties and relationships of the [deviceManagement](../resources/intune_shared_devicemanagement.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="89399-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="89399-104">Prerequisites</span></span>
<span data-ttu-id="89399-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="89399-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="89399-107">Permisos&nbsp;tipo&nbsp;(por&nbsp;flujo de trabajo)</span><span class="sxs-lookup"><span data-stu-id="89399-107">Permission&nbsp;type&nbsp;(by&nbsp;workflow)</span></span> | <span data-ttu-id="89399-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="89399-108">Permissions (from most to least privileged)</span></span> |
|:---|:---|
| <span data-ttu-id="89399-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="89399-109">Delegated (work or school account)</span></span> | |
| <span data-ttu-id="89399-110">&nbsp;&nbsp; Auditoría</span><span class="sxs-lookup"><span data-stu-id="89399-110">&nbsp; &nbsp; Auditing</span></span> | <span data-ttu-id="89399-111">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-111">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="89399-112">&nbsp;&nbsp; Los términos de la empresa</span><span class="sxs-lookup"><span data-stu-id="89399-112">&nbsp; &nbsp; Company terms</span></span> | <span data-ttu-id="89399-113">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-113">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="89399-114">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="89399-114">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="89399-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span> |
| <span data-ttu-id="89399-116">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="89399-116">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="89399-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="89399-118">&nbsp;&nbsp; Inscripción</span><span class="sxs-lookup"><span data-stu-id="89399-118">&nbsp; &nbsp; Enrollment</span></span> | <span data-ttu-id="89399-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="89399-120">&nbsp;&nbsp; Notificación</span><span class="sxs-lookup"><span data-stu-id="89399-120">&nbsp; &nbsp; Notification</span></span> | <span data-ttu-id="89399-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-121">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="89399-122">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="89399-122">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="89399-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-123">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="89399-124">&nbsp;&nbsp; RBAC</span><span class="sxs-lookup"><span data-stu-id="89399-124">&nbsp; &nbsp; RBAC</span></span> | <span data-ttu-id="89399-125">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-125">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span> |
| <span data-ttu-id="89399-126">&nbsp;&nbsp; Asistencia remota</span><span class="sxs-lookup"><span data-stu-id="89399-126">&nbsp; &nbsp; Remote assistance</span></span> | <span data-ttu-id="89399-127">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-127">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="89399-128">&nbsp;&nbsp; Gestión de gastos de telecomunicaciones</span><span class="sxs-lookup"><span data-stu-id="89399-128">&nbsp; &nbsp; Telecom expense management</span></span> | <span data-ttu-id="89399-129">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-129">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="89399-130">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="89399-130">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="89399-131">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-131">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
| <span data-ttu-id="89399-132">&nbsp;&nbsp; Protección de la información de Windows</span><span class="sxs-lookup"><span data-stu-id="89399-132">&nbsp; &nbsp; Windows Information Protection</span></span> | <span data-ttu-id="89399-133">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="89399-133">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
| <span data-ttu-id="89399-134">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89399-134">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="89399-135">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89399-135">Not supported.</span></span>|
| <span data-ttu-id="89399-136">Aplicación</span><span class="sxs-lookup"><span data-stu-id="89399-136">Application</span></span> | <span data-ttu-id="89399-137">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89399-137">Not supported.</span></span> |



## <a name="http-request"></a><span data-ttu-id="89399-138">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="89399-138">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="89399-139">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="89399-139">Optional query parameters</span></span>
<span data-ttu-id="89399-140">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89399-140">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="89399-141">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="89399-141">Request headers</span></span>
|<span data-ttu-id="89399-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89399-142">Header</span></span>|<span data-ttu-id="89399-143">Valor</span><span class="sxs-lookup"><span data-stu-id="89399-143">Value</span></span>|
|:---|:---|
|<span data-ttu-id="89399-144">Authorization</span><span class="sxs-lookup"><span data-stu-id="89399-144">Authorization</span></span>|<span data-ttu-id="89399-145">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="89399-145">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="89399-146">Aceptar</span><span class="sxs-lookup"><span data-stu-id="89399-146">Accept</span></span>|<span data-ttu-id="89399-147">application/json</span><span class="sxs-lookup"><span data-stu-id="89399-147">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="89399-148">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="89399-148">Request body</span></span>
<span data-ttu-id="89399-149">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="89399-149">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="89399-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89399-150">Response</span></span>
<span data-ttu-id="89399-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagement](../resources/intune_shared_devicemanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89399-151">If successful, this method returns a `200 OK` response code and [deviceManagement](../resources/intune_shared_devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="89399-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89399-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="89399-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="89399-153">Request</span></span>
<span data-ttu-id="89399-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="89399-154">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement
```

### <a name="response"></a><span data-ttu-id="89399-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89399-155">Response</span></span>
<span data-ttu-id="89399-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="89399-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




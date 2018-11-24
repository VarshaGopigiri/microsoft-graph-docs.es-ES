# <a name="update-devicemanagementpartner"></a><span data-ttu-id="55e93-101">Actualizar deviceManagementPartner</span><span class="sxs-lookup"><span data-stu-id="55e93-101">Update deviceManagementPartner</span></span>

> <span data-ttu-id="55e93-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="55e93-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="55e93-103">Actualice las propiedades de un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="55e93-103">Update the properties of a [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="55e93-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="55e93-104">Prerequisites</span></span>
<span data-ttu-id="55e93-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="55e93-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="55e93-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55e93-107">Permission type</span></span>|<span data-ttu-id="55e93-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55e93-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="55e93-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55e93-109">Delegated (work or school account)</span></span>|<span data-ttu-id="55e93-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="55e93-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="55e93-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55e93-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="55e93-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55e93-112">Not supported.</span></span>|
|<span data-ttu-id="55e93-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55e93-113">Application</span></span>|<span data-ttu-id="55e93-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55e93-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="55e93-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55e93-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="55e93-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55e93-116">Request headers</span></span>
|<span data-ttu-id="55e93-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55e93-117">Header</span></span>|<span data-ttu-id="55e93-118">Valor</span><span class="sxs-lookup"><span data-stu-id="55e93-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="55e93-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="55e93-119">Authorization</span></span>|<span data-ttu-id="55e93-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="55e93-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="55e93-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="55e93-121">Accept</span></span>|<span data-ttu-id="55e93-122">application/json</span><span class="sxs-lookup"><span data-stu-id="55e93-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="55e93-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55e93-123">Request body</span></span>
<span data-ttu-id="55e93-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="55e93-124">In the request body, supply a JSON representation for the [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md) object.</span></span>

<span data-ttu-id="55e93-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="55e93-125">The following table shows the properties that are required when you create the [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).</span></span>

|<span data-ttu-id="55e93-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55e93-126">Property</span></span>|<span data-ttu-id="55e93-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="55e93-127">Type</span></span>|<span data-ttu-id="55e93-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="55e93-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="55e93-129">id</span><span class="sxs-lookup"><span data-stu-id="55e93-129">id</span></span>|<span data-ttu-id="55e93-130">String</span><span class="sxs-lookup"><span data-stu-id="55e93-130">String</span></span>|<span data-ttu-id="55e93-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="55e93-131">Not yet documented</span></span>|
|<span data-ttu-id="55e93-132">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="55e93-132">lastHeartbeatDateTime</span></span>|<span data-ttu-id="55e93-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="55e93-133">DateTimeOffset</span></span>|<span data-ttu-id="55e93-134">Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="55e93-134">Timestamp of last heartbeat after admin enabled option Connect to Device management Partner</span></span>|
|<span data-ttu-id="55e93-135">partnerState</span><span class="sxs-lookup"><span data-stu-id="55e93-135">partnerState</span></span>|[<span data-ttu-id="55e93-136">deviceManagementPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="55e93-136">deviceManagementPartnerTenantState</span></span>](../resources/intune_onboarding_devicemanagementpartnertenantstate.md)|<span data-ttu-id="55e93-137">Estado de socio de este inquilino.</span><span class="sxs-lookup"><span data-stu-id="55e93-137">Partner state of this tenant.</span></span> <span data-ttu-id="55e93-138">Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="55e93-138">Possible values are: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span></span>|
|<span data-ttu-id="55e93-139">partnerAppType</span><span class="sxs-lookup"><span data-stu-id="55e93-139">partnerAppType</span></span>|[<span data-ttu-id="55e93-140">deviceManagementPartnerAppType</span><span class="sxs-lookup"><span data-stu-id="55e93-140">deviceManagementPartnerAppType</span></span>](../resources/intune_onboarding_devicemanagementpartnerapptype.md)|<span data-ttu-id="55e93-141">Tipo de aplicación de socio.</span><span class="sxs-lookup"><span data-stu-id="55e93-141">Partner App type.</span></span> <span data-ttu-id="55e93-142">Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.</span><span class="sxs-lookup"><span data-stu-id="55e93-142">Possible values are: `unknown`, `singleTenantApp`, `multiTenantApp`.</span></span>|
|<span data-ttu-id="55e93-143">singleTenantAppId</span><span class="sxs-lookup"><span data-stu-id="55e93-143">singleTenantAppId</span></span>|<span data-ttu-id="55e93-144">String</span><span class="sxs-lookup"><span data-stu-id="55e93-144">String</span></span>|<span data-ttu-id="55e93-145">Identificador de aplicación de espacio empresarial único de partner</span><span class="sxs-lookup"><span data-stu-id="55e93-145">Partner Single tenant App id</span></span>|
|<span data-ttu-id="55e93-146">displayName</span><span class="sxs-lookup"><span data-stu-id="55e93-146">displayName</span></span>|<span data-ttu-id="55e93-147">String</span><span class="sxs-lookup"><span data-stu-id="55e93-147">String</span></span>|<span data-ttu-id="55e93-148">Nombre para mostrar del partner</span><span class="sxs-lookup"><span data-stu-id="55e93-148">Partner display name</span></span>|
|<span data-ttu-id="55e93-149">isConfigured</span><span class="sxs-lookup"><span data-stu-id="55e93-149">isConfigured</span></span>|<span data-ttu-id="55e93-150">Booleano</span><span class="sxs-lookup"><span data-stu-id="55e93-150">Boolean</span></span>|<span data-ttu-id="55e93-151">Si el partner de administración de dispositivos está configurado o no</span><span class="sxs-lookup"><span data-stu-id="55e93-151">Whether device management partner is configured or not</span></span>|
|<span data-ttu-id="55e93-152">whenPartnerDevicesWillBeRemovedDateTime</span><span class="sxs-lookup"><span data-stu-id="55e93-152">whenPartnerDevicesWillBeRemovedDateTime</span></span>|<span data-ttu-id="55e93-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="55e93-153">DateTimeOffset</span></span>|<span data-ttu-id="55e93-154">Fecha y hora en UTC de cuándo se quitará PartnerDevices</span><span class="sxs-lookup"><span data-stu-id="55e93-154">DateTime in UTC when PartnerDevices will be removed</span></span>|
|<span data-ttu-id="55e93-155">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span><span class="sxs-lookup"><span data-stu-id="55e93-155">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span></span>|<span data-ttu-id="55e93-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="55e93-156">DateTimeOffset</span></span>|<span data-ttu-id="55e93-157">Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible</span><span class="sxs-lookup"><span data-stu-id="55e93-157">DateTime in UTC when PartnerDevices will be marked as NonCompliant</span></span>|



## <a name="response"></a><span data-ttu-id="55e93-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55e93-158">Response</span></span>
<span data-ttu-id="55e93-159">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55e93-159">If successful, this method returns a `200 OK` response code and an updated [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55e93-160">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55e93-160">Example</span></span>
### <a name="request"></a><span data-ttu-id="55e93-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55e93-161">Request</span></span>
<span data-ttu-id="55e93-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55e93-162">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
Content-type: application/json
Content-length: 502

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```

### <a name="response"></a><span data-ttu-id="55e93-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55e93-163">Response</span></span>
<span data-ttu-id="55e93-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="55e93-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 551

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "id": "d21e377a-377a-d21e-7a37-1ed27a371ed2",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```




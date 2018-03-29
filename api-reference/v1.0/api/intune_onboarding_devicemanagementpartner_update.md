# <a name="update-devicemanagementpartner"></a><span data-ttu-id="aa147-101">Actualizar deviceManagementPartner</span><span class="sxs-lookup"><span data-stu-id="aa147-101">Update deviceManagementPartner</span></span>

> <span data-ttu-id="aa147-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aa147-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aa147-103">Actualice las propiedades de un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="aa147-103">Update the properties of a [calendar](../resources/intune_onboarding_devicemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="aa147-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aa147-104">Prerequisites</span></span>
<span data-ttu-id="aa147-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="aa147-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="aa147-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aa147-107">Permission type</span></span>|<span data-ttu-id="aa147-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aa147-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="aa147-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aa147-109">Delegated (work or school account)</span></span>|<span data-ttu-id="aa147-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aa147-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="aa147-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aa147-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="aa147-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa147-112">Not supported.</span></span>|
|<span data-ttu-id="aa147-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aa147-113">Application</span></span>|<span data-ttu-id="aa147-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa147-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="aa147-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa147-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="aa147-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa147-116">Request headers</span></span>
|<span data-ttu-id="aa147-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa147-117">Header</span></span>|<span data-ttu-id="aa147-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aa147-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="aa147-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="aa147-119">Authorization</span></span>|<span data-ttu-id="aa147-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="aa147-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="aa147-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="aa147-121">Accept</span></span>|<span data-ttu-id="aa147-122">application/json</span><span class="sxs-lookup"><span data-stu-id="aa147-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="aa147-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa147-123">Request body</span></span>
<span data-ttu-id="aa147-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="aa147-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_onboarding_devicemanagementpartner.md) object.</span></span>

<span data-ttu-id="aa147-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="aa147-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="aa147-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa147-126">Property</span></span>|<span data-ttu-id="aa147-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa147-127">Type</span></span>|<span data-ttu-id="aa147-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa147-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aa147-129">id</span><span class="sxs-lookup"><span data-stu-id="aa147-129">id</span></span>|<span data-ttu-id="aa147-130">String</span><span class="sxs-lookup"><span data-stu-id="aa147-130">String</span></span>|<span data-ttu-id="aa147-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="aa147-131">Not yet documented</span></span>|
|<span data-ttu-id="aa147-132">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="aa147-132">lastHeartbeatDateTime</span></span>|<span data-ttu-id="aa147-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa147-133">DateTimeOffset</span></span>|<span data-ttu-id="aa147-134">Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="aa147-134">Timestamp of last heartbeat after admin enabled option Connect to Device management Partner</span></span>|
|<span data-ttu-id="aa147-135">partnerState</span><span class="sxs-lookup"><span data-stu-id="aa147-135">partnerState</span></span>|<span data-ttu-id="aa147-136">String</span><span class="sxs-lookup"><span data-stu-id="aa147-136">String</span></span>|<span data-ttu-id="aa147-137">Estado de partner de este espacio empresarial. Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="aa147-137">Partner state of this tenant Possible values are: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span></span>|
|<span data-ttu-id="aa147-138">partnerAppType</span><span class="sxs-lookup"><span data-stu-id="aa147-138">partnerAppType</span></span>|<span data-ttu-id="aa147-139">String</span><span class="sxs-lookup"><span data-stu-id="aa147-139">String</span></span>|<span data-ttu-id="aa147-140">Tipo de aplicación de partner. Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.</span><span class="sxs-lookup"><span data-stu-id="aa147-140">Partner App type Possible values are: `unknown`, `singleTenantApp`, `multiTenantApp`.</span></span>|
|<span data-ttu-id="aa147-141">singleTenantAppId</span><span class="sxs-lookup"><span data-stu-id="aa147-141">singleTenantAppId</span></span>|<span data-ttu-id="aa147-142">String</span><span class="sxs-lookup"><span data-stu-id="aa147-142">String</span></span>|<span data-ttu-id="aa147-143">Identificador de aplicación de espacio empresarial único de partner</span><span class="sxs-lookup"><span data-stu-id="aa147-143">Partner Single tenant App id</span></span>|
|<span data-ttu-id="aa147-144">displayName</span><span class="sxs-lookup"><span data-stu-id="aa147-144">displayName</span></span>|<span data-ttu-id="aa147-145">String</span><span class="sxs-lookup"><span data-stu-id="aa147-145">String</span></span>|<span data-ttu-id="aa147-146">Nombre para mostrar del partner</span><span class="sxs-lookup"><span data-stu-id="aa147-146">Partner display name</span></span>|
|<span data-ttu-id="aa147-147">isConfigured</span><span class="sxs-lookup"><span data-stu-id="aa147-147">isConfigured</span></span>|<span data-ttu-id="aa147-148">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa147-148">Boolean</span></span>|<span data-ttu-id="aa147-149">Si el partner de administración de dispositivos está configurado o no</span><span class="sxs-lookup"><span data-stu-id="aa147-149">Whether device management partner is configured or not</span></span>|
|<span data-ttu-id="aa147-150">whenPartnerDevicesWillBeRemovedDateTime</span><span class="sxs-lookup"><span data-stu-id="aa147-150">whenPartnerDevicesWillBeRemovedDateTime</span></span>|<span data-ttu-id="aa147-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa147-151">DateTimeOffset</span></span>|<span data-ttu-id="aa147-152">Fecha y hora en UTC de cuándo se quitará PartnerDevices</span><span class="sxs-lookup"><span data-stu-id="aa147-152">DateTime in UTC when PartnerDevices will be removed</span></span>|
|<span data-ttu-id="aa147-153">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span><span class="sxs-lookup"><span data-stu-id="aa147-153">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span></span>|<span data-ttu-id="aa147-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa147-154">DateTimeOffset</span></span>|<span data-ttu-id="aa147-155">Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible</span><span class="sxs-lookup"><span data-stu-id="aa147-155">DateTime in UTC when PartnerDevices will be marked as NonCompliant</span></span>|



## <a name="response"></a><span data-ttu-id="aa147-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa147-156">Response</span></span>
<span data-ttu-id="aa147-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa147-157">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_onboarding_devicemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aa147-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa147-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="aa147-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa147-159">Request</span></span>
<span data-ttu-id="aa147-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aa147-160">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
Content-type: application/json
Content-length: 440

{
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

### <a name="response"></a><span data-ttu-id="aa147-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa147-161">Response</span></span>
<span data-ttu-id="aa147-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa147-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




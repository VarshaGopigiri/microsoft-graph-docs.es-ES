# <a name="create-devicemanagementpartner"></a><span data-ttu-id="04463-101">Crear deviceManagementPartner</span><span class="sxs-lookup"><span data-stu-id="04463-101">Create deviceManagementPartner</span></span>

> <span data-ttu-id="04463-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="04463-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="04463-103">Cree un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="04463-103">Create a new [plannerBucket](../resources/intune_onboarding_devicemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="04463-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="04463-104">Prerequisites</span></span>
<span data-ttu-id="04463-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="04463-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="04463-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04463-107">Permission type</span></span>|<span data-ttu-id="04463-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04463-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="04463-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04463-109">Delegated (work or school account)</span></span>|<span data-ttu-id="04463-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04463-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="04463-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04463-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="04463-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04463-112">Not supported.</span></span>|
|<span data-ttu-id="04463-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04463-113">Application</span></span>|<span data-ttu-id="04463-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04463-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="04463-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04463-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceManagementPartners
```

## <a name="request-headers"></a><span data-ttu-id="04463-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="04463-116">Request headers</span></span>
|<span data-ttu-id="04463-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04463-117">Header</span></span>|<span data-ttu-id="04463-118">Valor</span><span class="sxs-lookup"><span data-stu-id="04463-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="04463-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="04463-119">Authorization</span></span>|<span data-ttu-id="04463-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="04463-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="04463-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="04463-121">Accept</span></span>|<span data-ttu-id="04463-122">application/json</span><span class="sxs-lookup"><span data-stu-id="04463-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="04463-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04463-123">Request body</span></span>
<span data-ttu-id="04463-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceManagementPartner.</span><span class="sxs-lookup"><span data-stu-id="04463-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="04463-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceManagementPartner.</span><span class="sxs-lookup"><span data-stu-id="04463-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="04463-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04463-126">Property</span></span>|<span data-ttu-id="04463-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="04463-127">Type</span></span>|<span data-ttu-id="04463-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="04463-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="04463-129">id</span><span class="sxs-lookup"><span data-stu-id="04463-129">id</span></span>|<span data-ttu-id="04463-130">String</span><span class="sxs-lookup"><span data-stu-id="04463-130">String</span></span>|<span data-ttu-id="04463-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="04463-131">Not yet documented</span></span>|
|<span data-ttu-id="04463-132">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="04463-132">lastHeartbeatDateTime</span></span>|<span data-ttu-id="04463-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="04463-133">DateTimeOffset</span></span>|<span data-ttu-id="04463-134">Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="04463-134">Timestamp of last heartbeat after admin enabled option Connect to Device management Partner</span></span>|
|<span data-ttu-id="04463-135">partnerState</span><span class="sxs-lookup"><span data-stu-id="04463-135">partnerState</span></span>|<span data-ttu-id="04463-136">String</span><span class="sxs-lookup"><span data-stu-id="04463-136">String</span></span>|<span data-ttu-id="04463-137">Estado de partner de este espacio empresarial. Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="04463-137">Partner state of this tenant Possible values are: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span></span>|
|<span data-ttu-id="04463-138">partnerAppType</span><span class="sxs-lookup"><span data-stu-id="04463-138">partnerAppType</span></span>|<span data-ttu-id="04463-139">String</span><span class="sxs-lookup"><span data-stu-id="04463-139">String</span></span>|<span data-ttu-id="04463-140">Tipo de aplicación de partner. Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.</span><span class="sxs-lookup"><span data-stu-id="04463-140">Partner App type Possible values are: `unknown`, `singleTenantApp`, `multiTenantApp`.</span></span>|
|<span data-ttu-id="04463-141">singleTenantAppId</span><span class="sxs-lookup"><span data-stu-id="04463-141">singleTenantAppId</span></span>|<span data-ttu-id="04463-142">String</span><span class="sxs-lookup"><span data-stu-id="04463-142">String</span></span>|<span data-ttu-id="04463-143">Identificador de aplicación de espacio empresarial único de partner</span><span class="sxs-lookup"><span data-stu-id="04463-143">Partner Single tenant App id</span></span>|
|<span data-ttu-id="04463-144">displayName</span><span class="sxs-lookup"><span data-stu-id="04463-144">displayName</span></span>|<span data-ttu-id="04463-145">String</span><span class="sxs-lookup"><span data-stu-id="04463-145">String</span></span>|<span data-ttu-id="04463-146">Nombre para mostrar del partner</span><span class="sxs-lookup"><span data-stu-id="04463-146">Partner display name</span></span>|
|<span data-ttu-id="04463-147">isConfigured</span><span class="sxs-lookup"><span data-stu-id="04463-147">isConfigured</span></span>|<span data-ttu-id="04463-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="04463-148">Boolean</span></span>|<span data-ttu-id="04463-149">Si el partner de administración de dispositivos está configurado o no</span><span class="sxs-lookup"><span data-stu-id="04463-149">Whether device management partner is configured or not</span></span>|
|<span data-ttu-id="04463-150">whenPartnerDevicesWillBeRemovedDateTime</span><span class="sxs-lookup"><span data-stu-id="04463-150">whenPartnerDevicesWillBeRemovedDateTime</span></span>|<span data-ttu-id="04463-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="04463-151">DateTimeOffset</span></span>|<span data-ttu-id="04463-152">Fecha y hora en UTC de cuándo se quitará PartnerDevices</span><span class="sxs-lookup"><span data-stu-id="04463-152">DateTime in UTC when PartnerDevices will be removed</span></span>|
|<span data-ttu-id="04463-153">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span><span class="sxs-lookup"><span data-stu-id="04463-153">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span></span>|<span data-ttu-id="04463-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="04463-154">DateTimeOffset</span></span>|<span data-ttu-id="04463-155">Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible</span><span class="sxs-lookup"><span data-stu-id="04463-155">DateTime in UTC when PartnerDevices will be marked as NonCompliant</span></span>|



## <a name="response"></a><span data-ttu-id="04463-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04463-156">Response</span></span>
<span data-ttu-id="04463-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04463-157">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_onboarding_devicemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04463-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04463-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="04463-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04463-159">Request</span></span>
<span data-ttu-id="04463-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04463-160">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceManagementPartners
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

### <a name="response"></a><span data-ttu-id="04463-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04463-161">Response</span></span>
<span data-ttu-id="04463-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="04463-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




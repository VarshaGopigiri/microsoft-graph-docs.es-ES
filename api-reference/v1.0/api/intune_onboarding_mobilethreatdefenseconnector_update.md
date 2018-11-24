# <a name="update-mobilethreatdefenseconnector"></a><span data-ttu-id="50525-101">Actualizar mobileThreatDefenseConnector</span><span class="sxs-lookup"><span data-stu-id="50525-101">Update mobileThreatDefenseConnector</span></span>

> <span data-ttu-id="50525-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="50525-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="50525-103">Actualice las propiedades de un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="50525-103">Update the properties of a [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="50525-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="50525-104">Prerequisites</span></span>
<span data-ttu-id="50525-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="50525-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="50525-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="50525-107">Permission type</span></span>|<span data-ttu-id="50525-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="50525-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="50525-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="50525-109">Delegated (work or school account)</span></span>|<span data-ttu-id="50525-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="50525-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="50525-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="50525-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="50525-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50525-112">Not supported.</span></span>|
|<span data-ttu-id="50525-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="50525-113">Application</span></span>|<span data-ttu-id="50525-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50525-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="50525-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50525-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="50525-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50525-116">Request headers</span></span>
|<span data-ttu-id="50525-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50525-117">Header</span></span>|<span data-ttu-id="50525-118">Valor</span><span class="sxs-lookup"><span data-stu-id="50525-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="50525-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="50525-119">Authorization</span></span>|<span data-ttu-id="50525-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="50525-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="50525-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="50525-121">Accept</span></span>|<span data-ttu-id="50525-122">application/json</span><span class="sxs-lookup"><span data-stu-id="50525-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="50525-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50525-123">Request body</span></span>
<span data-ttu-id="50525-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="50525-124">In the request body, supply a JSON representation for the [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object.</span></span>

<span data-ttu-id="50525-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="50525-125">The following table shows the properties that are required when you create the [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span></span>

|<span data-ttu-id="50525-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50525-126">Property</span></span>|<span data-ttu-id="50525-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="50525-127">Type</span></span>|<span data-ttu-id="50525-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="50525-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="50525-129">id</span><span class="sxs-lookup"><span data-stu-id="50525-129">id</span></span>|<span data-ttu-id="50525-130">String</span><span class="sxs-lookup"><span data-stu-id="50525-130">String</span></span>|<span data-ttu-id="50525-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="50525-131">Not yet documented</span></span>|
|<span data-ttu-id="50525-132">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="50525-132">lastHeartbeatDateTime</span></span>|<span data-ttu-id="50525-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="50525-133">DateTimeOffset</span></span>|<span data-ttu-id="50525-134">Fecha y hora del último latido recibido del Partner de sincronización de datos</span><span class="sxs-lookup"><span data-stu-id="50525-134">DateTime of last Heartbeat recieved from the Data Sync Partner</span></span>|
|<span data-ttu-id="50525-135">partnerState</span><span class="sxs-lookup"><span data-stu-id="50525-135">partnerState</span></span>|[<span data-ttu-id="50525-136">mobileThreatPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="50525-136">mobileThreatPartnerTenantState</span></span>](../resources/intune_onboarding_mobilethreatpartnertenantstate.md)|<span data-ttu-id="50525-137">Estado de socio de sincronización de datos para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="50525-137">Data Sync Partner state for this account.</span></span> <span data-ttu-id="50525-138">Los valores posibles son: `unavailable`, `available`, `enabled` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="50525-138">Possible values are: `unavailable`, `available`, `enabled`, `unresponsive`.</span></span>|
|<span data-ttu-id="50525-139">androidEnabled</span><span class="sxs-lookup"><span data-stu-id="50525-139">androidEnabled</span></span>|<span data-ttu-id="50525-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="50525-140">Boolean</span></span>|<span data-ttu-id="50525-141">Para Android, establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="50525-141">For Android, set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="50525-142">iosEnabled</span><span class="sxs-lookup"><span data-stu-id="50525-142">iosEnabled</span></span>|<span data-ttu-id="50525-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="50525-143">Boolean</span></span>|<span data-ttu-id="50525-144">Para iOS, obtiene o establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="50525-144">For IOS, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="50525-145">androidDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="50525-145">androidDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="50525-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="50525-146">Boolean</span></span>|<span data-ttu-id="50525-147">Para Android, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="50525-147">For Android, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="50525-148">iosDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="50525-148">iosDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="50525-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="50525-149">Boolean</span></span>|<span data-ttu-id="50525-150">Para iOS, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="50525-150">For IOS, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="50525-151">partnerUnsupportedOsVersionBlocked</span><span class="sxs-lookup"><span data-stu-id="50525-151">partnerUnsupportedOsVersionBlocked</span></span>|<span data-ttu-id="50525-152">Boolean</span><span class="sxs-lookup"><span data-stu-id="50525-152">Boolean</span></span>|<span data-ttu-id="50525-153">Obtiene o establece si se deben bloquear los dispositivos de las plataformas habilitadas que no cumplan los requisitos de versión mínima.</span><span class="sxs-lookup"><span data-stu-id="50525-153">Get or set whether to block devices on the enabled platforms that do not meet the minimum version requirements of the Data Sync Partner</span></span>|
|<span data-ttu-id="50525-154">partnerUnresponsivenessThresholdInDays</span><span class="sxs-lookup"><span data-stu-id="50525-154">partnerUnresponsivenessThresholdInDays</span></span>|<span data-ttu-id="50525-155">Int32</span><span class="sxs-lookup"><span data-stu-id="50525-155">Int32</span></span>|<span data-ttu-id="50525-156">Obtener o definir los días de tolerancia por espacio empresarial para la falta de respuesta de esta integración de partner.</span><span class="sxs-lookup"><span data-stu-id="50525-156">Get or Set days the per tenant tolerance to unresponsiveness for this partner integration</span></span>|



## <a name="response"></a><span data-ttu-id="50525-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50525-157">Response</span></span>
<span data-ttu-id="50525-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50525-158">If successful, this method returns a `200 OK` response code and an updated [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="50525-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50525-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="50525-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50525-160">Request</span></span>
<span data-ttu-id="50525-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50525-161">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
Content-type: application/json
Content-length: 414

{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "iosEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 6
}
```

### <a name="response"></a><span data-ttu-id="50525-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50525-162">Response</span></span>
<span data-ttu-id="50525-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="50525-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 463

{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "id": "e4bede14-de14-e4be-14de-bee414debee4",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "iosEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 6
}
```




# <a name="create-mobilethreatdefenseconnector"></a><span data-ttu-id="bca13-101">Crear mobileThreatDefenseConnector</span><span class="sxs-lookup"><span data-stu-id="bca13-101">Create mobileThreatDefenseConnector</span></span>

> <span data-ttu-id="bca13-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bca13-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bca13-103">Crear un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="bca13-103">Create a new [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bca13-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bca13-104">Prerequisites</span></span>
<span data-ttu-id="bca13-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bca13-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bca13-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bca13-107">Permission type</span></span>|<span data-ttu-id="bca13-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bca13-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bca13-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bca13-109">Delegated (work or school account)</span></span>|<span data-ttu-id="bca13-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bca13-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="bca13-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bca13-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bca13-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bca13-112">Not supported.</span></span>|
|<span data-ttu-id="bca13-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bca13-113">Application</span></span>|<span data-ttu-id="bca13-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bca13-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bca13-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bca13-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/mobileThreatDefenseConnectors
```

## <a name="request-headers"></a><span data-ttu-id="bca13-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bca13-116">Request headers</span></span>
|<span data-ttu-id="bca13-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bca13-117">Header</span></span>|<span data-ttu-id="bca13-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bca13-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bca13-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="bca13-119">Authorization</span></span>|<span data-ttu-id="bca13-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bca13-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bca13-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bca13-121">Accept</span></span>|<span data-ttu-id="bca13-122">application/json</span><span class="sxs-lookup"><span data-stu-id="bca13-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bca13-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bca13-123">Request body</span></span>
<span data-ttu-id="bca13-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileThreatDefenseConnector.</span><span class="sxs-lookup"><span data-stu-id="bca13-124">In the request body, supply a JSON representation for the mobileThreatDefenseConnector object.</span></span>

<span data-ttu-id="bca13-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileThreatDefenseConnector.</span><span class="sxs-lookup"><span data-stu-id="bca13-125">The following table shows the properties that are required when you create the mobileThreatDefenseConnector.</span></span>

|<span data-ttu-id="bca13-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bca13-126">Property</span></span>|<span data-ttu-id="bca13-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="bca13-127">Type</span></span>|<span data-ttu-id="bca13-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="bca13-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bca13-129">id</span><span class="sxs-lookup"><span data-stu-id="bca13-129">id</span></span>|<span data-ttu-id="bca13-130">String</span><span class="sxs-lookup"><span data-stu-id="bca13-130">String</span></span>|<span data-ttu-id="bca13-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="bca13-131">Not yet documented</span></span>|
|<span data-ttu-id="bca13-132">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="bca13-132">lastHeartbeatDateTime</span></span>|<span data-ttu-id="bca13-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bca13-133">DateTimeOffset</span></span>|<span data-ttu-id="bca13-134">Fecha y hora del último latido recibido del partner de sincronización de datos</span><span class="sxs-lookup"><span data-stu-id="bca13-134">DateTime of last Heartbeat recieved from the Data Sync Partner</span></span>|
|<span data-ttu-id="bca13-135">partnerState</span><span class="sxs-lookup"><span data-stu-id="bca13-135">partnerState</span></span>|[<span data-ttu-id="bca13-136">mobileThreatPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="bca13-136">mobileThreatPartnerTenantState</span></span>](../resources/intune_onboarding_mobilethreatpartnertenantstate.md)|<span data-ttu-id="bca13-137">Estado de socio de sincronización de datos para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="bca13-137">Data Sync Partner state for this account.</span></span> <span data-ttu-id="bca13-138">Los valores posibles son: `unavailable`, `available`, `enabled` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="bca13-138">Possible values are: `unavailable`, `available`, `enabled`, `unresponsive`.</span></span>|
|<span data-ttu-id="bca13-139">androidEnabled</span><span class="sxs-lookup"><span data-stu-id="bca13-139">androidEnabled</span></span>|<span data-ttu-id="bca13-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="bca13-140">Boolean</span></span>|<span data-ttu-id="bca13-141">Para Android, establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="bca13-141">For Android, set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="bca13-142">iosEnabled</span><span class="sxs-lookup"><span data-stu-id="bca13-142">iosEnabled</span></span>|<span data-ttu-id="bca13-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="bca13-143">Boolean</span></span>|<span data-ttu-id="bca13-144">Para iOS, obtiene o establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="bca13-144">For IOS, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="bca13-145">androidDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="bca13-145">androidDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="bca13-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="bca13-146">Boolean</span></span>|<span data-ttu-id="bca13-147">Para Android, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="bca13-147">For Android, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="bca13-148">iosDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="bca13-148">iosDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="bca13-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="bca13-149">Boolean</span></span>|<span data-ttu-id="bca13-150">Para iOS, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="bca13-150">For IOS, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="bca13-151">partnerUnsupportedOsVersionBlocked</span><span class="sxs-lookup"><span data-stu-id="bca13-151">partnerUnsupportedOsVersionBlocked</span></span>|<span data-ttu-id="bca13-152">Boolean</span><span class="sxs-lookup"><span data-stu-id="bca13-152">Boolean</span></span>|<span data-ttu-id="bca13-153">Obtiene o establece si se deben bloquear los dispositivos de las plataformas habilitadas que no cumplan los requisitos de versión mínima.</span><span class="sxs-lookup"><span data-stu-id="bca13-153">Get or set whether to block devices on the enabled platforms that do not meet the minimum version requirements of the Data Sync Partner</span></span>|
|<span data-ttu-id="bca13-154">partnerUnresponsivenessThresholdInDays</span><span class="sxs-lookup"><span data-stu-id="bca13-154">partnerUnresponsivenessThresholdInDays</span></span>|<span data-ttu-id="bca13-155">Int32</span><span class="sxs-lookup"><span data-stu-id="bca13-155">Int32</span></span>|<span data-ttu-id="bca13-156">Obtener o definir los días de tolerancia por espacio empresarial para la falta de respuesta de esta integración de partner.</span><span class="sxs-lookup"><span data-stu-id="bca13-156">Get or Set days the per tenant tolerance to unresponsiveness for this partner integration</span></span>|



## <a name="response"></a><span data-ttu-id="bca13-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bca13-157">Response</span></span>
<span data-ttu-id="bca13-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bca13-158">If successful, this method returns a `201 Created` response code and a [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bca13-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bca13-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="bca13-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bca13-160">Request</span></span>
<span data-ttu-id="bca13-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bca13-161">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/mobileThreatDefenseConnectors
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

### <a name="response"></a><span data-ttu-id="bca13-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bca13-162">Response</span></span>
<span data-ttu-id="bca13-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bca13-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




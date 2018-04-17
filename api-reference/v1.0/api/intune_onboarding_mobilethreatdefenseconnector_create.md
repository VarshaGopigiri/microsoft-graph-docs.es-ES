# <a name="create-mobilethreatdefenseconnector"></a><span data-ttu-id="8ec92-101">Crear mobileThreatDefenseConnector</span><span class="sxs-lookup"><span data-stu-id="8ec92-101">Create mobileThreatDefenseConnector</span></span>

> <span data-ttu-id="8ec92-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8ec92-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8ec92-103">Crear un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="8ec92-103">Create a new [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8ec92-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8ec92-104">Prerequisites</span></span>
<span data-ttu-id="8ec92-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8ec92-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8ec92-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ec92-107">Permission type</span></span>|<span data-ttu-id="8ec92-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ec92-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8ec92-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ec92-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8ec92-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8ec92-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="8ec92-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ec92-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8ec92-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ec92-112">Not supported.</span></span>|
|<span data-ttu-id="8ec92-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ec92-113">Application</span></span>|<span data-ttu-id="8ec92-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ec92-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8ec92-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ec92-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/mobileThreatDefenseConnectors
```

## <a name="request-headers"></a><span data-ttu-id="8ec92-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ec92-116">Request headers</span></span>
|<span data-ttu-id="8ec92-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ec92-117">Header</span></span>|<span data-ttu-id="8ec92-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8ec92-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8ec92-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="8ec92-119">Authorization</span></span>|<span data-ttu-id="8ec92-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8ec92-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8ec92-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8ec92-121">Accept</span></span>|<span data-ttu-id="8ec92-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8ec92-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8ec92-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8ec92-123">Request body</span></span>
<span data-ttu-id="8ec92-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileThreatDefenseConnector.</span><span class="sxs-lookup"><span data-stu-id="8ec92-124">In the request body, supply a JSON representation for the mobileThreatDefenseConnector object.</span></span>

<span data-ttu-id="8ec92-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileThreatDefenseConnector.</span><span class="sxs-lookup"><span data-stu-id="8ec92-125">The following table shows the properties that are required when you create the mobileThreatDefenseConnector.</span></span>

|<span data-ttu-id="8ec92-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ec92-126">Property</span></span>|<span data-ttu-id="8ec92-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ec92-127">Type</span></span>|<span data-ttu-id="8ec92-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ec92-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8ec92-129">id</span><span class="sxs-lookup"><span data-stu-id="8ec92-129">id</span></span>|<span data-ttu-id="8ec92-130">String</span><span class="sxs-lookup"><span data-stu-id="8ec92-130">String</span></span>|<span data-ttu-id="8ec92-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8ec92-131">Not yet documented</span></span>|
|<span data-ttu-id="8ec92-132">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="8ec92-132">lastHeartbeatDateTime</span></span>|<span data-ttu-id="8ec92-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8ec92-133">DateTimeOffset</span></span>|<span data-ttu-id="8ec92-134">Fecha y hora del último latido recibido del partner de sincronización de datos</span><span class="sxs-lookup"><span data-stu-id="8ec92-134">DateTime of last Heartbeat recieved from the Data Sync Partner</span></span>|
|<span data-ttu-id="8ec92-135">partnerState</span><span class="sxs-lookup"><span data-stu-id="8ec92-135">partnerState</span></span>|<span data-ttu-id="8ec92-136">String</span><span class="sxs-lookup"><span data-stu-id="8ec92-136">String</span></span>|<span data-ttu-id="8ec92-137">Estado del partner de sincronización de datos para esta cuenta. Los valores posibles son: `unavailable`, `available`, `enabled` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="8ec92-137">Data Sync Partner state for this account Possible values are: `unavailable`, `available`, `enabled`, `unresponsive`.</span></span>|
|<span data-ttu-id="8ec92-138">androidEnabled</span><span class="sxs-lookup"><span data-stu-id="8ec92-138">androidEnabled</span></span>|<span data-ttu-id="8ec92-139">Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec92-139">Boolean</span></span>|<span data-ttu-id="8ec92-140">Para Android, configure si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="8ec92-140">For Android, set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="8ec92-141">iosEnabled</span><span class="sxs-lookup"><span data-stu-id="8ec92-141">iosEnabled</span></span>|<span data-ttu-id="8ec92-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec92-142">Boolean</span></span>|<span data-ttu-id="8ec92-143">Para iOS, obtenga o configure si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="8ec92-143">For IOS, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="8ec92-144">androidDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="8ec92-144">androidDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="8ec92-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec92-145">Boolean</span></span>|<span data-ttu-id="8ec92-146">Para Android, configure si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="8ec92-146">For Android, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="8ec92-147">iosDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="8ec92-147">iosDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="8ec92-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec92-148">Boolean</span></span>|<span data-ttu-id="8ec92-149">Para iOS, configure si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="8ec92-149">For IOS, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="8ec92-150">partnerUnsupportedOsVersionBlocked</span><span class="sxs-lookup"><span data-stu-id="8ec92-150">partnerUnsupportedOsVersionBlocked</span></span>|<span data-ttu-id="8ec92-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec92-151">Boolean</span></span>|<span data-ttu-id="8ec92-152">Obtenga o configure si se deben bloquear los dispositivos de las plataformas habilitadas que no cumplan los requisitos de versión mínima.</span><span class="sxs-lookup"><span data-stu-id="8ec92-152">Get or set whether to block devices on the enabled platforms that do not meet the minimum version requirements of the Data Sync Partner</span></span>|
|<span data-ttu-id="8ec92-153">partnerUnresponsivenessThresholdInDays</span><span class="sxs-lookup"><span data-stu-id="8ec92-153">partnerUnresponsivenessThresholdInDays</span></span>|<span data-ttu-id="8ec92-154">Int32</span><span class="sxs-lookup"><span data-stu-id="8ec92-154">Int32</span></span>|<span data-ttu-id="8ec92-155">Obtener o definir los días de tolerancia por espacio empresarial para la falta de respuesta de esta integración de partner.</span><span class="sxs-lookup"><span data-stu-id="8ec92-155">Get or Set days the per tenant tolerance to unresponsiveness for this partner integration</span></span>|



## <a name="response"></a><span data-ttu-id="8ec92-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ec92-156">Response</span></span>
<span data-ttu-id="8ec92-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ec92-157">If successful, this method returns a `201 Created` response code and a [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8ec92-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ec92-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="8ec92-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ec92-159">Request</span></span>
<span data-ttu-id="8ec92-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ec92-160">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="8ec92-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ec92-161">Response</span></span>
<span data-ttu-id="8ec92-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ec92-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




# <a name="update-mobilethreatdefenseconnector"></a><span data-ttu-id="11784-101">Actualizar mobileThreatDefenseConnector</span><span class="sxs-lookup"><span data-stu-id="11784-101">Update mobileThreatDefenseConnector</span></span>

> <span data-ttu-id="11784-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11784-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11784-103">Actualice las propiedades de un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="11784-103">Update the properties of a [calendar](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="11784-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="11784-104">Prerequisites</span></span>
<span data-ttu-id="11784-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="11784-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="11784-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11784-107">Permission type</span></span>|<span data-ttu-id="11784-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11784-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="11784-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11784-109">Delegated (work or school account)</span></span>|<span data-ttu-id="11784-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="11784-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="11784-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11784-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="11784-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11784-112">Not supported.</span></span>|
|<span data-ttu-id="11784-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11784-113">Application</span></span>|<span data-ttu-id="11784-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11784-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="11784-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11784-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="11784-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11784-116">Request headers</span></span>
|<span data-ttu-id="11784-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11784-117">Header</span></span>|<span data-ttu-id="11784-118">Valor</span><span class="sxs-lookup"><span data-stu-id="11784-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="11784-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="11784-119">Authorization</span></span>|<span data-ttu-id="11784-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="11784-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="11784-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="11784-121">Accept</span></span>|<span data-ttu-id="11784-122">application/json</span><span class="sxs-lookup"><span data-stu-id="11784-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="11784-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11784-123">Request body</span></span>
<span data-ttu-id="11784-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="11784-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object.</span></span>

<span data-ttu-id="11784-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="11784-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="11784-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11784-126">Property</span></span>|<span data-ttu-id="11784-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="11784-127">Type</span></span>|<span data-ttu-id="11784-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="11784-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11784-129">id</span><span class="sxs-lookup"><span data-stu-id="11784-129">id</span></span>|<span data-ttu-id="11784-130">String</span><span class="sxs-lookup"><span data-stu-id="11784-130">String</span></span>|<span data-ttu-id="11784-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="11784-131">Not yet documented</span></span>|
|<span data-ttu-id="11784-132">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="11784-132">lastHeartbeatDateTime</span></span>|<span data-ttu-id="11784-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11784-133">DateTimeOffset</span></span>|<span data-ttu-id="11784-134">Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a MTP.</span><span class="sxs-lookup"><span data-stu-id="11784-134">Timestamp of last heartbeat after admin enabled option Connect to MTP</span></span>|
|<span data-ttu-id="11784-135">partnerState</span><span class="sxs-lookup"><span data-stu-id="11784-135">partnerState</span></span>|<span data-ttu-id="11784-136">String</span><span class="sxs-lookup"><span data-stu-id="11784-136">String</span></span>|<span data-ttu-id="11784-137">Estado de partner de este espacio empresarial. Los valores posibles son: `unavailable`, `available`, `enabled` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="11784-137">Partner state of this tenant Possible values are: `unavailable`, `available`, `enabled`, `unresponsive`.</span></span>|
|<span data-ttu-id="11784-138">androidEnabled</span><span class="sxs-lookup"><span data-stu-id="11784-138">androidEnabled</span></span>|<span data-ttu-id="11784-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="11784-139">Boolean</span></span>|<span data-ttu-id="11784-140">Alternancia de activación y desactivación de Android.</span><span class="sxs-lookup"><span data-stu-id="11784-140">Android Toggle On or Off</span></span>|
|<span data-ttu-id="11784-141">androidDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="11784-141">androidDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="11784-142">Booleano</span><span class="sxs-lookup"><span data-stu-id="11784-142">Boolean</span></span>|<span data-ttu-id="11784-143">Para Android, permite que el administrador configure que debe recibir datos del partner de sincronización de datos antes de que se considere compatible.</span><span class="sxs-lookup"><span data-stu-id="11784-143">For Android, Allows admin to config must receive data from the data sync partner prior to being considered compliant</span></span>|
|<span data-ttu-id="11784-144">iosDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="11784-144">iosDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="11784-145">Booleano</span><span class="sxs-lookup"><span data-stu-id="11784-145">Boolean</span></span>|<span data-ttu-id="11784-146">Para iOS, permite que el administrador configure que debe recibir datos del partner de sincronización de datos antes de que se considere compatible.</span><span class="sxs-lookup"><span data-stu-id="11784-146">For IOS, Allows admin to config must receive data from the data sync partner prior to being considered compliant</span></span>|
|<span data-ttu-id="11784-147">partnerUnsupportedOsVersionBlocked</span><span class="sxs-lookup"><span data-stu-id="11784-147">partnerUnsupportedOsVersionBlocked</span></span>|<span data-ttu-id="11784-148">Booleano</span><span class="sxs-lookup"><span data-stu-id="11784-148">Boolean</span></span>|<span data-ttu-id="11784-149">Permite que el administrador bloquee los dispositivos en las plataformas habilitadas que no cumplan los requisitos de versión mínima.</span><span class="sxs-lookup"><span data-stu-id="11784-149">Allows admin to block devices on the enabled platforms that do not meet minimum version requirements</span></span>|
|<span data-ttu-id="11784-150">iosEnabled</span><span class="sxs-lookup"><span data-stu-id="11784-150">iosEnabled</span></span>|<span data-ttu-id="11784-151">Booleano</span><span class="sxs-lookup"><span data-stu-id="11784-151">Boolean</span></span>|<span data-ttu-id="11784-152">Alternancia de activación y desactivación de IOS.</span><span class="sxs-lookup"><span data-stu-id="11784-152">IOS Toggle On or Off</span></span>|
|<span data-ttu-id="11784-153">partnerUnresponsivenessThresholdInDays</span><span class="sxs-lookup"><span data-stu-id="11784-153">partnerUnresponsivenessThresholdInDays</span></span>|<span data-ttu-id="11784-154">Int32</span><span class="sxs-lookup"><span data-stu-id="11784-154">Int32</span></span>|<span data-ttu-id="11784-155">Obtener o definir los días de tolerancia por espacio empresarial para la falta de respuesta de esta integración de partner.</span><span class="sxs-lookup"><span data-stu-id="11784-155">Get or Set days the per tenant tolerance to unresponsiveness for this partner integration</span></span>|



## <a name="response"></a><span data-ttu-id="11784-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11784-156">Response</span></span>
<span data-ttu-id="11784-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11784-157">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_onboarding_mobilethreatdefenseconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="11784-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11784-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="11784-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11784-159">Request</span></span>
<span data-ttu-id="11784-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="11784-160">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
Content-type: application/json
Content-length: 347

{
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "iosEnabled": true,
  "partnerUnresponsivenessThresholdInDays": 6
}
```

### <a name="response"></a><span data-ttu-id="11784-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11784-161">Response</span></span>
<span data-ttu-id="11784-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11784-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "iosEnabled": true,
  "partnerUnresponsivenessThresholdInDays": 6
}
```




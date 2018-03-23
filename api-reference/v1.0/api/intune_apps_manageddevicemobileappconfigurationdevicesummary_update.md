# <a name="update-manageddevicemobileappconfigurationdevicesummary"></a><span data-ttu-id="271be-101">Actualizar managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="271be-101">Update managedDeviceMobileAppConfigurationDeviceSummary</span></span>

> <span data-ttu-id="271be-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="271be-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="271be-103">Actualice las propiedades y las relaciones de un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="271be-103">Update the properties of a [calendar](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="271be-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="271be-104">Prerequisites</span></span>
<span data-ttu-id="271be-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="271be-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="271be-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="271be-107">Permission type</span></span>|<span data-ttu-id="271be-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="271be-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="271be-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="271be-109">Delegated (work or school account)</span></span>|<span data-ttu-id="271be-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="271be-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="271be-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="271be-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="271be-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="271be-112">Not supported.</span></span>|
|<span data-ttu-id="271be-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="271be-113">Application</span></span>|<span data-ttu-id="271be-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="271be-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="271be-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="271be-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatusSummary
```

## <a name="request-headers"></a><span data-ttu-id="271be-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="271be-116">Request headers</span></span>
|<span data-ttu-id="271be-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="271be-117">Header</span></span>|<span data-ttu-id="271be-118">Valor</span><span class="sxs-lookup"><span data-stu-id="271be-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="271be-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="271be-119">Authorization</span></span>|<span data-ttu-id="271be-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="271be-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="271be-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="271be-121">Accept</span></span>|<span data-ttu-id="271be-122">application/json</span><span class="sxs-lookup"><span data-stu-id="271be-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="271be-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="271be-123">Request body</span></span>
<span data-ttu-id="271be-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="271be-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>

<span data-ttu-id="271be-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="271be-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="271be-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="271be-126">Property</span></span>|<span data-ttu-id="271be-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="271be-127">Type</span></span>|<span data-ttu-id="271be-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="271be-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="271be-129">id</span><span class="sxs-lookup"><span data-stu-id="271be-129">id</span></span>|<span data-ttu-id="271be-130">String</span><span class="sxs-lookup"><span data-stu-id="271be-130">String</span></span>|<span data-ttu-id="271be-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="271be-131">Key of the setting.</span></span>|
|<span data-ttu-id="271be-132">pendingCount</span><span class="sxs-lookup"><span data-stu-id="271be-132">pendingCount</span></span>|<span data-ttu-id="271be-133">Int32</span><span class="sxs-lookup"><span data-stu-id="271be-133">Int32</span></span>|<span data-ttu-id="271be-134">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="271be-134">Number of pending devices</span></span>|
|<span data-ttu-id="271be-135">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="271be-135">notApplicableCount</span></span>|<span data-ttu-id="271be-136">Int32</span><span class="sxs-lookup"><span data-stu-id="271be-136">Int32</span></span>|<span data-ttu-id="271be-137">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="271be-137">Number of not applicable devices</span></span>|
|<span data-ttu-id="271be-138">successCount</span><span class="sxs-lookup"><span data-stu-id="271be-138">successCount</span></span>|<span data-ttu-id="271be-139">Int32</span><span class="sxs-lookup"><span data-stu-id="271be-139">Int32</span></span>|<span data-ttu-id="271be-140">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="271be-140">Number of succeeded devices</span></span>|
|<span data-ttu-id="271be-141">errorCount</span><span class="sxs-lookup"><span data-stu-id="271be-141">errorCount</span></span>|<span data-ttu-id="271be-142">Int32</span><span class="sxs-lookup"><span data-stu-id="271be-142">Int32</span></span>|<span data-ttu-id="271be-143">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="271be-143">Number of error devices</span></span>|
|<span data-ttu-id="271be-144">failedCount</span><span class="sxs-lookup"><span data-stu-id="271be-144">failedCount</span></span>|<span data-ttu-id="271be-145">Int32</span><span class="sxs-lookup"><span data-stu-id="271be-145">Int32</span></span>|<span data-ttu-id="271be-146">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="271be-146">Number of failed devices</span></span>|
|<span data-ttu-id="271be-147">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="271be-147">lastUpdateDateTime</span></span>|<span data-ttu-id="271be-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="271be-148">DateTimeOffset</span></span>|<span data-ttu-id="271be-149">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="271be-149">Last update time</span></span>|
|<span data-ttu-id="271be-150">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="271be-150">configurationVersion</span></span>|<span data-ttu-id="271be-151">Int32</span><span class="sxs-lookup"><span data-stu-id="271be-151">Int32</span></span>|<span data-ttu-id="271be-152">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="271be-152">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="271be-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="271be-153">Response</span></span>
<span data-ttu-id="271be-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="271be-154">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_apps_manageddevicemobileappconfigurationdevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="271be-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="271be-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="271be-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="271be-156">Request</span></span>
<span data-ttu-id="271be-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="271be-157">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatusSummary
Content-type: application/json
Content-length: 212

{
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="271be-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="271be-158">Response</span></span>
<span data-ttu-id="271be-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="271be-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 348

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceSummary",
  "id": "9997c455-c455-9997-55c4-979955c49799",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```




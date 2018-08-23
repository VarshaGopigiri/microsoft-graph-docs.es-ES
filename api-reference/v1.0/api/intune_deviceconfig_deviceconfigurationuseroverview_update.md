# <a name="update-deviceconfigurationuseroverview"></a><span data-ttu-id="39514-101">Actualizar deviceConfigurationUserOverview</span><span class="sxs-lookup"><span data-stu-id="39514-101">Update deviceConfigurationUserOverview</span></span>

> <span data-ttu-id="39514-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39514-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39514-103">Actualice las propiedades de un objeto [deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="39514-103">Update the properties of a [deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="39514-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="39514-104">Prerequisites</span></span>
<span data-ttu-id="39514-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="39514-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="39514-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39514-107">Permission type</span></span>|<span data-ttu-id="39514-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39514-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="39514-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39514-109">Delegated (work or school account)</span></span>|<span data-ttu-id="39514-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39514-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="39514-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39514-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="39514-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39514-112">Not supported.</span></span>|
|<span data-ttu-id="39514-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39514-113">Application</span></span>|<span data-ttu-id="39514-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39514-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="39514-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39514-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatusOverview
```

## <a name="request-headers"></a><span data-ttu-id="39514-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39514-116">Request headers</span></span>
|<span data-ttu-id="39514-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39514-117">Header</span></span>|<span data-ttu-id="39514-118">Valor</span><span class="sxs-lookup"><span data-stu-id="39514-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="39514-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="39514-119">Authorization</span></span>|<span data-ttu-id="39514-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="39514-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="39514-121">Accept</span><span class="sxs-lookup"><span data-stu-id="39514-121">Accept</span></span>|<span data-ttu-id="39514-122">application/json</span><span class="sxs-lookup"><span data-stu-id="39514-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="39514-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39514-123">Request body</span></span>
<span data-ttu-id="39514-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="39514-124">In the request body, supply a JSON representation for the [deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md) object.</span></span>

<span data-ttu-id="39514-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="39514-125">The following table shows the properties that are required when you create the [deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md).</span></span>

|<span data-ttu-id="39514-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39514-126">Property</span></span>|<span data-ttu-id="39514-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="39514-127">Type</span></span>|<span data-ttu-id="39514-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="39514-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="39514-129">id</span><span class="sxs-lookup"><span data-stu-id="39514-129">id</span></span>|<span data-ttu-id="39514-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="39514-130">String</span></span>|<span data-ttu-id="39514-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="39514-131">Key of the entity.</span></span>|
|<span data-ttu-id="39514-132">pendingCount</span><span class="sxs-lookup"><span data-stu-id="39514-132">pendingCount</span></span>|<span data-ttu-id="39514-133">Int32</span><span class="sxs-lookup"><span data-stu-id="39514-133">Int32</span></span>|<span data-ttu-id="39514-134">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="39514-134">Number of pending Users</span></span>|
|<span data-ttu-id="39514-135">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="39514-135">notApplicableCount</span></span>|<span data-ttu-id="39514-136">Int32</span><span class="sxs-lookup"><span data-stu-id="39514-136">Int32</span></span>|<span data-ttu-id="39514-137">Número de usuarios no aplicables</span><span class="sxs-lookup"><span data-stu-id="39514-137">Number of not applicable users.</span></span>|
|<span data-ttu-id="39514-138">successCount</span><span class="sxs-lookup"><span data-stu-id="39514-138">successCount</span></span>|<span data-ttu-id="39514-139">Int32</span><span class="sxs-lookup"><span data-stu-id="39514-139">Int32</span></span>|<span data-ttu-id="39514-140">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="39514-140">Number of succeeded Users</span></span>|
|<span data-ttu-id="39514-141">errorCount</span><span class="sxs-lookup"><span data-stu-id="39514-141">errorCount</span></span>|<span data-ttu-id="39514-142">Int32</span><span class="sxs-lookup"><span data-stu-id="39514-142">Int32</span></span>|<span data-ttu-id="39514-143">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="39514-143">Number of error Users</span></span>|
|<span data-ttu-id="39514-144">failedCount</span><span class="sxs-lookup"><span data-stu-id="39514-144">failedCount</span></span>|<span data-ttu-id="39514-145">Int32</span><span class="sxs-lookup"><span data-stu-id="39514-145">Int32</span></span>|<span data-ttu-id="39514-146">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="39514-146">Number of failed Users</span></span>|
|<span data-ttu-id="39514-147">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="39514-147">lastUpdateDateTime</span></span>|<span data-ttu-id="39514-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39514-148">DateTimeOffset</span></span>|<span data-ttu-id="39514-149">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="39514-149">Last update time</span></span>|
|<span data-ttu-id="39514-150">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="39514-150">configurationVersion</span></span>|<span data-ttu-id="39514-151">Int32</span><span class="sxs-lookup"><span data-stu-id="39514-151">Int32</span></span>|<span data-ttu-id="39514-152">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="39514-152">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="39514-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39514-153">Response</span></span>
<span data-ttu-id="39514-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39514-154">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="39514-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39514-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="39514-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39514-156">Request</span></span>
<span data-ttu-id="39514-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39514-157">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatusOverview
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

### <a name="response"></a><span data-ttu-id="39514-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39514-158">Response</span></span>
<span data-ttu-id="39514-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39514-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 331

{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserOverview",
  "id": "000e52d7-52d7-000e-d752-0e00d7520e00",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```




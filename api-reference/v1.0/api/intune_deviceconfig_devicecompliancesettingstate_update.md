# <a name="update-devicecompliancesettingstate"></a><span data-ttu-id="cc735-101">Actualizar deviceComplianceSettingState</span><span class="sxs-lookup"><span data-stu-id="cc735-101">Update deviceComplianceSettingState</span></span>

> <span data-ttu-id="cc735-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cc735-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cc735-103">Actualice las propiedades de un objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="cc735-103">Update the properties of a [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cc735-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cc735-104">Prerequisites</span></span>
<span data-ttu-id="cc735-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cc735-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cc735-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc735-107">Permission type</span></span>|<span data-ttu-id="cc735-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc735-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cc735-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc735-109">Delegated (work or school account)</span></span>|<span data-ttu-id="cc735-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cc735-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="cc735-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc735-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cc735-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc735-112">Not supported.</span></span>|
|<span data-ttu-id="cc735-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc735-113">Application</span></span>|<span data-ttu-id="cc735-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc735-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cc735-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc735-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates/{deviceComplianceSettingStateId}
```

## <a name="request-headers"></a><span data-ttu-id="cc735-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc735-116">Request headers</span></span>
|<span data-ttu-id="cc735-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc735-117">Header</span></span>|<span data-ttu-id="cc735-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cc735-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cc735-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc735-119">Authorization</span></span>|<span data-ttu-id="cc735-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cc735-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cc735-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cc735-121">Accept</span></span>|<span data-ttu-id="cc735-122">application/json</span><span class="sxs-lookup"><span data-stu-id="cc735-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cc735-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc735-123">Request body</span></span>
<span data-ttu-id="cc735-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="cc735-124">In the request body, supply a JSON representation for the [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md) object.</span></span>

<span data-ttu-id="cc735-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="cc735-125">The following table shows the properties that are required when you create the [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).</span></span>

|<span data-ttu-id="cc735-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cc735-126">Property</span></span>|<span data-ttu-id="cc735-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc735-127">Type</span></span>|<span data-ttu-id="cc735-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc735-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cc735-129">id</span><span class="sxs-lookup"><span data-stu-id="cc735-129">id</span></span>|<span data-ttu-id="cc735-130">String</span><span class="sxs-lookup"><span data-stu-id="cc735-130">String</span></span>|<span data-ttu-id="cc735-131">Clave de la entidad</span><span class="sxs-lookup"><span data-stu-id="cc735-131">Key of the entity</span></span>|
|<span data-ttu-id="cc735-132">ajustes</span><span class="sxs-lookup"><span data-stu-id="cc735-132">setting</span></span>|<span data-ttu-id="cc735-133">String</span><span class="sxs-lookup"><span data-stu-id="cc735-133">String</span></span>|<span data-ttu-id="cc735-134">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cc735-134">The setting class name and property name.</span></span>|
|<span data-ttu-id="cc735-135">settingName</span><span class="sxs-lookup"><span data-stu-id="cc735-135">settingName</span></span>|<span data-ttu-id="cc735-136">String</span><span class="sxs-lookup"><span data-stu-id="cc735-136">String</span></span>|<span data-ttu-id="cc735-137">El nombre de configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="cc735-137">The Setting Name that is being reported</span></span>|
|<span data-ttu-id="cc735-138">deviceId</span><span class="sxs-lookup"><span data-stu-id="cc735-138">deviceId</span></span>|<span data-ttu-id="cc735-139">String</span><span class="sxs-lookup"><span data-stu-id="cc735-139">String</span></span>|<span data-ttu-id="cc735-140">El identificador del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="cc735-140">The Device Id that is being reported</span></span>|
|<span data-ttu-id="cc735-141">deviceName</span><span class="sxs-lookup"><span data-stu-id="cc735-141">deviceName</span></span>|<span data-ttu-id="cc735-142">String</span><span class="sxs-lookup"><span data-stu-id="cc735-142">String</span></span>|<span data-ttu-id="cc735-143">El nombre del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="cc735-143">The Device Name that is being reported</span></span>|
|<span data-ttu-id="cc735-144">userId</span><span class="sxs-lookup"><span data-stu-id="cc735-144">userId</span></span>|<span data-ttu-id="cc735-145">String</span><span class="sxs-lookup"><span data-stu-id="cc735-145">String</span></span>|<span data-ttu-id="cc735-146">El identificador del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="cc735-146">The user Id that is being reported</span></span>|
|<span data-ttu-id="cc735-147">userEmail</span><span class="sxs-lookup"><span data-stu-id="cc735-147">userEmail</span></span>|<span data-ttu-id="cc735-148">String</span><span class="sxs-lookup"><span data-stu-id="cc735-148">String</span></span>|<span data-ttu-id="cc735-149">La dirección de correo electrónico del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="cc735-149">The User email address that is being reported</span></span>|
|<span data-ttu-id="cc735-150">userName</span><span class="sxs-lookup"><span data-stu-id="cc735-150">userName</span></span>|<span data-ttu-id="cc735-151">String</span><span class="sxs-lookup"><span data-stu-id="cc735-151">String</span></span>|<span data-ttu-id="cc735-152">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="cc735-152">The User Name that is being reported</span></span>|
|<span data-ttu-id="cc735-153">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc735-153">userPrincipalName</span></span>|<span data-ttu-id="cc735-154">String</span><span class="sxs-lookup"><span data-stu-id="cc735-154">String</span></span>|<span data-ttu-id="cc735-155">El nombre principal de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="cc735-155">The User PrincipalName that is being reported</span></span>|
|<span data-ttu-id="cc735-156">deviceModel</span><span class="sxs-lookup"><span data-stu-id="cc735-156">deviceModel</span></span>|<span data-ttu-id="cc735-157">String</span><span class="sxs-lookup"><span data-stu-id="cc735-157">String</span></span>|<span data-ttu-id="cc735-158">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="cc735-158">The device model that is being reported</span></span>|
|<span data-ttu-id="cc735-159">state</span><span class="sxs-lookup"><span data-stu-id="cc735-159">state</span></span>|[<span data-ttu-id="cc735-160">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="cc735-160">complianceStatus</span></span>](../resources/intune_shared_compliancestatus.md)|<span data-ttu-id="cc735-161">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="cc735-161">The compliance state of the setting.</span></span> <span data-ttu-id="cc735-162">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="cc735-162">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="cc735-163">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="cc735-163">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="cc735-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cc735-164">DateTimeOffset</span></span>|<span data-ttu-id="cc735-165">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="cc735-165">The DateTime when device compliance grace period expires</span></span>|



## <a name="response"></a><span data-ttu-id="cc735-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc735-166">Response</span></span>
<span data-ttu-id="cc735-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc735-167">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cc735-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc735-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="cc735-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc735-169">Request</span></span>
<span data-ttu-id="cc735-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc735-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates/{deviceComplianceSettingStateId}
Content-type: application/json
Content-length: 517

{
  "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "userId": "User Id value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "deviceModel": "Device Model value",
  "state": "notApplicable",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
}
```

### <a name="response"></a><span data-ttu-id="cc735-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc735-171">Response</span></span>
<span data-ttu-id="cc735-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cc735-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 566

{
  "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
  "id": "9905f955-f955-9905-55f9-059955f90599",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "userId": "User Id value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "deviceModel": "Device Model value",
  "state": "notApplicable",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
}
```




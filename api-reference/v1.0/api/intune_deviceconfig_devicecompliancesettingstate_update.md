# <a name="update-devicecompliancesettingstate"></a><span data-ttu-id="25e0c-101">Actualizar deviceComplianceSettingState</span><span class="sxs-lookup"><span data-stu-id="25e0c-101">Update deviceComplianceSettingState</span></span>

> <span data-ttu-id="25e0c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25e0c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25e0c-103">Actualice las propiedades de un objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="25e0c-103">Update the properties of a [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="25e0c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="25e0c-104">Prerequisites</span></span>
<span data-ttu-id="25e0c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="25e0c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="25e0c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25e0c-107">Permission type</span></span>|<span data-ttu-id="25e0c-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25e0c-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="25e0c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25e0c-109">Delegated (work or school account)</span></span>|<span data-ttu-id="25e0c-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="25e0c-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="25e0c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="25e0c-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="25e0c-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25e0c-112">Not supported.</span></span>|
|<span data-ttu-id="25e0c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25e0c-113">Application</span></span>|<span data-ttu-id="25e0c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25e0c-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="25e0c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25e0c-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates/{deviceComplianceSettingStateId}
```

## <a name="request-headers"></a><span data-ttu-id="25e0c-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25e0c-116">Request headers</span></span>
|<span data-ttu-id="25e0c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25e0c-117">Header</span></span>|<span data-ttu-id="25e0c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="25e0c-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="25e0c-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="25e0c-119">Authorization</span></span>|<span data-ttu-id="25e0c-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="25e0c-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="25e0c-121">Accept</span><span class="sxs-lookup"><span data-stu-id="25e0c-121">Accept</span></span>|<span data-ttu-id="25e0c-122">application/json</span><span class="sxs-lookup"><span data-stu-id="25e0c-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="25e0c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25e0c-123">Request body</span></span>
<span data-ttu-id="25e0c-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="25e0c-124">In the request body, supply a JSON representation for the [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md) object.</span></span>

<span data-ttu-id="25e0c-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="25e0c-125">The following table shows the properties that are required when you create the [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md).</span></span>

|<span data-ttu-id="25e0c-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25e0c-126">Property</span></span>|<span data-ttu-id="25e0c-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="25e0c-127">Type</span></span>|<span data-ttu-id="25e0c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="25e0c-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="25e0c-129">id</span><span class="sxs-lookup"><span data-stu-id="25e0c-129">id</span></span>|<span data-ttu-id="25e0c-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-130">String</span></span>|<span data-ttu-id="25e0c-131">Clave de la entidad</span><span class="sxs-lookup"><span data-stu-id="25e0c-131">Key of the entity</span></span>|
|<span data-ttu-id="25e0c-132">setting</span><span class="sxs-lookup"><span data-stu-id="25e0c-132">setting</span></span>|<span data-ttu-id="25e0c-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-133">String</span></span>|<span data-ttu-id="25e0c-134">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="25e0c-134">The setting class name and property name.</span></span>|
|<span data-ttu-id="25e0c-135">settingName</span><span class="sxs-lookup"><span data-stu-id="25e0c-135">settingName</span></span>|<span data-ttu-id="25e0c-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-136">String</span></span>|<span data-ttu-id="25e0c-137">El nombre de configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="25e0c-137">The Setting Name that is being reported</span></span>|
|<span data-ttu-id="25e0c-138">deviceId</span><span class="sxs-lookup"><span data-stu-id="25e0c-138">deviceId</span></span>|<span data-ttu-id="25e0c-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-139">String</span></span>|<span data-ttu-id="25e0c-140">El identificador del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="25e0c-140">The Device Id that is being reported</span></span>|
|<span data-ttu-id="25e0c-141">deviceName</span><span class="sxs-lookup"><span data-stu-id="25e0c-141">deviceName</span></span>|<span data-ttu-id="25e0c-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-142">String</span></span>|<span data-ttu-id="25e0c-143">El nombre del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="25e0c-143">The Device Name that is being reported</span></span>|
|<span data-ttu-id="25e0c-144">userId</span><span class="sxs-lookup"><span data-stu-id="25e0c-144">userId</span></span>|<span data-ttu-id="25e0c-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-145">String</span></span>|<span data-ttu-id="25e0c-146">El identificador del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="25e0c-146">The user Id that is being reported</span></span>|
|<span data-ttu-id="25e0c-147">userEmail</span><span class="sxs-lookup"><span data-stu-id="25e0c-147">userEmail</span></span>|<span data-ttu-id="25e0c-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-148">String</span></span>|<span data-ttu-id="25e0c-149">La dirección de correo electrónico del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="25e0c-149">The User email address that is being reported</span></span>|
|<span data-ttu-id="25e0c-150">userName</span><span class="sxs-lookup"><span data-stu-id="25e0c-150">userName</span></span>|<span data-ttu-id="25e0c-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-151">String</span></span>|<span data-ttu-id="25e0c-152">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="25e0c-152">The User Name that is being reported</span></span>|
|<span data-ttu-id="25e0c-153">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="25e0c-153">userPrincipalName</span></span>|<span data-ttu-id="25e0c-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-154">String</span></span>|<span data-ttu-id="25e0c-155">El nombre principal de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="25e0c-155">The User PrincipalName that is being reported</span></span>|
|<span data-ttu-id="25e0c-156">deviceModel</span><span class="sxs-lookup"><span data-stu-id="25e0c-156">deviceModel</span></span>|<span data-ttu-id="25e0c-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="25e0c-157">String</span></span>|<span data-ttu-id="25e0c-158">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="25e0c-158">The device model that is being reported</span></span>|
|<span data-ttu-id="25e0c-159">state</span><span class="sxs-lookup"><span data-stu-id="25e0c-159">state</span></span>|[<span data-ttu-id="25e0c-160">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="25e0c-160">complianceStatus</span></span>](../resources/intune_shared_compliancestatus.md)|<span data-ttu-id="25e0c-p102">El estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="25e0c-p102">The compliance state of the setting Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`.</span></span>|
|<span data-ttu-id="25e0c-163">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="25e0c-163">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="25e0c-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="25e0c-164">DateTimeOffset</span></span>|<span data-ttu-id="25e0c-165">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="25e0c-165">The DateTime when device compliance grace period expires</span></span>|



## <a name="response"></a><span data-ttu-id="25e0c-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25e0c-166">Response</span></span>
<span data-ttu-id="25e0c-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25e0c-167">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceSettingState](../resources/intune_deviceconfig_devicecompliancesettingstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="25e0c-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25e0c-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="25e0c-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25e0c-169">Request</span></span>
<span data-ttu-id="25e0c-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25e0c-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates/{deviceComplianceSettingStateId}
Content-type: application/json
Content-length: 450

{
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

### <a name="response"></a><span data-ttu-id="25e0c-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25e0c-171">Response</span></span>
<span data-ttu-id="25e0c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="25e0c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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









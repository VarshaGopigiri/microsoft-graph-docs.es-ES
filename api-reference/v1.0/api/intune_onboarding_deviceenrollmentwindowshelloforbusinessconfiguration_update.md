# <a name="update-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="cf19b-101">Actualizar deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf19b-101">Update deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="cf19b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf19b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf19b-103">Actualice las propiedades de un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cf19b-103">Update the properties of a [calendar](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cf19b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cf19b-104">Prerequisites</span></span>
<span data-ttu-id="cf19b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cf19b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cf19b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf19b-107">Permission type</span></span>|<span data-ttu-id="cf19b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf19b-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cf19b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf19b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="cf19b-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf19b-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="cf19b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf19b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cf19b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf19b-112">Not supported.</span></span>|
|<span data-ttu-id="cf19b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf19b-113">Application</span></span>|<span data-ttu-id="cf19b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf19b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cf19b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf19b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="cf19b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf19b-116">Request headers</span></span>
|<span data-ttu-id="cf19b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf19b-117">Header</span></span>|<span data-ttu-id="cf19b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cf19b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cf19b-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="cf19b-119">Authorization</span></span>|<span data-ttu-id="cf19b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cf19b-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="cf19b-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cf19b-121">Accept</span></span>|<span data-ttu-id="cf19b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="cf19b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cf19b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf19b-123">Request body</span></span>
<span data-ttu-id="cf19b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cf19b-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>

<span data-ttu-id="cf19b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cf19b-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="cf19b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf19b-126">Property</span></span>|<span data-ttu-id="cf19b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf19b-127">Type</span></span>|<span data-ttu-id="cf19b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf19b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf19b-129">id</span><span class="sxs-lookup"><span data-stu-id="cf19b-129">id</span></span>|<span data-ttu-id="cf19b-130">String</span><span class="sxs-lookup"><span data-stu-id="cf19b-130">String</span></span>|<span data-ttu-id="cf19b-131">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf19b-131">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cf19b-132">displayName</span><span class="sxs-lookup"><span data-stu-id="cf19b-132">displayName</span></span>|<span data-ttu-id="cf19b-133">String</span><span class="sxs-lookup"><span data-stu-id="cf19b-133">String</span></span>|<span data-ttu-id="cf19b-134">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf19b-134">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cf19b-135">description</span><span class="sxs-lookup"><span data-stu-id="cf19b-135">description</span></span>|<span data-ttu-id="cf19b-136">String</span><span class="sxs-lookup"><span data-stu-id="cf19b-136">String</span></span>|<span data-ttu-id="cf19b-137">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf19b-137">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cf19b-138">prioridad</span><span class="sxs-lookup"><span data-stu-id="cf19b-138">priority</span></span>|<span data-ttu-id="cf19b-139">Int32</span><span class="sxs-lookup"><span data-stu-id="cf19b-139">Int32</span></span>|<span data-ttu-id="cf19b-140">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf19b-140">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cf19b-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cf19b-141">createdDateTime</span></span>|<span data-ttu-id="cf19b-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf19b-142">DateTimeOffset</span></span>|<span data-ttu-id="cf19b-143">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf19b-143">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cf19b-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cf19b-144">lastModifiedDateTime</span></span>|<span data-ttu-id="cf19b-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf19b-145">DateTimeOffset</span></span>|<span data-ttu-id="cf19b-146">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf19b-146">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cf19b-147">version</span><span class="sxs-lookup"><span data-stu-id="cf19b-147">version</span></span>|<span data-ttu-id="cf19b-148">Int32</span><span class="sxs-lookup"><span data-stu-id="cf19b-148">Int32</span></span>|<span data-ttu-id="cf19b-149">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf19b-149">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="cf19b-150">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="cf19b-150">pinMinimumLength</span></span>|<span data-ttu-id="cf19b-151">Int32</span><span class="sxs-lookup"><span data-stu-id="cf19b-151">Int32</span></span>|<span data-ttu-id="cf19b-152">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf19b-152">Not yet documented</span></span>|
|<span data-ttu-id="cf19b-153">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="cf19b-153">pinMaximumLength</span></span>|<span data-ttu-id="cf19b-154">Int32</span><span class="sxs-lookup"><span data-stu-id="cf19b-154">Int32</span></span>|<span data-ttu-id="cf19b-155">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf19b-155">Not yet documented</span></span>|
|<span data-ttu-id="cf19b-156">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="cf19b-156">pinUppercaseCharactersUsage</span></span>|<span data-ttu-id="cf19b-157">String</span><span class="sxs-lookup"><span data-stu-id="cf19b-157">String</span></span>|<span data-ttu-id="cf19b-158">Todavía no documentado Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="cf19b-158">Not yet documented Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="cf19b-159">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="cf19b-159">pinLowercaseCharactersUsage</span></span>|<span data-ttu-id="cf19b-160">String</span><span class="sxs-lookup"><span data-stu-id="cf19b-160">String</span></span>|<span data-ttu-id="cf19b-161">Todavía no documentado Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="cf19b-161">Not yet documented Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="cf19b-162">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="cf19b-162">pinSpecialCharactersUsage</span></span>|<span data-ttu-id="cf19b-163">String</span><span class="sxs-lookup"><span data-stu-id="cf19b-163">String</span></span>|<span data-ttu-id="cf19b-164">Todavía no documentado Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="cf19b-164">Not yet documented Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="cf19b-165">state</span><span class="sxs-lookup"><span data-stu-id="cf19b-165">state</span></span>|<span data-ttu-id="cf19b-166">String</span><span class="sxs-lookup"><span data-stu-id="cf19b-166">String</span></span>|<span data-ttu-id="cf19b-167">Todavía no documentado Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="cf19b-167">Not yet documented Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="cf19b-168">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="cf19b-168">securityDeviceRequired</span></span>|<span data-ttu-id="cf19b-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf19b-169">Boolean</span></span>|<span data-ttu-id="cf19b-170">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf19b-170">Not yet documented</span></span>|
|<span data-ttu-id="cf19b-171">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="cf19b-171">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="cf19b-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf19b-172">Boolean</span></span>|<span data-ttu-id="cf19b-173">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf19b-173">Not yet documented</span></span>|
|<span data-ttu-id="cf19b-174">remotePassportEnabled</span><span class="sxs-lookup"><span data-stu-id="cf19b-174">remotePassportEnabled</span></span>|<span data-ttu-id="cf19b-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf19b-175">Boolean</span></span>|<span data-ttu-id="cf19b-176">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf19b-176">Not yet documented</span></span>|
|<span data-ttu-id="cf19b-177">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="cf19b-177">pinPreviousBlockCount</span></span>|<span data-ttu-id="cf19b-178">Int32</span><span class="sxs-lookup"><span data-stu-id="cf19b-178">Int32</span></span>|<span data-ttu-id="cf19b-179">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf19b-179">Not yet documented</span></span>|
|<span data-ttu-id="cf19b-180">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="cf19b-180">pinExpirationInDays</span></span>|<span data-ttu-id="cf19b-181">Int32</span><span class="sxs-lookup"><span data-stu-id="cf19b-181">Int32</span></span>|<span data-ttu-id="cf19b-182">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf19b-182">Not yet documented</span></span>|
|<span data-ttu-id="cf19b-183">enhancedBiometricsState</span><span class="sxs-lookup"><span data-stu-id="cf19b-183">enhancedBiometricsState</span></span>|<span data-ttu-id="cf19b-184">String</span><span class="sxs-lookup"><span data-stu-id="cf19b-184">String</span></span>|<span data-ttu-id="cf19b-185">Todavía no documentado Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="cf19b-185">Not yet documented Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|



## <a name="response"></a><span data-ttu-id="cf19b-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf19b-186">Response</span></span>
<span data-ttu-id="cf19b-187">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf19b-187">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf19b-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf19b-188">Example</span></span>
### <a name="request"></a><span data-ttu-id="cf19b-189">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf19b-189">Request</span></span>
<span data-ttu-id="cf19b-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf19b-190">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 602

{
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "state": "enabled",
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "remotePassportEnabled": true,
  "pinPreviousBlockCount": 5,
  "pinExpirationInDays": 3,
  "enhancedBiometricsState": "enabled"
}
```

### <a name="response"></a><span data-ttu-id="cf19b-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf19b-191">Response</span></span>
<span data-ttu-id="cf19b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf19b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 801

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
  "id": "3068e0cd-e0cd-3068-cde0-6830cde06830",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "state": "enabled",
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "remotePassportEnabled": true,
  "pinPreviousBlockCount": 5,
  "pinExpirationInDays": 3,
  "enhancedBiometricsState": "enabled"
}
```




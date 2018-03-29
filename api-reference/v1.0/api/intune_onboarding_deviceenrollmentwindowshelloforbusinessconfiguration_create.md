# <a name="create-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="e5f92-101">Crear deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5f92-101">Create deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="e5f92-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e5f92-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e5f92-103">Cree un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e5f92-103">Create a new [plannerBucket](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e5f92-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e5f92-104">Prerequisites</span></span>
<span data-ttu-id="e5f92-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e5f92-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e5f92-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5f92-107">Permission type</span></span>|<span data-ttu-id="e5f92-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5f92-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e5f92-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5f92-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e5f92-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e5f92-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="e5f92-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5f92-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e5f92-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5f92-112">Not supported.</span></span>|
|<span data-ttu-id="e5f92-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5f92-113">Application</span></span>|<span data-ttu-id="e5f92-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5f92-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e5f92-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5f92-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="e5f92-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5f92-116">Request headers</span></span>
|<span data-ttu-id="e5f92-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5f92-117">Header</span></span>|<span data-ttu-id="e5f92-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e5f92-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e5f92-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5f92-119">Authorization</span></span>|<span data-ttu-id="e5f92-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e5f92-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="e5f92-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e5f92-121">Accept</span></span>|<span data-ttu-id="e5f92-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e5f92-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e5f92-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e5f92-123">Request body</span></span>
<span data-ttu-id="e5f92-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5f92-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="e5f92-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5f92-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="e5f92-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5f92-126">Property</span></span>|<span data-ttu-id="e5f92-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5f92-127">Type</span></span>|<span data-ttu-id="e5f92-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5f92-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e5f92-129">id</span><span class="sxs-lookup"><span data-stu-id="e5f92-129">id</span></span>|<span data-ttu-id="e5f92-130">String</span><span class="sxs-lookup"><span data-stu-id="e5f92-130">String</span></span>|<span data-ttu-id="e5f92-131">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e5f92-131">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e5f92-132">displayName</span><span class="sxs-lookup"><span data-stu-id="e5f92-132">displayName</span></span>|<span data-ttu-id="e5f92-133">String</span><span class="sxs-lookup"><span data-stu-id="e5f92-133">String</span></span>|<span data-ttu-id="e5f92-134">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e5f92-134">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e5f92-135">description</span><span class="sxs-lookup"><span data-stu-id="e5f92-135">description</span></span>|<span data-ttu-id="e5f92-136">String</span><span class="sxs-lookup"><span data-stu-id="e5f92-136">String</span></span>|<span data-ttu-id="e5f92-137">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e5f92-137">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e5f92-138">prioridad</span><span class="sxs-lookup"><span data-stu-id="e5f92-138">priority</span></span>|<span data-ttu-id="e5f92-139">Int32</span><span class="sxs-lookup"><span data-stu-id="e5f92-139">Int32</span></span>|<span data-ttu-id="e5f92-140">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e5f92-140">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e5f92-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e5f92-141">createdDateTime</span></span>|<span data-ttu-id="e5f92-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e5f92-142">DateTimeOffset</span></span>|<span data-ttu-id="e5f92-143">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e5f92-143">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e5f92-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e5f92-144">lastModifiedDateTime</span></span>|<span data-ttu-id="e5f92-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e5f92-145">DateTimeOffset</span></span>|<span data-ttu-id="e5f92-146">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e5f92-146">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e5f92-147">version</span><span class="sxs-lookup"><span data-stu-id="e5f92-147">version</span></span>|<span data-ttu-id="e5f92-148">Int32</span><span class="sxs-lookup"><span data-stu-id="e5f92-148">Int32</span></span>|<span data-ttu-id="e5f92-149">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e5f92-149">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="e5f92-150">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="e5f92-150">pinMinimumLength</span></span>|<span data-ttu-id="e5f92-151">Int32</span><span class="sxs-lookup"><span data-stu-id="e5f92-151">Int32</span></span>|<span data-ttu-id="e5f92-152">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e5f92-152">Not yet documented</span></span>|
|<span data-ttu-id="e5f92-153">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="e5f92-153">pinMaximumLength</span></span>|<span data-ttu-id="e5f92-154">Int32</span><span class="sxs-lookup"><span data-stu-id="e5f92-154">Int32</span></span>|<span data-ttu-id="e5f92-155">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e5f92-155">Not yet documented</span></span>|
|<span data-ttu-id="e5f92-156">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="e5f92-156">pinUppercaseCharactersUsage</span></span>|<span data-ttu-id="e5f92-157">String</span><span class="sxs-lookup"><span data-stu-id="e5f92-157">String</span></span>|<span data-ttu-id="e5f92-158">Todavía no documentado Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="e5f92-158">Not yet documented Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="e5f92-159">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="e5f92-159">pinLowercaseCharactersUsage</span></span>|<span data-ttu-id="e5f92-160">String</span><span class="sxs-lookup"><span data-stu-id="e5f92-160">String</span></span>|<span data-ttu-id="e5f92-161">Todavía no documentado Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="e5f92-161">Not yet documented Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="e5f92-162">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="e5f92-162">pinSpecialCharactersUsage</span></span>|<span data-ttu-id="e5f92-163">String</span><span class="sxs-lookup"><span data-stu-id="e5f92-163">String</span></span>|<span data-ttu-id="e5f92-164">Todavía no documentado Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="e5f92-164">Not yet documented Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="e5f92-165">state</span><span class="sxs-lookup"><span data-stu-id="e5f92-165">state</span></span>|<span data-ttu-id="e5f92-166">String</span><span class="sxs-lookup"><span data-stu-id="e5f92-166">String</span></span>|<span data-ttu-id="e5f92-167">Todavía no documentado Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="e5f92-167">Not yet documented Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="e5f92-168">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="e5f92-168">securityDeviceRequired</span></span>|<span data-ttu-id="e5f92-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="e5f92-169">Boolean</span></span>|<span data-ttu-id="e5f92-170">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e5f92-170">Not yet documented</span></span>|
|<span data-ttu-id="e5f92-171">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="e5f92-171">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="e5f92-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="e5f92-172">Boolean</span></span>|<span data-ttu-id="e5f92-173">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e5f92-173">Not yet documented</span></span>|
|<span data-ttu-id="e5f92-174">remotePassportEnabled</span><span class="sxs-lookup"><span data-stu-id="e5f92-174">remotePassportEnabled</span></span>|<span data-ttu-id="e5f92-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="e5f92-175">Boolean</span></span>|<span data-ttu-id="e5f92-176">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e5f92-176">Not yet documented</span></span>|
|<span data-ttu-id="e5f92-177">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="e5f92-177">pinPreviousBlockCount</span></span>|<span data-ttu-id="e5f92-178">Int32</span><span class="sxs-lookup"><span data-stu-id="e5f92-178">Int32</span></span>|<span data-ttu-id="e5f92-179">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e5f92-179">Not yet documented</span></span>|
|<span data-ttu-id="e5f92-180">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="e5f92-180">pinExpirationInDays</span></span>|<span data-ttu-id="e5f92-181">Int32</span><span class="sxs-lookup"><span data-stu-id="e5f92-181">Int32</span></span>|<span data-ttu-id="e5f92-182">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e5f92-182">Not yet documented</span></span>|
|<span data-ttu-id="e5f92-183">enhancedBiometricsState</span><span class="sxs-lookup"><span data-stu-id="e5f92-183">enhancedBiometricsState</span></span>|<span data-ttu-id="e5f92-184">String</span><span class="sxs-lookup"><span data-stu-id="e5f92-184">String</span></span>|<span data-ttu-id="e5f92-185">Todavía no documentado Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="e5f92-185">Not yet documented Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|



## <a name="response"></a><span data-ttu-id="e5f92-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5f92-186">Response</span></span>
<span data-ttu-id="e5f92-187">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5f92-187">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e5f92-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5f92-188">Example</span></span>
### <a name="request"></a><span data-ttu-id="e5f92-189">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5f92-189">Request</span></span>
<span data-ttu-id="e5f92-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5f92-190">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations
Content-type: application/json
Content-length: 693

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
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

### <a name="response"></a><span data-ttu-id="e5f92-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5f92-191">Response</span></span>
<span data-ttu-id="e5f92-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e5f92-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




# <a name="create-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="296e5-101">Crear deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="296e5-101">Create deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="296e5-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="296e5-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="296e5-103">Cree un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="296e5-103">Create a new [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="296e5-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="296e5-104">Prerequisites</span></span>
<span data-ttu-id="296e5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="296e5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="296e5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="296e5-107">Permission type</span></span>|<span data-ttu-id="296e5-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="296e5-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="296e5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="296e5-109">Delegated (work or school account)</span></span>|<span data-ttu-id="296e5-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="296e5-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="296e5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="296e5-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="296e5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="296e5-112">Not supported.</span></span>|
|<span data-ttu-id="296e5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="296e5-113">Application</span></span>|<span data-ttu-id="296e5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="296e5-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="296e5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="296e5-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="296e5-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="296e5-116">Request headers</span></span>
|<span data-ttu-id="296e5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="296e5-117">Header</span></span>|<span data-ttu-id="296e5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="296e5-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="296e5-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="296e5-119">Authorization</span></span>|<span data-ttu-id="296e5-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="296e5-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="296e5-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="296e5-121">Accept</span></span>|<span data-ttu-id="296e5-122">application/json</span><span class="sxs-lookup"><span data-stu-id="296e5-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="296e5-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="296e5-123">Request body</span></span>
<span data-ttu-id="296e5-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="296e5-124">In the request body, supply a JSON representation for the deviceEnrollmentWindowsHelloForBusinessConfiguration object.</span></span>

<span data-ttu-id="296e5-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentWindowsHelloForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="296e5-125">The following table shows the properties that are required when you create the deviceEnrollmentWindowsHelloForBusinessConfiguration.</span></span>

|<span data-ttu-id="296e5-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="296e5-126">Property</span></span>|<span data-ttu-id="296e5-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="296e5-127">Type</span></span>|<span data-ttu-id="296e5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="296e5-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="296e5-129">id</span><span class="sxs-lookup"><span data-stu-id="296e5-129">id</span></span>|<span data-ttu-id="296e5-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="296e5-130">String</span></span>|<span data-ttu-id="296e5-131">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="296e5-131">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="296e5-132">displayName</span><span class="sxs-lookup"><span data-stu-id="296e5-132">displayName</span></span>|<span data-ttu-id="296e5-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="296e5-133">String</span></span>|<span data-ttu-id="296e5-134">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="296e5-134">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="296e5-135">descripción</span><span class="sxs-lookup"><span data-stu-id="296e5-135">description</span></span>|<span data-ttu-id="296e5-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="296e5-136">String</span></span>|<span data-ttu-id="296e5-137">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="296e5-137">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="296e5-138">prioridad</span><span class="sxs-lookup"><span data-stu-id="296e5-138">priority</span></span>|<span data-ttu-id="296e5-139">Int32</span><span class="sxs-lookup"><span data-stu-id="296e5-139">Int32</span></span>|<span data-ttu-id="296e5-140">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="296e5-140">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="296e5-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="296e5-141">createdDateTime</span></span>|<span data-ttu-id="296e5-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="296e5-142">DateTimeOffset</span></span>|<span data-ttu-id="296e5-143">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="296e5-143">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="296e5-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="296e5-144">lastModifiedDateTime</span></span>|<span data-ttu-id="296e5-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="296e5-145">DateTimeOffset</span></span>|<span data-ttu-id="296e5-146">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="296e5-146">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="296e5-147">version</span><span class="sxs-lookup"><span data-stu-id="296e5-147">version</span></span>|<span data-ttu-id="296e5-148">Int32</span><span class="sxs-lookup"><span data-stu-id="296e5-148">Int32</span></span>|<span data-ttu-id="296e5-149">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="296e5-149">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="296e5-150">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="296e5-150">pinMinimumLength</span></span>|<span data-ttu-id="296e5-151">Int32</span><span class="sxs-lookup"><span data-stu-id="296e5-151">Int32</span></span>|<span data-ttu-id="296e5-152">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="296e5-152">Not yet documented</span></span>|
|<span data-ttu-id="296e5-153">pinMaximumLength</span><span class="sxs-lookup"><span data-stu-id="296e5-153">pinMaximumLength</span></span>|<span data-ttu-id="296e5-154">Int32</span><span class="sxs-lookup"><span data-stu-id="296e5-154">Int32</span></span>|<span data-ttu-id="296e5-155">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="296e5-155">Not yet documented</span></span>|
|<span data-ttu-id="296e5-156">pinUppercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="296e5-156">pinUppercaseCharactersUsage</span></span>|[<span data-ttu-id="296e5-157">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="296e5-157">windowsHelloForBusinessPinUsage</span></span>](../resources/intune_onboarding_windowshelloforbusinesspinusage.md)|<span data-ttu-id="296e5-p102">Todavía no documentado. Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="296e5-p102">Not yet documented Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="296e5-160">pinLowercaseCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="296e5-160">pinLowercaseCharactersUsage</span></span>|[<span data-ttu-id="296e5-161">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="296e5-161">windowsHelloForBusinessPinUsage</span></span>](../resources/intune_onboarding_windowshelloforbusinesspinusage.md)|<span data-ttu-id="296e5-p103">Todavía no documentado. Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="296e5-p103">Not yet documented Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="296e5-164">pinSpecialCharactersUsage</span><span class="sxs-lookup"><span data-stu-id="296e5-164">pinSpecialCharactersUsage</span></span>|[<span data-ttu-id="296e5-165">windowsHelloForBusinessPinUsage</span><span class="sxs-lookup"><span data-stu-id="296e5-165">windowsHelloForBusinessPinUsage</span></span>](../resources/intune_onboarding_windowshelloforbusinesspinusage.md)|<span data-ttu-id="296e5-p104">Todavía no documentado. Los valores posibles son: `allowed`, `required` y `disallowed`.</span><span class="sxs-lookup"><span data-stu-id="296e5-p104">Not yet documented Possible values are: `allowed`, `required`, `disallowed`.</span></span>|
|<span data-ttu-id="296e5-168">state</span><span class="sxs-lookup"><span data-stu-id="296e5-168">state</span></span>|[<span data-ttu-id="296e5-169">habilitación</span><span class="sxs-lookup"><span data-stu-id="296e5-169">Enablement</span></span>](../resources/intune_onboarding_enablement.md)|<span data-ttu-id="296e5-p105">Todavía no documentado. Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="296e5-p105">Not yet documented Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|
|<span data-ttu-id="296e5-172">securityDeviceRequired</span><span class="sxs-lookup"><span data-stu-id="296e5-172">securityDeviceRequired</span></span>|<span data-ttu-id="296e5-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="296e5-173">Boolean</span></span>|<span data-ttu-id="296e5-174">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="296e5-174">Not yet documented</span></span>|
|<span data-ttu-id="296e5-175">unlockWithBiometricsEnabled</span><span class="sxs-lookup"><span data-stu-id="296e5-175">unlockWithBiometricsEnabled</span></span>|<span data-ttu-id="296e5-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="296e5-176">Boolean</span></span>|<span data-ttu-id="296e5-177">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="296e5-177">Not yet documented</span></span>|
|<span data-ttu-id="296e5-178">remotePassportEnabled</span><span class="sxs-lookup"><span data-stu-id="296e5-178">remotePassportEnabled</span></span>|<span data-ttu-id="296e5-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="296e5-179">Boolean</span></span>|<span data-ttu-id="296e5-180">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="296e5-180">Not yet documented</span></span>|
|<span data-ttu-id="296e5-181">pinPreviousBlockCount</span><span class="sxs-lookup"><span data-stu-id="296e5-181">pinPreviousBlockCount</span></span>|<span data-ttu-id="296e5-182">Int32</span><span class="sxs-lookup"><span data-stu-id="296e5-182">Int32</span></span>|<span data-ttu-id="296e5-183">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="296e5-183">Not yet documented</span></span>|
|<span data-ttu-id="296e5-184">pinExpirationInDays</span><span class="sxs-lookup"><span data-stu-id="296e5-184">pinExpirationInDays</span></span>|<span data-ttu-id="296e5-185">Int32</span><span class="sxs-lookup"><span data-stu-id="296e5-185">Int32</span></span>|<span data-ttu-id="296e5-186">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="296e5-186">Not yet documented</span></span>|
|<span data-ttu-id="296e5-187">enhancedBiometricsState</span><span class="sxs-lookup"><span data-stu-id="296e5-187">enhancedBiometricsState</span></span>|[<span data-ttu-id="296e5-188">habilitación</span><span class="sxs-lookup"><span data-stu-id="296e5-188">Enablement</span></span>](../resources/intune_onboarding_enablement.md)|<span data-ttu-id="296e5-p106">Todavía no documentado. Los valores posibles son: `notConfigured`, `enabled` y `disabled`.</span><span class="sxs-lookup"><span data-stu-id="296e5-p106">Not yet documented Possible values are: `notConfigured`, `enabled`, `disabled`.</span></span>|



## <a name="response"></a><span data-ttu-id="296e5-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="296e5-191">Response</span></span>
<span data-ttu-id="296e5-192">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="296e5-192">If successful, this method returns a `201 Created` response code and a [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="296e5-193">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="296e5-193">Example</span></span>
### <a name="request"></a><span data-ttu-id="296e5-194">Solicitud</span><span class="sxs-lookup"><span data-stu-id="296e5-194">Request</span></span>
<span data-ttu-id="296e5-195">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="296e5-195">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="296e5-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="296e5-196">Response</span></span>
<span data-ttu-id="296e5-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="296e5-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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









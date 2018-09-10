# <a name="update-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="61ddc-101">Actualizar deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="61ddc-101">Update deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="61ddc-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="61ddc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="61ddc-103">Actualice las propiedades de un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="61ddc-103">Update the properties of a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="61ddc-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="61ddc-104">Prerequisites</span></span>
<span data-ttu-id="61ddc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="61ddc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="61ddc-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="61ddc-107">Permission type</span></span>|<span data-ttu-id="61ddc-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="61ddc-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="61ddc-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="61ddc-109">Delegated (work or school account)</span></span>|<span data-ttu-id="61ddc-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61ddc-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="61ddc-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="61ddc-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="61ddc-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="61ddc-112">Not supported.</span></span>|
|<span data-ttu-id="61ddc-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="61ddc-113">Application</span></span>|<span data-ttu-id="61ddc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="61ddc-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="61ddc-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="61ddc-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="61ddc-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="61ddc-116">Request headers</span></span>
|<span data-ttu-id="61ddc-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61ddc-117">Header</span></span>|<span data-ttu-id="61ddc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="61ddc-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="61ddc-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="61ddc-119">Authorization</span></span>|<span data-ttu-id="61ddc-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="61ddc-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="61ddc-121">Accept</span><span class="sxs-lookup"><span data-stu-id="61ddc-121">Accept</span></span>|<span data-ttu-id="61ddc-122">application/json</span><span class="sxs-lookup"><span data-stu-id="61ddc-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="61ddc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="61ddc-123">Request body</span></span>
<span data-ttu-id="61ddc-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="61ddc-124">In the request body, supply a JSON representation for the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>

<span data-ttu-id="61ddc-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="61ddc-125">The following table shows the properties that are required when you create the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span></span>

|<span data-ttu-id="61ddc-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61ddc-126">Property</span></span>|<span data-ttu-id="61ddc-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="61ddc-127">Type</span></span>|<span data-ttu-id="61ddc-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="61ddc-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="61ddc-129">id</span><span class="sxs-lookup"><span data-stu-id="61ddc-129">id</span></span>|<span data-ttu-id="61ddc-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="61ddc-130">String</span></span>|<span data-ttu-id="61ddc-131">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="61ddc-131">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="61ddc-132">displayName</span><span class="sxs-lookup"><span data-stu-id="61ddc-132">displayName</span></span>|<span data-ttu-id="61ddc-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="61ddc-133">String</span></span>|<span data-ttu-id="61ddc-134">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="61ddc-134">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="61ddc-135">description</span><span class="sxs-lookup"><span data-stu-id="61ddc-135">description</span></span>|<span data-ttu-id="61ddc-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="61ddc-136">String</span></span>|<span data-ttu-id="61ddc-137">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="61ddc-137">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="61ddc-138">prioridad</span><span class="sxs-lookup"><span data-stu-id="61ddc-138">priority</span></span>|<span data-ttu-id="61ddc-139">Int32</span><span class="sxs-lookup"><span data-stu-id="61ddc-139">Int32</span></span>|<span data-ttu-id="61ddc-140">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="61ddc-140">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="61ddc-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="61ddc-141">createdDateTime</span></span>|<span data-ttu-id="61ddc-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61ddc-142">DateTimeOffset</span></span>|<span data-ttu-id="61ddc-143">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="61ddc-143">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="61ddc-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="61ddc-144">lastModifiedDateTime</span></span>|<span data-ttu-id="61ddc-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61ddc-145">DateTimeOffset</span></span>|<span data-ttu-id="61ddc-146">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="61ddc-146">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="61ddc-147">version</span><span class="sxs-lookup"><span data-stu-id="61ddc-147">version</span></span>|<span data-ttu-id="61ddc-148">Int32</span><span class="sxs-lookup"><span data-stu-id="61ddc-148">Int32</span></span>|<span data-ttu-id="61ddc-149">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="61ddc-149">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="61ddc-150">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-150">iosRestriction</span></span>|[<span data-ttu-id="61ddc-151">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-151">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="61ddc-152">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="61ddc-152">Not yet documented</span></span>|
|<span data-ttu-id="61ddc-153">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-153">windowsRestriction</span></span>|[<span data-ttu-id="61ddc-154">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-154">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="61ddc-155">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="61ddc-155">Not yet documented</span></span>|
|<span data-ttu-id="61ddc-156">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-156">windowsMobileRestriction</span></span>|[<span data-ttu-id="61ddc-157">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-157">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="61ddc-158">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="61ddc-158">Not yet documented</span></span>|
|<span data-ttu-id="61ddc-159">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-159">androidRestriction</span></span>|[<span data-ttu-id="61ddc-160">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-160">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="61ddc-161">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="61ddc-161">Not yet documented</span></span>|
|<span data-ttu-id="61ddc-162">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-162">macOSRestriction</span></span>|[<span data-ttu-id="61ddc-163">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="61ddc-163">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="61ddc-164">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="61ddc-164">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="61ddc-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61ddc-165">Response</span></span>
<span data-ttu-id="61ddc-166">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61ddc-166">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="61ddc-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61ddc-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="61ddc-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="61ddc-168">Request</span></span>
<span data-ttu-id="61ddc-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="61ddc-169">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 1626

{
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "iosRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "windowsRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "windowsMobileRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "androidRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "macOSRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  }
}
```

### <a name="response"></a><span data-ttu-id="61ddc-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61ddc-170">Response</span></span>
<span data-ttu-id="61ddc-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="61ddc-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1822

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration",
  "id": "3acb2d75-2d75-3acb-752d-cb3a752dcb3a",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "iosRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "windowsRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "windowsMobileRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "androidRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  },
  "macOSRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value"
  }
}
```









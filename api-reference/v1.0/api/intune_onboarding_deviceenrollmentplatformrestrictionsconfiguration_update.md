# <a name="update-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="024b5-101">Actualizar deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="024b5-101">Update deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="024b5-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="024b5-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="024b5-103">Actualice las propiedades de un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="024b5-103">Update the properties of a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="024b5-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="024b5-104">Prerequisites</span></span>
<span data-ttu-id="024b5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="024b5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="024b5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="024b5-107">Permission type</span></span>|<span data-ttu-id="024b5-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="024b5-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="024b5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="024b5-109">Delegated (work or school account)</span></span>|<span data-ttu-id="024b5-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="024b5-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="024b5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="024b5-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="024b5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="024b5-112">Not supported.</span></span>|
|<span data-ttu-id="024b5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="024b5-113">Application</span></span>|<span data-ttu-id="024b5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="024b5-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="024b5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="024b5-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="024b5-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="024b5-116">Request headers</span></span>
|<span data-ttu-id="024b5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="024b5-117">Header</span></span>|<span data-ttu-id="024b5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="024b5-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="024b5-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="024b5-119">Authorization</span></span>|<span data-ttu-id="024b5-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="024b5-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="024b5-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="024b5-121">Accept</span></span>|<span data-ttu-id="024b5-122">application/json</span><span class="sxs-lookup"><span data-stu-id="024b5-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="024b5-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="024b5-123">Request body</span></span>
<span data-ttu-id="024b5-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="024b5-124">In the request body, supply a JSON representation for the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>

<span data-ttu-id="024b5-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="024b5-125">The following table shows the properties that are required when you create the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span></span>

|<span data-ttu-id="024b5-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="024b5-126">Property</span></span>|<span data-ttu-id="024b5-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="024b5-127">Type</span></span>|<span data-ttu-id="024b5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="024b5-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="024b5-129">id</span><span class="sxs-lookup"><span data-stu-id="024b5-129">id</span></span>|<span data-ttu-id="024b5-130">String</span><span class="sxs-lookup"><span data-stu-id="024b5-130">String</span></span>|<span data-ttu-id="024b5-131">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="024b5-131">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="024b5-132">displayName</span><span class="sxs-lookup"><span data-stu-id="024b5-132">displayName</span></span>|<span data-ttu-id="024b5-133">String</span><span class="sxs-lookup"><span data-stu-id="024b5-133">String</span></span>|<span data-ttu-id="024b5-134">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="024b5-134">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="024b5-135">description</span><span class="sxs-lookup"><span data-stu-id="024b5-135">description</span></span>|<span data-ttu-id="024b5-136">String</span><span class="sxs-lookup"><span data-stu-id="024b5-136">String</span></span>|<span data-ttu-id="024b5-137">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="024b5-137">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="024b5-138">prioridad</span><span class="sxs-lookup"><span data-stu-id="024b5-138">priority</span></span>|<span data-ttu-id="024b5-139">Int32</span><span class="sxs-lookup"><span data-stu-id="024b5-139">Int32</span></span>|<span data-ttu-id="024b5-140">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="024b5-140">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="024b5-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="024b5-141">createdDateTime</span></span>|<span data-ttu-id="024b5-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="024b5-142">DateTimeOffset</span></span>|<span data-ttu-id="024b5-143">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="024b5-143">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="024b5-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="024b5-144">lastModifiedDateTime</span></span>|<span data-ttu-id="024b5-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="024b5-145">DateTimeOffset</span></span>|<span data-ttu-id="024b5-146">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="024b5-146">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="024b5-147">version</span><span class="sxs-lookup"><span data-stu-id="024b5-147">version</span></span>|<span data-ttu-id="024b5-148">Int32</span><span class="sxs-lookup"><span data-stu-id="024b5-148">Int32</span></span>|<span data-ttu-id="024b5-149">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="024b5-149">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="024b5-150">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-150">iosRestriction</span></span>|[<span data-ttu-id="024b5-151">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-151">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="024b5-152">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="024b5-152">Not yet documented</span></span>|
|<span data-ttu-id="024b5-153">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-153">windowsRestriction</span></span>|[<span data-ttu-id="024b5-154">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-154">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="024b5-155">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="024b5-155">Not yet documented</span></span>|
|<span data-ttu-id="024b5-156">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-156">windowsMobileRestriction</span></span>|[<span data-ttu-id="024b5-157">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-157">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="024b5-158">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="024b5-158">Not yet documented</span></span>|
|<span data-ttu-id="024b5-159">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-159">androidRestriction</span></span>|[<span data-ttu-id="024b5-160">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-160">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="024b5-161">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="024b5-161">Not yet documented</span></span>|
|<span data-ttu-id="024b5-162">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-162">macOSRestriction</span></span>|[<span data-ttu-id="024b5-163">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="024b5-163">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="024b5-164">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="024b5-164">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="024b5-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="024b5-165">Response</span></span>
<span data-ttu-id="024b5-166">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="024b5-166">If successful, this method returns a `200 OK` response code and an updated [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="024b5-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="024b5-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="024b5-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="024b5-168">Request</span></span>
<span data-ttu-id="024b5-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="024b5-169">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
Content-type: application/json
Content-length: 1650

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
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

### <a name="response"></a><span data-ttu-id="024b5-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="024b5-170">Response</span></span>
<span data-ttu-id="024b5-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="024b5-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




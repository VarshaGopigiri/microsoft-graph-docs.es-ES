# <a name="create-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="4e5d6-101">Crear deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e5d6-101">Create deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="4e5d6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4e5d6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4e5d6-103">Cree un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4e5d6-103">Create a new [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4e5d6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4e5d6-104">Prerequisites</span></span>
<span data-ttu-id="4e5d6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4e5d6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4e5d6-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4e5d6-107">Permission type</span></span>|<span data-ttu-id="4e5d6-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4e5d6-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-109">Delegated (work or school account)</span></span>|<span data-ttu-id="4e5d6-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4e5d6-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="4e5d6-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4e5d6-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4e5d6-112">Not supported.</span></span>|
|<span data-ttu-id="4e5d6-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4e5d6-113">Application</span></span>|<span data-ttu-id="4e5d6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4e5d6-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4e5d6-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4e5d6-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="4e5d6-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4e5d6-116">Request headers</span></span>
|<span data-ttu-id="4e5d6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e5d6-117">Header</span></span>|<span data-ttu-id="4e5d6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4e5d6-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4e5d6-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="4e5d6-119">Authorization</span></span>|<span data-ttu-id="4e5d6-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4e5d6-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4e5d6-121">Accept</span><span class="sxs-lookup"><span data-stu-id="4e5d6-121">Accept</span></span>|<span data-ttu-id="4e5d6-122">application/json</span><span class="sxs-lookup"><span data-stu-id="4e5d6-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4e5d6-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4e5d6-123">Request body</span></span>
<span data-ttu-id="4e5d6-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceEnrollmentPlatformRestrictionsConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4e5d6-124">In the request body, supply a JSON representation for the deviceEnrollmentPlatformRestrictionsConfiguration object.</span></span>

<span data-ttu-id="4e5d6-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceEnrollmentPlatformRestrictionsConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4e5d6-125">The following table shows the properties that are required when you create the deviceEnrollmentPlatformRestrictionsConfiguration.</span></span>

|<span data-ttu-id="4e5d6-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4e5d6-126">Property</span></span>|<span data-ttu-id="4e5d6-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e5d6-127">Type</span></span>|<span data-ttu-id="4e5d6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e5d6-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4e5d6-129">id</span><span class="sxs-lookup"><span data-stu-id="4e5d6-129">id</span></span>|<span data-ttu-id="4e5d6-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e5d6-130">String</span></span>|<span data-ttu-id="4e5d6-131">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-131">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4e5d6-132">displayName</span><span class="sxs-lookup"><span data-stu-id="4e5d6-132">displayName</span></span>|<span data-ttu-id="4e5d6-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e5d6-133">String</span></span>|<span data-ttu-id="4e5d6-134">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-134">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4e5d6-135">description</span><span class="sxs-lookup"><span data-stu-id="4e5d6-135">description</span></span>|<span data-ttu-id="4e5d6-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e5d6-136">String</span></span>|<span data-ttu-id="4e5d6-137">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-137">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4e5d6-138">prioridad</span><span class="sxs-lookup"><span data-stu-id="4e5d6-138">priority</span></span>|<span data-ttu-id="4e5d6-139">Int32</span><span class="sxs-lookup"><span data-stu-id="4e5d6-139">Int32</span></span>|<span data-ttu-id="4e5d6-140">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-140">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4e5d6-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4e5d6-141">createdDateTime</span></span>|<span data-ttu-id="4e5d6-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4e5d6-142">DateTimeOffset</span></span>|<span data-ttu-id="4e5d6-143">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-143">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4e5d6-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4e5d6-144">lastModifiedDateTime</span></span>|<span data-ttu-id="4e5d6-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4e5d6-145">DateTimeOffset</span></span>|<span data-ttu-id="4e5d6-146">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-146">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4e5d6-147">version</span><span class="sxs-lookup"><span data-stu-id="4e5d6-147">version</span></span>|<span data-ttu-id="4e5d6-148">Int32</span><span class="sxs-lookup"><span data-stu-id="4e5d6-148">Int32</span></span>|<span data-ttu-id="4e5d6-149">Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4e5d6-149">Not yet documented Inherited from [deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md)</span></span>|
|<span data-ttu-id="4e5d6-150">iosRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-150">iosRestriction</span></span>|[<span data-ttu-id="4e5d6-151">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-151">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="4e5d6-152">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4e5d6-152">Not yet documented</span></span>|
|<span data-ttu-id="4e5d6-153">windowsRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-153">windowsRestriction</span></span>|[<span data-ttu-id="4e5d6-154">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-154">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="4e5d6-155">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4e5d6-155">Not yet documented</span></span>|
|<span data-ttu-id="4e5d6-156">windowsMobileRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-156">windowsMobileRestriction</span></span>|[<span data-ttu-id="4e5d6-157">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-157">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="4e5d6-158">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4e5d6-158">Not yet documented</span></span>|
|<span data-ttu-id="4e5d6-159">androidRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-159">androidRestriction</span></span>|[<span data-ttu-id="4e5d6-160">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-160">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="4e5d6-161">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4e5d6-161">Not yet documented</span></span>|
|<span data-ttu-id="4e5d6-162">macOSRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-162">macOSRestriction</span></span>|[<span data-ttu-id="4e5d6-163">deviceEnrollmentPlatformRestriction</span><span class="sxs-lookup"><span data-stu-id="4e5d6-163">deviceEnrollmentPlatformRestriction</span></span>](../resources/intune_onboarding_deviceenrollmentplatformrestriction.md)|<span data-ttu-id="4e5d6-164">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4e5d6-164">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="4e5d6-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e5d6-165">Response</span></span>
<span data-ttu-id="4e5d6-166">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4e5d6-166">If successful, this method returns a `201 Created` response code and a [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4e5d6-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e5d6-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="4e5d6-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4e5d6-168">Request</span></span>
<span data-ttu-id="4e5d6-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4e5d6-169">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations
Content-type: application/json
Content-length: 1714

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration",
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

### <a name="response"></a><span data-ttu-id="4e5d6-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e5d6-170">Response</span></span>
<span data-ttu-id="4e5d6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4e5d6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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









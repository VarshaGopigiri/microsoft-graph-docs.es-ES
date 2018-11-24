# <a name="create-windowsdefenderadvancedthreatprotectionconfiguration"></a><span data-ttu-id="bc4b9-101">Crear windowsDefenderAdvancedThreatProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc4b9-101">Create windowsDefenderAdvancedThreatProtectionConfiguration</span></span>

> <span data-ttu-id="bc4b9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bc4b9-103">Cree un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune_deviceconfig_windowsdefenderadvancedthreatprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="bc4b9-103">Create a new [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune_deviceconfig_windowsdefenderadvancedthreatprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bc4b9-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bc4b9-104">Prerequisites</span></span>
<span data-ttu-id="bc4b9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bc4b9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bc4b9-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc4b9-107">Permission type</span></span>|<span data-ttu-id="bc4b9-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bc4b9-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-109">Delegated (work or school account)</span></span>|<span data-ttu-id="bc4b9-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bc4b9-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="bc4b9-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bc4b9-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-112">Not supported.</span></span>|
|<span data-ttu-id="bc4b9-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc4b9-113">Application</span></span>|<span data-ttu-id="bc4b9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bc4b9-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc4b9-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="bc4b9-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc4b9-116">Request headers</span></span>
|<span data-ttu-id="bc4b9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc4b9-117">Header</span></span>|<span data-ttu-id="bc4b9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bc4b9-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bc4b9-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="bc4b9-119">Authorization</span></span>|<span data-ttu-id="bc4b9-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bc4b9-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bc4b9-121">Accept</span></span>|<span data-ttu-id="bc4b9-122">application/json</span><span class="sxs-lookup"><span data-stu-id="bc4b9-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bc4b9-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc4b9-123">Request body</span></span>
<span data-ttu-id="bc4b9-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsDefenderAdvancedThreatProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-124">In the request body, supply a JSON representation for the windowsDefenderAdvancedThreatProtectionConfiguration object.</span></span>

<span data-ttu-id="bc4b9-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsDefenderAdvancedThreatProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-125">The following table shows the properties that are required when you create the windowsDefenderAdvancedThreatProtectionConfiguration.</span></span>

|<span data-ttu-id="bc4b9-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bc4b9-126">Property</span></span>|<span data-ttu-id="bc4b9-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc4b9-127">Type</span></span>|<span data-ttu-id="bc4b9-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc4b9-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bc4b9-129">id</span><span class="sxs-lookup"><span data-stu-id="bc4b9-129">id</span></span>|<span data-ttu-id="bc4b9-130">String</span><span class="sxs-lookup"><span data-stu-id="bc4b9-130">String</span></span>|<span data-ttu-id="bc4b9-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-131">Key of the entity.</span></span> <span data-ttu-id="bc4b9-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc4b9-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bc4b9-133">lastModifiedDateTime</span></span>|<span data-ttu-id="bc4b9-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bc4b9-134">DateTimeOffset</span></span>|<span data-ttu-id="bc4b9-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-135">DateTime the object was last modified.</span></span> <span data-ttu-id="bc4b9-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc4b9-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="bc4b9-137">createdDateTime</span></span>|<span data-ttu-id="bc4b9-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bc4b9-138">DateTimeOffset</span></span>|<span data-ttu-id="bc4b9-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-139">DateTime the object was created.</span></span> <span data-ttu-id="bc4b9-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc4b9-141">description</span><span class="sxs-lookup"><span data-stu-id="bc4b9-141">description</span></span>|<span data-ttu-id="bc4b9-142">String</span><span class="sxs-lookup"><span data-stu-id="bc4b9-142">String</span></span>|<span data-ttu-id="bc4b9-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="bc4b9-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc4b9-145">displayName</span><span class="sxs-lookup"><span data-stu-id="bc4b9-145">displayName</span></span>|<span data-ttu-id="bc4b9-146">String</span><span class="sxs-lookup"><span data-stu-id="bc4b9-146">String</span></span>|<span data-ttu-id="bc4b9-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="bc4b9-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc4b9-149">version</span><span class="sxs-lookup"><span data-stu-id="bc4b9-149">version</span></span>|<span data-ttu-id="bc4b9-150">Int32</span><span class="sxs-lookup"><span data-stu-id="bc4b9-150">Int32</span></span>|<span data-ttu-id="bc4b9-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-151">Version of the device configuration.</span></span> <span data-ttu-id="bc4b9-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc4b9-153">allowSampleSharing</span><span class="sxs-lookup"><span data-stu-id="bc4b9-153">allowSampleSharing</span></span>|<span data-ttu-id="bc4b9-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="bc4b9-154">Boolean</span></span>|<span data-ttu-id="bc4b9-155">Regla "Permitir el uso compartido de muestras" de Windows Defender AdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="bc4b9-155">Windows Defender AdvancedThreatProtection "Allow Sample Sharing" Rule</span></span>|
|<span data-ttu-id="bc4b9-156">enableExpeditedTelemetryReporting</span><span class="sxs-lookup"><span data-stu-id="bc4b9-156">enableExpeditedTelemetryReporting</span></span>|<span data-ttu-id="bc4b9-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="bc4b9-157">Boolean</span></span>|<span data-ttu-id="bc4b9-158">Acelere la frecuencia de informes de telemetría de Protección contra amenazas avanzada de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-158">Expedite Windows Defender Advanced Threat Protection telemetry reporting frequency.</span></span>|



## <a name="response"></a><span data-ttu-id="bc4b9-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc4b9-159">Response</span></span>
<span data-ttu-id="bc4b9-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune_deviceconfig_windowsdefenderadvancedthreatprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-160">If successful, this method returns a `201 Created` response code and a [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune_deviceconfig_windowsdefenderadvancedthreatprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc4b9-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc4b9-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="bc4b9-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc4b9-162">Request</span></span>
<span data-ttu-id="bc4b9-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 267

{
  "@odata.type": "#microsoft.graph.windowsDefenderAdvancedThreatProtectionConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "allowSampleSharing": true,
  "enableExpeditedTelemetryReporting": true
}
```

### <a name="response"></a><span data-ttu-id="bc4b9-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc4b9-164">Response</span></span>
<span data-ttu-id="bc4b9-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 439

{
  "@odata.type": "#microsoft.graph.windowsDefenderAdvancedThreatProtectionConfiguration",
  "id": "294373aa-73aa-2943-aa73-4329aa734329",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "allowSampleSharing": true,
  "enableExpeditedTelemetryReporting": true
}
```




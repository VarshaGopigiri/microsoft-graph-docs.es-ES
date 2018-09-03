# <a name="create-editionupgradeconfiguration"></a><span data-ttu-id="2bfb3-101">Crear editionUpgradeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bfb3-101">Create editionUpgradeConfiguration</span></span>

> <span data-ttu-id="2bfb3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2bfb3-103">Cree un objeto [editionUpgradeConfiguration](../resources/intune_deviceconfig_editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2bfb3-103">Create a new [editionUpgradeConfiguration](../resources/intune_deviceconfig_editionupgradeconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2bfb3-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2bfb3-104">Prerequisites</span></span>
<span data-ttu-id="2bfb3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2bfb3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2bfb3-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2bfb3-107">Permission type</span></span>|<span data-ttu-id="2bfb3-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2bfb3-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2bfb3-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2bfb3-109">Delegated (work or school account)</span></span>|<span data-ttu-id="2bfb3-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2bfb3-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2bfb3-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2bfb3-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2bfb3-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-112">Not supported.</span></span>|
|<span data-ttu-id="2bfb3-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2bfb3-113">Application</span></span>|<span data-ttu-id="2bfb3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2bfb3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2bfb3-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="2bfb3-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2bfb3-116">Request headers</span></span>
|<span data-ttu-id="2bfb3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bfb3-117">Header</span></span>|<span data-ttu-id="2bfb3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2bfb3-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2bfb3-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="2bfb3-119">Authorization</span></span>|<span data-ttu-id="2bfb3-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2bfb3-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2bfb3-121">Accept</span></span>|<span data-ttu-id="2bfb3-122">application/json</span><span class="sxs-lookup"><span data-stu-id="2bfb3-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2bfb3-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2bfb3-123">Request body</span></span>
<span data-ttu-id="2bfb3-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto editionUpgradeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-124">In the request body, supply a JSON representation for the editionUpgradeConfiguration object.</span></span>

<span data-ttu-id="2bfb3-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto editionUpgradeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-125">The following table shows the properties that are required when you create the editionUpgradeConfiguration.</span></span>

|<span data-ttu-id="2bfb3-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2bfb3-126">Property</span></span>|<span data-ttu-id="2bfb3-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bfb3-127">Type</span></span>|<span data-ttu-id="2bfb3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bfb3-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2bfb3-129">id</span><span class="sxs-lookup"><span data-stu-id="2bfb3-129">id</span></span>|<span data-ttu-id="2bfb3-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="2bfb3-130">String</span></span>|<span data-ttu-id="2bfb3-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-131">Key of the entity.</span></span> <span data-ttu-id="2bfb3-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2bfb3-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2bfb3-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2bfb3-133">lastModifiedDateTime</span></span>|<span data-ttu-id="2bfb3-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2bfb3-134">DateTimeOffset</span></span>|<span data-ttu-id="2bfb3-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-135">DateTime the object was last modified.</span></span> <span data-ttu-id="2bfb3-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2bfb3-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2bfb3-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2bfb3-137">createdDateTime</span></span>|<span data-ttu-id="2bfb3-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2bfb3-138">DateTimeOffset</span></span>|<span data-ttu-id="2bfb3-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-139">DateTime the object was created.</span></span> <span data-ttu-id="2bfb3-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2bfb3-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2bfb3-141">descripción</span><span class="sxs-lookup"><span data-stu-id="2bfb3-141">description</span></span>|<span data-ttu-id="2bfb3-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="2bfb3-142">String</span></span>|<span data-ttu-id="2bfb3-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="2bfb3-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2bfb3-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2bfb3-145">displayName</span><span class="sxs-lookup"><span data-stu-id="2bfb3-145">displayName</span></span>|<span data-ttu-id="2bfb3-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="2bfb3-146">String</span></span>|<span data-ttu-id="2bfb3-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="2bfb3-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2bfb3-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2bfb3-149">version</span><span class="sxs-lookup"><span data-stu-id="2bfb3-149">version</span></span>|<span data-ttu-id="2bfb3-150">Int32</span><span class="sxs-lookup"><span data-stu-id="2bfb3-150">Int32</span></span>|<span data-ttu-id="2bfb3-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-151">Version of the device configuration.</span></span> <span data-ttu-id="2bfb3-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2bfb3-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2bfb3-153">licenseType</span><span class="sxs-lookup"><span data-stu-id="2bfb3-153">licenseType</span></span>|[<span data-ttu-id="2bfb3-154">editionUpgradeLicenseType</span><span class="sxs-lookup"><span data-stu-id="2bfb3-154">editionUpgradeLicenseType</span></span>](../resources/intune_deviceconfig_editionupgradelicensetype.md)|<span data-ttu-id="2bfb3-155">Tipo de licencia de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-155">Edition Upgrade License Type.</span></span> <span data-ttu-id="2bfb3-156">Los valores posibles son: `productKey` y `licenseFile`.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-156">The possible values are:</span></span>|
|<span data-ttu-id="2bfb3-157">targetEdition</span><span class="sxs-lookup"><span data-stu-id="2bfb3-157">targetEdition</span></span>|[<span data-ttu-id="2bfb3-158">windows10EditionType</span><span class="sxs-lookup"><span data-stu-id="2bfb3-158">windows10EditionType</span></span>](../resources/intune_deviceconfig_windows10editiontype.md)|<span data-ttu-id="2bfb3-159">Edición de destino de la actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-159">Edition Upgrade Target Edition.</span></span> <span data-ttu-id="2bfb3-160">Los valores posibles son: `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation` y `windows10ProfessionalWorkstationN`.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-160">The possible values are `windows10Enterprise`, `windows10EnterpriseN`, `windows10Education`, `windows10EducationN`, `windows10MobileEnterprise`, `windows10HolographicEnterprise`, `windows10Professional`, `windows10ProfessionalN`, `windows10ProfessionalEducation`, `windows10ProfessionalEducationN`, `windows10ProfessionalWorkstation`, or `windows10ProfessionalWorkstationN`.</span></span>|
|<span data-ttu-id="2bfb3-161">license</span><span class="sxs-lookup"><span data-stu-id="2bfb3-161">license</span></span>|<span data-ttu-id="2bfb3-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="2bfb3-162">String</span></span>|<span data-ttu-id="2bfb3-163">Contenido de archivo de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-163">Edition Upgrade License File Content.</span></span>|
|<span data-ttu-id="2bfb3-164">productKey</span><span class="sxs-lookup"><span data-stu-id="2bfb3-164">productKey</span></span>|<span data-ttu-id="2bfb3-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="2bfb3-165">String</span></span>|<span data-ttu-id="2bfb3-166">Clave de producto de actualización de edición.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-166">Edition Upgrade Product Key.</span></span>|



## <a name="response"></a><span data-ttu-id="2bfb3-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bfb3-167">Response</span></span>
<span data-ttu-id="2bfb3-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [editionUpgradeConfiguration](../resources/intune_deviceconfig_editionupgradeconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-168">If successful, this method returns a `201 Created` response code and a [editionUpgradeConfiguration](../resources/intune_deviceconfig_editionupgradeconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2bfb3-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2bfb3-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="2bfb3-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2bfb3-170">Request</span></span>
<span data-ttu-id="2bfb3-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-171">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 375

{
  "@odata.type": "#microsoft.graph.editionUpgradeConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "licenseType": "licenseFile",
  "targetEdition": "windows10EnterpriseN",
  "license": "License value",
  "productKey": "Product Key value"
}
```

### <a name="response"></a><span data-ttu-id="2bfb3-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bfb3-172">Response</span></span>
<span data-ttu-id="2bfb3-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 483

{
  "@odata.type": "#microsoft.graph.editionUpgradeConfiguration",
  "id": "f39fc471-c471-f39f-71c4-9ff371c49ff3",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "licenseType": "licenseFile",
  "targetEdition": "windows10EnterpriseN",
  "license": "License value",
  "productKey": "Product Key value"
}
```




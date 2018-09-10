# <a name="create-windows10secureassessmentconfiguration"></a><span data-ttu-id="93df9-101">Crear windows10SecureAssessmentConfiguration</span><span class="sxs-lookup"><span data-stu-id="93df9-101">Create windows10SecureAssessmentConfiguration</span></span>

> <span data-ttu-id="93df9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="93df9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="93df9-103">Crear un objeto [windows10SecureAssessmentConfiguration](../resources/intune_deviceconfig_windows10secureassessmentconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="93df9-103">Create a new [windows10SecureAssessmentConfiguration](../resources/intune_deviceconfig_windows10secureassessmentconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="93df9-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="93df9-104">Prerequisites</span></span>
<span data-ttu-id="93df9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="93df9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="93df9-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="93df9-107">Permission type</span></span>|<span data-ttu-id="93df9-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="93df9-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="93df9-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="93df9-109">Delegated (work or school account)</span></span>|<span data-ttu-id="93df9-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="93df9-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="93df9-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="93df9-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="93df9-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="93df9-112">Not supported.</span></span>|
|<span data-ttu-id="93df9-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="93df9-113">Application</span></span>|<span data-ttu-id="93df9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="93df9-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="93df9-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93df9-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="93df9-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="93df9-116">Request headers</span></span>
|<span data-ttu-id="93df9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93df9-117">Header</span></span>|<span data-ttu-id="93df9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="93df9-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="93df9-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="93df9-119">Authorization</span></span>|<span data-ttu-id="93df9-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="93df9-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="93df9-121">Accept</span><span class="sxs-lookup"><span data-stu-id="93df9-121">Accept</span></span>|<span data-ttu-id="93df9-122">application/json</span><span class="sxs-lookup"><span data-stu-id="93df9-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="93df9-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="93df9-123">Request body</span></span>
<span data-ttu-id="93df9-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10SecureAssessmentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="93df9-124">In the request body, supply a JSON representation for the windows10SecureAssessmentConfiguration object.</span></span>

<span data-ttu-id="93df9-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10SecureAssessmentConfiguration.</span><span class="sxs-lookup"><span data-stu-id="93df9-125">The following table shows the properties that are required when you create the windows10SecureAssessmentConfiguration.</span></span>

|<span data-ttu-id="93df9-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="93df9-126">Property</span></span>|<span data-ttu-id="93df9-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="93df9-127">Type</span></span>|<span data-ttu-id="93df9-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="93df9-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="93df9-129">id</span><span class="sxs-lookup"><span data-stu-id="93df9-129">id</span></span>|<span data-ttu-id="93df9-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="93df9-130">String</span></span>|<span data-ttu-id="93df9-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="93df9-131">Key of the entity.</span></span> <span data-ttu-id="93df9-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="93df9-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="93df9-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="93df9-133">lastModifiedDateTime</span></span>|<span data-ttu-id="93df9-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="93df9-134">DateTimeOffset</span></span>|<span data-ttu-id="93df9-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="93df9-135">DateTime the object was last modified.</span></span> <span data-ttu-id="93df9-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="93df9-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="93df9-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="93df9-137">createdDateTime</span></span>|<span data-ttu-id="93df9-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="93df9-138">DateTimeOffset</span></span>|<span data-ttu-id="93df9-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="93df9-139">DateTime the object was created.</span></span> <span data-ttu-id="93df9-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="93df9-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="93df9-141">description</span><span class="sxs-lookup"><span data-stu-id="93df9-141">description</span></span>|<span data-ttu-id="93df9-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="93df9-142">String</span></span>|<span data-ttu-id="93df9-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93df9-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="93df9-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="93df9-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="93df9-145">displayName</span><span class="sxs-lookup"><span data-stu-id="93df9-145">displayName</span></span>|<span data-ttu-id="93df9-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="93df9-146">String</span></span>|<span data-ttu-id="93df9-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93df9-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="93df9-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="93df9-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="93df9-149">version</span><span class="sxs-lookup"><span data-stu-id="93df9-149">version</span></span>|<span data-ttu-id="93df9-150">Int32</span><span class="sxs-lookup"><span data-stu-id="93df9-150">Int32</span></span>|<span data-ttu-id="93df9-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93df9-151">Version of the device configuration.</span></span> <span data-ttu-id="93df9-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="93df9-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="93df9-153">launchUri</span><span class="sxs-lookup"><span data-stu-id="93df9-153">launchUri</span></span>|<span data-ttu-id="93df9-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="93df9-154">String</span></span>|<span data-ttu-id="93df9-155">Vínculo de dirección URL a una evaluación que se carga automáticamente al iniciar el explorador de evaluaciones seguras.</span><span class="sxs-lookup"><span data-stu-id="93df9-155">Url link to an assessment that's automatically loaded when the secure assessment browser is launched.</span></span> <span data-ttu-id="93df9-156">Tiene que ser una dirección URL válida (http\[s\]://msdn.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="93df9-156">It has to be a valid Url (http\[s\]://msdn.microsoft.com/).</span></span>|
|<span data-ttu-id="93df9-157">configurationAccount</span><span class="sxs-lookup"><span data-stu-id="93df9-157">configurationAccount</span></span>|<span data-ttu-id="93df9-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="93df9-158">String</span></span>|<span data-ttu-id="93df9-159">Cuenta usada al configurar el dispositivo Windows para realizar la prueba.</span><span class="sxs-lookup"><span data-stu-id="93df9-159">The account used to configure the Windows device for taking the test.</span></span> <span data-ttu-id="93df9-160">El usuario puede ser una cuenta de dominio (dominio\usuario), una cuenta de AAD (nombredeusuario@espacioempresarial.com) o una cuenta local (nombredeusuario).</span><span class="sxs-lookup"><span data-stu-id="93df9-160">The user can be a domain account (domain\user), an AAD account (username@tenant.com) or a local account (username).</span></span>|
|<span data-ttu-id="93df9-161">allowPrinting</span><span class="sxs-lookup"><span data-stu-id="93df9-161">allowPrinting</span></span>|<span data-ttu-id="93df9-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="93df9-162">Boolean</span></span>|<span data-ttu-id="93df9-163">Indica si se va a permitir que la aplicación imprima durante la prueba.</span><span class="sxs-lookup"><span data-stu-id="93df9-163">Indicates whether or not to allow the app from printing during the test.</span></span>|
|<span data-ttu-id="93df9-164">allowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="93df9-164">allowScreenCapture</span></span>|<span data-ttu-id="93df9-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="93df9-165">Boolean</span></span>|<span data-ttu-id="93df9-166">Indica si se va a permitir la funcionalidad de captura de pantalla durante una prueba.</span><span class="sxs-lookup"><span data-stu-id="93df9-166">Indicates whether or not to allow screen capture capability during a test.</span></span>|
|<span data-ttu-id="93df9-167">allowTextSuggestion</span><span class="sxs-lookup"><span data-stu-id="93df9-167">allowTextSuggestion</span></span>|<span data-ttu-id="93df9-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="93df9-168">Boolean</span></span>|<span data-ttu-id="93df9-169">Indica si se van a permitir las sugerencias de texto durante la prueba.</span><span class="sxs-lookup"><span data-stu-id="93df9-169">Indicates whether or not to allow text suggestions during the test.</span></span>|



## <a name="response"></a><span data-ttu-id="93df9-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93df9-170">Response</span></span>
<span data-ttu-id="93df9-171">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10SecureAssessmentConfiguration](../resources/intune_deviceconfig_windows10secureassessmentconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93df9-171">If successful, this method returns a `201 Created` response code and a [windows10SecureAssessmentConfiguration](../resources/intune_deviceconfig_windows10secureassessmentconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="93df9-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="93df9-172">Example</span></span>
### <a name="request"></a><span data-ttu-id="93df9-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="93df9-173">Request</span></span>
<span data-ttu-id="93df9-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="93df9-174">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 423

{
  "@odata.type": "#microsoft.graph.windows10SecureAssessmentConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "launchUri": "Launch Uri value",
  "configurationAccount": "Configuration Account value",
  "allowPrinting": true,
  "allowScreenCapture": true,
  "allowTextSuggestion": true
}
```

### <a name="response"></a><span data-ttu-id="93df9-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93df9-175">Response</span></span>
<span data-ttu-id="93df9-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="93df9-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 531

{
  "@odata.type": "#microsoft.graph.windows10SecureAssessmentConfiguration",
  "id": "f60d71be-71be-f60d-be71-0df6be710df6",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "launchUri": "Launch Uri value",
  "configurationAccount": "Configuration Account value",
  "allowPrinting": true,
  "allowScreenCapture": true,
  "allowTextSuggestion": true
}
```









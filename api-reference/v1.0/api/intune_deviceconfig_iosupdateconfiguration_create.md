# <a name="create-iosupdateconfiguration"></a><span data-ttu-id="d0938-101">Crear iosUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0938-101">Create iosUpdateConfiguration</span></span>

> <span data-ttu-id="d0938-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d0938-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d0938-103">Cree un objeto [iosUpdateConfiguration](../resources/intune_deviceconfig_iosupdateconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d0938-103">Create a new [plannerBucket](../resources/intune_deviceconfig_iosupdateconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d0938-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d0938-104">Prerequisites</span></span>
<span data-ttu-id="d0938-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d0938-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d0938-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0938-107">Permission type</span></span>|<span data-ttu-id="d0938-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0938-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d0938-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0938-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d0938-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0938-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d0938-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0938-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d0938-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0938-112">Not supported.</span></span>|
|<span data-ttu-id="d0938-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0938-113">Application</span></span>|<span data-ttu-id="d0938-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0938-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d0938-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0938-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="d0938-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0938-116">Request headers</span></span>
|<span data-ttu-id="d0938-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0938-117">Header</span></span>|<span data-ttu-id="d0938-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d0938-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d0938-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d0938-119">Authorization</span></span>|<span data-ttu-id="d0938-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d0938-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="d0938-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d0938-121">Accept</span></span>|<span data-ttu-id="d0938-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d0938-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d0938-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0938-123">Request body</span></span>
<span data-ttu-id="d0938-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d0938-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="d0938-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d0938-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="d0938-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0938-126">Property</span></span>|<span data-ttu-id="d0938-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0938-127">Type</span></span>|<span data-ttu-id="d0938-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0938-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d0938-129">id</span><span class="sxs-lookup"><span data-stu-id="d0938-129">id</span></span>|<span data-ttu-id="d0938-130">String</span><span class="sxs-lookup"><span data-stu-id="d0938-130">String</span></span>|<span data-ttu-id="d0938-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d0938-131">Key of the setting.</span></span> <span data-ttu-id="d0938-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d0938-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d0938-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d0938-133">lastModifiedDateTime</span></span>|<span data-ttu-id="d0938-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0938-134">DateTimeOffset</span></span>|<span data-ttu-id="d0938-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d0938-135">Indicates the date the object was last modified.</span></span> <span data-ttu-id="d0938-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d0938-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d0938-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d0938-137">createdDateTime</span></span>|<span data-ttu-id="d0938-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0938-138">DateTimeOffset</span></span>|<span data-ttu-id="d0938-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d0938-139">DateTime the object was created.</span></span> <span data-ttu-id="d0938-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d0938-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d0938-141">description</span><span class="sxs-lookup"><span data-stu-id="d0938-141">description</span></span>|<span data-ttu-id="d0938-142">String</span><span class="sxs-lookup"><span data-stu-id="d0938-142">String</span></span>|<span data-ttu-id="d0938-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0938-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d0938-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d0938-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d0938-145">displayName</span><span class="sxs-lookup"><span data-stu-id="d0938-145">displayName</span></span>|<span data-ttu-id="d0938-146">String</span><span class="sxs-lookup"><span data-stu-id="d0938-146">String</span></span>|<span data-ttu-id="d0938-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0938-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d0938-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d0938-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d0938-149">version</span><span class="sxs-lookup"><span data-stu-id="d0938-149">version</span></span>|<span data-ttu-id="d0938-150">Int32</span><span class="sxs-lookup"><span data-stu-id="d0938-150">Int32</span></span>|<span data-ttu-id="d0938-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0938-151">Version of the device configuration.</span></span> <span data-ttu-id="d0938-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d0938-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d0938-153">activeHoursStart</span><span class="sxs-lookup"><span data-stu-id="d0938-153">activeHoursStart</span></span>|<span data-ttu-id="d0938-154">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="d0938-154">TimeOfDay</span></span>|<span data-ttu-id="d0938-155">Inicio de horas activas (las horas activas son el intervalo de tiempo en que no se deberían instalar actualizaciones)</span><span class="sxs-lookup"><span data-stu-id="d0938-155">Active Hours Start (active hours mean the time window when updates install should not happen)</span></span>|
|<span data-ttu-id="d0938-156">activeHoursEnd</span><span class="sxs-lookup"><span data-stu-id="d0938-156">activeHoursEnd</span></span>|<span data-ttu-id="d0938-157">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="d0938-157">TimeOfDay</span></span>|<span data-ttu-id="d0938-158">Fin de horas activas (las horas activas son el intervalo de tiempo en que no se deberían instalar actualizaciones)</span><span class="sxs-lookup"><span data-stu-id="d0938-158">Active Hours End (active hours mean the time window when updates install should not happen)</span></span>|
|<span data-ttu-id="d0938-159">scheduledInstallDays</span><span class="sxs-lookup"><span data-stu-id="d0938-159">scheduledInstallDays</span></span>|<span data-ttu-id="d0938-160">Colección string</span><span class="sxs-lookup"><span data-stu-id="d0938-160">String collection</span></span>|<span data-ttu-id="d0938-161">Días de la semana para los que se configuran las horas activas.</span><span class="sxs-lookup"><span data-stu-id="d0938-161">Days in week for which active hours are configured.</span></span> <span data-ttu-id="d0938-162">Esta colección puede contener un máximo de 7 elementos.</span><span class="sxs-lookup"><span data-stu-id="d0938-162">This collection can contain a maximum of 7 elements.</span></span> <span data-ttu-id="d0938-163">Valores posibles: `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday` y `sunday`.</span><span class="sxs-lookup"><span data-stu-id="d0938-163">Possible values are: `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="d0938-164">utcTimeOffsetInMinutes</span><span class="sxs-lookup"><span data-stu-id="d0938-164">utcTimeOffsetInMinutes</span></span>|<span data-ttu-id="d0938-165">Int32</span><span class="sxs-lookup"><span data-stu-id="d0938-165">Int32</span></span>|<span data-ttu-id="d0938-166">Diferencia horaria UTC indicada en minutos</span><span class="sxs-lookup"><span data-stu-id="d0938-166">UTC Time Offset indicated in minutes</span></span>|



## <a name="response"></a><span data-ttu-id="d0938-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0938-167">Response</span></span>
<span data-ttu-id="d0938-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosUpdateConfiguration](../resources/intune_deviceconfig_iosupdateconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0938-168">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_iosupdateconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d0938-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0938-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="d0938-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0938-170">Request</span></span>
<span data-ttu-id="d0938-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0938-171">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 389

{
  "@odata.type": "#microsoft.graph.iosUpdateConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "activeHoursStart": "12:00:05.5020000",
  "activeHoursEnd": "11:59:00.8990000",
  "scheduledInstallDays": [
    "monday"
  ],
  "utcTimeOffsetInMinutes": 6
}
```

### <a name="response"></a><span data-ttu-id="d0938-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0938-172">Response</span></span>
<span data-ttu-id="d0938-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0938-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 497

{
  "@odata.type": "#microsoft.graph.iosUpdateConfiguration",
  "id": "321aef09-ef09-321a-09ef-1a3209ef1a32",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "activeHoursStart": "12:00:05.5020000",
  "activeHoursEnd": "11:59:00.8990000",
  "scheduledInstallDays": [
    "monday"
  ],
  "utcTimeOffsetInMinutes": 6
}
```




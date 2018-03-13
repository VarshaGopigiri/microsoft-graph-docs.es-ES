# <a name="create-iosmanagedappregistration"></a><span data-ttu-id="8efc2-101">Crear iosManagedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="8efc2-101">Create iosManagedAppRegistration</span></span>

> <span data-ttu-id="8efc2-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8efc2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8efc2-103">Crear un objeto [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="8efc2-103">Create a new [plannerBucket](../resources/intune_mam_iosmanagedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8efc2-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8efc2-104">Prerequisites</span></span>
<span data-ttu-id="8efc2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8efc2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8efc2-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8efc2-107">Permission type</span></span>|<span data-ttu-id="8efc2-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8efc2-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8efc2-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8efc2-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8efc2-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8efc2-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8efc2-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8efc2-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8efc2-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8efc2-112">Not supported.</span></span>|
|<span data-ttu-id="8efc2-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8efc2-113">Application</span></span>|<span data-ttu-id="8efc2-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="8efc2-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8efc2-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8efc2-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="8efc2-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8efc2-116">Request headers</span></span>
|<span data-ttu-id="8efc2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8efc2-117">Header</span></span>|<span data-ttu-id="8efc2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8efc2-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8efc2-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="8efc2-119">Authorization</span></span>|<span data-ttu-id="8efc2-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8efc2-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="8efc2-121">Accept</span><span class="sxs-lookup"><span data-stu-id="8efc2-121">Accept</span></span>|<span data-ttu-id="8efc2-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8efc2-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8efc2-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8efc2-123">Request body</span></span>
<span data-ttu-id="8efc2-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="8efc2-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="8efc2-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="8efc2-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="8efc2-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8efc2-126">Property</span></span>|<span data-ttu-id="8efc2-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="8efc2-127">Type</span></span>|<span data-ttu-id="8efc2-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8efc2-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8efc2-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8efc2-129">createdDateTime</span></span>|<span data-ttu-id="8efc2-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8efc2-130">DateTimeOffset</span></span>|<span data-ttu-id="8efc2-131">Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8efc2-131">Date and time of creation Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-132">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="8efc2-132">lastSyncDateTime</span></span>|<span data-ttu-id="8efc2-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8efc2-133">DateTimeOffset</span></span>|<span data-ttu-id="8efc2-134">Fecha y hora de la última sincronización de la aplicación con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="8efc2-134">Date and time of last the app synced with management service.</span></span> <span data-ttu-id="8efc2-135">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="8efc2-135">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-136">applicationVersion</span><span class="sxs-lookup"><span data-stu-id="8efc2-136">applicationVersion</span></span>|<span data-ttu-id="8efc2-137">String</span><span class="sxs-lookup"><span data-stu-id="8efc2-137">String</span></span>|<span data-ttu-id="8efc2-138">Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8efc2-138">App version Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-139">managementSdkVersion</span><span class="sxs-lookup"><span data-stu-id="8efc2-139">managementSdkVersion</span></span>|<span data-ttu-id="8efc2-140">String</span><span class="sxs-lookup"><span data-stu-id="8efc2-140">String</span></span>|<span data-ttu-id="8efc2-141">Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8efc2-141">App management SDK version Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-142">platformVersion</span><span class="sxs-lookup"><span data-stu-id="8efc2-142">platformVersion</span></span>|<span data-ttu-id="8efc2-143">String</span><span class="sxs-lookup"><span data-stu-id="8efc2-143">String</span></span>|<span data-ttu-id="8efc2-144">Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8efc2-144">Operating System version Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-145">deviceType</span><span class="sxs-lookup"><span data-stu-id="8efc2-145">deviceType</span></span>|<span data-ttu-id="8efc2-146">String</span><span class="sxs-lookup"><span data-stu-id="8efc2-146">String</span></span>|<span data-ttu-id="8efc2-147">Tipo de dispositivo host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8efc2-147">Host device type Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-148">deviceTag</span><span class="sxs-lookup"><span data-stu-id="8efc2-148">deviceTag</span></span>|<span data-ttu-id="8efc2-149">String</span><span class="sxs-lookup"><span data-stu-id="8efc2-149">String</span></span>|<span data-ttu-id="8efc2-150">Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8efc2-150">App management SDK generated tag, which helps relate apps hosted on the same device.</span></span> <span data-ttu-id="8efc2-151">No garantiza que las aplicaciones se relacionen en todas las condiciones.</span><span class="sxs-lookup"><span data-stu-id="8efc2-151">Not guaranteed to relate apps in all conditions.</span></span> <span data-ttu-id="8efc2-152">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="8efc2-152">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-153">deviceName</span><span class="sxs-lookup"><span data-stu-id="8efc2-153">deviceName</span></span>|<span data-ttu-id="8efc2-154">String</span><span class="sxs-lookup"><span data-stu-id="8efc2-154">String</span></span>|<span data-ttu-id="8efc2-155">Nombre del dispositivo host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8efc2-155">Host device name Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-156">flaggedReasons</span><span class="sxs-lookup"><span data-stu-id="8efc2-156">flaggedReasons</span></span>|<span data-ttu-id="8efc2-157">Colección String</span><span class="sxs-lookup"><span data-stu-id="8efc2-157">String collection</span></span>|<span data-ttu-id="8efc2-158">Cero o más razones por las que se ha marcado el registro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8efc2-158">Zero or more reasons an app registration is flagged.</span></span> <span data-ttu-id="8efc2-159">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="8efc2-159">E.g.</span></span> <span data-ttu-id="8efc2-160">Aplicación que se ejecuta en un dispositivo con rooting. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md). Los valores posibles son: `none` y `rootedDevice`.</span><span class="sxs-lookup"><span data-stu-id="8efc2-160">app running on rooted device Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md) Possible values are: `none`, `rootedDevice`.</span></span>|
|<span data-ttu-id="8efc2-161">userId</span><span class="sxs-lookup"><span data-stu-id="8efc2-161">userID</span></span>|<span data-ttu-id="8efc2-162">String</span><span class="sxs-lookup"><span data-stu-id="8efc2-162">String</span></span>|<span data-ttu-id="8efc2-163">Identificador de usuario al que pertenece este registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8efc2-163">The user Id to who this app registration belongs.</span></span> <span data-ttu-id="8efc2-164">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="8efc2-164">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-165">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="8efc2-165">appIdentifier</span></span>|[<span data-ttu-id="8efc2-166">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="8efc2-166">mobileAppIdentifier</span></span>](../resources/intune_mam_mobileappidentifier.md)|<span data-ttu-id="8efc2-167">Identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="8efc2-167">The app package Identifier Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-168">id</span><span class="sxs-lookup"><span data-stu-id="8efc2-168">id</span></span>|<span data-ttu-id="8efc2-169">String</span><span class="sxs-lookup"><span data-stu-id="8efc2-169">String</span></span>|<span data-ttu-id="8efc2-170">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8efc2-170">Key of the setting.</span></span> <span data-ttu-id="8efc2-171">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="8efc2-171">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="8efc2-172">version</span><span class="sxs-lookup"><span data-stu-id="8efc2-172">version</span></span>|<span data-ttu-id="8efc2-173">String</span><span class="sxs-lookup"><span data-stu-id="8efc2-173">String</span></span>|<span data-ttu-id="8efc2-174">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8efc2-174">Version of the entity.</span></span> <span data-ttu-id="8efc2-175">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="8efc2-175">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="8efc2-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8efc2-176">Response</span></span>
<span data-ttu-id="8efc2-177">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8efc2-177">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_mam_iosmanagedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8efc2-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8efc2-178">Example</span></span>
### <a name="request"></a><span data-ttu-id="8efc2-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8efc2-179">Request</span></span>
<span data-ttu-id="8efc2-180">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8efc2-180">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations
Content-type: application/json
Content-length: 635

{
  "@odata.type": "#microsoft.graph.iosManagedAppRegistration",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "applicationVersion": "Application Version value",
  "managementSdkVersion": "Management Sdk Version value",
  "platformVersion": "Platform Version value",
  "deviceType": "Device Type value",
  "deviceTag": "Device Tag value",
  "deviceName": "Device Name value",
  "flaggedReasons": [
    "rootedDevice"
  ],
  "userId": "User Id value",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.iosMobileAppIdentifier",
    "bundleId": "Bundle Id value"
  },
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="8efc2-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8efc2-181">Response</span></span>
<span data-ttu-id="8efc2-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8efc2-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 743

{
  "@odata.type": "#microsoft.graph.iosManagedAppRegistration",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "applicationVersion": "Application Version value",
  "managementSdkVersion": "Management Sdk Version value",
  "platformVersion": "Platform Version value",
  "deviceType": "Device Type value",
  "deviceTag": "Device Tag value",
  "deviceName": "Device Name value",
  "flaggedReasons": [
    "rootedDevice"
  ],
  "userId": "User Id value",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.iosMobileAppIdentifier",
    "bundleId": "Bundle Id value"
  },
  "id": "47632c19-2c19-4763-192c-6347192c6347",
  "version": "Version value"
}
```




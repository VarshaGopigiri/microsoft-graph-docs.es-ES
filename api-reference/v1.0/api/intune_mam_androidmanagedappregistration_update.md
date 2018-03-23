# <a name="update-androidmanagedappregistration"></a><span data-ttu-id="99934-101">Actualizar androidManagedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="99934-101">Update androidManagedAppRegistration</span></span>

> <span data-ttu-id="99934-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="99934-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="99934-103">Actualice las propiedades de un objeto [androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="99934-103">Update the properties of a [calendar](../resources/intune_mam_androidmanagedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="99934-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="99934-104">Prerequisites</span></span>
<span data-ttu-id="99934-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="99934-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="99934-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="99934-107">Permission type</span></span>|<span data-ttu-id="99934-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="99934-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="99934-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="99934-109">Delegated (work or school account)</span></span>|<span data-ttu-id="99934-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="99934-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="99934-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="99934-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="99934-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99934-112">Not supported.</span></span>|
|<span data-ttu-id="99934-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="99934-113">Application</span></span>|<span data-ttu-id="99934-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99934-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="99934-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="99934-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

## <a name="request-headers"></a><span data-ttu-id="99934-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="99934-116">Request headers</span></span>
|<span data-ttu-id="99934-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99934-117">Header</span></span>|<span data-ttu-id="99934-118">Valor</span><span class="sxs-lookup"><span data-stu-id="99934-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="99934-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="99934-119">Authorization</span></span>|<span data-ttu-id="99934-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="99934-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="99934-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="99934-121">Accept</span></span>|<span data-ttu-id="99934-122">application/json</span><span class="sxs-lookup"><span data-stu-id="99934-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="99934-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="99934-123">Request body</span></span>
<span data-ttu-id="99934-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="99934-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_mam_androidmanagedappregistration.md) object.</span></span>

<span data-ttu-id="99934-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="99934-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="99934-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99934-126">Property</span></span>|<span data-ttu-id="99934-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="99934-127">Type</span></span>|<span data-ttu-id="99934-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="99934-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="99934-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="99934-129">createdDateTime</span></span>|<span data-ttu-id="99934-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="99934-130">DateTimeOffset</span></span>|<span data-ttu-id="99934-131">Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="99934-131">Date and time of creation Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-132">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="99934-132">lastSyncDateTime</span></span>|<span data-ttu-id="99934-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="99934-133">DateTimeOffset</span></span>|<span data-ttu-id="99934-134">Fecha y hora de la última sincronización de la aplicación con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="99934-134">Date and time of last the app synced with management service.</span></span> <span data-ttu-id="99934-135">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="99934-135">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-136">applicationVersion</span><span class="sxs-lookup"><span data-stu-id="99934-136">applicationVersion</span></span>|<span data-ttu-id="99934-137">String</span><span class="sxs-lookup"><span data-stu-id="99934-137">String</span></span>|<span data-ttu-id="99934-138">Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="99934-138">App version Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-139">managementSdkVersion</span><span class="sxs-lookup"><span data-stu-id="99934-139">managementSdkVersion</span></span>|<span data-ttu-id="99934-140">String</span><span class="sxs-lookup"><span data-stu-id="99934-140">String</span></span>|<span data-ttu-id="99934-141">Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="99934-141">App management SDK version Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-142">platformVersion</span><span class="sxs-lookup"><span data-stu-id="99934-142">platformVersion</span></span>|<span data-ttu-id="99934-143">String</span><span class="sxs-lookup"><span data-stu-id="99934-143">String</span></span>|<span data-ttu-id="99934-144">Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="99934-144">Operating System version Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-145">deviceType</span><span class="sxs-lookup"><span data-stu-id="99934-145">deviceType</span></span>|<span data-ttu-id="99934-146">String</span><span class="sxs-lookup"><span data-stu-id="99934-146">String</span></span>|<span data-ttu-id="99934-147">Tipo de dispositivo host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="99934-147">Host device type Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-148">deviceTag</span><span class="sxs-lookup"><span data-stu-id="99934-148">deviceTag</span></span>|<span data-ttu-id="99934-149">String</span><span class="sxs-lookup"><span data-stu-id="99934-149">String</span></span>|<span data-ttu-id="99934-150">Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99934-150">App management SDK generated tag, which helps relate apps hosted on the same device.</span></span> <span data-ttu-id="99934-151">No garantiza que las aplicaciones se relacionen en todas las condiciones.</span><span class="sxs-lookup"><span data-stu-id="99934-151">Not guaranteed to relate apps in all conditions.</span></span> <span data-ttu-id="99934-152">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="99934-152">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-153">deviceName</span><span class="sxs-lookup"><span data-stu-id="99934-153">deviceName</span></span>|<span data-ttu-id="99934-154">String</span><span class="sxs-lookup"><span data-stu-id="99934-154">String</span></span>|<span data-ttu-id="99934-155">Nombre del dispositivo host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="99934-155">Host device name Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-156">flaggedReasons</span><span class="sxs-lookup"><span data-stu-id="99934-156">flaggedReasons</span></span>|<span data-ttu-id="99934-157">Colección string</span><span class="sxs-lookup"><span data-stu-id="99934-157">String collection</span></span>|<span data-ttu-id="99934-158">Cero o más razones por las que se ha marcado el registro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="99934-158">Zero or more reasons an app registration is flagged.</span></span> <span data-ttu-id="99934-159">E.g.</span><span class="sxs-lookup"><span data-stu-id="99934-159">E.g.</span></span> <span data-ttu-id="99934-160">Aplicación que se ejecuta en un dispositivo con rooting. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md). Los valores posibles son: `none` y `rootedDevice`.</span><span class="sxs-lookup"><span data-stu-id="99934-160">app running on rooted device Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md) Possible values are: `none`, `rootedDevice`.</span></span>|
|<span data-ttu-id="99934-161">userId</span><span class="sxs-lookup"><span data-stu-id="99934-161">userID</span></span>|<span data-ttu-id="99934-162">String</span><span class="sxs-lookup"><span data-stu-id="99934-162">String</span></span>|<span data-ttu-id="99934-163">Identificador de usuario al que pertenece este registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="99934-163">The user Id to who this app registration belongs.</span></span> <span data-ttu-id="99934-164">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="99934-164">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-165">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="99934-165">appIdentifier</span></span>|[<span data-ttu-id="99934-166">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="99934-166">mobileAppIdentifier</span></span>](../resources/intune_mam_mobileappidentifier.md)|<span data-ttu-id="99934-167">Identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="99934-167">The app package Identifier Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-168">id</span><span class="sxs-lookup"><span data-stu-id="99934-168">id</span></span>|<span data-ttu-id="99934-169">String</span><span class="sxs-lookup"><span data-stu-id="99934-169">String</span></span>|<span data-ttu-id="99934-170">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="99934-170">Key of the setting.</span></span> <span data-ttu-id="99934-171">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="99934-171">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="99934-172">version</span><span class="sxs-lookup"><span data-stu-id="99934-172">version</span></span>|<span data-ttu-id="99934-173">String</span><span class="sxs-lookup"><span data-stu-id="99934-173">String</span></span>|<span data-ttu-id="99934-174">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="99934-174">Version of the entity.</span></span> <span data-ttu-id="99934-175">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="99934-175">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="99934-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99934-176">Response</span></span>
<span data-ttu-id="99934-177">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99934-177">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_mam_androidmanagedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="99934-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99934-178">Example</span></span>
### <a name="request"></a><span data-ttu-id="99934-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99934-179">Request</span></span>
<span data-ttu-id="99934-180">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99934-180">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
Content-type: application/json
Content-length: 577

{
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
    "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
    "packageId": "Package Id value"
  },
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="99934-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99934-181">Response</span></span>
<span data-ttu-id="99934-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="99934-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 753

{
  "@odata.type": "#microsoft.graph.androidManagedAppRegistration",
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
    "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
    "packageId": "Package Id value"
  },
  "id": "0e064997-4997-0e06-9749-060e9749060e",
  "version": "Version value"
}
```




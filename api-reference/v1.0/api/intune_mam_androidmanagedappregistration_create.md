# <a name="create-androidmanagedappregistration"></a><span data-ttu-id="5e8bd-101">Crear androidManagedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="5e8bd-101">Create androidManagedAppRegistration</span></span>

> <span data-ttu-id="5e8bd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5e8bd-103">Cree un objeto [androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5e8bd-103">Create a new [androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5e8bd-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5e8bd-104">Prerequisites</span></span>
<span data-ttu-id="5e8bd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5e8bd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5e8bd-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5e8bd-107">Permission type</span></span>|<span data-ttu-id="5e8bd-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5e8bd-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5e8bd-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5e8bd-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5e8bd-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5e8bd-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-112">Not supported.</span></span>|
|<span data-ttu-id="5e8bd-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5e8bd-113">Application</span></span>|<span data-ttu-id="5e8bd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5e8bd-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5e8bd-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="5e8bd-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5e8bd-116">Request headers</span></span>
|<span data-ttu-id="5e8bd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e8bd-117">Header</span></span>|<span data-ttu-id="5e8bd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5e8bd-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5e8bd-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="5e8bd-119">Authorization</span></span>|<span data-ttu-id="5e8bd-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5e8bd-121">Accept</span><span class="sxs-lookup"><span data-stu-id="5e8bd-121">Accept</span></span>|<span data-ttu-id="5e8bd-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5e8bd-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5e8bd-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5e8bd-123">Request body</span></span>
<span data-ttu-id="5e8bd-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-124">In the request body, supply a JSON representation for the androidManagedAppRegistration object.</span></span>

<span data-ttu-id="5e8bd-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidManagedAppRegistration.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-125">The following table shows the properties that are required when you create the androidManagedAppRegistration.</span></span>

|<span data-ttu-id="5e8bd-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5e8bd-126">Property</span></span>|<span data-ttu-id="5e8bd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e8bd-127">Type</span></span>|<span data-ttu-id="5e8bd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e8bd-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5e8bd-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5e8bd-129">createdDateTime</span></span>|<span data-ttu-id="5e8bd-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5e8bd-130">DateTimeOffset</span></span>|<span data-ttu-id="5e8bd-131">Fecha y hora de creación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-131">Date and time of creation Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-132">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="5e8bd-132">lastSyncDateTime</span></span>|<span data-ttu-id="5e8bd-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5e8bd-133">DateTimeOffset</span></span>|<span data-ttu-id="5e8bd-134">Fecha y hora de la última sincronización de la aplicación con el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-134">Date and time of last the app synced with management service.</span></span> <span data-ttu-id="5e8bd-135">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-135">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-136">applicationVersion</span><span class="sxs-lookup"><span data-stu-id="5e8bd-136">applicationVersion</span></span>|<span data-ttu-id="5e8bd-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e8bd-137">String</span></span>|<span data-ttu-id="5e8bd-138">Versión de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-138">App version Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-139">managementSdkVersion</span><span class="sxs-lookup"><span data-stu-id="5e8bd-139">managementSdkVersion</span></span>|<span data-ttu-id="5e8bd-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e8bd-140">String</span></span>|<span data-ttu-id="5e8bd-141">Versión del SDK de administración de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-141">App management SDK version Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-142">platformVersion</span><span class="sxs-lookup"><span data-stu-id="5e8bd-142">platformVersion</span></span>|<span data-ttu-id="5e8bd-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e8bd-143">String</span></span>|<span data-ttu-id="5e8bd-144">Versión del sistema operativo. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-144">Operating System version Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-145">deviceType</span><span class="sxs-lookup"><span data-stu-id="5e8bd-145">deviceType</span></span>|<span data-ttu-id="5e8bd-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e8bd-146">String</span></span>|<span data-ttu-id="5e8bd-147">Tipo de dispositivo host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-147">Host device type Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-148">deviceTag</span><span class="sxs-lookup"><span data-stu-id="5e8bd-148">deviceTag</span></span>|<span data-ttu-id="5e8bd-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e8bd-149">String</span></span>|<span data-ttu-id="5e8bd-150">Etiqueta generada por el SDK de administración de la aplicación, que ayuda a relacionar las aplicaciones que se hospedan en el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-150">App management SDK generated tag, which helps relate apps hosted on the same device.</span></span> <span data-ttu-id="5e8bd-151">No garantiza que las aplicaciones se relacionen en todas las condiciones.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-151">Not guaranteed to relate apps in all conditions.</span></span> <span data-ttu-id="5e8bd-152">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-152">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-153">deviceName</span><span class="sxs-lookup"><span data-stu-id="5e8bd-153">deviceName</span></span>|<span data-ttu-id="5e8bd-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e8bd-154">String</span></span>|<span data-ttu-id="5e8bd-155">Nombre del dispositivo host. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-155">Host device name Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-156">flaggedReasons</span><span class="sxs-lookup"><span data-stu-id="5e8bd-156">flaggedReasons</span></span>|<span data-ttu-id="5e8bd-157">Colección [managedAppFlaggedReason enum](../resources/intune_mam_managedappflaggedreason.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-157">[managedAppFlaggedReason enum](../resources/intune_mam_managedappflaggedreason.md) collection</span></span>|<span data-ttu-id="5e8bd-p104">Cero o más motivos por las que se marca un registro de aplicación. Por ejemplo, la aplicación se está ejecutando en un dispositivo con permisos de administrador. Heredado desde [managedAppRegistration](../resources/intune_mam_managedappregistration.md). Los valores posibles son: `none`, `rootedDevice`.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-p104">Zero or more reasons an app registration is flagged. E.g. app running on rooted device Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md). The possible values are: `none`, `rootedDevice`.</span></span>|
|<span data-ttu-id="5e8bd-162">userId</span><span class="sxs-lookup"><span data-stu-id="5e8bd-162">userId</span></span>|<span data-ttu-id="5e8bd-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e8bd-163">String</span></span>|<span data-ttu-id="5e8bd-164">Identificador de usuario al que pertenece este registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-164">The user Id to who this app registration belongs.</span></span> <span data-ttu-id="5e8bd-165">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-165">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-166">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="5e8bd-166">appIdentifier</span></span>|[<span data-ttu-id="5e8bd-167">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="5e8bd-167">mobileAppIdentifier</span></span>](../resources/intune_mam_mobileappidentifier.md)|<span data-ttu-id="5e8bd-168">Identificador del paquete de la aplicación. Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-168">The app package Identifier Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-169">id</span><span class="sxs-lookup"><span data-stu-id="5e8bd-169">id</span></span>|<span data-ttu-id="5e8bd-170">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e8bd-170">String</span></span>|<span data-ttu-id="5e8bd-171">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-171">Key of the entity.</span></span> <span data-ttu-id="5e8bd-172">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="5e8bd-172">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|
|<span data-ttu-id="5e8bd-173">version</span><span class="sxs-lookup"><span data-stu-id="5e8bd-173">version</span></span>|<span data-ttu-id="5e8bd-174">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e8bd-174">String</span></span>|<span data-ttu-id="5e8bd-175">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-175">Version of the entity.</span></span> <span data-ttu-id="5e8bd-176">Heredado de [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5e8bd-176">Inherited from [managedAppRegistration](../resources/intune_mam_managedappregistration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="5e8bd-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e8bd-177">Response</span></span>
<span data-ttu-id="5e8bd-178">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-178">If successful, this method returns a `201 Created` response code and a [androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5e8bd-179">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e8bd-179">Example</span></span>
### <a name="request"></a><span data-ttu-id="5e8bd-180">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5e8bd-180">Request</span></span>
<span data-ttu-id="5e8bd-181">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-181">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations
Content-type: application/json
Content-length: 645

{
  "@odata.type": "#microsoft.graph.androidManagedAppRegistration",
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

### <a name="response"></a><span data-ttu-id="5e8bd-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e8bd-182">Response</span></span>
<span data-ttu-id="5e8bd-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5e8bd-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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









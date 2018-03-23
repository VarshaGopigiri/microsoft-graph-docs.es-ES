# <a name="update-targetedmanagedappconfiguration"></a><span data-ttu-id="31dfd-101">Actualizar targetedManagedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="31dfd-101">Update targetedManagedAppConfiguration</span></span>

> <span data-ttu-id="31dfd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="31dfd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="31dfd-103">Actualice las propiedades de un objeto [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-103">Update the properties of a [calendar](../resources/intune_mam_targetedmanagedappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="31dfd-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="31dfd-104">Prerequisites</span></span>
<span data-ttu-id="31dfd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="31dfd-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="31dfd-107">Permission type</span></span>|<span data-ttu-id="31dfd-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="31dfd-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="31dfd-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="31dfd-109">Delegated (work or school account)</span></span>|<span data-ttu-id="31dfd-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="31dfd-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="31dfd-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="31dfd-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="31dfd-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31dfd-112">Not supported.</span></span>|
|<span data-ttu-id="31dfd-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="31dfd-113">Application</span></span>|<span data-ttu-id="31dfd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31dfd-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="31dfd-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31dfd-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="31dfd-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="31dfd-116">Request headers</span></span>
|<span data-ttu-id="31dfd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31dfd-117">Header</span></span>|<span data-ttu-id="31dfd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="31dfd-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="31dfd-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="31dfd-119">Authorization</span></span>|<span data-ttu-id="31dfd-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="31dfd-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="31dfd-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="31dfd-121">Accept</span></span>|<span data-ttu-id="31dfd-122">application/json</span><span class="sxs-lookup"><span data-stu-id="31dfd-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="31dfd-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="31dfd-123">Request body</span></span>
<span data-ttu-id="31dfd-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_mam_targetedmanagedappconfiguration.md) object.</span></span>

<span data-ttu-id="31dfd-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="31dfd-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31dfd-126">Property</span></span>|<span data-ttu-id="31dfd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="31dfd-127">Type</span></span>|<span data-ttu-id="31dfd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="31dfd-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="31dfd-129">displayName</span><span class="sxs-lookup"><span data-stu-id="31dfd-129">displayName</span></span>|<span data-ttu-id="31dfd-130">String</span><span class="sxs-lookup"><span data-stu-id="31dfd-130">String</span></span>|<span data-ttu-id="31dfd-131">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="31dfd-131">Policy display name.</span></span> <span data-ttu-id="31dfd-132">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-132">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="31dfd-133">description</span><span class="sxs-lookup"><span data-stu-id="31dfd-133">description</span></span>|<span data-ttu-id="31dfd-134">String</span><span class="sxs-lookup"><span data-stu-id="31dfd-134">String</span></span>|<span data-ttu-id="31dfd-135">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="31dfd-135">The policy's description.</span></span> <span data-ttu-id="31dfd-136">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-136">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="31dfd-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="31dfd-137">createdDateTime</span></span>|<span data-ttu-id="31dfd-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="31dfd-138">DateTimeOffset</span></span>|<span data-ttu-id="31dfd-139">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="31dfd-139">The date and time when the page was created.</span></span> <span data-ttu-id="31dfd-140">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-140">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="31dfd-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="31dfd-141">lastModifiedDateTime</span></span>|<span data-ttu-id="31dfd-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="31dfd-142">DateTimeOffset</span></span>|<span data-ttu-id="31dfd-143">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="31dfd-143">Last time the policy was modified.</span></span> <span data-ttu-id="31dfd-144">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-144">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="31dfd-145">id</span><span class="sxs-lookup"><span data-stu-id="31dfd-145">id</span></span>|<span data-ttu-id="31dfd-146">String</span><span class="sxs-lookup"><span data-stu-id="31dfd-146">String</span></span>|<span data-ttu-id="31dfd-147">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="31dfd-147">Key of the setting.</span></span> <span data-ttu-id="31dfd-148">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-148">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="31dfd-149">version</span><span class="sxs-lookup"><span data-stu-id="31dfd-149">version</span></span>|<span data-ttu-id="31dfd-150">String</span><span class="sxs-lookup"><span data-stu-id="31dfd-150">String</span></span>|<span data-ttu-id="31dfd-151">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="31dfd-151">Version of the entity.</span></span> <span data-ttu-id="31dfd-152">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="31dfd-152">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="31dfd-153">customSettings</span><span class="sxs-lookup"><span data-stu-id="31dfd-153">customSettings</span></span>|<span data-ttu-id="31dfd-154">Colección [keyValuePair](../resources/intune_mam_keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="31dfd-154">[keyValuePair](../resources/intune_mam_keyvaluepair.md) collection</span></span>|<span data-ttu-id="31dfd-155">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio. Heredado de [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="31dfd-155">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service Inherited from [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md)</span></span>|
|<span data-ttu-id="31dfd-156">deployedAppCount</span><span class="sxs-lookup"><span data-stu-id="31dfd-156">deployedAppCount</span></span>|<span data-ttu-id="31dfd-157">Int32</span><span class="sxs-lookup"><span data-stu-id="31dfd-157">Int32</span></span>|<span data-ttu-id="31dfd-158">Número de aplicaciones en las que se implementará la directiva actual.</span><span class="sxs-lookup"><span data-stu-id="31dfd-158">Count of apps to which the current policy is deployed.</span></span>|
|<span data-ttu-id="31dfd-159">isAssigned</span><span class="sxs-lookup"><span data-stu-id="31dfd-159">isAssigned</span></span>|<span data-ttu-id="31dfd-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="31dfd-160">Boolean</span></span>|<span data-ttu-id="31dfd-161">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="31dfd-161">Indicates if the policy is deployed to any inclusion groups or not.</span></span>|



## <a name="response"></a><span data-ttu-id="31dfd-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31dfd-162">Response</span></span>
<span data-ttu-id="31dfd-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31dfd-163">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_mam_targetedmanagedappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="31dfd-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31dfd-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="31dfd-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="31dfd-165">Request</span></span>
<span data-ttu-id="31dfd-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31dfd-166">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
Content-type: application/json
Content-length: 382

{
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": "Version value",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "deployedAppCount": 0,
  "isAssigned": true
}
```

### <a name="response"></a><span data-ttu-id="31dfd-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31dfd-167">Response</span></span>
<span data-ttu-id="31dfd-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="31dfd-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 560

{
  "@odata.type": "#microsoft.graph.targetedManagedAppConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "id": "2444e029-e029-2444-29e0-442429e04424",
  "version": "Version value",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "deployedAppCount": 0,
  "isAssigned": true
}
```




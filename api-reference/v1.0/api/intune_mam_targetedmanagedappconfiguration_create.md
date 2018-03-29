# <a name="create-targetedmanagedappconfiguration"></a><span data-ttu-id="2d196-101">Crear targetedManagedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d196-101">Create targetedManagedAppConfiguration</span></span>

> <span data-ttu-id="2d196-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2d196-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2d196-103">Cree un objeto [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2d196-103">Create a new [plannerBucket](../resources/intune_mam_targetedmanagedappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2d196-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2d196-104">Prerequisites</span></span>
<span data-ttu-id="2d196-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2d196-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2d196-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2d196-107">Permission type</span></span>|<span data-ttu-id="2d196-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2d196-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2d196-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2d196-109">Delegated (work or school account)</span></span>|<span data-ttu-id="2d196-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2d196-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="2d196-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d196-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2d196-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d196-112">Not supported.</span></span>|
|<span data-ttu-id="2d196-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2d196-113">Application</span></span>|<span data-ttu-id="2d196-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d196-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2d196-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d196-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/targetedManagedAppConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="2d196-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2d196-116">Request headers</span></span>
|<span data-ttu-id="2d196-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d196-117">Header</span></span>|<span data-ttu-id="2d196-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2d196-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2d196-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="2d196-119">Authorization</span></span>|<span data-ttu-id="2d196-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2d196-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="2d196-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2d196-121">Accept</span></span>|<span data-ttu-id="2d196-122">application/json</span><span class="sxs-lookup"><span data-stu-id="2d196-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2d196-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d196-123">Request body</span></span>
<span data-ttu-id="2d196-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto targetedManagedAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d196-124">In the request body, supply a JSON representation of user object.</span></span>

<span data-ttu-id="2d196-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto targetedManagedAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d196-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="2d196-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2d196-126">Property</span></span>|<span data-ttu-id="2d196-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d196-127">Type</span></span>|<span data-ttu-id="2d196-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d196-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2d196-129">displayName</span><span class="sxs-lookup"><span data-stu-id="2d196-129">displayName</span></span>|<span data-ttu-id="2d196-130">String</span><span class="sxs-lookup"><span data-stu-id="2d196-130">String</span></span>|<span data-ttu-id="2d196-131">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2d196-131">Policy display name.</span></span> <span data-ttu-id="2d196-132">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2d196-132">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="2d196-133">description</span><span class="sxs-lookup"><span data-stu-id="2d196-133">description</span></span>|<span data-ttu-id="2d196-134">String</span><span class="sxs-lookup"><span data-stu-id="2d196-134">String</span></span>|<span data-ttu-id="2d196-135">Descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2d196-135">The policy's description.</span></span> <span data-ttu-id="2d196-136">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2d196-136">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="2d196-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2d196-137">createdDateTime</span></span>|<span data-ttu-id="2d196-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2d196-138">DateTimeOffset</span></span>|<span data-ttu-id="2d196-139">Fecha y hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="2d196-139">The date and time when the page was created.</span></span> <span data-ttu-id="2d196-140">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2d196-140">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="2d196-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2d196-141">lastModifiedDateTime</span></span>|<span data-ttu-id="2d196-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2d196-142">DateTimeOffset</span></span>|<span data-ttu-id="2d196-143">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="2d196-143">Last time the policy was modified.</span></span> <span data-ttu-id="2d196-144">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2d196-144">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="2d196-145">id</span><span class="sxs-lookup"><span data-stu-id="2d196-145">id</span></span>|<span data-ttu-id="2d196-146">String</span><span class="sxs-lookup"><span data-stu-id="2d196-146">String</span></span>|<span data-ttu-id="2d196-147">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2d196-147">Key of the setting.</span></span> <span data-ttu-id="2d196-148">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2d196-148">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="2d196-149">version</span><span class="sxs-lookup"><span data-stu-id="2d196-149">version</span></span>|<span data-ttu-id="2d196-150">String</span><span class="sxs-lookup"><span data-stu-id="2d196-150">String</span></span>|<span data-ttu-id="2d196-151">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2d196-151">Version of the entity.</span></span> <span data-ttu-id="2d196-152">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="2d196-152">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="2d196-153">customSettings</span><span class="sxs-lookup"><span data-stu-id="2d196-153">customSettings</span></span>|<span data-ttu-id="2d196-154">Colección [keyValuePair](../resources/intune_mam_keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="2d196-154">[keyValuePair](../resources/intune_mam_keyvaluepair.md) collection</span></span>|<span data-ttu-id="2d196-155">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio. Heredado de [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2d196-155">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service Inherited from [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md)</span></span>|
|<span data-ttu-id="2d196-156">deployedAppCount</span><span class="sxs-lookup"><span data-stu-id="2d196-156">deployedAppCount</span></span>|<span data-ttu-id="2d196-157">Int32</span><span class="sxs-lookup"><span data-stu-id="2d196-157">Int32</span></span>|<span data-ttu-id="2d196-158">Número de aplicaciones en las que se implementará la directiva actual.</span><span class="sxs-lookup"><span data-stu-id="2d196-158">Count of apps to which the current policy is deployed.</span></span>|
|<span data-ttu-id="2d196-159">isAssigned</span><span class="sxs-lookup"><span data-stu-id="2d196-159">isAssigned</span></span>|<span data-ttu-id="2d196-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="2d196-160">Boolean</span></span>|<span data-ttu-id="2d196-161">Indica si la directiva se implementará en los grupos de inclusión.</span><span class="sxs-lookup"><span data-stu-id="2d196-161">Indicates if the policy is deployed to any inclusion groups or not.</span></span>|



## <a name="response"></a><span data-ttu-id="2d196-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d196-162">Response</span></span>
<span data-ttu-id="2d196-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [targetedManagedAppConfiguration](../resources/intune_mam_targetedmanagedappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d196-163">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_mam_targetedmanagedappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2d196-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d196-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="2d196-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d196-165">Request</span></span>
<span data-ttu-id="2d196-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2d196-166">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/targetedManagedAppConfigurations
Content-type: application/json
Content-length: 452

{
  "@odata.type": "#microsoft.graph.targetedManagedAppConfiguration",
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

### <a name="response"></a><span data-ttu-id="2d196-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d196-167">Response</span></span>
<span data-ttu-id="2d196-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2d196-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




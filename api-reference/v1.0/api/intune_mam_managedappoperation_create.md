# <a name="create-managedappoperation"></a><span data-ttu-id="01f2d-101">Crear managedAppOperation</span><span class="sxs-lookup"><span data-stu-id="01f2d-101">Create managedAppOperation</span></span>

> <span data-ttu-id="01f2d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01f2d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01f2d-103">Cree un objeto [managedAppOperation](../resources/intune_mam_managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="01f2d-103">Create a new [managedAppOperation](../resources/intune_mam_managedappoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="01f2d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01f2d-104">Prerequisites</span></span>
<span data-ttu-id="01f2d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="01f2d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="01f2d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01f2d-107">Permission type</span></span>|<span data-ttu-id="01f2d-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01f2d-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="01f2d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01f2d-109">Delegated (work or school account)</span></span>|<span data-ttu-id="01f2d-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01f2d-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="01f2d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01f2d-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="01f2d-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01f2d-112">Not supported.</span></span>|
|<span data-ttu-id="01f2d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01f2d-113">Application</span></span>|<span data-ttu-id="01f2d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01f2d-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="01f2d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01f2d-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations
```

## <a name="request-headers"></a><span data-ttu-id="01f2d-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01f2d-116">Request headers</span></span>
|<span data-ttu-id="01f2d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01f2d-117">Header</span></span>|<span data-ttu-id="01f2d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="01f2d-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="01f2d-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="01f2d-119">Authorization</span></span>|<span data-ttu-id="01f2d-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="01f2d-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="01f2d-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="01f2d-121">Accept</span></span>|<span data-ttu-id="01f2d-122">application/json</span><span class="sxs-lookup"><span data-stu-id="01f2d-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="01f2d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01f2d-123">Request body</span></span>
<span data-ttu-id="01f2d-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedAppOperation.</span><span class="sxs-lookup"><span data-stu-id="01f2d-124">In the request body, supply a JSON representation for the managedAppOperation object.</span></span>

<span data-ttu-id="01f2d-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedAppOperation.</span><span class="sxs-lookup"><span data-stu-id="01f2d-125">The following table shows the properties that are required when you create the managedAppOperation.</span></span>

|<span data-ttu-id="01f2d-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01f2d-126">Property</span></span>|<span data-ttu-id="01f2d-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="01f2d-127">Type</span></span>|<span data-ttu-id="01f2d-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="01f2d-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01f2d-129">displayName</span><span class="sxs-lookup"><span data-stu-id="01f2d-129">displayName</span></span>|<span data-ttu-id="01f2d-130">String</span><span class="sxs-lookup"><span data-stu-id="01f2d-130">String</span></span>|<span data-ttu-id="01f2d-131">El nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="01f2d-131">The operation name.</span></span>|
|<span data-ttu-id="01f2d-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="01f2d-132">lastModifiedDateTime</span></span>|<span data-ttu-id="01f2d-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01f2d-133">DateTimeOffset</span></span>|<span data-ttu-id="01f2d-134">La última vez que se modificó el funcionamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="01f2d-134">The last time the app operation was modified.</span></span>|
|<span data-ttu-id="01f2d-135">state</span><span class="sxs-lookup"><span data-stu-id="01f2d-135">state</span></span>|<span data-ttu-id="01f2d-136">String</span><span class="sxs-lookup"><span data-stu-id="01f2d-136">String</span></span>|<span data-ttu-id="01f2d-137">El estado actual de la operación</span><span class="sxs-lookup"><span data-stu-id="01f2d-137">The current state of the operation</span></span>|
|<span data-ttu-id="01f2d-138">id</span><span class="sxs-lookup"><span data-stu-id="01f2d-138">id</span></span>|<span data-ttu-id="01f2d-139">String</span><span class="sxs-lookup"><span data-stu-id="01f2d-139">String</span></span>|<span data-ttu-id="01f2d-140">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="01f2d-140">Key of the entity.</span></span>|
|<span data-ttu-id="01f2d-141">version</span><span class="sxs-lookup"><span data-stu-id="01f2d-141">version</span></span>|<span data-ttu-id="01f2d-142">String</span><span class="sxs-lookup"><span data-stu-id="01f2d-142">String</span></span>|<span data-ttu-id="01f2d-143">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="01f2d-143">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="01f2d-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01f2d-144">Response</span></span>
<span data-ttu-id="01f2d-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedAppOperation](../resources/intune_mam_managedappoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01f2d-145">If successful, this method returns a `201 Created` response code and a [managedAppOperation](../resources/intune_mam_managedappoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01f2d-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01f2d-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="01f2d-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01f2d-147">Request</span></span>
<span data-ttu-id="01f2d-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01f2d-148">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations
Content-type: application/json
Content-length: 159

{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "Display Name value",
  "state": "State value",
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="01f2d-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01f2d-149">Response</span></span>
<span data-ttu-id="01f2d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01f2d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 272

{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "State value",
  "id": "f2867b06-7b06-f286-067b-86f2067b86f2",
  "version": "Version value"
}
```




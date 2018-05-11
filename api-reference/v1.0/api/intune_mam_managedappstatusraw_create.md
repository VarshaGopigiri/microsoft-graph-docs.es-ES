# <a name="create-managedappstatusraw"></a><span data-ttu-id="1f3cc-101">Crear managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="1f3cc-101">Create managedAppStatusRaw</span></span>

> <span data-ttu-id="1f3cc-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1f3cc-103">Cree un objeto [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="1f3cc-103">Create a new [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1f3cc-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1f3cc-104">Prerequisites</span></span>
<span data-ttu-id="1f3cc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1f3cc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1f3cc-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1f3cc-107">Permission type</span></span>|<span data-ttu-id="1f3cc-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1f3cc-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1f3cc-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1f3cc-109">Delegated (work or school account)</span></span>|<span data-ttu-id="1f3cc-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1f3cc-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1f3cc-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1f3cc-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1f3cc-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-112">Not supported.</span></span>|
|<span data-ttu-id="1f3cc-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1f3cc-113">Application</span></span>|<span data-ttu-id="1f3cc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1f3cc-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1f3cc-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppStatuses
```

## <a name="request-headers"></a><span data-ttu-id="1f3cc-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1f3cc-116">Request headers</span></span>
|<span data-ttu-id="1f3cc-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f3cc-117">Header</span></span>|<span data-ttu-id="1f3cc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1f3cc-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1f3cc-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="1f3cc-119">Authorization</span></span>|<span data-ttu-id="1f3cc-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1f3cc-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1f3cc-121">Accept</span></span>|<span data-ttu-id="1f3cc-122">application/json</span><span class="sxs-lookup"><span data-stu-id="1f3cc-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1f3cc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1f3cc-123">Request body</span></span>
<span data-ttu-id="1f3cc-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedAppStatusRaw.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-124">In the request body, supply a JSON representation for the managedAppStatusRaw object.</span></span>

<span data-ttu-id="1f3cc-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedAppStatusRaw.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-125">The following table shows the properties that are required when you create the managedAppStatusRaw.</span></span>

|<span data-ttu-id="1f3cc-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1f3cc-126">Property</span></span>|<span data-ttu-id="1f3cc-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f3cc-127">Type</span></span>|<span data-ttu-id="1f3cc-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f3cc-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1f3cc-129">displayName</span><span class="sxs-lookup"><span data-stu-id="1f3cc-129">displayName</span></span>|<span data-ttu-id="1f3cc-130">String</span><span class="sxs-lookup"><span data-stu-id="1f3cc-130">String</span></span>|<span data-ttu-id="1f3cc-131">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-131">Friendly name of the status report.</span></span> <span data-ttu-id="1f3cc-132">Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="1f3cc-132">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="1f3cc-133">id</span><span class="sxs-lookup"><span data-stu-id="1f3cc-133">id</span></span>|<span data-ttu-id="1f3cc-134">String</span><span class="sxs-lookup"><span data-stu-id="1f3cc-134">String</span></span>|<span data-ttu-id="1f3cc-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-135">Key of the entity.</span></span> <span data-ttu-id="1f3cc-136">Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="1f3cc-136">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="1f3cc-137">version</span><span class="sxs-lookup"><span data-stu-id="1f3cc-137">version</span></span>|<span data-ttu-id="1f3cc-138">String</span><span class="sxs-lookup"><span data-stu-id="1f3cc-138">String</span></span>|<span data-ttu-id="1f3cc-139">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-139">Version of the entity.</span></span> <span data-ttu-id="1f3cc-140">Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="1f3cc-140">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="1f3cc-141">content</span><span class="sxs-lookup"><span data-stu-id="1f3cc-141">content</span></span>|[<span data-ttu-id="1f3cc-142">Json</span><span class="sxs-lookup"><span data-stu-id="1f3cc-142">Json</span></span>](../resources/intune_mam_json.md)|<span data-ttu-id="1f3cc-143">Contenido del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-143">Status report content.</span></span>|



## <a name="response"></a><span data-ttu-id="1f3cc-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f3cc-144">Response</span></span>
<span data-ttu-id="1f3cc-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-145">If successful, this method returns a `201 Created` response code and a [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1f3cc-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1f3cc-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="1f3cc-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1f3cc-147">Request</span></span>
<span data-ttu-id="1f3cc-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-148">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppStatuses
Content-type: application/json
Content-length: 197

{
  "@odata.type": "#microsoft.graph.managedAppStatusRaw",
  "displayName": "Display Name value",
  "version": "Version value",
  "content": {
    "@odata.type": "microsoft.graph.Json"
  }
}
```

### <a name="response"></a><span data-ttu-id="1f3cc-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f3cc-149">Response</span></span>
<span data-ttu-id="1f3cc-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 246

{
  "@odata.type": "#microsoft.graph.managedAppStatusRaw",
  "displayName": "Display Name value",
  "id": "80847581-7581-8084-8175-848081758480",
  "version": "Version value",
  "content": {
    "@odata.type": "microsoft.graph.Json"
  }
}
```




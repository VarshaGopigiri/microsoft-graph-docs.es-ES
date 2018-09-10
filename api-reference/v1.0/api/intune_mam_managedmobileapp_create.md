# <a name="create-managedmobileapp"></a><span data-ttu-id="29492-101">Crear managedMobileApp</span><span class="sxs-lookup"><span data-stu-id="29492-101">Create managedMobileApp</span></span>

> <span data-ttu-id="29492-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="29492-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="29492-103">Cree un objeto [managedMobileApp](../resources/intune_mam_managedmobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="29492-103">Create a new [managedMobileApp](../resources/intune_mam_managedmobileapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="29492-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="29492-104">Prerequisites</span></span>
<span data-ttu-id="29492-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="29492-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="29492-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="29492-107">Permission type</span></span>|<span data-ttu-id="29492-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="29492-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="29492-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="29492-109">Delegated (work or school account)</span></span>|<span data-ttu-id="29492-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="29492-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="29492-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="29492-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="29492-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="29492-112">Not supported.</span></span>|
|<span data-ttu-id="29492-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="29492-113">Application</span></span>|<span data-ttu-id="29492-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="29492-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="29492-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="29492-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/apps
POST /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/apps
POST /deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}/apps
POST /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/apps
```

## <a name="request-headers"></a><span data-ttu-id="29492-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="29492-116">Request headers</span></span>
|<span data-ttu-id="29492-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29492-117">Header</span></span>|<span data-ttu-id="29492-118">Valor</span><span class="sxs-lookup"><span data-stu-id="29492-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="29492-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="29492-119">Authorization</span></span>|<span data-ttu-id="29492-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="29492-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="29492-121">Accept</span><span class="sxs-lookup"><span data-stu-id="29492-121">Accept</span></span>|<span data-ttu-id="29492-122">application/json</span><span class="sxs-lookup"><span data-stu-id="29492-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="29492-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="29492-123">Request body</span></span>
<span data-ttu-id="29492-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedMobileApp.</span><span class="sxs-lookup"><span data-stu-id="29492-124">In the request body, supply a JSON representation for the managedMobileApp object.</span></span>

<span data-ttu-id="29492-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedMobileApp.</span><span class="sxs-lookup"><span data-stu-id="29492-125">The following table shows the properties that are required when you create the managedMobileApp.</span></span>

|<span data-ttu-id="29492-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="29492-126">Property</span></span>|<span data-ttu-id="29492-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="29492-127">Type</span></span>|<span data-ttu-id="29492-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="29492-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="29492-129">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="29492-129">mobileAppIdentifier</span></span>|[<span data-ttu-id="29492-130">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="29492-130">mobileAppIdentifier</span></span>](../resources/intune_mam_mobileappidentifier.md)|<span data-ttu-id="29492-131">El identificador de una aplicación con el tipo de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="29492-131">The identifier for an app with it's operating system type.</span></span>|
|<span data-ttu-id="29492-132">id</span><span class="sxs-lookup"><span data-stu-id="29492-132">id</span></span>|<span data-ttu-id="29492-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="29492-133">String</span></span>|<span data-ttu-id="29492-134">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="29492-134">Key of the entity.</span></span>|
|<span data-ttu-id="29492-135">version</span><span class="sxs-lookup"><span data-stu-id="29492-135">version</span></span>|<span data-ttu-id="29492-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="29492-136">String</span></span>|<span data-ttu-id="29492-137">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="29492-137">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="29492-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29492-138">Response</span></span>
<span data-ttu-id="29492-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedMobileApp](../resources/intune_mam_managedmobileapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="29492-139">If successful, this method returns a `201 Created` response code and a [managedMobileApp](../resources/intune_mam_managedmobileapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="29492-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="29492-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="29492-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="29492-141">Request</span></span>
<span data-ttu-id="29492-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="29492-142">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/apps
Content-type: application/json
Content-length: 181

{
  "@odata.type": "#microsoft.graph.managedMobileApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="29492-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29492-143">Response</span></span>
<span data-ttu-id="29492-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="29492-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 230

{
  "@odata.type": "#microsoft.graph.managedMobileApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "id": "0a129715-9715-0a12-1597-120a1597120a",
  "version": "Version value"
}
```









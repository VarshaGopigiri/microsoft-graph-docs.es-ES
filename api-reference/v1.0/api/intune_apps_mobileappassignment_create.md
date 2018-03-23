# <a name="create-mobileappassignment"></a><span data-ttu-id="fbf86-101">Crear mobileAppAssignment</span><span class="sxs-lookup"><span data-stu-id="fbf86-101">Create mobileAppAssignment</span></span>

> <span data-ttu-id="fbf86-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fbf86-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fbf86-103">Cree un objeto [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="fbf86-103">Create a new [plannerBucket](../resources/intune_apps_mobileappassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fbf86-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fbf86-104">Prerequisites</span></span>
<span data-ttu-id="fbf86-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fbf86-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fbf86-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fbf86-107">Permission type</span></span>|<span data-ttu-id="fbf86-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fbf86-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fbf86-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fbf86-109">Delegated (work or school account)</span></span>|<span data-ttu-id="fbf86-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fbf86-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="fbf86-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fbf86-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fbf86-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbf86-112">Not supported.</span></span>|
|<span data-ttu-id="fbf86-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fbf86-113">Application</span></span>|<span data-ttu-id="fbf86-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbf86-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fbf86-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fbf86-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="fbf86-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fbf86-116">Request headers</span></span>
|<span data-ttu-id="fbf86-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbf86-117">Header</span></span>|<span data-ttu-id="fbf86-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fbf86-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fbf86-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="fbf86-119">Authorization</span></span>|<span data-ttu-id="fbf86-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fbf86-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="fbf86-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fbf86-121">Accept</span></span>|<span data-ttu-id="fbf86-122">application/json</span><span class="sxs-lookup"><span data-stu-id="fbf86-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fbf86-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fbf86-123">Request body</span></span>
<span data-ttu-id="fbf86-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppAssignment.</span><span class="sxs-lookup"><span data-stu-id="fbf86-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="fbf86-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppAssignment.</span><span class="sxs-lookup"><span data-stu-id="fbf86-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="fbf86-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbf86-126">Property</span></span>|<span data-ttu-id="fbf86-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbf86-127">Type</span></span>|<span data-ttu-id="fbf86-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbf86-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fbf86-129">id</span><span class="sxs-lookup"><span data-stu-id="fbf86-129">id</span></span>|<span data-ttu-id="fbf86-130">String</span><span class="sxs-lookup"><span data-stu-id="fbf86-130">String</span></span>|<span data-ttu-id="fbf86-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fbf86-131">Key of the setting.</span></span>|
|<span data-ttu-id="fbf86-132">objetivo</span><span class="sxs-lookup"><span data-stu-id="fbf86-132">intent</span></span>|<span data-ttu-id="fbf86-133">String</span><span class="sxs-lookup"><span data-stu-id="fbf86-133">String</span></span>|<span data-ttu-id="fbf86-134">El objetivo de instalación definido por el administrador. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="fbf86-134">The install intent defined by the admin. Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|
|<span data-ttu-id="fbf86-135">target</span><span class="sxs-lookup"><span data-stu-id="fbf86-135">target</span></span>|[<span data-ttu-id="fbf86-136">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="fbf86-136">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_apps_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="fbf86-137">La asignación de grupo de destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="fbf86-137">The target group assignment defined by the admin.</span></span>|
|<span data-ttu-id="fbf86-138">configuración</span><span class="sxs-lookup"><span data-stu-id="fbf86-138">settings</span></span>|[<span data-ttu-id="fbf86-139">mobileAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="fbf86-139">mobileAppAssignmentSettings</span></span>](../resources/intune_apps_mobileappassignmentsettings.md)|<span data-ttu-id="fbf86-140">La asignación de la configuración para el destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="fbf86-140">The settings for target assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="fbf86-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbf86-141">Response</span></span>
<span data-ttu-id="fbf86-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbf86-142">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_mobileappassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fbf86-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fbf86-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="fbf86-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fbf86-144">Request</span></span>
<span data-ttu-id="fbf86-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbf86-145">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/assignments
Content-type: application/json
Content-length: 273

{
  "@odata.type": "#microsoft.graph.mobileAppAssignment",
  "intent": "required",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "settings": {
    "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
  }
}
```

### <a name="response"></a><span data-ttu-id="fbf86-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbf86-146">Response</span></span>
<span data-ttu-id="fbf86-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fbf86-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 322

{
  "@odata.type": "#microsoft.graph.mobileAppAssignment",
  "id": "591620b7-20b7-5916-b720-1659b7201659",
  "intent": "required",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "settings": {
    "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
  }
}
```




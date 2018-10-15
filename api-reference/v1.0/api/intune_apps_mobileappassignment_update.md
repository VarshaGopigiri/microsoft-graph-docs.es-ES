# <a name="update-mobileappassignment"></a><span data-ttu-id="5f93c-101">Actualizar mobileAppAssignment</span><span class="sxs-lookup"><span data-stu-id="5f93c-101">Update mobileAppAssignment</span></span>

> <span data-ttu-id="5f93c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5f93c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5f93c-103">Actualice las propiedades de un objeto [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="5f93c-103">Update the properties of a [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5f93c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5f93c-104">Prerequisites</span></span>
<span data-ttu-id="5f93c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5f93c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5f93c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f93c-107">Permission type</span></span>|<span data-ttu-id="5f93c-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f93c-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5f93c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f93c-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5f93c-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f93c-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5f93c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f93c-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5f93c-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f93c-112">Not supported.</span></span>|
|<span data-ttu-id="5f93c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f93c-113">Application</span></span>|<span data-ttu-id="5f93c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f93c-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5f93c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f93c-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/assignments/{mobileAppAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="5f93c-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f93c-116">Request headers</span></span>
|<span data-ttu-id="5f93c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f93c-117">Header</span></span>|<span data-ttu-id="5f93c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5f93c-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5f93c-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f93c-119">Authorization</span></span>|<span data-ttu-id="5f93c-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5f93c-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5f93c-121">Accept</span><span class="sxs-lookup"><span data-stu-id="5f93c-121">Accept</span></span>|<span data-ttu-id="5f93c-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5f93c-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5f93c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f93c-123">Request body</span></span>
<span data-ttu-id="5f93c-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="5f93c-124">In the request body, supply a JSON representation for the [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) object.</span></span>

<span data-ttu-id="5f93c-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).</span><span class="sxs-lookup"><span data-stu-id="5f93c-125">The following table shows the properties that are required when you create the [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md).</span></span>

|<span data-ttu-id="5f93c-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f93c-126">Property</span></span>|<span data-ttu-id="5f93c-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f93c-127">Type</span></span>|<span data-ttu-id="5f93c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f93c-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5f93c-129">id</span><span class="sxs-lookup"><span data-stu-id="5f93c-129">id</span></span>|<span data-ttu-id="5f93c-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f93c-130">String</span></span>|<span data-ttu-id="5f93c-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5f93c-131">Key of the entity.</span></span>|
|<span data-ttu-id="5f93c-132">intent</span><span class="sxs-lookup"><span data-stu-id="5f93c-132">intent</span></span>|[<span data-ttu-id="5f93c-133">installIntent</span><span class="sxs-lookup"><span data-stu-id="5f93c-133">installIntent</span></span>](../resources/intune_shared_installintent.md)|<span data-ttu-id="5f93c-134">El objetivo de instalación definido por el administrador. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="5f93c-134">The install intent defined by the admin. Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|
|<span data-ttu-id="5f93c-135">target</span><span class="sxs-lookup"><span data-stu-id="5f93c-135">target</span></span>|[<span data-ttu-id="5f93c-136">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="5f93c-136">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="5f93c-137">La asignación de grupo de destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="5f93c-137">The target group assignment defined by the admin.</span></span>|
|<span data-ttu-id="5f93c-138">settings</span><span class="sxs-lookup"><span data-stu-id="5f93c-138">settings</span></span>|[<span data-ttu-id="5f93c-139">mobileAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="5f93c-139">mobileAppAssignmentSettings</span></span>](../resources/intune_apps_mobileappassignmentsettings.md)|<span data-ttu-id="5f93c-140">La asignación de la configuración para el destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="5f93c-140">The settings for target assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="5f93c-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f93c-141">Response</span></span>
<span data-ttu-id="5f93c-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f93c-142">If successful, this method returns a `200 OK` response code and an updated [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5f93c-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f93c-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="5f93c-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f93c-144">Request</span></span>
<span data-ttu-id="5f93c-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f93c-145">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/assignments/{mobileAppAssignmentId}
Content-type: application/json
Content-length: 215

{
  "intent": "required",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "settings": {
    "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
  }
}
```

### <a name="response"></a><span data-ttu-id="5f93c-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f93c-146">Response</span></span>
<span data-ttu-id="5f93c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5f93c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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









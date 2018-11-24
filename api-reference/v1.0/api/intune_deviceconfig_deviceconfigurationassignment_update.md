# <a name="update-deviceconfigurationassignment"></a><span data-ttu-id="3fafe-101">Actualizar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="3fafe-101">Update deviceConfigurationAssignment</span></span>

> <span data-ttu-id="3fafe-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3fafe-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3fafe-103">Actualice las propiedades de un objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="3fafe-103">Update the properties of a [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3fafe-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3fafe-104">Prerequisites</span></span>
<span data-ttu-id="3fafe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3fafe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3fafe-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3fafe-107">Permission type</span></span>|<span data-ttu-id="3fafe-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3fafe-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3fafe-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3fafe-109">Delegated (work or school account)</span></span>|<span data-ttu-id="3fafe-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3fafe-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="3fafe-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3fafe-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3fafe-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3fafe-112">Not supported.</span></span>|
|<span data-ttu-id="3fafe-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3fafe-113">Application</span></span>|<span data-ttu-id="3fafe-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3fafe-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3fafe-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3fafe-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments/{deviceConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="3fafe-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3fafe-116">Request headers</span></span>
|<span data-ttu-id="3fafe-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fafe-117">Header</span></span>|<span data-ttu-id="3fafe-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3fafe-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3fafe-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="3fafe-119">Authorization</span></span>|<span data-ttu-id="3fafe-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3fafe-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3fafe-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3fafe-121">Accept</span></span>|<span data-ttu-id="3fafe-122">application/json</span><span class="sxs-lookup"><span data-stu-id="3fafe-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3fafe-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3fafe-123">Request body</span></span>
<span data-ttu-id="3fafe-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="3fafe-124">In the request body, supply a JSON representation for the [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) object.</span></span>

<span data-ttu-id="3fafe-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="3fafe-125">The following table shows the properties that are required when you create the [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md).</span></span>

|<span data-ttu-id="3fafe-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3fafe-126">Property</span></span>|<span data-ttu-id="3fafe-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fafe-127">Type</span></span>|<span data-ttu-id="3fafe-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fafe-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3fafe-129">id</span><span class="sxs-lookup"><span data-stu-id="3fafe-129">id</span></span>|<span data-ttu-id="3fafe-130">String</span><span class="sxs-lookup"><span data-stu-id="3fafe-130">String</span></span>|<span data-ttu-id="3fafe-131">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="3fafe-131">The key of the assignment.</span></span>|
|<span data-ttu-id="3fafe-132">target</span><span class="sxs-lookup"><span data-stu-id="3fafe-132">target</span></span>|[<span data-ttu-id="3fafe-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="3fafe-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="3fafe-134">El destino de la tarea para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3fafe-134">The assignment target for the device configuration.</span></span>|



## <a name="response"></a><span data-ttu-id="3fafe-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3fafe-135">Response</span></span>
<span data-ttu-id="3fafe-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3fafe-136">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3fafe-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3fafe-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="3fafe-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3fafe-138">Request</span></span>
<span data-ttu-id="3fafe-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3fafe-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments/{deviceConfigurationAssignmentId}
Content-type: application/json
Content-length: 169

{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="3fafe-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3fafe-140">Response</span></span>
<span data-ttu-id="3fafe-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3fafe-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 218

{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "id": "d59b6342-6342-d59b-4263-9bd542639bd5",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```




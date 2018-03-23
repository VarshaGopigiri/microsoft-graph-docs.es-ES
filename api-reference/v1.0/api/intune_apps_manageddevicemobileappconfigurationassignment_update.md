# <a name="update-manageddevicemobileappconfigurationassignment"></a><span data-ttu-id="1b22b-101">Actualizar managedDeviceMobileAppConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="1b22b-101">Update managedDeviceMobileAppConfigurationAssignment</span></span>

> <span data-ttu-id="1b22b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1b22b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1b22b-103">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="1b22b-103">Update the properties of a [calendar](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1b22b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1b22b-104">Prerequisites</span></span>
<span data-ttu-id="1b22b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1b22b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1b22b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1b22b-107">Permission type</span></span>|<span data-ttu-id="1b22b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1b22b-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1b22b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1b22b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="1b22b-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1b22b-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1b22b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1b22b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1b22b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b22b-112">Not supported.</span></span>|
|<span data-ttu-id="1b22b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1b22b-113">Application</span></span>|<span data-ttu-id="1b22b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b22b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1b22b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b22b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assignments/{managedDeviceMobileAppConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="1b22b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b22b-116">Request headers</span></span>
|<span data-ttu-id="1b22b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b22b-117">Header</span></span>|<span data-ttu-id="1b22b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1b22b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1b22b-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="1b22b-119">Authorization</span></span>|<span data-ttu-id="1b22b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1b22b-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="1b22b-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1b22b-121">Accept</span></span>|<span data-ttu-id="1b22b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="1b22b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1b22b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1b22b-123">Request body</span></span>
<span data-ttu-id="1b22b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="1b22b-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md) object.</span></span>

<span data-ttu-id="1b22b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="1b22b-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="1b22b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1b22b-126">Property</span></span>|<span data-ttu-id="1b22b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b22b-127">Type</span></span>|<span data-ttu-id="1b22b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b22b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1b22b-129">id</span><span class="sxs-lookup"><span data-stu-id="1b22b-129">id</span></span>|<span data-ttu-id="1b22b-130">String</span><span class="sxs-lookup"><span data-stu-id="1b22b-130">String</span></span>|<span data-ttu-id="1b22b-131">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1b22b-131">Unique identifier of the folder.</span></span>|
|<span data-ttu-id="1b22b-132">target</span><span class="sxs-lookup"><span data-stu-id="1b22b-132">target</span></span>|[<span data-ttu-id="1b22b-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="1b22b-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_apps_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="1b22b-134">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="1b22b-134">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="1b22b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b22b-135">Response</span></span>
<span data-ttu-id="1b22b-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b22b-136">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_apps_manageddevicemobileappconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1b22b-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b22b-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="1b22b-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b22b-138">Request</span></span>
<span data-ttu-id="1b22b-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b22b-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assignments/{managedDeviceMobileAppConfigurationAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="1b22b-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b22b-140">Response</span></span>
<span data-ttu-id="1b22b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1b22b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 234

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationAssignment",
  "id": "4df81c9c-1c9c-4df8-9c1c-f84d9c1cf84d",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```




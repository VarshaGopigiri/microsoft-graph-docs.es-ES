# <a name="update-enrollmentconfigurationassignment"></a><span data-ttu-id="e6488-101">Actualizar enrollmentConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e6488-101">Update enrollmentConfigurationAssignment</span></span>

> <span data-ttu-id="e6488-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6488-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6488-103">Actualice las propiedades de un objeto [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e6488-103">Update the properties of a [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e6488-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e6488-104">Prerequisites</span></span>
<span data-ttu-id="e6488-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e6488-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e6488-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6488-107">Permission type</span></span>|<span data-ttu-id="e6488-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6488-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e6488-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6488-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e6488-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6488-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="e6488-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6488-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e6488-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6488-112">Not supported.</span></span>|
|<span data-ttu-id="e6488-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6488-113">Application</span></span>|<span data-ttu-id="e6488-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6488-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e6488-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6488-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments/{enrollmentConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="e6488-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6488-116">Request headers</span></span>
|<span data-ttu-id="e6488-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6488-117">Header</span></span>|<span data-ttu-id="e6488-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e6488-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e6488-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="e6488-119">Authorization</span></span>|<span data-ttu-id="e6488-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e6488-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e6488-121">Accept</span><span class="sxs-lookup"><span data-stu-id="e6488-121">Accept</span></span>|<span data-ttu-id="e6488-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e6488-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6488-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6488-123">Request body</span></span>
<span data-ttu-id="e6488-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e6488-124">In the request body, supply a JSON representation for the [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md) object.</span></span>

<span data-ttu-id="e6488-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="e6488-125">The following table shows the properties that are required when you create the [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).</span></span>

|<span data-ttu-id="e6488-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6488-126">Property</span></span>|<span data-ttu-id="e6488-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6488-127">Type</span></span>|<span data-ttu-id="e6488-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6488-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e6488-129">id</span><span class="sxs-lookup"><span data-stu-id="e6488-129">id</span></span>|<span data-ttu-id="e6488-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6488-130">String</span></span>|<span data-ttu-id="e6488-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e6488-131">Not yet documented</span></span>|
|<span data-ttu-id="e6488-132">target</span><span class="sxs-lookup"><span data-stu-id="e6488-132">target</span></span>|[<span data-ttu-id="e6488-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="e6488-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="e6488-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e6488-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="e6488-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6488-135">Response</span></span>
<span data-ttu-id="e6488-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6488-136">If successful, this method returns a `200 OK` response code and an updated [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e6488-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6488-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="e6488-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6488-138">Request</span></span>
<span data-ttu-id="e6488-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6488-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments/{enrollmentConfigurationAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="e6488-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6488-140">Response</span></span>
<span data-ttu-id="e6488-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6488-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 222

{
  "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
  "id": "705b021c-021c-705b-1c02-5b701c025b70",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```









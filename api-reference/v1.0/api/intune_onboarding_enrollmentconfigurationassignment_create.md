# <a name="create-enrollmentconfigurationassignment"></a><span data-ttu-id="4be71-101">Crear enrollmentConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="4be71-101">Create enrollmentConfigurationAssignment</span></span>

> <span data-ttu-id="4be71-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4be71-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4be71-103">Cree un objeto [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="4be71-103">Create a new [plannerBucket](../resources/intune_onboarding_enrollmentconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4be71-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4be71-104">Prerequisites</span></span>
<span data-ttu-id="4be71-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4be71-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4be71-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4be71-107">Permission type</span></span>|<span data-ttu-id="4be71-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4be71-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4be71-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4be71-109">Delegated (work or school account)</span></span>|<span data-ttu-id="4be71-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4be71-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="4be71-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4be71-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4be71-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4be71-112">Not supported.</span></span>|
|<span data-ttu-id="4be71-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4be71-113">Application</span></span>|<span data-ttu-id="4be71-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4be71-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4be71-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4be71-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="4be71-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4be71-116">Request headers</span></span>
|<span data-ttu-id="4be71-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4be71-117">Header</span></span>|<span data-ttu-id="4be71-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4be71-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4be71-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="4be71-119">Authorization</span></span>|<span data-ttu-id="4be71-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4be71-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="4be71-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4be71-121">Accept</span></span>|<span data-ttu-id="4be71-122">application/json</span><span class="sxs-lookup"><span data-stu-id="4be71-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4be71-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4be71-123">Request body</span></span>
<span data-ttu-id="4be71-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto enrollmentConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="4be71-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="4be71-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto enrollmentConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="4be71-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="4be71-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4be71-126">Property</span></span>|<span data-ttu-id="4be71-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="4be71-127">Type</span></span>|<span data-ttu-id="4be71-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="4be71-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4be71-129">id</span><span class="sxs-lookup"><span data-stu-id="4be71-129">id</span></span>|<span data-ttu-id="4be71-130">String</span><span class="sxs-lookup"><span data-stu-id="4be71-130">String</span></span>|<span data-ttu-id="4be71-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4be71-131">Not yet documented</span></span>|
|<span data-ttu-id="4be71-132">target</span><span class="sxs-lookup"><span data-stu-id="4be71-132">target</span></span>|[<span data-ttu-id="4be71-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="4be71-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_onboarding_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="4be71-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4be71-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="4be71-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4be71-135">Response</span></span>
<span data-ttu-id="4be71-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4be71-136">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_onboarding_enrollmentconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4be71-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4be71-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="4be71-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4be71-138">Request</span></span>
<span data-ttu-id="4be71-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4be71-139">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments
Content-type: application/json
Content-length: 173

{
  "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="4be71-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4be71-140">Response</span></span>
<span data-ttu-id="4be71-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4be71-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




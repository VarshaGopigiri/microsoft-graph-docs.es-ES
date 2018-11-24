# <a name="update-targetedmanagedapppolicyassignment"></a><span data-ttu-id="609e3-101">Actualizar targetedManagedAppPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="609e3-101">Update targetedManagedAppPolicyAssignment</span></span>

> <span data-ttu-id="609e3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="609e3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="609e3-103">Actualice las propiedades de un objeto [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="609e3-103">Update the properties of a [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="609e3-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="609e3-104">Prerequisites</span></span>
<span data-ttu-id="609e3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="609e3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="609e3-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="609e3-107">Permission type</span></span>|<span data-ttu-id="609e3-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="609e3-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="609e3-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="609e3-109">Delegated (work or school account)</span></span>|<span data-ttu-id="609e3-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="609e3-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="609e3-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="609e3-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="609e3-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="609e3-112">Not supported.</span></span>|
|<span data-ttu-id="609e3-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="609e3-113">Application</span></span>|<span data-ttu-id="609e3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="609e3-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="609e3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="609e3-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
PATCH /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
PATCH /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/assignments/{targetedManagedAppPolicyAssignmentId}
PATCH /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/assignments/{targetedManagedAppPolicyAssignmentId}
PATCH /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/assignments/{targetedManagedAppPolicyAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="609e3-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="609e3-116">Request headers</span></span>
|<span data-ttu-id="609e3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="609e3-117">Header</span></span>|<span data-ttu-id="609e3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="609e3-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="609e3-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="609e3-119">Authorization</span></span>|<span data-ttu-id="609e3-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="609e3-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="609e3-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="609e3-121">Accept</span></span>|<span data-ttu-id="609e3-122">application/json</span><span class="sxs-lookup"><span data-stu-id="609e3-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="609e3-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="609e3-123">Request body</span></span>
<span data-ttu-id="609e3-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="609e3-124">In the request body, supply a JSON representation for the [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md) object.</span></span>

<span data-ttu-id="609e3-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="609e3-125">The following table shows the properties that are required when you create the [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md).</span></span>

|<span data-ttu-id="609e3-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="609e3-126">Property</span></span>|<span data-ttu-id="609e3-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="609e3-127">Type</span></span>|<span data-ttu-id="609e3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="609e3-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="609e3-129">id</span><span class="sxs-lookup"><span data-stu-id="609e3-129">id</span></span>|<span data-ttu-id="609e3-130">String</span><span class="sxs-lookup"><span data-stu-id="609e3-130">String</span></span>|<span data-ttu-id="609e3-131">Id</span><span class="sxs-lookup"><span data-stu-id="609e3-131">Id</span></span>|
|<span data-ttu-id="609e3-132">target</span><span class="sxs-lookup"><span data-stu-id="609e3-132">target</span></span>|[<span data-ttu-id="609e3-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="609e3-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="609e3-134">Identificador para la implementación de un grupo o una aplicación</span><span class="sxs-lookup"><span data-stu-id="609e3-134">Identifier for deployment of a group or app</span></span>|



## <a name="response"></a><span data-ttu-id="609e3-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="609e3-135">Response</span></span>
<span data-ttu-id="609e3-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="609e3-136">If successful, this method returns a `200 OK` response code and an updated [targetedManagedAppPolicyAssignment](../resources/intune_mam_targetedmanagedapppolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="609e3-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="609e3-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="609e3-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="609e3-138">Request</span></span>
<span data-ttu-id="609e3-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="609e3-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/assignments/{targetedManagedAppPolicyAssignmentId}
Content-type: application/json
Content-length: 174

{
  "@odata.type": "#microsoft.graph.targetedManagedAppPolicyAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="609e3-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="609e3-140">Response</span></span>
<span data-ttu-id="609e3-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="609e3-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 223

{
  "@odata.type": "#microsoft.graph.targetedManagedAppPolicyAssignment",
  "id": "8b68c4a6-c4a6-8b68-a6c4-688ba6c4688b",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```




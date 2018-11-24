# <a name="update-termsandconditionsassignment"></a><span data-ttu-id="9bfe1-101">Actualizar termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="9bfe1-101">Update termsAndConditionsAssignment</span></span>

> <span data-ttu-id="9bfe1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9bfe1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9bfe1-103">Actualice las propiedades de un objeto [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="9bfe1-103">Update the properties of a [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9bfe1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9bfe1-104">Prerequisites</span></span>
<span data-ttu-id="9bfe1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9bfe1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9bfe1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9bfe1-107">Permission type</span></span>|<span data-ttu-id="9bfe1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9bfe1-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9bfe1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9bfe1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="9bfe1-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9bfe1-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="9bfe1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9bfe1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9bfe1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9bfe1-112">Not supported.</span></span>|
|<span data-ttu-id="9bfe1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9bfe1-113">Application</span></span>|<span data-ttu-id="9bfe1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9bfe1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9bfe1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9bfe1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="9bfe1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9bfe1-116">Request headers</span></span>
|<span data-ttu-id="9bfe1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9bfe1-117">Header</span></span>|<span data-ttu-id="9bfe1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9bfe1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9bfe1-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="9bfe1-119">Authorization</span></span>|<span data-ttu-id="9bfe1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9bfe1-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9bfe1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9bfe1-121">Accept</span></span>|<span data-ttu-id="9bfe1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="9bfe1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9bfe1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9bfe1-123">Request body</span></span>
<span data-ttu-id="9bfe1-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="9bfe1-124">In the request body, supply a JSON representation for the [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md) object.</span></span>

<span data-ttu-id="9bfe1-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="9bfe1-125">The following table shows the properties that are required when you create the [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md).</span></span>

|<span data-ttu-id="9bfe1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9bfe1-126">Property</span></span>|<span data-ttu-id="9bfe1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bfe1-127">Type</span></span>|<span data-ttu-id="9bfe1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bfe1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9bfe1-129">id</span><span class="sxs-lookup"><span data-stu-id="9bfe1-129">id</span></span>|<span data-ttu-id="9bfe1-130">String</span><span class="sxs-lookup"><span data-stu-id="9bfe1-130">String</span></span>|<span data-ttu-id="9bfe1-131">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9bfe1-131">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="9bfe1-132">target</span><span class="sxs-lookup"><span data-stu-id="9bfe1-132">target</span></span>|[<span data-ttu-id="9bfe1-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="9bfe1-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="9bfe1-134">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="9bfe1-134">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="9bfe1-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9bfe1-135">Response</span></span>
<span data-ttu-id="9bfe1-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9bfe1-136">If successful, this method returns a `200 OK` response code and an updated [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9bfe1-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9bfe1-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="9bfe1-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9bfe1-138">Request</span></span>
<span data-ttu-id="9bfe1-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9bfe1-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
Content-type: application/json
Content-length: 168

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="9bfe1-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9bfe1-140">Response</span></span>
<span data-ttu-id="9bfe1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9bfe1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 217

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "id": "64c1a196-a196-64c1-96a1-c16496a1c164",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```




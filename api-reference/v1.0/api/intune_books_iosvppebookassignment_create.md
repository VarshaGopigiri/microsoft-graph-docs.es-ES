# <a name="create-iosvppebookassignment"></a><span data-ttu-id="4a8a1-101">Crear iosVppEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="4a8a1-101">Create iosVppEBookAssignment</span></span>

> <span data-ttu-id="4a8a1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4a8a1-103">Cree un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="4a8a1-103">Create a new [plannerBucket](../resources/intune_books_iosvppebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4a8a1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4a8a1-104">Prerequisites</span></span>
<span data-ttu-id="4a8a1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4a8a1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4a8a1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a8a1-107">Permission type</span></span>|<span data-ttu-id="4a8a1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a8a1-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4a8a1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a8a1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="4a8a1-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a8a1-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="4a8a1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a8a1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4a8a1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-112">Not supported.</span></span>|
|<span data-ttu-id="4a8a1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a8a1-113">Application</span></span>|<span data-ttu-id="4a8a1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4a8a1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a8a1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="4a8a1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4a8a1-116">Request headers</span></span>
|<span data-ttu-id="4a8a1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a8a1-117">Header</span></span>|<span data-ttu-id="4a8a1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4a8a1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4a8a1-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="4a8a1-119">Authorization</span></span>|<span data-ttu-id="4a8a1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="4a8a1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4a8a1-121">Accept</span></span>|<span data-ttu-id="4a8a1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="4a8a1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4a8a1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a8a1-123">Request body</span></span>
<span data-ttu-id="4a8a1-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="4a8a1-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="4a8a1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a8a1-126">Property</span></span>|<span data-ttu-id="4a8a1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a8a1-127">Type</span></span>|<span data-ttu-id="4a8a1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a8a1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4a8a1-129">id</span><span class="sxs-lookup"><span data-stu-id="4a8a1-129">id</span></span>|<span data-ttu-id="4a8a1-130">String</span><span class="sxs-lookup"><span data-stu-id="4a8a1-130">String</span></span>|<span data-ttu-id="4a8a1-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-131">Key of the setting.</span></span> <span data-ttu-id="4a8a1-132">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="4a8a1-132">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span></span>|
|<span data-ttu-id="4a8a1-133">target</span><span class="sxs-lookup"><span data-stu-id="4a8a1-133">target</span></span>|[<span data-ttu-id="4a8a1-134">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="4a8a1-134">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_books_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="4a8a1-135">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-135">The assignment target for eBook.</span></span> <span data-ttu-id="4a8a1-136">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="4a8a1-136">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span></span>|
|<span data-ttu-id="4a8a1-137">installIntent</span><span class="sxs-lookup"><span data-stu-id="4a8a1-137">installIntent</span></span>|<span data-ttu-id="4a8a1-138">String</span><span class="sxs-lookup"><span data-stu-id="4a8a1-138">String</span></span>|<span data-ttu-id="4a8a1-139">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-139">The install intent for eBook.</span></span> <span data-ttu-id="4a8a1-140">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md). Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-140">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="4a8a1-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a8a1-141">Response</span></span>
<span data-ttu-id="4a8a1-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-142">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_books_iosvppebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4a8a1-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a8a1-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="4a8a1-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4a8a1-144">Request</span></span>
<span data-ttu-id="4a8a1-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-145">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
Content-type: application/json
Content-length: 193

{
  "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```

### <a name="response"></a><span data-ttu-id="4a8a1-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a8a1-146">Response</span></span>
<span data-ttu-id="4a8a1-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4a8a1-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 242

{
  "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
  "id": "48f05789-5789-48f0-8957-f0488957f048",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```




# <a name="create-iosvppebookassignment"></a><span data-ttu-id="70a02-101">Crear iosVppEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="70a02-101">Create iosVppEBookAssignment</span></span>

> <span data-ttu-id="70a02-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="70a02-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="70a02-103">Cree un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="70a02-103">Create a new [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="70a02-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="70a02-104">Prerequisites</span></span>
<span data-ttu-id="70a02-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="70a02-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="70a02-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70a02-107">Permission type</span></span>|<span data-ttu-id="70a02-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70a02-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="70a02-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70a02-109">Delegated (work or school account)</span></span>|<span data-ttu-id="70a02-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="70a02-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="70a02-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70a02-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="70a02-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70a02-112">Not supported.</span></span>|
|<span data-ttu-id="70a02-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70a02-113">Application</span></span>|<span data-ttu-id="70a02-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70a02-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="70a02-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70a02-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="70a02-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70a02-116">Request headers</span></span>
|<span data-ttu-id="70a02-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70a02-117">Header</span></span>|<span data-ttu-id="70a02-118">Valor</span><span class="sxs-lookup"><span data-stu-id="70a02-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="70a02-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="70a02-119">Authorization</span></span>|<span data-ttu-id="70a02-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="70a02-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="70a02-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="70a02-121">Accept</span></span>|<span data-ttu-id="70a02-122">application/json</span><span class="sxs-lookup"><span data-stu-id="70a02-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="70a02-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70a02-123">Request body</span></span>
<span data-ttu-id="70a02-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="70a02-124">In the request body, supply a JSON representation for the iosVppEBookAssignment object.</span></span>

<span data-ttu-id="70a02-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="70a02-125">The following table shows the properties that are required when you create the iosVppEBookAssignment.</span></span>

|<span data-ttu-id="70a02-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="70a02-126">Property</span></span>|<span data-ttu-id="70a02-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="70a02-127">Type</span></span>|<span data-ttu-id="70a02-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="70a02-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="70a02-129">id</span><span class="sxs-lookup"><span data-stu-id="70a02-129">id</span></span>|<span data-ttu-id="70a02-130">String</span><span class="sxs-lookup"><span data-stu-id="70a02-130">String</span></span>|<span data-ttu-id="70a02-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="70a02-131">Key of the entity.</span></span> <span data-ttu-id="70a02-132">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="70a02-132">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span></span>|
|<span data-ttu-id="70a02-133">target</span><span class="sxs-lookup"><span data-stu-id="70a02-133">target</span></span>|[<span data-ttu-id="70a02-134">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="70a02-134">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="70a02-135">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="70a02-135">The assignment target for eBook.</span></span> <span data-ttu-id="70a02-136">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="70a02-136">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span></span>|
|<span data-ttu-id="70a02-137">installIntent</span><span class="sxs-lookup"><span data-stu-id="70a02-137">installIntent</span></span>|[<span data-ttu-id="70a02-138">installIntent</span><span class="sxs-lookup"><span data-stu-id="70a02-138">installIntent</span></span>](../resources/intune_shared_installintent.md)|<span data-ttu-id="70a02-139">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="70a02-139">The install intent for eBook.</span></span> <span data-ttu-id="70a02-140">Se hereda de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="70a02-140">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).</span></span> <span data-ttu-id="70a02-141">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="70a02-141">Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="70a02-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70a02-142">Response</span></span>
<span data-ttu-id="70a02-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70a02-143">If successful, this method returns a `201 Created` response code and a [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="70a02-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70a02-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="70a02-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70a02-145">Request</span></span>
<span data-ttu-id="70a02-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70a02-146">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="70a02-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70a02-147">Response</span></span>
<span data-ttu-id="70a02-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70a02-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




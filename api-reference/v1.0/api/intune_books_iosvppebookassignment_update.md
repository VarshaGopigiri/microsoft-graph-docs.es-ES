# <a name="update-iosvppebookassignment"></a><span data-ttu-id="fd61a-101">Actualizar iosVppEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="fd61a-101">Update iosVppEBookAssignment</span></span>

> <span data-ttu-id="fd61a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fd61a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fd61a-103">Actualice las propiedades de un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="fd61a-103">Update the properties of a [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fd61a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fd61a-104">Prerequisites</span></span>
<span data-ttu-id="fd61a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fd61a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fd61a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fd61a-107">Permission type</span></span>|<span data-ttu-id="fd61a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fd61a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fd61a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fd61a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="fd61a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fd61a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="fd61a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fd61a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fd61a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd61a-112">Not supported.</span></span>|
|<span data-ttu-id="fd61a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fd61a-113">Application</span></span>|<span data-ttu-id="fd61a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd61a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fd61a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fd61a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="fd61a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fd61a-116">Request headers</span></span>
|<span data-ttu-id="fd61a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd61a-117">Header</span></span>|<span data-ttu-id="fd61a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fd61a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fd61a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="fd61a-119">Authorization</span></span>|<span data-ttu-id="fd61a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fd61a-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fd61a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fd61a-121">Accept</span></span>|<span data-ttu-id="fd61a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="fd61a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fd61a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fd61a-123">Request body</span></span>
<span data-ttu-id="fd61a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="fd61a-124">In the request body, supply a JSON representation for the [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object.</span></span>

<span data-ttu-id="fd61a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="fd61a-125">The following table shows the properties that are required when you create the [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span></span>

|<span data-ttu-id="fd61a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fd61a-126">Property</span></span>|<span data-ttu-id="fd61a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd61a-127">Type</span></span>|<span data-ttu-id="fd61a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd61a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fd61a-129">id</span><span class="sxs-lookup"><span data-stu-id="fd61a-129">id</span></span>|<span data-ttu-id="fd61a-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="fd61a-130">String</span></span>|<span data-ttu-id="fd61a-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fd61a-131">Key of the entity.</span></span> <span data-ttu-id="fd61a-132">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="fd61a-132">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span></span>|
|<span data-ttu-id="fd61a-133">target</span><span class="sxs-lookup"><span data-stu-id="fd61a-133">target</span></span>|[<span data-ttu-id="fd61a-134">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="fd61a-134">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="fd61a-135">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="fd61a-135">The assignment target for eBook.</span></span> <span data-ttu-id="fd61a-136">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="fd61a-136">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span></span>|
|<span data-ttu-id="fd61a-137">installIntent</span><span class="sxs-lookup"><span data-stu-id="fd61a-137">installIntent</span></span>|[<span data-ttu-id="fd61a-138">installIntent</span><span class="sxs-lookup"><span data-stu-id="fd61a-138">installIntent</span></span>](../resources/intune_shared_installintent.md)|<span data-ttu-id="fd61a-p104">La intención de instalación para el libro electrónico. Se hereda de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md). Los valores posibles son: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="fd61a-p104">The install intent for eBook. Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md). The possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="fd61a-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd61a-142">Response</span></span>
<span data-ttu-id="fd61a-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fd61a-143">If successful, this method returns a `200 OK` response code and an updated [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fd61a-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fd61a-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="fd61a-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fd61a-145">Request</span></span>
<span data-ttu-id="fd61a-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fd61a-146">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
Content-type: application/json
Content-length: 133

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```

### <a name="response"></a><span data-ttu-id="fd61a-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd61a-147">Response</span></span>
<span data-ttu-id="fd61a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fd61a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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









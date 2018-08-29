# <a name="update-iosvppebookassignment"></a><span data-ttu-id="9b882-101">Actualizar iosVppEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="9b882-101">Update iosVppEBookAssignment</span></span>

> <span data-ttu-id="9b882-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b882-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b882-103">Actualice las propiedades de un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="9b882-103">Update the properties of a [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9b882-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9b882-104">Prerequisites</span></span>
<span data-ttu-id="9b882-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9b882-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9b882-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b882-107">Permission type</span></span>|<span data-ttu-id="9b882-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b882-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9b882-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b882-109">Delegated (work or school account)</span></span>|<span data-ttu-id="9b882-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b882-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9b882-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b882-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9b882-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b882-112">Not supported.</span></span>|
|<span data-ttu-id="9b882-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b882-113">Application</span></span>|<span data-ttu-id="9b882-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b882-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9b882-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b882-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="9b882-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b882-116">Request headers</span></span>
|<span data-ttu-id="9b882-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b882-117">Header</span></span>|<span data-ttu-id="9b882-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9b882-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9b882-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b882-119">Authorization</span></span>|<span data-ttu-id="9b882-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9b882-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9b882-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9b882-121">Accept</span></span>|<span data-ttu-id="9b882-122">application/json</span><span class="sxs-lookup"><span data-stu-id="9b882-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9b882-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b882-123">Request body</span></span>
<span data-ttu-id="9b882-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="9b882-124">In the request body, supply a JSON representation for the [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object.</span></span>

<span data-ttu-id="9b882-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="9b882-125">The following table shows the properties that are required when you create the [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md).</span></span>

|<span data-ttu-id="9b882-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b882-126">Property</span></span>|<span data-ttu-id="9b882-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b882-127">Type</span></span>|<span data-ttu-id="9b882-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b882-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9b882-129">id</span><span class="sxs-lookup"><span data-stu-id="9b882-129">id</span></span>|<span data-ttu-id="9b882-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="9b882-130">String</span></span>|<span data-ttu-id="9b882-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9b882-131">Key of the entity.</span></span> <span data-ttu-id="9b882-132">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="9b882-132">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span></span>|
|<span data-ttu-id="9b882-133">target</span><span class="sxs-lookup"><span data-stu-id="9b882-133">target</span></span>|[<span data-ttu-id="9b882-134">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="9b882-134">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="9b882-135">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="9b882-135">The assignment target for eBook.</span></span> <span data-ttu-id="9b882-136">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="9b882-136">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span></span>|
|<span data-ttu-id="9b882-137">installIntent</span><span class="sxs-lookup"><span data-stu-id="9b882-137">installIntent</span></span>|[<span data-ttu-id="9b882-138">installIntent</span><span class="sxs-lookup"><span data-stu-id="9b882-138">installIntent</span></span>](../resources/intune_shared_installintent.md)|<span data-ttu-id="9b882-139">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="9b882-139">The install intent for eBook.</span></span> <span data-ttu-id="9b882-140">Heredado de [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="9b882-140">Inherited from [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span></span> <span data-ttu-id="9b882-141">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="9b882-141">The possible values are `available`, `required`, `uninstall`, `availableWithoutEnrollment`, , , , , , , , or .</span></span>|



## <a name="response"></a><span data-ttu-id="9b882-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b882-142">Response</span></span>
<span data-ttu-id="9b882-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b882-143">If successful, this method returns a `200 OK` response code and an updated [iosVppEBookAssignment](../resources/intune_books_iosvppebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b882-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b882-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="9b882-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b882-145">Request</span></span>
<span data-ttu-id="9b882-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b882-146">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="9b882-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b882-147">Response</span></span>
<span data-ttu-id="9b882-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b882-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




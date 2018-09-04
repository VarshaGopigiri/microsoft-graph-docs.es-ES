# <a name="update-managedebookassignment"></a><span data-ttu-id="56597-101">Actualizar managedEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="56597-101">Update managedEBookAssignment</span></span>

> <span data-ttu-id="56597-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="56597-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="56597-103">Actualice las propiedades de un objeto [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="56597-103">Update the properties of a [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="56597-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="56597-104">Prerequisites</span></span>
<span data-ttu-id="56597-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="56597-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="56597-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="56597-107">Permission type</span></span>|<span data-ttu-id="56597-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="56597-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="56597-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="56597-109">Delegated (work or school account)</span></span>|<span data-ttu-id="56597-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56597-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="56597-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56597-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="56597-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56597-112">Not supported.</span></span>|
|<span data-ttu-id="56597-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="56597-113">Application</span></span>|<span data-ttu-id="56597-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56597-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="56597-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56597-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="56597-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="56597-116">Request headers</span></span>
|<span data-ttu-id="56597-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56597-117">Header</span></span>|<span data-ttu-id="56597-118">Valor</span><span class="sxs-lookup"><span data-stu-id="56597-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="56597-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="56597-119">Authorization</span></span>|<span data-ttu-id="56597-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="56597-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="56597-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="56597-121">Accept</span></span>|<span data-ttu-id="56597-122">aplicación/json</span><span class="sxs-lookup"><span data-stu-id="56597-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="56597-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56597-123">Request body</span></span>
<span data-ttu-id="56597-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="56597-124">In the request body, supply a JSON representation for the [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) object.</span></span>

<span data-ttu-id="56597-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="56597-125">The following table shows the properties that are required when you create the [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).</span></span>

|<span data-ttu-id="56597-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56597-126">Property</span></span>|<span data-ttu-id="56597-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="56597-127">Type</span></span>|<span data-ttu-id="56597-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="56597-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56597-129">id</span><span class="sxs-lookup"><span data-stu-id="56597-129">id</span></span>|<span data-ttu-id="56597-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="56597-130">String</span></span>|<span data-ttu-id="56597-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="56597-131">Key of the entity.</span></span>|
|<span data-ttu-id="56597-132">target</span><span class="sxs-lookup"><span data-stu-id="56597-132">target</span></span>|[<span data-ttu-id="56597-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="56597-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="56597-134">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="56597-134">The assignment target for eBook.</span></span>|
|<span data-ttu-id="56597-135">installIntent</span><span class="sxs-lookup"><span data-stu-id="56597-135">installIntent</span></span>|[<span data-ttu-id="56597-136">installIntent</span><span class="sxs-lookup"><span data-stu-id="56597-136">installIntent</span></span>](../resources/intune_shared_installintent.md)|<span data-ttu-id="56597-137">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="56597-137">The install intent for eBook.</span></span> <span data-ttu-id="56597-138">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="56597-138">The possible values are `available`, `required`, `uninstall`, `availableWithoutEnrollment`, , , , , , , , or .</span></span>|



## <a name="response"></a><span data-ttu-id="56597-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56597-139">Response</span></span>
<span data-ttu-id="56597-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56597-140">If successful, this method returns a `200 OK` response code and an updated [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="56597-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56597-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="56597-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56597-142">Request</span></span>
<span data-ttu-id="56597-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56597-143">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="56597-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56597-144">Response</span></span>
<span data-ttu-id="56597-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="56597-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 243

{
  "@odata.type": "#microsoft.graph.managedEBookAssignment",
  "id": "ae8b0d27-0d27-ae8b-270d-8bae270d8bae",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```




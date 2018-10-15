# <a name="create-managedebookassignment"></a><span data-ttu-id="f062a-101">Crear managedEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="f062a-101">Create managedEBookAssignment</span></span>

> <span data-ttu-id="f062a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f062a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f062a-103">Cree un objeto [managedEBookAssignment](../resources/intune_books_managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="f062a-103">Create a new [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f062a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f062a-104">Prerequisites</span></span>
<span data-ttu-id="f062a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f062a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f062a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f062a-107">Permission type</span></span>|<span data-ttu-id="f062a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f062a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f062a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f062a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f062a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f062a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f062a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f062a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f062a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f062a-112">Not supported.</span></span>|
|<span data-ttu-id="f062a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f062a-113">Application</span></span>|<span data-ttu-id="f062a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f062a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f062a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f062a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="f062a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f062a-116">Request headers</span></span>
|<span data-ttu-id="f062a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f062a-117">Header</span></span>|<span data-ttu-id="f062a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f062a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f062a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f062a-119">Authorization</span></span>|<span data-ttu-id="f062a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f062a-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f062a-121">Accept</span><span class="sxs-lookup"><span data-stu-id="f062a-121">Accept</span></span>|<span data-ttu-id="f062a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f062a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f062a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f062a-123">Request body</span></span>
<span data-ttu-id="f062a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="f062a-124">In the request body, supply a JSON representation for the managedEBookAssignment object.</span></span>

<span data-ttu-id="f062a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="f062a-125">The following table shows the properties that are required when you create the managedEBookAssignment.</span></span>

|<span data-ttu-id="f062a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f062a-126">Property</span></span>|<span data-ttu-id="f062a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f062a-127">Type</span></span>|<span data-ttu-id="f062a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f062a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f062a-129">id</span><span class="sxs-lookup"><span data-stu-id="f062a-129">id</span></span>|<span data-ttu-id="f062a-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="f062a-130">String</span></span>|<span data-ttu-id="f062a-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f062a-131">Key of the entity.</span></span>|
|<span data-ttu-id="f062a-132">target</span><span class="sxs-lookup"><span data-stu-id="f062a-132">target</span></span>|[<span data-ttu-id="f062a-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="f062a-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="f062a-134">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="f062a-134">The assignment target for eBook.</span></span>|
|<span data-ttu-id="f062a-135">installIntent</span><span class="sxs-lookup"><span data-stu-id="f062a-135">installIntent</span></span>|[<span data-ttu-id="f062a-136">installIntent</span><span class="sxs-lookup"><span data-stu-id="f062a-136">installIntent</span></span>](../resources/intune_shared_installintent.md)|<span data-ttu-id="f062a-p102">La intención de instalación para el libro electrónico. Los valores posibles son: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="f062a-p102">The install intent for eBook. The possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="f062a-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f062a-139">Response</span></span>
<span data-ttu-id="f062a-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f062a-140">If successful, this method returns a `201 Created` response code and a [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f062a-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f062a-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="f062a-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f062a-142">Request</span></span>
<span data-ttu-id="f062a-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f062a-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
Content-type: application/json
Content-length: 194

{
  "@odata.type": "#microsoft.graph.managedEBookAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```

### <a name="response"></a><span data-ttu-id="f062a-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f062a-144">Response</span></span>
<span data-ttu-id="f062a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f062a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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









# <a name="managedebook-resource-type"></a><span data-ttu-id="46371-101">Tipo de recurso managedEBook</span><span class="sxs-lookup"><span data-stu-id="46371-101">managedEBook resource type</span></span>

> <span data-ttu-id="46371-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46371-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46371-103">Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.</span><span class="sxs-lookup"><span data-stu-id="46371-103">An abstract class containing the base properties for Managed eBook.</span></span>
## <a name="methods"></a><span data-ttu-id="46371-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="46371-104">Methods</span></span>
|<span data-ttu-id="46371-105">Método</span><span class="sxs-lookup"><span data-stu-id="46371-105">Method</span></span>|<span data-ttu-id="46371-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46371-106">Return Type</span></span>|<span data-ttu-id="46371-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="46371-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="46371-108">Enumerar managedEBooks</span><span class="sxs-lookup"><span data-stu-id="46371-108">List managedEBooks</span></span>](../api/intune_books_managedebook_list.md)|<span data-ttu-id="46371-109">Colección [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="46371-109">[managedEBook](../resources/intune_books_managedebook.md) collection</span></span>|<span data-ttu-id="46371-110">Enumere las propiedades y las relaciones de los objetos [managedEBook](../resources/intune_books_managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="46371-110">List properties and relationships of the [managedEBook](../resources/intune_books_managedebook.md) objects.</span></span>|
|[<span data-ttu-id="46371-111">Obtener managedEBook</span><span class="sxs-lookup"><span data-stu-id="46371-111">Get managedEBook</span></span>](../api/intune_books_managedebook_get.md)|[<span data-ttu-id="46371-112">managedEBook</span><span class="sxs-lookup"><span data-stu-id="46371-112">managedEBook</span></span>](../resources/intune_books_managedebook.md)|<span data-ttu-id="46371-113">Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune_books_managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="46371-113">Read properties and relationships of the [managedEBook](../resources/intune_books_managedebook.md) object.</span></span>|
|[<span data-ttu-id="46371-114">Acción assign</span><span class="sxs-lookup"><span data-stu-id="46371-114">assign action</span></span>](../api/intune_books_managedebook_assign.md)|<span data-ttu-id="46371-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="46371-115">None</span></span>|<span data-ttu-id="46371-116">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="46371-116">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="46371-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46371-117">Properties</span></span>
|<span data-ttu-id="46371-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46371-118">Property</span></span>|<span data-ttu-id="46371-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="46371-119">Type</span></span>|<span data-ttu-id="46371-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="46371-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46371-121">id</span><span class="sxs-lookup"><span data-stu-id="46371-121">id</span></span>|<span data-ttu-id="46371-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="46371-122">String</span></span>|<span data-ttu-id="46371-123">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="46371-123">Key of the entity.</span></span>|
|<span data-ttu-id="46371-124">displayName</span><span class="sxs-lookup"><span data-stu-id="46371-124">displayName</span></span>|<span data-ttu-id="46371-125">String</span><span class="sxs-lookup"><span data-stu-id="46371-125">String</span></span>|<span data-ttu-id="46371-126">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="46371-126">Name of the eBook.</span></span>|
|<span data-ttu-id="46371-127">descripción</span><span class="sxs-lookup"><span data-stu-id="46371-127">description</span></span>|<span data-ttu-id="46371-128">String</span><span class="sxs-lookup"><span data-stu-id="46371-128">String</span></span>|<span data-ttu-id="46371-129">Descripción.</span><span class="sxs-lookup"><span data-stu-id="46371-129">Description.</span></span>|
|<span data-ttu-id="46371-130">publicador</span><span class="sxs-lookup"><span data-stu-id="46371-130">publisher</span></span>|<span data-ttu-id="46371-131">String</span><span class="sxs-lookup"><span data-stu-id="46371-131">String</span></span>|<span data-ttu-id="46371-132">Publicador.</span><span class="sxs-lookup"><span data-stu-id="46371-132">Publisher.</span></span>|
|<span data-ttu-id="46371-133">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="46371-133">publishedDateTime</span></span>|<span data-ttu-id="46371-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46371-134">DateTimeOffset</span></span>|<span data-ttu-id="46371-135">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="46371-135">The date and time when the eBook was published.</span></span>|
|<span data-ttu-id="46371-136">largeCover</span><span class="sxs-lookup"><span data-stu-id="46371-136">largeCover</span></span>|[<span data-ttu-id="46371-137">mimeContent</span><span class="sxs-lookup"><span data-stu-id="46371-137">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="46371-138">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="46371-138">Book cover.</span></span>|
|<span data-ttu-id="46371-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="46371-139">createdDateTime</span></span>|<span data-ttu-id="46371-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46371-140">DateTimeOffset</span></span>|<span data-ttu-id="46371-141">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="46371-141">The date and time when the eBook file was created.</span></span>|
|<span data-ttu-id="46371-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="46371-142">lastModifiedDateTime</span></span>|<span data-ttu-id="46371-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46371-143">DateTimeOffset</span></span>|<span data-ttu-id="46371-144">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="46371-144">The date and time when the eBook was last modified.</span></span>|
|<span data-ttu-id="46371-145">informationUrl</span><span class="sxs-lookup"><span data-stu-id="46371-145">informationUrl</span></span>|<span data-ttu-id="46371-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="46371-146">String</span></span>|<span data-ttu-id="46371-147">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="46371-147">The more information Url.</span></span>|
|<span data-ttu-id="46371-148">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="46371-148">privacyInformationUrl</span></span>|<span data-ttu-id="46371-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="46371-149">String</span></span>|<span data-ttu-id="46371-150">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="46371-150">The privacy statement Url.</span></span>|

## <a name="relationships"></a><span data-ttu-id="46371-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="46371-151">Relationships</span></span>
|<span data-ttu-id="46371-152">Relación</span><span class="sxs-lookup"><span data-stu-id="46371-152">Relationship</span></span>|<span data-ttu-id="46371-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="46371-153">Type</span></span>|<span data-ttu-id="46371-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="46371-154">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46371-155">asignaciones</span><span class="sxs-lookup"><span data-stu-id="46371-155">assignments</span></span>|<span data-ttu-id="46371-156">Colección [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="46371-156">[managedEBookAssignment](../resources/intune_books_managedebookassignment.md) collection</span></span>|<span data-ttu-id="46371-157">La lista de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="46371-157">The list of assignments for this eBook.</span></span>|
|<span data-ttu-id="46371-158">installSummary</span><span class="sxs-lookup"><span data-stu-id="46371-158">installSummary</span></span>|[<span data-ttu-id="46371-159">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="46371-159">eBookInstallSummary</span></span>](../resources/intune_books_ebookinstallsummary.md)|<span data-ttu-id="46371-160">Resumen de instalación de las aplicaciones para móviles.</span><span class="sxs-lookup"><span data-stu-id="46371-160">Mobile App Install Summary.</span></span>|
|<span data-ttu-id="46371-161">deviceStates</span><span class="sxs-lookup"><span data-stu-id="46371-161">deviceStates</span></span>|<span data-ttu-id="46371-162">Colección [deviceInstallState](../resources/intune_books_deviceinstallstate.md)</span><span class="sxs-lookup"><span data-stu-id="46371-162">[deviceInstallState](../resources/intune_books_deviceinstallstate.md) collection</span></span>|<span data-ttu-id="46371-163">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="46371-163">The list of installation states for this eBook.</span></span>|
|<span data-ttu-id="46371-164">userStateSummary</span><span class="sxs-lookup"><span data-stu-id="46371-164">userStateSummary</span></span>|<span data-ttu-id="46371-165">Colección [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)</span><span class="sxs-lookup"><span data-stu-id="46371-165">[userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md) collection</span></span>|<span data-ttu-id="46371-166">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="46371-166">The list of installation states for this eBook.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="46371-167">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="46371-167">JSON Representation</span></span>
<span data-ttu-id="46371-168">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="46371-168">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBook"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedEBook",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "publishedDateTime": "String (timestamp)",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "informationUrl": "String",
  "privacyInformationUrl": "String"
}
```









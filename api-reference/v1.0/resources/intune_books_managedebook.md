# <a name="managedebook-resource-type"></a><span data-ttu-id="270ac-101">Tipo de recurso managedEBook</span><span class="sxs-lookup"><span data-stu-id="270ac-101">managedEBook resource type</span></span>

> <span data-ttu-id="270ac-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="270ac-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="270ac-103">Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.</span><span class="sxs-lookup"><span data-stu-id="270ac-103">An abstract class containing the base properties for Managed eBook.</span></span>
## <a name="methods"></a><span data-ttu-id="270ac-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="270ac-104">Methods</span></span>
|<span data-ttu-id="270ac-105">Método</span><span class="sxs-lookup"><span data-stu-id="270ac-105">Method</span></span>|<span data-ttu-id="270ac-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="270ac-106">Return Type</span></span>|<span data-ttu-id="270ac-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="270ac-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="270ac-108">Enumerar managedEBooks</span><span class="sxs-lookup"><span data-stu-id="270ac-108">List managedEBooks</span></span>](../api/intune_books_managedebook_list.md)|<span data-ttu-id="270ac-109">Colección [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="270ac-109">[managedEBook](../resources/intune_books_managedebook.md) collection</span></span>|<span data-ttu-id="270ac-110">Enumere las propiedades y las relaciones de los objetos [managedEBook](../resources/intune_books_managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="270ac-110">List properties and relationships of the [managedEBook](../resources/intune_books_managedebook.md) objects.</span></span>|
|[<span data-ttu-id="270ac-111">Obtener managedEBook</span><span class="sxs-lookup"><span data-stu-id="270ac-111">Get managedEBook</span></span>](../api/intune_books_managedebook_get.md)|[<span data-ttu-id="270ac-112">managedEBook</span><span class="sxs-lookup"><span data-stu-id="270ac-112">managedEBook</span></span>](../resources/intune_books_managedebook.md)|<span data-ttu-id="270ac-113">Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune_books_managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="270ac-113">Read properties and relationships of [plannerTaskDetails](../resources/intune_books_managedebook.md) object.</span></span>|
|[<span data-ttu-id="270ac-114">Acción assign</span><span class="sxs-lookup"><span data-stu-id="270ac-114">assign action</span></span>](../api/intune_books_managedebook_assign.md)|<span data-ttu-id="270ac-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="270ac-115">None</span></span>|<span data-ttu-id="270ac-116">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="270ac-116">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="270ac-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="270ac-117">Properties</span></span>
|<span data-ttu-id="270ac-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="270ac-118">Property</span></span>|<span data-ttu-id="270ac-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="270ac-119">Type</span></span>|<span data-ttu-id="270ac-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="270ac-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="270ac-121">id</span><span class="sxs-lookup"><span data-stu-id="270ac-121">id</span></span>|<span data-ttu-id="270ac-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="270ac-122">String</span></span>|<span data-ttu-id="270ac-123">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="270ac-123">Key of the setting.</span></span>|
|<span data-ttu-id="270ac-124">displayName</span><span class="sxs-lookup"><span data-stu-id="270ac-124">displayName</span></span>|<span data-ttu-id="270ac-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="270ac-125">String</span></span>|<span data-ttu-id="270ac-126">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="270ac-126">Name of the folder.</span></span>|
|<span data-ttu-id="270ac-127">descripción</span><span class="sxs-lookup"><span data-stu-id="270ac-127">description</span></span>|<span data-ttu-id="270ac-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="270ac-128">String</span></span>|<span data-ttu-id="270ac-129">Descripción.</span><span class="sxs-lookup"><span data-stu-id="270ac-129">Description.</span></span>|
|<span data-ttu-id="270ac-130">publicador</span><span class="sxs-lookup"><span data-stu-id="270ac-130">Publisher</span></span>|<span data-ttu-id="270ac-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="270ac-131">String</span></span>|<span data-ttu-id="270ac-132">Publicador.</span><span class="sxs-lookup"><span data-stu-id="270ac-132">Publisher</span></span>|
|<span data-ttu-id="270ac-133">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="270ac-133">publishedDateTime</span></span>|<span data-ttu-id="270ac-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="270ac-134">DateTimeOffset</span></span>|<span data-ttu-id="270ac-135">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="270ac-135">The date and time when the page was created.</span></span>|
|<span data-ttu-id="270ac-136">largeCover</span><span class="sxs-lookup"><span data-stu-id="270ac-136">largeCover</span></span>|[<span data-ttu-id="270ac-137">mimeContent</span><span class="sxs-lookup"><span data-stu-id="270ac-137">mimeContent</span></span>](../resources/intune_books_mimecontent.md)|<span data-ttu-id="270ac-138">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="270ac-138">Book cover</span></span>|
|<span data-ttu-id="270ac-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="270ac-139">createdDateTime</span></span>|<span data-ttu-id="270ac-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="270ac-140">DateTimeOffset</span></span>|<span data-ttu-id="270ac-141">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="270ac-141">The date and time when the page was created.</span></span>|
|<span data-ttu-id="270ac-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="270ac-142">lastModifiedDateTime</span></span>|<span data-ttu-id="270ac-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="270ac-143">DateTimeOffset</span></span>|<span data-ttu-id="270ac-144">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="270ac-144">The date and time when the attachment was last modified.</span></span>|
|<span data-ttu-id="270ac-145">informationUrl</span><span class="sxs-lookup"><span data-stu-id="270ac-145">informationUrl</span></span>|<span data-ttu-id="270ac-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="270ac-146">String</span></span>|<span data-ttu-id="270ac-147">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="270ac-147">The more information Url.</span></span>|
|<span data-ttu-id="270ac-148">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="270ac-148">privacyInformationUrl</span></span>|<span data-ttu-id="270ac-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="270ac-149">String</span></span>|<span data-ttu-id="270ac-150">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="270ac-150">The privacy statement Url.</span></span>|

## <a name="relationships"></a><span data-ttu-id="270ac-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="270ac-151">Relationships</span></span>
|<span data-ttu-id="270ac-152">Relación</span><span class="sxs-lookup"><span data-stu-id="270ac-152">Relationship</span></span>|<span data-ttu-id="270ac-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="270ac-153">Type</span></span>|<span data-ttu-id="270ac-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="270ac-154">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="270ac-155">asignaciones</span><span class="sxs-lookup"><span data-stu-id="270ac-155">assignments</span></span>|<span data-ttu-id="270ac-156">Colección [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="270ac-156">[managedEBookAssignment](../resources/intune_books_managedebookassignment.md) collection</span></span>|<span data-ttu-id="270ac-157">La lista de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="270ac-157">The list of assignments for this eBook.</span></span>|
|<span data-ttu-id="270ac-158">installSummary</span><span class="sxs-lookup"><span data-stu-id="270ac-158">installSummary</span></span>|[<span data-ttu-id="270ac-159">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="270ac-159">eBookInstallSummary</span></span>](../resources/intune_books_ebookinstallsummary.md)|<span data-ttu-id="270ac-160">Resumen de instalación de las aplicaciones para móviles.</span><span class="sxs-lookup"><span data-stu-id="270ac-160">Mobile App Install Summary.</span></span>|
|<span data-ttu-id="270ac-161">deviceStates</span><span class="sxs-lookup"><span data-stu-id="270ac-161">deviceStates</span></span>|<span data-ttu-id="270ac-162">Colección [deviceInstallState](../resources/intune_books_deviceinstallstate.md)</span><span class="sxs-lookup"><span data-stu-id="270ac-162">[deviceInstallState](../resources/intune_books_deviceinstallstate.md) collection</span></span>|<span data-ttu-id="270ac-163">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="270ac-163">The list of installation states for this eBook.</span></span>|
|<span data-ttu-id="270ac-164">userStateSummary</span><span class="sxs-lookup"><span data-stu-id="270ac-164">userStateSummary</span></span>|<span data-ttu-id="270ac-165">Colección [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)</span><span class="sxs-lookup"><span data-stu-id="270ac-165">[userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md) collection</span></span>|<span data-ttu-id="270ac-166">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="270ac-166">The list of installation states for this eBook.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="270ac-167">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="270ac-167">JSON Representation</span></span>
<span data-ttu-id="270ac-168">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="270ac-168">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBook"
}
-->
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




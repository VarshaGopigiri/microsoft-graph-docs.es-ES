# <a name="managedebook-resource-type"></a><span data-ttu-id="a53fd-101">Tipo de recurso managedEBook</span><span class="sxs-lookup"><span data-stu-id="a53fd-101">managedEBook resource type</span></span>

> <span data-ttu-id="a53fd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a53fd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a53fd-103">Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.</span><span class="sxs-lookup"><span data-stu-id="a53fd-103">An abstract class containing the base properties for Managed eBook.</span></span>
## <a name="methods"></a><span data-ttu-id="a53fd-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="a53fd-104">Methods</span></span>
|<span data-ttu-id="a53fd-105">Método</span><span class="sxs-lookup"><span data-stu-id="a53fd-105">Method</span></span>|<span data-ttu-id="a53fd-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a53fd-106">Return Type</span></span>|<span data-ttu-id="a53fd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a53fd-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="a53fd-108">Enumerar managedEBooks</span><span class="sxs-lookup"><span data-stu-id="a53fd-108">List managedEBooks</span></span>](../api/intune_books_managedebook_list.md)|<span data-ttu-id="a53fd-109">Colección [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="a53fd-109">[managedEBook](../resources/intune_books_managedebook.md) collection</span></span>|<span data-ttu-id="a53fd-110">Enumere las propiedades y las relaciones de los objetos [managedEBook](../resources/intune_books_managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="a53fd-110">List properties and relationships of the [managedEBook](../resources/intune_books_managedebook.md) objects.</span></span>|
|[<span data-ttu-id="a53fd-111">Obtener managedEBook</span><span class="sxs-lookup"><span data-stu-id="a53fd-111">Get managedEBook</span></span>](../api/intune_books_managedebook_get.md)|[<span data-ttu-id="a53fd-112">managedEBook</span><span class="sxs-lookup"><span data-stu-id="a53fd-112">managedEBook</span></span>](../resources/intune_books_managedebook.md)|<span data-ttu-id="a53fd-113">Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune_books_managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="a53fd-113">Read properties and relationships of the [managedEBook](../resources/intune_books_managedebook.md) object.</span></span>|
|[<span data-ttu-id="a53fd-114">Acción assign</span><span class="sxs-lookup"><span data-stu-id="a53fd-114">assign action</span></span>](../api/intune_books_managedebook_assign.md)|<span data-ttu-id="a53fd-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a53fd-115">None</span></span>|<span data-ttu-id="a53fd-116">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a53fd-116">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="a53fd-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a53fd-117">Properties</span></span>
|<span data-ttu-id="a53fd-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a53fd-118">Property</span></span>|<span data-ttu-id="a53fd-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="a53fd-119">Type</span></span>|<span data-ttu-id="a53fd-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a53fd-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a53fd-121">id</span><span class="sxs-lookup"><span data-stu-id="a53fd-121">id</span></span>|<span data-ttu-id="a53fd-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="a53fd-122">String</span></span>|<span data-ttu-id="a53fd-123">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a53fd-123">Key of the entity.</span></span>|
|<span data-ttu-id="a53fd-124">displayName</span><span class="sxs-lookup"><span data-stu-id="a53fd-124">displayName</span></span>|<span data-ttu-id="a53fd-125">String</span><span class="sxs-lookup"><span data-stu-id="a53fd-125">String</span></span>|<span data-ttu-id="a53fd-126">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="a53fd-126">Name of the eBook.</span></span>|
|<span data-ttu-id="a53fd-127">descripción</span><span class="sxs-lookup"><span data-stu-id="a53fd-127">description</span></span>|<span data-ttu-id="a53fd-128">String</span><span class="sxs-lookup"><span data-stu-id="a53fd-128">String</span></span>|<span data-ttu-id="a53fd-129">Descripción.</span><span class="sxs-lookup"><span data-stu-id="a53fd-129">Description.</span></span>|
|<span data-ttu-id="a53fd-130">publicador</span><span class="sxs-lookup"><span data-stu-id="a53fd-130">publisher</span></span>|<span data-ttu-id="a53fd-131">String</span><span class="sxs-lookup"><span data-stu-id="a53fd-131">String</span></span>|<span data-ttu-id="a53fd-132">Publicador.</span><span class="sxs-lookup"><span data-stu-id="a53fd-132">Publisher.</span></span>|
|<span data-ttu-id="a53fd-133">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="a53fd-133">publishedDateTime</span></span>|<span data-ttu-id="a53fd-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a53fd-134">DateTimeOffset</span></span>|<span data-ttu-id="a53fd-135">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="a53fd-135">The date and time when the eBook was published.</span></span>|
|<span data-ttu-id="a53fd-136">largeCover</span><span class="sxs-lookup"><span data-stu-id="a53fd-136">largeCover</span></span>|[<span data-ttu-id="a53fd-137">mimeContent</span><span class="sxs-lookup"><span data-stu-id="a53fd-137">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="a53fd-138">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="a53fd-138">Book cover.</span></span>|
|<span data-ttu-id="a53fd-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a53fd-139">createdDateTime</span></span>|<span data-ttu-id="a53fd-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a53fd-140">DateTimeOffset</span></span>|<span data-ttu-id="a53fd-141">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="a53fd-141">The date and time when the eBook file was created.</span></span>|
|<span data-ttu-id="a53fd-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a53fd-142">lastModifiedDateTime</span></span>|<span data-ttu-id="a53fd-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a53fd-143">DateTimeOffset</span></span>|<span data-ttu-id="a53fd-144">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="a53fd-144">The date and time when the eBook was last modified.</span></span>|
|<span data-ttu-id="a53fd-145">informationUrl</span><span class="sxs-lookup"><span data-stu-id="a53fd-145">informationUrl</span></span>|<span data-ttu-id="a53fd-146">String</span><span class="sxs-lookup"><span data-stu-id="a53fd-146">String</span></span>|<span data-ttu-id="a53fd-147">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a53fd-147">The more information Url.</span></span>|
|<span data-ttu-id="a53fd-148">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="a53fd-148">privacyInformationUrl</span></span>|<span data-ttu-id="a53fd-149">String</span><span class="sxs-lookup"><span data-stu-id="a53fd-149">String</span></span>|<span data-ttu-id="a53fd-150">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="a53fd-150">The privacy statement Url.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a53fd-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a53fd-151">Relationships</span></span>
|<span data-ttu-id="a53fd-152">Relación</span><span class="sxs-lookup"><span data-stu-id="a53fd-152">Relationship</span></span>|<span data-ttu-id="a53fd-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="a53fd-153">Type</span></span>|<span data-ttu-id="a53fd-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="a53fd-154">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a53fd-155">asignaciones</span><span class="sxs-lookup"><span data-stu-id="a53fd-155">assignments</span></span>|<span data-ttu-id="a53fd-156">Colección [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="a53fd-156">[managedEBookAssignment](../resources/intune_books_managedebookassignment.md) collection</span></span>|<span data-ttu-id="a53fd-157">La lista de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="a53fd-157">The list of assignments for this eBook.</span></span>|
|<span data-ttu-id="a53fd-158">installSummary</span><span class="sxs-lookup"><span data-stu-id="a53fd-158">installSummary</span></span>|[<span data-ttu-id="a53fd-159">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="a53fd-159">eBookInstallSummary</span></span>](../resources/intune_books_ebookinstallsummary.md)|<span data-ttu-id="a53fd-160">Resumen de instalación de las aplicaciones para móviles.</span><span class="sxs-lookup"><span data-stu-id="a53fd-160">Mobile App Install Summary.</span></span>|
|<span data-ttu-id="a53fd-161">deviceStates</span><span class="sxs-lookup"><span data-stu-id="a53fd-161">deviceStates</span></span>|<span data-ttu-id="a53fd-162">Colección [deviceInstallState](../resources/intune_books_deviceinstallstate.md)</span><span class="sxs-lookup"><span data-stu-id="a53fd-162">[deviceInstallState](../resources/intune_books_deviceinstallstate.md) collection</span></span>|<span data-ttu-id="a53fd-163">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="a53fd-163">The list of installation states for this eBook.</span></span>|
|<span data-ttu-id="a53fd-164">userStateSummary</span><span class="sxs-lookup"><span data-stu-id="a53fd-164">userStateSummary</span></span>|<span data-ttu-id="a53fd-165">Colección [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)</span><span class="sxs-lookup"><span data-stu-id="a53fd-165">[userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md) collection</span></span>|<span data-ttu-id="a53fd-166">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="a53fd-166">The list of installation states for this eBook.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a53fd-167">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a53fd-167">JSON Representation</span></span>
<span data-ttu-id="a53fd-168">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a53fd-168">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "abstract": true,
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
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




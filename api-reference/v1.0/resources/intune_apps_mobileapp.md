# <a name="mobileapp-resource-type"></a><span data-ttu-id="b2030-101">Tipo de recurso mobileApp</span><span class="sxs-lookup"><span data-stu-id="b2030-101">mobileApp resource type</span></span>

> <span data-ttu-id="b2030-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b2030-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b2030-103">Una clase abstracta que contiene las propiedades base para las aplicaciones móviles de Intune.</span><span class="sxs-lookup"><span data-stu-id="b2030-103">An abstract class containing the base properties for Intune mobile apps.</span></span>
## <a name="methods"></a><span data-ttu-id="b2030-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="b2030-104">Methods</span></span>
|<span data-ttu-id="b2030-105">Método</span><span class="sxs-lookup"><span data-stu-id="b2030-105">Method</span></span>|<span data-ttu-id="b2030-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2030-106">Return Type</span></span>|<span data-ttu-id="b2030-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2030-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="b2030-108">Enumerar mobileApps</span><span class="sxs-lookup"><span data-stu-id="b2030-108">List mobileApps</span></span>](../api/intune_apps_mobileapp_list.md)|<span data-ttu-id="b2030-109">Colección [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="b2030-109">[mobileApp](../resources/intune_apps_mobileapp.md) collection</span></span>|<span data-ttu-id="b2030-110">Enumere las propiedades y las relaciones de los objetos [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2030-110">List properties and relationships of the [mobileApp](../resources/intune_apps_mobileapp.md) objects.</span></span>|
|[<span data-ttu-id="b2030-111">Obtener mobileApp</span><span class="sxs-lookup"><span data-stu-id="b2030-111">Get mobileApp</span></span>](../api/intune_apps_mobileapp_get.md)|[<span data-ttu-id="b2030-112">mobileApp</span><span class="sxs-lookup"><span data-stu-id="b2030-112">mobileApp</span></span>](../resources/intune_apps_mobileapp.md)|<span data-ttu-id="b2030-113">Lea las propiedades y las relaciones del objeto [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2030-113">Read properties and relationships of the [mobileApp](../resources/intune_apps_mobileapp.md) object.</span></span>|
|[<span data-ttu-id="b2030-114">Acción assign</span><span class="sxs-lookup"><span data-stu-id="b2030-114">assign action</span></span>](../api/intune_apps_mobileapp_assign.md)|<span data-ttu-id="b2030-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b2030-115">None</span></span>|<span data-ttu-id="b2030-116">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b2030-116">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="b2030-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2030-117">Properties</span></span>
|<span data-ttu-id="b2030-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b2030-118">Property</span></span>|<span data-ttu-id="b2030-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2030-119">Type</span></span>|<span data-ttu-id="b2030-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2030-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b2030-121">id</span><span class="sxs-lookup"><span data-stu-id="b2030-121">id</span></span>|<span data-ttu-id="b2030-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2030-122">String</span></span>|<span data-ttu-id="b2030-123">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b2030-123">Key of the entity.</span></span>|
|<span data-ttu-id="b2030-124">displayName</span><span class="sxs-lookup"><span data-stu-id="b2030-124">displayName</span></span>|<span data-ttu-id="b2030-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2030-125">String</span></span>|<span data-ttu-id="b2030-126">El título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="b2030-126">The admin provided or imported title of the app.</span></span>|
|<span data-ttu-id="b2030-127">description</span><span class="sxs-lookup"><span data-stu-id="b2030-127">description</span></span>|<span data-ttu-id="b2030-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2030-128">String</span></span>|<span data-ttu-id="b2030-129">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2030-129">The description of the app.</span></span>|
|<span data-ttu-id="b2030-130">publisher</span><span class="sxs-lookup"><span data-stu-id="b2030-130">publisher</span></span>|<span data-ttu-id="b2030-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2030-131">String</span></span>|<span data-ttu-id="b2030-132">El publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2030-132">The publisher of the app.</span></span>|
|<span data-ttu-id="b2030-133">largeIcon</span><span class="sxs-lookup"><span data-stu-id="b2030-133">largeIcon</span></span>|[<span data-ttu-id="b2030-134">mimeContent</span><span class="sxs-lookup"><span data-stu-id="b2030-134">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="b2030-135">El icono grande, se muestra en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="b2030-135">The large icon, to be displayed in the app details and used for upload of the icon.</span></span>|
|<span data-ttu-id="b2030-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b2030-136">createdDateTime</span></span>|<span data-ttu-id="b2030-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b2030-137">DateTimeOffset</span></span>|<span data-ttu-id="b2030-138">La fecha y la hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2030-138">The date and time the app was created.</span></span>|
|<span data-ttu-id="b2030-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b2030-139">lastModifiedDateTime</span></span>|<span data-ttu-id="b2030-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b2030-140">DateTimeOffset</span></span>|<span data-ttu-id="b2030-141">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2030-141">The date and time the app was last modified.</span></span>|
|<span data-ttu-id="b2030-142">isFeatured</span><span class="sxs-lookup"><span data-stu-id="b2030-142">isFeatured</span></span>|<span data-ttu-id="b2030-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="b2030-143">Boolean</span></span>|<span data-ttu-id="b2030-144">El valor que indica si el administrador ha marcado la aplicación como destacada.</span><span class="sxs-lookup"><span data-stu-id="b2030-144">The value indicating whether the app is marked as featured by the admin.</span></span>|
|<span data-ttu-id="b2030-145">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="b2030-145">privacyInformationUrl</span></span>|<span data-ttu-id="b2030-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2030-146">String</span></span>|<span data-ttu-id="b2030-147">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="b2030-147">The privacy statement Url.</span></span>|
|<span data-ttu-id="b2030-148">informationUrl</span><span class="sxs-lookup"><span data-stu-id="b2030-148">informationUrl</span></span>|<span data-ttu-id="b2030-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2030-149">String</span></span>|<span data-ttu-id="b2030-150">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b2030-150">The more information Url.</span></span>|
|<span data-ttu-id="b2030-151">propietario</span><span class="sxs-lookup"><span data-stu-id="b2030-151">owner</span></span>|<span data-ttu-id="b2030-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2030-152">String</span></span>|<span data-ttu-id="b2030-153">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2030-153">The owner of the app.</span></span>|
|<span data-ttu-id="b2030-154">desarrollador</span><span class="sxs-lookup"><span data-stu-id="b2030-154">developer</span></span>|<span data-ttu-id="b2030-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2030-155">String</span></span>|<span data-ttu-id="b2030-156">El desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2030-156">The developer of the app.</span></span>|
|<span data-ttu-id="b2030-157">notes</span><span class="sxs-lookup"><span data-stu-id="b2030-157">notes</span></span>|<span data-ttu-id="b2030-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2030-158">String</span></span>|<span data-ttu-id="b2030-159">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2030-159">Notes for the app.</span></span>|
|<span data-ttu-id="b2030-160">publishingState</span><span class="sxs-lookup"><span data-stu-id="b2030-160">publishingState</span></span>|[<span data-ttu-id="b2030-161">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="b2030-161">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="b2030-p101">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="b2030-p101">The publishing state for the app. The app cannot be assigned unless the app is published. The possible values are: `notPublished`, `processing`, `published`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b2030-165">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b2030-165">Relationships</span></span>
|<span data-ttu-id="b2030-166">Relación</span><span class="sxs-lookup"><span data-stu-id="b2030-166">Relationship</span></span>|<span data-ttu-id="b2030-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2030-167">Type</span></span>|<span data-ttu-id="b2030-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2030-168">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b2030-169">categorías</span><span class="sxs-lookup"><span data-stu-id="b2030-169">categories</span></span>|<span data-ttu-id="b2030-170">Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)</span><span class="sxs-lookup"><span data-stu-id="b2030-170">[mobileAppCategory](../resources/intune_apps_mobileappcategory.md) collection</span></span>|<span data-ttu-id="b2030-171">La lista de categorías para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2030-171">The list of categories for this app.</span></span>|
|<span data-ttu-id="b2030-172">asignaciones</span><span class="sxs-lookup"><span data-stu-id="b2030-172">assignments</span></span>|<span data-ttu-id="b2030-173">Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)</span><span class="sxs-lookup"><span data-stu-id="b2030-173">[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) collection</span></span>|<span data-ttu-id="b2030-174">La lista de asignaciones de grupo para esta aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="b2030-174">The list of group assignments for this mobile app.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b2030-175">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b2030-175">JSON Representation</span></span>
<span data-ttu-id="b2030-176">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b2030-176">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileApp"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileApp",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "isFeatured": true,
  "privacyInformationUrl": "String",
  "informationUrl": "String",
  "owner": "String",
  "developer": "String",
  "notes": "String",
  "publishingState": "String"
}
```









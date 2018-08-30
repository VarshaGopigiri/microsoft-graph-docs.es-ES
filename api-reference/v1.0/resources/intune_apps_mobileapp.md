# <a name="mobileapp-resource-type"></a><span data-ttu-id="41b42-101">Tipo de recurso mobileApp</span><span class="sxs-lookup"><span data-stu-id="41b42-101">mobileApp resource type</span></span>

> <span data-ttu-id="41b42-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="41b42-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="41b42-103">Una clase abstracta que contiene las propiedades base para las aplicaciones móviles de Intune.</span><span class="sxs-lookup"><span data-stu-id="41b42-103">An abstract class containing the base properties for Intune mobile apps.</span></span>
## <a name="methods"></a><span data-ttu-id="41b42-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="41b42-104">Methods</span></span>
|<span data-ttu-id="41b42-105">Método</span><span class="sxs-lookup"><span data-stu-id="41b42-105">Method</span></span>|<span data-ttu-id="41b42-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41b42-106">Return Type</span></span>|<span data-ttu-id="41b42-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="41b42-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="41b42-108">Enumerar mobileApps</span><span class="sxs-lookup"><span data-stu-id="41b42-108">List mobileApps</span></span>](../api/intune_apps_mobileapp_list.md)|<span data-ttu-id="41b42-109">Colección [mobileApp](../resources/intune_apps_mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="41b42-109">[mobileApp](../resources/intune_apps_mobileapp.md) collection</span></span>|<span data-ttu-id="41b42-110">Enumere las propiedades y las relaciones de los objetos [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="41b42-110">List properties and relationships of the [mobileApp](../resources/intune_apps_mobileapp.md) objects.</span></span>|
|[<span data-ttu-id="41b42-111">Obtener mobileApp</span><span class="sxs-lookup"><span data-stu-id="41b42-111">Get mobileApp</span></span>](../api/intune_apps_mobileapp_get.md)|[<span data-ttu-id="41b42-112">mobileApp</span><span class="sxs-lookup"><span data-stu-id="41b42-112">mobileApp</span></span>](../resources/intune_apps_mobileapp.md)|<span data-ttu-id="41b42-113">Lea las propiedades y las relaciones del objeto [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="41b42-113">Read properties and relationships of the [mobileApp](../resources/intune_apps_mobileapp.md) object.</span></span>|
|[<span data-ttu-id="41b42-114">Acción assign</span><span class="sxs-lookup"><span data-stu-id="41b42-114">assign action</span></span>](../api/intune_apps_mobileapp_assign.md)|<span data-ttu-id="41b42-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="41b42-115">None</span></span>|<span data-ttu-id="41b42-116">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="41b42-116">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="41b42-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41b42-117">Properties</span></span>
|<span data-ttu-id="41b42-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41b42-118">Property</span></span>|<span data-ttu-id="41b42-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="41b42-119">Type</span></span>|<span data-ttu-id="41b42-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="41b42-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="41b42-121">id</span><span class="sxs-lookup"><span data-stu-id="41b42-121">id</span></span>|<span data-ttu-id="41b42-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="41b42-122">String</span></span>|<span data-ttu-id="41b42-123">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="41b42-123">Key of the entity.</span></span>|
|<span data-ttu-id="41b42-124">displayName</span><span class="sxs-lookup"><span data-stu-id="41b42-124">displayName</span></span>|<span data-ttu-id="41b42-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="41b42-125">String</span></span>|<span data-ttu-id="41b42-126">El título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="41b42-126">The admin provided or imported title of the app.</span></span>|
|<span data-ttu-id="41b42-127">descripción</span><span class="sxs-lookup"><span data-stu-id="41b42-127">description</span></span>|<span data-ttu-id="41b42-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="41b42-128">String</span></span>|<span data-ttu-id="41b42-129">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41b42-129">The description of the app.</span></span>|
|<span data-ttu-id="41b42-130">publicador</span><span class="sxs-lookup"><span data-stu-id="41b42-130">publisher</span></span>|<span data-ttu-id="41b42-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="41b42-131">String</span></span>|<span data-ttu-id="41b42-132">El publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41b42-132">The publisher of the app.</span></span>|
|<span data-ttu-id="41b42-133">largeIcon</span><span class="sxs-lookup"><span data-stu-id="41b42-133">largeIcon</span></span>|[<span data-ttu-id="41b42-134">mimeContent</span><span class="sxs-lookup"><span data-stu-id="41b42-134">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="41b42-135">El icono grande, se muestra en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="41b42-135">The large icon, to be displayed in the app details and used for upload of the icon.</span></span>|
|<span data-ttu-id="41b42-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="41b42-136">createdDateTime</span></span>|<span data-ttu-id="41b42-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="41b42-137">DateTimeOffset</span></span>|<span data-ttu-id="41b42-138">La fecha y la hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41b42-138">The date and time the app was created.</span></span>|
|<span data-ttu-id="41b42-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="41b42-139">lastModifiedDateTime</span></span>|<span data-ttu-id="41b42-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="41b42-140">DateTimeOffset</span></span>|<span data-ttu-id="41b42-141">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41b42-141">The date and time the app was last modified.</span></span>|
|<span data-ttu-id="41b42-142">isFeatured</span><span class="sxs-lookup"><span data-stu-id="41b42-142">isFeatured</span></span>|<span data-ttu-id="41b42-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="41b42-143">Boolean</span></span>|<span data-ttu-id="41b42-144">El valor que indica si el administrador ha marcado la aplicación como destacada.</span><span class="sxs-lookup"><span data-stu-id="41b42-144">The value indicating whether the app is marked as featured by the admin.</span></span>|
|<span data-ttu-id="41b42-145">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="41b42-145">privacyInformationUrl</span></span>|<span data-ttu-id="41b42-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="41b42-146">String</span></span>|<span data-ttu-id="41b42-147">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="41b42-147">The privacy statement Url.</span></span>|
|<span data-ttu-id="41b42-148">informationUrl</span><span class="sxs-lookup"><span data-stu-id="41b42-148">informationUrl</span></span>|<span data-ttu-id="41b42-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="41b42-149">String</span></span>|<span data-ttu-id="41b42-150">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="41b42-150">The more information Url.</span></span>|
|<span data-ttu-id="41b42-151">propietario</span><span class="sxs-lookup"><span data-stu-id="41b42-151">owner</span></span>|<span data-ttu-id="41b42-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="41b42-152">String</span></span>|<span data-ttu-id="41b42-153">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41b42-153">The owner of the app.</span></span>|
|<span data-ttu-id="41b42-154">desarrollador</span><span class="sxs-lookup"><span data-stu-id="41b42-154">developer</span></span>|<span data-ttu-id="41b42-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="41b42-155">String</span></span>|<span data-ttu-id="41b42-156">El desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41b42-156">The developer of the app.</span></span>|
|<span data-ttu-id="41b42-157">notas</span><span class="sxs-lookup"><span data-stu-id="41b42-157">notes</span></span>|<span data-ttu-id="41b42-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="41b42-158">String</span></span>|<span data-ttu-id="41b42-159">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41b42-159">Notes for the app.</span></span>|
|<span data-ttu-id="41b42-160">publishingState</span><span class="sxs-lookup"><span data-stu-id="41b42-160">publishingState</span></span>|[<span data-ttu-id="41b42-161">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="41b42-161">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="41b42-162">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41b42-162">The publishing state for the app.</span></span> <span data-ttu-id="41b42-163">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="41b42-163">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="41b42-164">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="41b42-164">The possible values are `notPublished`, `processing`, `published`, , , , , , , , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="41b42-165">Relaciones</span><span class="sxs-lookup"><span data-stu-id="41b42-165">Relationships</span></span>
|<span data-ttu-id="41b42-166">Relación</span><span class="sxs-lookup"><span data-stu-id="41b42-166">Relationship</span></span>|<span data-ttu-id="41b42-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="41b42-167">Type</span></span>|<span data-ttu-id="41b42-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="41b42-168">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="41b42-169">categorías</span><span class="sxs-lookup"><span data-stu-id="41b42-169">categories</span></span>|<span data-ttu-id="41b42-170">Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)</span><span class="sxs-lookup"><span data-stu-id="41b42-170">[mobileAppCategory](../resources/intune_apps_mobileappcategory.md) collection</span></span>|<span data-ttu-id="41b42-171">La lista de categorías para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="41b42-171">The list of categories for this app.</span></span>|
|<span data-ttu-id="41b42-172">asignaciones</span><span class="sxs-lookup"><span data-stu-id="41b42-172">assignments</span></span>|<span data-ttu-id="41b42-173">Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)</span><span class="sxs-lookup"><span data-stu-id="41b42-173">[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) collection</span></span>|<span data-ttu-id="41b42-174">La lista de asignaciones de grupo para esta aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="41b42-174">The list of group assignments for this mobile app.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="41b42-175">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="41b42-175">JSON Representation</span></span>
<span data-ttu-id="41b42-176">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="41b42-176">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "abstract": true,
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
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




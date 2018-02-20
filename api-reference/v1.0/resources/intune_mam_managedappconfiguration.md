# <a name="managedappconfiguration-resource-type"></a><span data-ttu-id="f51a9-101">Tipo de recurso managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="f51a9-101">managedAppConfiguration resource type</span></span>

> <span data-ttu-id="f51a9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f51a9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f51a9-103">Configuración usada para proporcionar un conjunto de configuración personalizada tal cual a aplicaciones para usuarios que tienen limitada la configuración.</span><span class="sxs-lookup"><span data-stu-id="f51a9-103">Configuration used to deliver a set of custom settings as-is to apps for users to whom the configuration is scoped</span></span>

<span data-ttu-id="f51a9-104">Hereda de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f51a9-104">Inherits from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>

## <a name="methods"></a><span data-ttu-id="f51a9-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="f51a9-105">Methods</span></span>
|<span data-ttu-id="f51a9-106">Método</span><span class="sxs-lookup"><span data-stu-id="f51a9-106">Method</span></span>|<span data-ttu-id="f51a9-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f51a9-107">Return Type</span></span>|<span data-ttu-id="f51a9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f51a9-108">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="f51a9-109">Enumerar managedAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="f51a9-109">List managedAppConfigurations</span></span>](../api/intune_mam_managedappconfiguration_list.md)|<span data-ttu-id="f51a9-110">Colección [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f51a9-110">[managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md) collection</span></span>|<span data-ttu-id="f51a9-111">Enumere las propiedades y las relaciones de los objetos [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f51a9-111">List properties and relationships of the [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="f51a9-112">Obtener managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="f51a9-112">Get managedAppConfiguration</span></span>](../api/intune_mam_managedappconfiguration_get.md)|[<span data-ttu-id="f51a9-113">managedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="f51a9-113">managedAppConfiguration</span></span>](../resources/intune_mam_managedappconfiguration.md)|<span data-ttu-id="f51a9-114">Lea las propiedades y las relaciones del objeto [managedAppConfiguration](../resources/intune_mam_managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f51a9-114">Read properties and relationships of [plannerTaskDetails](../resources/intune_mam_managedappconfiguration.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="f51a9-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f51a9-115">Properties</span></span>
|<span data-ttu-id="f51a9-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f51a9-116">Property</span></span>|<span data-ttu-id="f51a9-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="f51a9-117">Type</span></span>|<span data-ttu-id="f51a9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f51a9-118">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f51a9-119">displayName</span><span class="sxs-lookup"><span data-stu-id="f51a9-119">displayName</span></span>|<span data-ttu-id="f51a9-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="f51a9-120">String</span></span>|<span data-ttu-id="f51a9-121">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f51a9-121">Policy display name.</span></span> <span data-ttu-id="f51a9-122">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f51a9-122">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f51a9-123">descripción</span><span class="sxs-lookup"><span data-stu-id="f51a9-123">description</span></span>|<span data-ttu-id="f51a9-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="f51a9-124">String</span></span>|<span data-ttu-id="f51a9-125">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f51a9-125">The policy's description.</span></span> <span data-ttu-id="f51a9-126">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f51a9-126">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f51a9-127">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f51a9-127">createdDateTime</span></span>|<span data-ttu-id="f51a9-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f51a9-128">DateTimeOffset</span></span>|<span data-ttu-id="f51a9-129">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f51a9-129">The date and time when the page was created.</span></span> <span data-ttu-id="f51a9-130">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f51a9-130">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f51a9-131">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f51a9-131">lastModifiedDateTime</span></span>|<span data-ttu-id="f51a9-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f51a9-132">DateTimeOffset</span></span>|<span data-ttu-id="f51a9-133">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="f51a9-133">Last time the policy was modified.</span></span> <span data-ttu-id="f51a9-134">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f51a9-134">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f51a9-135">id</span><span class="sxs-lookup"><span data-stu-id="f51a9-135">id</span></span>|<span data-ttu-id="f51a9-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="f51a9-136">String</span></span>|<span data-ttu-id="f51a9-137">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f51a9-137">Key of the setting.</span></span> <span data-ttu-id="f51a9-138">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f51a9-138">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f51a9-139">versión</span><span class="sxs-lookup"><span data-stu-id="f51a9-139">version</span></span>|<span data-ttu-id="f51a9-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="f51a9-140">String</span></span>|<span data-ttu-id="f51a9-141">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f51a9-141">Version of the entity.</span></span> <span data-ttu-id="f51a9-142">Heredado de [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f51a9-142">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="f51a9-143">customSettings</span><span class="sxs-lookup"><span data-stu-id="f51a9-143">customSettings</span></span>|<span data-ttu-id="f51a9-144">Colección [keyValuePair](../resources/intune_mam_keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="f51a9-144">[keyValuePair](../resources/intune_mam_keyvaluepair.md) collection</span></span>|<span data-ttu-id="f51a9-145">Un conjunto de pares de clave de cadena y valor de cadena que se va a enviar a las aplicaciones para aquellos usuarios que tienen limitada la configuración, sin modificar por este servicio</span><span class="sxs-lookup"><span data-stu-id="f51a9-145">A set of string key and string value pairs to be sent to apps for users to whom the configuration is scoped, unalterned by this service</span></span>|

## <a name="relationships"></a><span data-ttu-id="f51a9-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f51a9-146">Relationships</span></span>
<span data-ttu-id="f51a9-147">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f51a9-147">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f51a9-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f51a9-148">JSON Representation</span></span>
<span data-ttu-id="f51a9-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f51a9-149">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppConfiguration",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "customSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ]
}
```




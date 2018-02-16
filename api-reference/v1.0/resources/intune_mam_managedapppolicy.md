# <a name="managedapppolicy-resource-type"></a><span data-ttu-id="f6f7a-101">Tipo de recurso managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="f6f7a-101">managedAppPolicy resource type</span></span>

> <span data-ttu-id="f6f7a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6f7a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6f7a-103">El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="f6f7a-103">The ManagedAppPolicy resource represents a base type for platform specific policies.</span></span>
## <a name="methods"></a><span data-ttu-id="f6f7a-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="f6f7a-104">Methods</span></span>
|<span data-ttu-id="f6f7a-105">Método</span><span class="sxs-lookup"><span data-stu-id="f6f7a-105">Method</span></span>|<span data-ttu-id="f6f7a-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6f7a-106">Return Type</span></span>|<span data-ttu-id="f6f7a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6f7a-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="f6f7a-108">Enumerar managedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="f6f7a-108">List managedAppPolicies</span></span>](../api/intune_mam_managedapppolicy_list.md)|<span data-ttu-id="f6f7a-109">Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f6f7a-109">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) collection</span></span>|<span data-ttu-id="f6f7a-110">Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f6f7a-110">List properties and relationships of the [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) objects.</span></span>|
|[<span data-ttu-id="f6f7a-111">Obtener managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="f6f7a-111">Get managedAppPolicy</span></span>](../api/intune_mam_managedapppolicy_get.md)|[<span data-ttu-id="f6f7a-112">managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="f6f7a-112">managedAppPolicy</span></span>](../resources/intune_mam_managedapppolicy.md)|<span data-ttu-id="f6f7a-113">Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f6f7a-113">Read properties and relationships of [plannerTaskDetails](../resources/intune_mam_managedapppolicy.md) object.</span></span>|
|[<span data-ttu-id="f6f7a-114">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="f6f7a-114">targetApps action</span></span>](../api/intune_mam_managedapppolicy_targetapps.md)|<span data-ttu-id="f6f7a-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f6f7a-115">None</span></span>|<span data-ttu-id="f6f7a-116">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f6f7a-116">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="f6f7a-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6f7a-117">Properties</span></span>
|<span data-ttu-id="f6f7a-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6f7a-118">Property</span></span>|<span data-ttu-id="f6f7a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6f7a-119">Type</span></span>|<span data-ttu-id="f6f7a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6f7a-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f6f7a-121">displayName</span><span class="sxs-lookup"><span data-stu-id="f6f7a-121">displayName</span></span>|<span data-ttu-id="f6f7a-122">cadena</span><span class="sxs-lookup"><span data-stu-id="f6f7a-122">String</span></span>|<span data-ttu-id="f6f7a-123">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f6f7a-123">Policy display name.</span></span>|
|<span data-ttu-id="f6f7a-124">descripción</span><span class="sxs-lookup"><span data-stu-id="f6f7a-124">description</span></span>|<span data-ttu-id="f6f7a-125">cadena</span><span class="sxs-lookup"><span data-stu-id="f6f7a-125">String</span></span>|<span data-ttu-id="f6f7a-126">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f6f7a-126">The policy's description.</span></span>|
|<span data-ttu-id="f6f7a-127">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f6f7a-127">createdDateTime</span></span>|<span data-ttu-id="f6f7a-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f6f7a-128">DateTimeOffset</span></span>|<span data-ttu-id="f6f7a-129">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f6f7a-129">The date and time when the page was created.</span></span>|
|<span data-ttu-id="f6f7a-130">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f6f7a-130">lastModifiedDateTime</span></span>|<span data-ttu-id="f6f7a-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f6f7a-131">DateTimeOffset</span></span>|<span data-ttu-id="f6f7a-132">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="f6f7a-132">Last time the policy was modified.</span></span>|
|<span data-ttu-id="f6f7a-133">id</span><span class="sxs-lookup"><span data-stu-id="f6f7a-133">id</span></span>|<span data-ttu-id="f6f7a-134">cadena</span><span class="sxs-lookup"><span data-stu-id="f6f7a-134">String</span></span>|<span data-ttu-id="f6f7a-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f6f7a-135">Key of the setting.</span></span>|
|<span data-ttu-id="f6f7a-136">versión</span><span class="sxs-lookup"><span data-stu-id="f6f7a-136">version</span></span>|<span data-ttu-id="f6f7a-137">cadena</span><span class="sxs-lookup"><span data-stu-id="f6f7a-137">String</span></span>|<span data-ttu-id="f6f7a-138">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f6f7a-138">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f6f7a-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f6f7a-139">Relationships</span></span>
<span data-ttu-id="f6f7a-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f6f7a-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f6f7a-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f6f7a-141">JSON Representation</span></span>
<span data-ttu-id="f6f7a-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f6f7a-142">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicy",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String"
}
```




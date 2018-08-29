# <a name="managedapppolicy-resource-type"></a><span data-ttu-id="c8e99-101">Tipo de recurso managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e99-101">managedAppPolicy resource type</span></span>

> <span data-ttu-id="c8e99-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c8e99-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c8e99-103">El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c8e99-103">The ManagedAppPolicy resource represents a base type for platform specific policies.</span></span>
## <a name="methods"></a><span data-ttu-id="c8e99-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8e99-104">Methods</span></span>
|<span data-ttu-id="c8e99-105">Método</span><span class="sxs-lookup"><span data-stu-id="c8e99-105">Method</span></span>|<span data-ttu-id="c8e99-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8e99-106">Return Type</span></span>|<span data-ttu-id="c8e99-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8e99-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="c8e99-108">Enumerar managedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="c8e99-108">List managedAppPolicies</span></span>](../api/intune_mam_managedapppolicy_list.md)|<span data-ttu-id="c8e99-109">Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c8e99-109">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) collection</span></span>|<span data-ttu-id="c8e99-110">Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c8e99-110">List properties and relationships of the [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) objects.</span></span>|
|[<span data-ttu-id="c8e99-111">Obtener managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e99-111">Get managedAppPolicy</span></span>](../api/intune_mam_managedapppolicy_get.md)|[<span data-ttu-id="c8e99-112">managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="c8e99-112">managedAppPolicy</span></span>](../resources/intune_mam_managedapppolicy.md)|<span data-ttu-id="c8e99-113">Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c8e99-113">Read properties and relationships of the [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) object.</span></span>|
|[<span data-ttu-id="c8e99-114">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="c8e99-114">targetApps action</span></span>](../api/intune_mam_managedapppolicy_targetapps.md)|<span data-ttu-id="c8e99-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c8e99-115">None</span></span>|<span data-ttu-id="c8e99-116">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c8e99-116">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="c8e99-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8e99-117">Properties</span></span>
|<span data-ttu-id="c8e99-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8e99-118">Property</span></span>|<span data-ttu-id="c8e99-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8e99-119">Type</span></span>|<span data-ttu-id="c8e99-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8e99-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c8e99-121">displayName</span><span class="sxs-lookup"><span data-stu-id="c8e99-121">displayName</span></span>|<span data-ttu-id="c8e99-122">String</span><span class="sxs-lookup"><span data-stu-id="c8e99-122">String</span></span>|<span data-ttu-id="c8e99-123">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c8e99-123">Policy display name.</span></span>|
|<span data-ttu-id="c8e99-124">descripción</span><span class="sxs-lookup"><span data-stu-id="c8e99-124">description</span></span>|<span data-ttu-id="c8e99-125">String</span><span class="sxs-lookup"><span data-stu-id="c8e99-125">String</span></span>|<span data-ttu-id="c8e99-126">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c8e99-126">The policy's description.</span></span>|
|<span data-ttu-id="c8e99-127">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c8e99-127">createdDateTime</span></span>|<span data-ttu-id="c8e99-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8e99-128">DateTimeOffset</span></span>|<span data-ttu-id="c8e99-129">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c8e99-129">The date and time the policy was created.</span></span>|
|<span data-ttu-id="c8e99-130">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c8e99-130">lastModifiedDateTime</span></span>|<span data-ttu-id="c8e99-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8e99-131">DateTimeOffset</span></span>|<span data-ttu-id="c8e99-132">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="c8e99-132">Last time the policy was modified.</span></span>|
|<span data-ttu-id="c8e99-133">id</span><span class="sxs-lookup"><span data-stu-id="c8e99-133">id</span></span>|<span data-ttu-id="c8e99-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8e99-134">String</span></span>|<span data-ttu-id="c8e99-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c8e99-135">Key of the entity.</span></span>|
|<span data-ttu-id="c8e99-136">version</span><span class="sxs-lookup"><span data-stu-id="c8e99-136">version</span></span>|<span data-ttu-id="c8e99-137">String</span><span class="sxs-lookup"><span data-stu-id="c8e99-137">String</span></span>|<span data-ttu-id="c8e99-138">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c8e99-138">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c8e99-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c8e99-139">Relationships</span></span>
<span data-ttu-id="c8e99-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c8e99-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c8e99-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c8e99-141">JSON Representation</span></span>
<span data-ttu-id="c8e99-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c8e99-142">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "abstract": true,
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.managedAppPolicy"
}-->
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




# <a name="managedapppolicy-resource-type"></a><span data-ttu-id="f644c-101">Tipo de recurso managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="f644c-101">managedAppPolicy resource type</span></span>

> <span data-ttu-id="f644c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f644c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f644c-103">El recurso ManagedAppPolicy representa un tipo base para las directivas específicas de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="f644c-103">The ManagedAppPolicy resource represents a base type for platform specific policies.</span></span>
## <a name="methods"></a><span data-ttu-id="f644c-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="f644c-104">Methods</span></span>
|<span data-ttu-id="f644c-105">Método</span><span class="sxs-lookup"><span data-stu-id="f644c-105">Method</span></span>|<span data-ttu-id="f644c-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f644c-106">Return Type</span></span>|<span data-ttu-id="f644c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f644c-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="f644c-108">Enumerar managedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="f644c-108">List managedAppPolicies</span></span>](../api/intune_mam_managedapppolicy_list.md)|<span data-ttu-id="f644c-109">Colección [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f644c-109">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) collection</span></span>|<span data-ttu-id="f644c-110">Enumere las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f644c-110">List properties and relationships of the [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) objects.</span></span>|
|[<span data-ttu-id="f644c-111">Obtener managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="f644c-111">Get managedAppPolicy</span></span>](../api/intune_mam_managedapppolicy_get.md)|[<span data-ttu-id="f644c-112">managedAppPolicy</span><span class="sxs-lookup"><span data-stu-id="f644c-112">managedAppPolicy</span></span>](../resources/intune_mam_managedapppolicy.md)|<span data-ttu-id="f644c-113">Incluya en una lista las propiedades y las relaciones de los objetos [managedAppPolicy](../resources/intune_mam_managedapppolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f644c-113">Read properties and relationships of the [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) object.</span></span>|
|[<span data-ttu-id="f644c-114">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="f644c-114">targetApps action</span></span>](../api/intune_mam_managedapppolicy_targetapps.md)|<span data-ttu-id="f644c-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f644c-115">None</span></span>|<span data-ttu-id="f644c-116">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f644c-116">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="f644c-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f644c-117">Properties</span></span>
|<span data-ttu-id="f644c-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f644c-118">Property</span></span>|<span data-ttu-id="f644c-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="f644c-119">Type</span></span>|<span data-ttu-id="f644c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f644c-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f644c-121">displayName</span><span class="sxs-lookup"><span data-stu-id="f644c-121">displayName</span></span>|<span data-ttu-id="f644c-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="f644c-122">String</span></span>|<span data-ttu-id="f644c-123">Nombre para mostrar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f644c-123">Policy display name.</span></span>|
|<span data-ttu-id="f644c-124">descripción</span><span class="sxs-lookup"><span data-stu-id="f644c-124">description</span></span>|<span data-ttu-id="f644c-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="f644c-125">String</span></span>|<span data-ttu-id="f644c-126">La descripción de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f644c-126">The policy's description.</span></span>|
|<span data-ttu-id="f644c-127">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f644c-127">createdDateTime</span></span>|<span data-ttu-id="f644c-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f644c-128">DateTimeOffset</span></span>|<span data-ttu-id="f644c-129">La fecha y la hora de creación de la directiva.</span><span class="sxs-lookup"><span data-stu-id="f644c-129">The date and time the policy was created.</span></span>|
|<span data-ttu-id="f644c-130">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f644c-130">lastModifiedDateTime</span></span>|<span data-ttu-id="f644c-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f644c-131">DateTimeOffset</span></span>|<span data-ttu-id="f644c-132">Última vez que se modificó la directiva.</span><span class="sxs-lookup"><span data-stu-id="f644c-132">Last time the policy was modified.</span></span>|
|<span data-ttu-id="f644c-133">id</span><span class="sxs-lookup"><span data-stu-id="f644c-133">id</span></span>|<span data-ttu-id="f644c-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="f644c-134">String</span></span>|<span data-ttu-id="f644c-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f644c-135">Key of the entity.</span></span>|
|<span data-ttu-id="f644c-136">version</span><span class="sxs-lookup"><span data-stu-id="f644c-136">version</span></span>|<span data-ttu-id="f644c-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="f644c-137">String</span></span>|<span data-ttu-id="f644c-138">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f644c-138">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f644c-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f644c-139">Relationships</span></span>
<span data-ttu-id="f644c-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f644c-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f644c-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f644c-141">JSON Representation</span></span>
<span data-ttu-id="f644c-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f644c-142">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
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









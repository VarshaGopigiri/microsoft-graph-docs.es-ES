# <a name="devicemanagement-resource-type"></a><span data-ttu-id="a6ec9-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="a6ec9-101">deviceManagement resource type</span></span>

> <span data-ttu-id="a6ec9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a6ec9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a6ec9-103">Entidad singleton que actúa como un contenedor para la funcionalidad de configuración de Android for Work en la administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a6ec9-103">Singleton entity that acts as a container for Android for Work settings functionality under device management.</span></span>
## <a name="methods"></a><span data-ttu-id="a6ec9-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="a6ec9-104">Methods</span></span>
|<span data-ttu-id="a6ec9-105">Método</span><span class="sxs-lookup"><span data-stu-id="a6ec9-105">Method</span></span>|<span data-ttu-id="a6ec9-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6ec9-106">Return Type</span></span>|<span data-ttu-id="a6ec9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6ec9-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="a6ec9-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="a6ec9-108">Get deviceManagement</span></span>](../api/intune_androidforwork_devicemanagement_get.md)|[<span data-ttu-id="a6ec9-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="a6ec9-109">deviceManagement</span></span>](../resources/intune_androidforwork_devicemanagement.md)|<span data-ttu-id="a6ec9-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_androidforwork_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="a6ec9-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_androidforwork_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="a6ec9-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="a6ec9-111">Update deviceManagement</span></span>](../api/intune_androidforwork_devicemanagement_update.md)|[<span data-ttu-id="a6ec9-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="a6ec9-112">deviceManagement</span></span>](../resources/intune_androidforwork_devicemanagement.md)|<span data-ttu-id="a6ec9-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_androidforwork_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="a6ec9-113">Update the properties of a [calendar](../resources/intune_androidforwork_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="a6ec9-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a6ec9-114">Properties</span></span>
|<span data-ttu-id="a6ec9-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a6ec9-115">Property</span></span>|<span data-ttu-id="a6ec9-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6ec9-116">Type</span></span>|<span data-ttu-id="a6ec9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6ec9-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a6ec9-118">id</span><span class="sxs-lookup"><span data-stu-id="a6ec9-118">id</span></span>|<span data-ttu-id="a6ec9-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="a6ec9-119">String</span></span>|<span data-ttu-id="a6ec9-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a6ec9-120">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="a6ec9-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a6ec9-121">Relationships</span></span>
|<span data-ttu-id="a6ec9-122">Relación</span><span class="sxs-lookup"><span data-stu-id="a6ec9-122">Relationship</span></span>|<span data-ttu-id="a6ec9-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6ec9-123">Type</span></span>|<span data-ttu-id="a6ec9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6ec9-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a6ec9-125">androidForWorkSettings</span><span class="sxs-lookup"><span data-stu-id="a6ec9-125">androidForWorkSettings</span></span>|[<span data-ttu-id="a6ec9-126">androidForWorkSettings</span><span class="sxs-lookup"><span data-stu-id="a6ec9-126">androidForWorkSettings</span></span>](../resources/intune_androidforwork_androidforworksettings.md)|<span data-ttu-id="a6ec9-127">La entidad singleton de configuración de Android for Work.</span><span class="sxs-lookup"><span data-stu-id="a6ec9-127">The singleton Android for Work settings entity.</span></span>|
|<span data-ttu-id="a6ec9-128">androidForWorkAppConfigurationSchemas</span><span class="sxs-lookup"><span data-stu-id="a6ec9-128">androidForWorkAppConfigurationSchemas</span></span>|<span data-ttu-id="a6ec9-129">Colección [androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md)</span><span class="sxs-lookup"><span data-stu-id="a6ec9-129">[androidForWorkAppConfigurationSchema](../resources/intune_androidforwork_androidforworkappconfigurationschema.md) collection</span></span>|<span data-ttu-id="a6ec9-130">Entidades de esquema de configuración de la aplicación Android for Work.</span><span class="sxs-lookup"><span data-stu-id="a6ec9-130">Android for Work app configuration schema entities.</span></span>|
|<span data-ttu-id="a6ec9-131">androidForWorkEnrollmentProfiles</span><span class="sxs-lookup"><span data-stu-id="a6ec9-131">androidForWorkEnrollmentProfiles</span></span>|<span data-ttu-id="a6ec9-132">Colección [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="a6ec9-132">[androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md) collection</span></span>|<span data-ttu-id="a6ec9-133">Entidades del perfil de inscripción de Android for Work</span><span class="sxs-lookup"><span data-stu-id="a6ec9-133">Android for Work enrollment profile entities.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a6ec9-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a6ec9-134">JSON Representation</span></span>
<span data-ttu-id="a6ec9-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a6ec9-135">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)"
}
```




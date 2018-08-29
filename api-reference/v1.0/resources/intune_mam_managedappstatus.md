# <a name="managedappstatus-resource-type"></a><span data-ttu-id="b68b3-101">Tipo de recurso managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="b68b3-101">managedAppStatus resource type</span></span>

> <span data-ttu-id="b68b3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b68b3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b68b3-103">Representa el estado de protección y configuración de la aplicación para la organización.</span><span class="sxs-lookup"><span data-stu-id="b68b3-103">Represents app protection and configuration status for the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="b68b3-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="b68b3-104">Methods</span></span>
|<span data-ttu-id="b68b3-105">Método</span><span class="sxs-lookup"><span data-stu-id="b68b3-105">Method</span></span>|<span data-ttu-id="b68b3-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b68b3-106">Return Type</span></span>|<span data-ttu-id="b68b3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b68b3-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="b68b3-108">Enumerar managedAppStatuses</span><span class="sxs-lookup"><span data-stu-id="b68b3-108">List managedAppStatuses</span></span>](../api/intune_mam_managedappstatus_list.md)|<span data-ttu-id="b68b3-109">Colección [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="b68b3-109">[managedAppStatus](../resources/intune_mam_managedappstatus.md) collection</span></span>|<span data-ttu-id="b68b3-110">Enumere las propiedades y las relaciones de los objetos [managedAppStatus](../resources/intune_mam_managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="b68b3-110">List properties and relationships of the [managedAppStatus](../resources/intune_mam_managedappstatus.md) objects.</span></span>|
|[<span data-ttu-id="b68b3-111">Obtener managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="b68b3-111">Get managedAppStatus</span></span>](../api/intune_mam_managedappstatus_get.md)|[<span data-ttu-id="b68b3-112">managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="b68b3-112">managedAppStatus</span></span>](../resources/intune_mam_managedappstatus.md)|<span data-ttu-id="b68b3-113">Lea las propiedades y las relaciones del objeto [managedAppStatus](../resources/intune_mam_managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="b68b3-113">Read properties and relationships of the [managedAppStatus](../resources/intune_mam_managedappstatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="b68b3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b68b3-114">Properties</span></span>
|<span data-ttu-id="b68b3-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b68b3-115">Property</span></span>|<span data-ttu-id="b68b3-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="b68b3-116">Type</span></span>|<span data-ttu-id="b68b3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b68b3-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b68b3-118">displayName</span><span class="sxs-lookup"><span data-stu-id="b68b3-118">displayName</span></span>|<span data-ttu-id="b68b3-119">String</span><span class="sxs-lookup"><span data-stu-id="b68b3-119">String</span></span>|<span data-ttu-id="b68b3-120">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="b68b3-120">Friendly name of the status report.</span></span>|
|<span data-ttu-id="b68b3-121">id</span><span class="sxs-lookup"><span data-stu-id="b68b3-121">id</span></span>|<span data-ttu-id="b68b3-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="b68b3-122">String</span></span>|<span data-ttu-id="b68b3-123">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b68b3-123">Key of the entity.</span></span>|
|<span data-ttu-id="b68b3-124">version</span><span class="sxs-lookup"><span data-stu-id="b68b3-124">version</span></span>|<span data-ttu-id="b68b3-125">String</span><span class="sxs-lookup"><span data-stu-id="b68b3-125">String</span></span>|<span data-ttu-id="b68b3-126">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b68b3-126">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b68b3-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b68b3-127">Relationships</span></span>
<span data-ttu-id="b68b3-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b68b3-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b68b3-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b68b3-129">JSON Representation</span></span>
<span data-ttu-id="b68b3-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b68b3-130">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "abstract": true,
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.managedAppStatus"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppStatus",
  "displayName": "String",
  "id": "String (identifier)",
  "version": "String"
}
```




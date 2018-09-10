# <a name="managedappstatus-resource-type"></a><span data-ttu-id="6fcb6-101">Tipo de recurso managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="6fcb6-101">managedAppStatus resource type</span></span>

> <span data-ttu-id="6fcb6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6fcb6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6fcb6-103">Representa el estado de protección y configuración de la aplicación para la organización.</span><span class="sxs-lookup"><span data-stu-id="6fcb6-103">Represents app protection and configuration status for the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="6fcb6-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="6fcb6-104">Methods</span></span>
|<span data-ttu-id="6fcb6-105">Método</span><span class="sxs-lookup"><span data-stu-id="6fcb6-105">Method</span></span>|<span data-ttu-id="6fcb6-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fcb6-106">Return Type</span></span>|<span data-ttu-id="6fcb6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fcb6-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="6fcb6-108">Enumerar managedAppStatuses</span><span class="sxs-lookup"><span data-stu-id="6fcb6-108">List managedAppStatuses</span></span>](../api/intune_mam_managedappstatus_list.md)|<span data-ttu-id="6fcb6-109">Colección [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="6fcb6-109">[managedAppStatus](../resources/intune_mam_managedappstatus.md) collection</span></span>|<span data-ttu-id="6fcb6-110">Enumere las propiedades y las relaciones de los objetos [managedAppStatus](../resources/intune_mam_managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="6fcb6-110">List properties and relationships of the [managedAppStatus](../resources/intune_mam_managedappstatus.md) objects.</span></span>|
|[<span data-ttu-id="6fcb6-111">Obtener managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="6fcb6-111">Get managedAppStatus</span></span>](../api/intune_mam_managedappstatus_get.md)|[<span data-ttu-id="6fcb6-112">managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="6fcb6-112">managedAppStatus</span></span>](../resources/intune_mam_managedappstatus.md)|<span data-ttu-id="6fcb6-113">Lea las propiedades y las relaciones del objeto [managedAppStatus](../resources/intune_mam_managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="6fcb6-113">Read properties and relationships of the [managedAppStatus](../resources/intune_mam_managedappstatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="6fcb6-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6fcb6-114">Properties</span></span>
|<span data-ttu-id="6fcb6-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6fcb6-115">Property</span></span>|<span data-ttu-id="6fcb6-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="6fcb6-116">Type</span></span>|<span data-ttu-id="6fcb6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fcb6-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6fcb6-118">displayName</span><span class="sxs-lookup"><span data-stu-id="6fcb6-118">displayName</span></span>|<span data-ttu-id="6fcb6-119">String</span><span class="sxs-lookup"><span data-stu-id="6fcb6-119">String</span></span>|<span data-ttu-id="6fcb6-120">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="6fcb6-120">Friendly name of the status report.</span></span>|
|<span data-ttu-id="6fcb6-121">id</span><span class="sxs-lookup"><span data-stu-id="6fcb6-121">id</span></span>|<span data-ttu-id="6fcb6-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="6fcb6-122">String</span></span>|<span data-ttu-id="6fcb6-123">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6fcb6-123">Key of the entity.</span></span>|
|<span data-ttu-id="6fcb6-124">version</span><span class="sxs-lookup"><span data-stu-id="6fcb6-124">version</span></span>|<span data-ttu-id="6fcb6-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="6fcb6-125">String</span></span>|<span data-ttu-id="6fcb6-126">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6fcb6-126">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6fcb6-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6fcb6-127">Relationships</span></span>
<span data-ttu-id="6fcb6-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6fcb6-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6fcb6-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6fcb6-129">JSON Representation</span></span>
<span data-ttu-id="6fcb6-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6fcb6-130">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
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









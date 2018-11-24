# <a name="managedappstatus-resource-type"></a><span data-ttu-id="030ce-101">Tipo de recurso managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="030ce-101">managedAppStatus resource type</span></span>

> <span data-ttu-id="030ce-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="030ce-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="030ce-103">Representa el estado de protección y configuración de la aplicación para la organización.</span><span class="sxs-lookup"><span data-stu-id="030ce-103">Represents app protection and configuration status for the organization.</span></span>
## <a name="methods"></a><span data-ttu-id="030ce-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="030ce-104">Methods</span></span>
|<span data-ttu-id="030ce-105">Método</span><span class="sxs-lookup"><span data-stu-id="030ce-105">Method</span></span>|<span data-ttu-id="030ce-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="030ce-106">Return Type</span></span>|<span data-ttu-id="030ce-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="030ce-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="030ce-108">Enumerar managedAppStatuses</span><span class="sxs-lookup"><span data-stu-id="030ce-108">List managedAppStatuses</span></span>](../api/intune_mam_managedappstatus_list.md)|<span data-ttu-id="030ce-109">Colección [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="030ce-109">[managedAppStatus](../resources/intune_mam_managedappstatus.md) collection</span></span>|<span data-ttu-id="030ce-110">Enumere las propiedades y las relaciones de los objetos [managedAppStatus](../resources/intune_mam_managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="030ce-110">List properties and relationships of the [managedAppStatus](../resources/intune_mam_managedappstatus.md) objects.</span></span>|
|[<span data-ttu-id="030ce-111">Obtener managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="030ce-111">Get managedAppStatus</span></span>](../api/intune_mam_managedappstatus_get.md)|[<span data-ttu-id="030ce-112">managedAppStatus</span><span class="sxs-lookup"><span data-stu-id="030ce-112">managedAppStatus</span></span>](../resources/intune_mam_managedappstatus.md)|<span data-ttu-id="030ce-113">Lea las propiedades y las relaciones del objeto [managedAppStatus](../resources/intune_mam_managedappstatus.md).</span><span class="sxs-lookup"><span data-stu-id="030ce-113">Read properties and relationships of the [managedAppStatus](../resources/intune_mam_managedappstatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="030ce-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="030ce-114">Properties</span></span>
|<span data-ttu-id="030ce-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="030ce-115">Property</span></span>|<span data-ttu-id="030ce-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="030ce-116">Type</span></span>|<span data-ttu-id="030ce-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="030ce-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="030ce-118">displayName</span><span class="sxs-lookup"><span data-stu-id="030ce-118">displayName</span></span>|<span data-ttu-id="030ce-119">cadena</span><span class="sxs-lookup"><span data-stu-id="030ce-119">String</span></span>|<span data-ttu-id="030ce-120">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="030ce-120">Friendly name of the status report.</span></span>|
|<span data-ttu-id="030ce-121">id</span><span class="sxs-lookup"><span data-stu-id="030ce-121">id</span></span>|<span data-ttu-id="030ce-122">cadena</span><span class="sxs-lookup"><span data-stu-id="030ce-122">String</span></span>|<span data-ttu-id="030ce-123">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="030ce-123">Key of the entity.</span></span>|
|<span data-ttu-id="030ce-124">versión</span><span class="sxs-lookup"><span data-stu-id="030ce-124">version</span></span>|<span data-ttu-id="030ce-125">cadena</span><span class="sxs-lookup"><span data-stu-id="030ce-125">String</span></span>|<span data-ttu-id="030ce-126">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="030ce-126">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="030ce-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="030ce-127">Relationships</span></span>
<span data-ttu-id="030ce-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="030ce-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="030ce-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="030ce-129">JSON Representation</span></span>
<span data-ttu-id="030ce-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="030ce-130">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppStatus",
  "displayName": "String",
  "id": "String (identifier)",
  "version": "String"
}
```




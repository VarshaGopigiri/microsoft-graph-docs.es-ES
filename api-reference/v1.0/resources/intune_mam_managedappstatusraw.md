# <a name="managedappstatusraw-resource-type"></a><span data-ttu-id="39061-101">Tipo de recurso managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="39061-101">managedAppStatusRaw resource type</span></span>

> <span data-ttu-id="39061-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39061-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39061-103">Representa un informe de estado sin tipo sobre la configuración y la protección de la aplicación de las organizaciones.</span><span class="sxs-lookup"><span data-stu-id="39061-103">Represents an un-typed status report about organizations app protection and configuration.</span></span>

<span data-ttu-id="39061-104">Hereda de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="39061-104">Inherits from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>

## <a name="methods"></a><span data-ttu-id="39061-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="39061-105">Methods</span></span>
|<span data-ttu-id="39061-106">Método</span><span class="sxs-lookup"><span data-stu-id="39061-106">Method</span></span>|<span data-ttu-id="39061-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39061-107">Return Type</span></span>|<span data-ttu-id="39061-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="39061-108">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="39061-109">Enumerar managedAppStatusRaws</span><span class="sxs-lookup"><span data-stu-id="39061-109">List managedAppStatusRaws</span></span>](../api/intune_mam_managedappstatusraw_list.md)|<span data-ttu-id="39061-110">Colección [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md)</span><span class="sxs-lookup"><span data-stu-id="39061-110">[managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) collection</span></span>|<span data-ttu-id="39061-111">Enumere las propiedades y las relaciones de los objetos [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="39061-111">List properties and relationships of the [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) objects.</span></span>|
|[<span data-ttu-id="39061-112">Obtener managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="39061-112">Get managedAppStatusRaw</span></span>](../api/intune_mam_managedappstatusraw_get.md)|[<span data-ttu-id="39061-113">managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="39061-113">managedAppStatusRaw</span></span>](../resources/intune_mam_managedappstatusraw.md)|<span data-ttu-id="39061-114">Lea las propiedades y las relaciones del objeto [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="39061-114">Read properties and relationships of the [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="39061-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39061-115">Properties</span></span>
|<span data-ttu-id="39061-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39061-116">Property</span></span>|<span data-ttu-id="39061-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="39061-117">Type</span></span>|<span data-ttu-id="39061-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="39061-118">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="39061-119">displayName</span><span class="sxs-lookup"><span data-stu-id="39061-119">displayName</span></span>|<span data-ttu-id="39061-120">String</span><span class="sxs-lookup"><span data-stu-id="39061-120">String</span></span>|<span data-ttu-id="39061-121">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="39061-121">Friendly name of the status report.</span></span> <span data-ttu-id="39061-122">Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="39061-122">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="39061-123">id</span><span class="sxs-lookup"><span data-stu-id="39061-123">id</span></span>|<span data-ttu-id="39061-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="39061-124">String</span></span>|<span data-ttu-id="39061-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="39061-125">Key of the entity.</span></span> <span data-ttu-id="39061-126">Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="39061-126">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="39061-127">version</span><span class="sxs-lookup"><span data-stu-id="39061-127">version</span></span>|<span data-ttu-id="39061-128">String</span><span class="sxs-lookup"><span data-stu-id="39061-128">String</span></span>|<span data-ttu-id="39061-129">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="39061-129">Version of the entity.</span></span> <span data-ttu-id="39061-130">Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="39061-130">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="39061-131">content</span><span class="sxs-lookup"><span data-stu-id="39061-131">content</span></span>|[<span data-ttu-id="39061-132">Json</span><span class="sxs-lookup"><span data-stu-id="39061-132">Json</span></span>](../resources/intune_mam_json.md)|<span data-ttu-id="39061-133">Contenido del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="39061-133">Status report content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="39061-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="39061-134">Relationships</span></span>
<span data-ttu-id="39061-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="39061-135">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="39061-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="39061-136">JSON Representation</span></span>
<span data-ttu-id="39061-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="39061-137">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.managedAppStatus",
  "@odata.type": "microsoft.graph.managedAppStatusRaw"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppStatusRaw",
  "displayName": "String",
  "id": "String (identifier)",
  "version": "String",
  "content": {
    "@odata.type": "microsoft.graph.Json"
  }
}
```




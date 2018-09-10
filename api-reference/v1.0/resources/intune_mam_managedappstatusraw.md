# <a name="managedappstatusraw-resource-type"></a><span data-ttu-id="16c62-101">Tipo de recurso managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="16c62-101">managedAppStatusRaw resource type</span></span>

> <span data-ttu-id="16c62-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16c62-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16c62-103">Representa un informe de estado sin tipo sobre la configuración y la protección de la aplicación de las organizaciones.</span><span class="sxs-lookup"><span data-stu-id="16c62-103">Represents an un-typed status report about organizations app protection and configuration.</span></span>

<span data-ttu-id="16c62-104">Hereda de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="16c62-104">Inherits from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>

## <a name="methods"></a><span data-ttu-id="16c62-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="16c62-105">Methods</span></span>
|<span data-ttu-id="16c62-106">Método</span><span class="sxs-lookup"><span data-stu-id="16c62-106">Method</span></span>|<span data-ttu-id="16c62-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16c62-107">Return Type</span></span>|<span data-ttu-id="16c62-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="16c62-108">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="16c62-109">Enumerar managedAppStatusRaws</span><span class="sxs-lookup"><span data-stu-id="16c62-109">List managedAppStatusRaws</span></span>](../api/intune_mam_managedappstatusraw_list.md)|<span data-ttu-id="16c62-110">Colección [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md)</span><span class="sxs-lookup"><span data-stu-id="16c62-110">[managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) collection</span></span>|<span data-ttu-id="16c62-111">Enumere las propiedades y las relaciones de los objetos [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="16c62-111">List properties and relationships of the [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) objects.</span></span>|
|[<span data-ttu-id="16c62-112">Obtener managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="16c62-112">Get managedAppStatusRaw</span></span>](../api/intune_mam_managedappstatusraw_get.md)|[<span data-ttu-id="16c62-113">managedAppStatusRaw</span><span class="sxs-lookup"><span data-stu-id="16c62-113">managedAppStatusRaw</span></span>](../resources/intune_mam_managedappstatusraw.md)|<span data-ttu-id="16c62-114">Lea las propiedades y las relaciones del objeto [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md).</span><span class="sxs-lookup"><span data-stu-id="16c62-114">Read properties and relationships of the [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="16c62-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16c62-115">Properties</span></span>
|<span data-ttu-id="16c62-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16c62-116">Property</span></span>|<span data-ttu-id="16c62-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="16c62-117">Type</span></span>|<span data-ttu-id="16c62-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="16c62-118">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16c62-119">displayName</span><span class="sxs-lookup"><span data-stu-id="16c62-119">displayName</span></span>|<span data-ttu-id="16c62-120">String</span><span class="sxs-lookup"><span data-stu-id="16c62-120">String</span></span>|<span data-ttu-id="16c62-121">Nombre descriptivo del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="16c62-121">Friendly name of the status report.</span></span> <span data-ttu-id="16c62-122">Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="16c62-122">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="16c62-123">id</span><span class="sxs-lookup"><span data-stu-id="16c62-123">id</span></span>|<span data-ttu-id="16c62-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="16c62-124">String</span></span>|<span data-ttu-id="16c62-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="16c62-125">Key of the entity.</span></span> <span data-ttu-id="16c62-126">Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="16c62-126">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="16c62-127">version</span><span class="sxs-lookup"><span data-stu-id="16c62-127">version</span></span>|<span data-ttu-id="16c62-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="16c62-128">String</span></span>|<span data-ttu-id="16c62-129">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="16c62-129">Version of the entity.</span></span> <span data-ttu-id="16c62-130">Heredado de [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span><span class="sxs-lookup"><span data-stu-id="16c62-130">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="16c62-131">content</span><span class="sxs-lookup"><span data-stu-id="16c62-131">content</span></span>|[<span data-ttu-id="16c62-132">Json</span><span class="sxs-lookup"><span data-stu-id="16c62-132">Json</span></span>](../resources/json.md)|<span data-ttu-id="16c62-133">Contenido del informe de estado.</span><span class="sxs-lookup"><span data-stu-id="16c62-133">Status report content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="16c62-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="16c62-134">Relationships</span></span>
<span data-ttu-id="16c62-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="16c62-135">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="16c62-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="16c62-136">JSON Representation</span></span>
<span data-ttu-id="16c62-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="16c62-137">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.managedAppStatus",
  "keyProperty": "id",
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









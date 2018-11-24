# <a name="deviceactionresult-resource-type"></a><span data-ttu-id="dfba9-101">Tipo de recurso deviceActionResult</span><span class="sxs-lookup"><span data-stu-id="dfba9-101">deviceActionResult resource type</span></span>

> <span data-ttu-id="dfba9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dfba9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dfba9-103">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="dfba9-103">Device action result</span></span>
## <a name="properties"></a><span data-ttu-id="dfba9-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dfba9-104">Properties</span></span>
|<span data-ttu-id="dfba9-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dfba9-105">Property</span></span>|<span data-ttu-id="dfba9-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfba9-106">Type</span></span>|<span data-ttu-id="dfba9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfba9-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dfba9-108">actionName</span><span class="sxs-lookup"><span data-stu-id="dfba9-108">actionName</span></span>|<span data-ttu-id="dfba9-109">cadena</span><span class="sxs-lookup"><span data-stu-id="dfba9-109">String</span></span>|<span data-ttu-id="dfba9-110">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="dfba9-110">Action name</span></span>|
|<span data-ttu-id="dfba9-111">actionState</span><span class="sxs-lookup"><span data-stu-id="dfba9-111">actionState</span></span>|[<span data-ttu-id="dfba9-112">actionState</span><span class="sxs-lookup"><span data-stu-id="dfba9-112">actionState</span></span>](../resources/intune_devices_actionstate.md)|<span data-ttu-id="dfba9-113">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="dfba9-113">State of the action.</span></span> <span data-ttu-id="dfba9-114">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="dfba9-114">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="dfba9-115">startDateTime</span><span class="sxs-lookup"><span data-stu-id="dfba9-115">startDateTime</span></span>|<span data-ttu-id="dfba9-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dfba9-116">DateTimeOffset</span></span>|<span data-ttu-id="dfba9-117">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="dfba9-117">Time the action was initiated</span></span>|
|<span data-ttu-id="dfba9-118">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="dfba9-118">lastUpdatedDateTime</span></span>|<span data-ttu-id="dfba9-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dfba9-119">DateTimeOffset</span></span>|<span data-ttu-id="dfba9-120">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="dfba9-120">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="dfba9-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dfba9-121">Relationships</span></span>
<span data-ttu-id="dfba9-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="dfba9-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="dfba9-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dfba9-123">JSON Representation</span></span>
<span data-ttu-id="dfba9-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dfba9-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)"
}
```




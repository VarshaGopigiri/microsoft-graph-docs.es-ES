# <a name="deviceactionresult-resource-type"></a><span data-ttu-id="6769b-101">Tipo de recurso deviceActionResult</span><span class="sxs-lookup"><span data-stu-id="6769b-101">deviceActionResult resource type</span></span>

> <span data-ttu-id="6769b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6769b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6769b-103">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6769b-103">Device action result</span></span>
## <a name="properties"></a><span data-ttu-id="6769b-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6769b-104">Properties</span></span>
|<span data-ttu-id="6769b-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6769b-105">Property</span></span>|<span data-ttu-id="6769b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="6769b-106">Type</span></span>|<span data-ttu-id="6769b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6769b-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6769b-108">actionName</span><span class="sxs-lookup"><span data-stu-id="6769b-108">actionName</span></span>|<span data-ttu-id="6769b-109">cadena</span><span class="sxs-lookup"><span data-stu-id="6769b-109">String</span></span>|<span data-ttu-id="6769b-110">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="6769b-110">Action name</span></span>|
|<span data-ttu-id="6769b-111">actionState</span><span class="sxs-lookup"><span data-stu-id="6769b-111">actionState</span></span>|[<span data-ttu-id="6769b-112">actionState</span><span class="sxs-lookup"><span data-stu-id="6769b-112">actionState</span></span>](../resources/intune_devices_actionstate.md)|<span data-ttu-id="6769b-p101">Estado de la acción. Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="6769b-p101">State of the action Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="6769b-115">startDateTime</span><span class="sxs-lookup"><span data-stu-id="6769b-115">startDateTime</span></span>|<span data-ttu-id="6769b-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6769b-116">DateTimeOffset</span></span>|<span data-ttu-id="6769b-117">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="6769b-117">Time the action was initiated</span></span>|
|<span data-ttu-id="6769b-118">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="6769b-118">lastUpdatedDateTime</span></span>|<span data-ttu-id="6769b-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6769b-119">DateTimeOffset</span></span>|<span data-ttu-id="6769b-120">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="6769b-120">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="6769b-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6769b-121">Relationships</span></span>
<span data-ttu-id="6769b-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6769b-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6769b-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6769b-123">JSON Representation</span></span>
<span data-ttu-id="6769b-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6769b-124">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceActionResult"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)"
}
```









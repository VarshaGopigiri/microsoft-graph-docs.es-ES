# <a name="importedwindowsautopilotdeviceidentitystate-resource-type"></a><span data-ttu-id="5480b-101">Tipo de recurso importedWindowsAutopilotDeviceIdentityState resource type</span><span class="sxs-lookup"><span data-stu-id="5480b-101">importedWindowsAutopilotDeviceIdentityState resource type</span></span>

> <span data-ttu-id="5480b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5480b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5480b-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="5480b-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="5480b-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5480b-104">Properties</span></span>
|<span data-ttu-id="5480b-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5480b-105">Property</span></span>|<span data-ttu-id="5480b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="5480b-106">Type</span></span>|<span data-ttu-id="5480b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5480b-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5480b-108">deviceImportStatus</span><span class="sxs-lookup"><span data-stu-id="5480b-108">deviceImportStatus</span></span>|[<span data-ttu-id="5480b-109">importedWindowsAutopilotDeviceIdentityImportStatus</span><span class="sxs-lookup"><span data-stu-id="5480b-109">importedWindowsAutopilotDeviceIdentityImportStatus</span></span>](../resources/intune_enrollment_importedwindowsautopilotdeviceidentityimportstatus.md)|<span data-ttu-id="5480b-p101">Estado del dispositivo notificado por el Servicio de administración de directorios (DDS). Los valores posibles son: `unknown`, `pending`, `partial`, `complete`, `error`.</span><span class="sxs-lookup"><span data-stu-id="5480b-p101">Device status reported by Device Directory Service(DDS). The possible values are: `unknown`, `pending`, `partial`, `complete`, `error`.</span></span>|
|<span data-ttu-id="5480b-112">deviceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="5480b-112">deviceRegistrationId</span></span>|<span data-ttu-id="5480b-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="5480b-113">String</span></span>|<span data-ttu-id="5480b-114">Identificador del registro del dispositivo para el dispositivo agregado correctamente notificado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="5480b-114">Device Registration ID for successfully added device reported by Device Directory Service(DDS).</span></span>|
|<span data-ttu-id="5480b-115">deviceErrorCode</span><span class="sxs-lookup"><span data-stu-id="5480b-115">deviceErrorCode</span></span>|<span data-ttu-id="5480b-116">Int32</span><span class="sxs-lookup"><span data-stu-id="5480b-116">Int32</span></span>|<span data-ttu-id="5480b-117">Código de error de dispositivo detectado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="5480b-117">Device error code reported by Device Directory Service(DDS).</span></span>|
|<span data-ttu-id="5480b-118">deviceErrorName</span><span class="sxs-lookup"><span data-stu-id="5480b-118">deviceErrorName</span></span>|<span data-ttu-id="5480b-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="5480b-119">String</span></span>|<span data-ttu-id="5480b-120">Nombre de error de dispositivo detectado por el servicio de directorio de dispositivo (DDS).</span><span class="sxs-lookup"><span data-stu-id="5480b-120">Device error name reported by Device Directory Service(DDS).</span></span>|

## <a name="relationships"></a><span data-ttu-id="5480b-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5480b-121">Relationships</span></span>
<span data-ttu-id="5480b-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5480b-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5480b-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5480b-123">JSON Representation</span></span>
<span data-ttu-id="5480b-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5480b-124">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
  "deviceImportStatus": "String",
  "deviceRegistrationId": "String",
  "deviceErrorCode": 1024,
  "deviceErrorName": "String"
}
```









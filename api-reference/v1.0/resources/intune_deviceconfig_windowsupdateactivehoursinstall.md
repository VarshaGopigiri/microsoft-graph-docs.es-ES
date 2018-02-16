# <a name="windowsupdateactivehoursinstall-resource-type"></a><span data-ttu-id="023fc-101">Tipo de recurso windowsUpdateActiveHoursInstall</span><span class="sxs-lookup"><span data-stu-id="023fc-101">windowsUpdateActiveHoursInstall resource type</span></span>

> <span data-ttu-id="023fc-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="023fc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="023fc-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="023fc-103">Not yet documented</span></span>

<span data-ttu-id="023fc-104">Hereda de [windowsUpdateInstallScheduleType](../resources/intune_deviceconfig_windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="023fc-104">Inherits from [windowsUpdateInstallScheduleType](../resources/intune_deviceconfig_windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="023fc-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="023fc-105">Properties</span></span>
|<span data-ttu-id="023fc-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="023fc-106">Property</span></span>|<span data-ttu-id="023fc-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="023fc-107">Type</span></span>|<span data-ttu-id="023fc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="023fc-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="023fc-109">activeHoursStart</span><span class="sxs-lookup"><span data-stu-id="023fc-109">activeHoursStart</span></span>|<span data-ttu-id="023fc-110">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="023fc-110">TimeOfDay</span></span>|<span data-ttu-id="023fc-111">Inicio de horas activas</span><span class="sxs-lookup"><span data-stu-id="023fc-111">Active Hours Start</span></span>|
|<span data-ttu-id="023fc-112">activeHoursEnd</span><span class="sxs-lookup"><span data-stu-id="023fc-112">activeHoursEnd</span></span>|<span data-ttu-id="023fc-113">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="023fc-113">TimeOfDay</span></span>|<span data-ttu-id="023fc-114">Fin de horas activas</span><span class="sxs-lookup"><span data-stu-id="023fc-114">Active Hours End</span></span>|

## <a name="relationships"></a><span data-ttu-id="023fc-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="023fc-115">Relationships</span></span>
<span data-ttu-id="023fc-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="023fc-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="023fc-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="023fc-117">JSON Representation</span></span>
<span data-ttu-id="023fc-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="023fc-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsUpdateActiveHoursInstall"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdateActiveHoursInstall",
  "activeHoursStart": "String (time of day)",
  "activeHoursEnd": "String (time of day)"
}
```




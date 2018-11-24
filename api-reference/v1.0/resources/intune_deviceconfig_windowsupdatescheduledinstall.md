# <a name="windowsupdatescheduledinstall-resource-type"></a><span data-ttu-id="0afa1-101">Tipo de recurso windowsUpdateScheduledInstall</span><span class="sxs-lookup"><span data-stu-id="0afa1-101">windowsUpdateScheduledInstall resource type</span></span>

> <span data-ttu-id="0afa1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0afa1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0afa1-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0afa1-103">Not yet documented</span></span>

<span data-ttu-id="0afa1-104">Hereda de [windowsUpdateInstallScheduleType](../resources/intune_deviceconfig_windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="0afa1-104">Inherits from [windowsUpdateInstallScheduleType](../resources/intune_deviceconfig_windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="0afa1-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0afa1-105">Properties</span></span>
|<span data-ttu-id="0afa1-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0afa1-106">Property</span></span>|<span data-ttu-id="0afa1-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0afa1-107">Type</span></span>|<span data-ttu-id="0afa1-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0afa1-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0afa1-109">scheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="0afa1-109">scheduledInstallDay</span></span>|[<span data-ttu-id="0afa1-110">weeklySchedule</span><span class="sxs-lookup"><span data-stu-id="0afa1-110">weeklySchedule</span></span>](../resources/intune_deviceconfig_weeklyschedule.md)|<span data-ttu-id="0afa1-111">Programada instalar día de la semana.</span><span class="sxs-lookup"><span data-stu-id="0afa1-111">Scheduled Install Day in week.</span></span> <span data-ttu-id="0afa1-112">Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.</span><span class="sxs-lookup"><span data-stu-id="0afa1-112">Possible values are: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="0afa1-113">scheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="0afa1-113">scheduledInstallTime</span></span>|<span data-ttu-id="0afa1-114">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="0afa1-114">TimeOfDay</span></span>|<span data-ttu-id="0afa1-115">Hora de instalación programada durante el día</span><span class="sxs-lookup"><span data-stu-id="0afa1-115">Scheduled Install Time during day</span></span>|

## <a name="relationships"></a><span data-ttu-id="0afa1-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0afa1-116">Relationships</span></span>
<span data-ttu-id="0afa1-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0afa1-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0afa1-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0afa1-118">JSON Representation</span></span>
<span data-ttu-id="0afa1-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0afa1-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdateScheduledInstall",
  "scheduledInstallDay": "String",
  "scheduledInstallTime": "String (time of day)"
}
```




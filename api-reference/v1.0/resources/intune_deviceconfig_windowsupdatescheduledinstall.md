# <a name="windowsupdatescheduledinstall-resource-type"></a><span data-ttu-id="13ed9-101">Tipo de recurso windowsUpdateScheduledInstall</span><span class="sxs-lookup"><span data-stu-id="13ed9-101">windowsUpdateScheduledInstall resource type</span></span>

> <span data-ttu-id="13ed9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="13ed9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="13ed9-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="13ed9-103">Not yet documented</span></span>

<span data-ttu-id="13ed9-104">Hereda de [windowsUpdateInstallScheduleType](../resources/intune_deviceconfig_windowsupdateinstallscheduletype.md)</span><span class="sxs-lookup"><span data-stu-id="13ed9-104">Inherits from [windowsUpdateInstallScheduleType](../resources/intune_deviceconfig_windowsupdateinstallscheduletype.md)</span></span>

## <a name="properties"></a><span data-ttu-id="13ed9-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13ed9-105">Properties</span></span>
|<span data-ttu-id="13ed9-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13ed9-106">Property</span></span>|<span data-ttu-id="13ed9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="13ed9-107">Type</span></span>|<span data-ttu-id="13ed9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="13ed9-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="13ed9-109">scheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="13ed9-109">scheduledInstallDay</span></span>|<span data-ttu-id="13ed9-110">cadena</span><span class="sxs-lookup"><span data-stu-id="13ed9-110">String</span></span>|<span data-ttu-id="13ed9-111">Día de instalación programada durante la semana. Los valores posibles son: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday` y `saturday`.</span><span class="sxs-lookup"><span data-stu-id="13ed9-111">Scheduled Install Day in week Possible values are: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="13ed9-112">scheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="13ed9-112">scheduledInstallTime</span></span>|<span data-ttu-id="13ed9-113">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="13ed9-113">TimeOfDay</span></span>|<span data-ttu-id="13ed9-114">Hora de instalación programada durante el día</span><span class="sxs-lookup"><span data-stu-id="13ed9-114">Scheduled Install Time during day</span></span>|

## <a name="relationships"></a><span data-ttu-id="13ed9-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="13ed9-115">Relationships</span></span>
<span data-ttu-id="13ed9-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="13ed9-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="13ed9-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="13ed9-117">JSON Representation</span></span>
<span data-ttu-id="13ed9-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="13ed9-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
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




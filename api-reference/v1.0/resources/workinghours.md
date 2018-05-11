# <a name="workinghours-resource-type"></a><span data-ttu-id="10310-101">Tipo de recurso workingHours</span><span class="sxs-lookup"><span data-stu-id="10310-101">workingHours resource type</span></span>

<span data-ttu-id="10310-102">Representa los días de la semana y las horas de la zona horaria específica en la que trabaja el usuario.</span><span class="sxs-lookup"><span data-stu-id="10310-102">Represents the days of the week and hours in a specific time zone that the user works.</span></span>

<span data-ttu-id="10310-103">Tener acceso al horario laboral de un usuario resulta útil en escenarios en los que se administran la planeación de recursos o actividades.</span><span class="sxs-lookup"><span data-stu-id="10310-103">Having access to a user's working hours is useful in scenarios that handle activity or resource planning.</span></span> <span data-ttu-id="10310-104">Puede [obtener](../api/user_get_mailboxsettings.md#request-3) y [establecer](../api/user_update_mailboxsettings.md#request-2) el horario laboral de un usuario como parte de la [configuración de buzón](mailboxSettings.md) del usuario.</span><span class="sxs-lookup"><span data-stu-id="10310-104">You can [get](../api/user_get_mailboxsettings.md#request-3) and [set](../api/user_update_mailboxsettings.md#request-2) the working hours of a user as part of the user's [mailbox settings](mailboxSettings.md).</span></span> 

<span data-ttu-id="10310-105">Puede establecer una zona horaria para el horario laboral distinta de la zona horaria que haya configurado en el cliente de Outlook.</span><span class="sxs-lookup"><span data-stu-id="10310-105">You can choose to set a time zone for your working hours differently from the time zone you have set on your Outlook client.</span></span> <span data-ttu-id="10310-106">Esto puede resultar útil, por ejemplo, si se desplaza a una zona horaria distinta de aquella en la que habitualmente trabaja.</span><span class="sxs-lookup"><span data-stu-id="10310-106">This can be useful in cases like when you travel to a different time zone than you usually work in.</span></span> <span data-ttu-id="10310-107">Puede establecer el cliente de Outlook</span><span class="sxs-lookup"><span data-stu-id="10310-107">You can set the Outlook client</span></span>  
<span data-ttu-id="10310-108">en la zona horaria de destino para que los valores de hora de Outlook se muestren en la hora local mientras está allí.</span><span class="sxs-lookup"><span data-stu-id="10310-108">to the destination time zone so that Outlook time values are displayed in local time while you are there.</span></span>
<span data-ttu-id="10310-109">Cuando otras personas solicitan reuniones de trabajo con usted en su lugar de trabajo habitual, aún pueden respetar su horario laboral en la zona horaria correspondiente.</span><span class="sxs-lookup"><span data-stu-id="10310-109">When other people request work meetings with you in your usual place of work, they can still respect your working hours in the appropriate time zone.</span></span>


## <a name="properties"></a><span data-ttu-id="10310-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10310-110">Properties</span></span>
| <span data-ttu-id="10310-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10310-111">Property</span></span>     | <span data-ttu-id="10310-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="10310-112">Type</span></span>   |<span data-ttu-id="10310-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="10310-113">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="10310-114">daysOfWeek</span><span class="sxs-lookup"><span data-stu-id="10310-114">daysOfWeek</span></span> | <span data-ttu-id="10310-115">Colección String</span><span class="sxs-lookup"><span data-stu-id="10310-115">String collection</span></span> | <span data-ttu-id="10310-116">Días de la semana en los que el usuario trabaja.</span><span class="sxs-lookup"><span data-stu-id="10310-116">The days of the week on which the user works.</span></span> |
| <span data-ttu-id="10310-117">startTime</span><span class="sxs-lookup"><span data-stu-id="10310-117"><starttime></span></span> | <span data-ttu-id="10310-118">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="10310-118">Edm.TimeOfDay</span></span> | <span data-ttu-id="10310-119">Hora del día en la que el usuario empieza a trabajar.</span><span class="sxs-lookup"><span data-stu-id="10310-119">The time of the day that the user starts working.</span></span> |
| <span data-ttu-id="10310-120">endTime</span><span class="sxs-lookup"><span data-stu-id="10310-120"><endtime></span></span> | <span data-ttu-id="10310-121">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="10310-121">Edm.TimeOfDay</span></span> | <span data-ttu-id="10310-122">Hora del día en la que el usuario deja de trabajar.</span><span class="sxs-lookup"><span data-stu-id="10310-122">The time of the day that the user stops working.</span></span> |
| <span data-ttu-id="10310-123">timeZone</span><span class="sxs-lookup"><span data-stu-id="10310-123">timeZone</span></span> | [<span data-ttu-id="10310-124">timeZoneBase</span><span class="sxs-lookup"><span data-stu-id="10310-124">timeZoneBase</span></span>](timezonebase.md) | <span data-ttu-id="10310-125">Zona horaria a la que se aplica el horario laboral.</span><span class="sxs-lookup"><span data-stu-id="10310-125">The time zone to which the working hours apply.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="10310-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="10310-126">JSON representation</span></span>

<span data-ttu-id="10310-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="10310-127">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workingHours"
}-->

```json
{
  "daysOfWeek": ["string"],
  "startTime": "TimeOfDay",
  "endTime": "TimeOfDay",
  "timeZone": {"@odata.type": "microsoft.graph.timeZoneBase"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "workingHours resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
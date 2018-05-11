# <a name="mailboxsettings-resource-type"></a><span data-ttu-id="df358-101">Tipo de recurso mailboxSettings</span><span class="sxs-lookup"><span data-stu-id="df358-101">mailboxSettings resource type</span></span>

<span data-ttu-id="df358-102">Configuración del buzón principal del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="df358-102">Settings for the primary mailbox of the signed-in user.</span></span>


## <a name="properties"></a><span data-ttu-id="df358-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df358-103">Properties</span></span>
| <span data-ttu-id="df358-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="df358-104">Property</span></span>     | <span data-ttu-id="df358-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="df358-105">Type</span></span>   |<span data-ttu-id="df358-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="df358-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="df358-107">archiveFolder</span><span class="sxs-lookup"><span data-stu-id="df358-107">archiveFolder</span></span>|<span data-ttu-id="df358-108">string</span><span class="sxs-lookup"><span data-stu-id="df358-108">string</span></span>|<span data-ttu-id="df358-109">Identificador de una carpeta de archivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="df358-109">Folder ID of an archive folder for the user.</span></span>|
|<span data-ttu-id="df358-110">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="df358-110">automaticRepliesSetting</span></span>|[<span data-ttu-id="df358-111">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="df358-111">automaticRepliesSetting</span></span>](automaticrepliessetting.md)|<span data-ttu-id="df358-112">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="df358-112">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user.</span></span>|
|<span data-ttu-id="df358-113">language</span><span class="sxs-lookup"><span data-stu-id="df358-113">language</span></span>|[<span data-ttu-id="df358-114">localeInfo</span><span class="sxs-lookup"><span data-stu-id="df358-114">localeInfo</span></span>](localeinfo.md)|<span data-ttu-id="df358-115">Representación de la configuración regional del usuario, como el idioma preferido y el país o región.</span><span class="sxs-lookup"><span data-stu-id="df358-115">The locale information for the user, including the preferred language and country/region.</span></span>|
|<span data-ttu-id="df358-116">timeZone</span><span class="sxs-lookup"><span data-stu-id="df358-116">timeZone</span></span>|<span data-ttu-id="df358-117">string</span><span class="sxs-lookup"><span data-stu-id="df358-117">string</span></span>|<span data-ttu-id="df358-118">Zona horaria predeterminada del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="df358-118">The default time zone for the user's mailbox.</span></span>|
|<span data-ttu-id="df358-119">workingHours</span><span class="sxs-lookup"><span data-stu-id="df358-119">workingHours</span></span>|[<span data-ttu-id="df358-120">workingHours</span><span class="sxs-lookup"><span data-stu-id="df358-120">workingHours</span></span>](workinghours.md)|<span data-ttu-id="df358-121">Días de la semana y horas de la zona horaria específica en la que trabaja el usuario.</span><span class="sxs-lookup"><span data-stu-id="df358-121">The days of the week and hours in a specific time zone that the user works.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="df358-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="df358-122">JSON representation</span></span>

<span data-ttu-id="df358-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="df358-123">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "archiveFolder"
  ],
  "@odata.type": "microsoft.graph.mailboxSettings"
}-->

```json
{
  "archiveFolder": "string",
  "automaticRepliesSetting": {"@odata.type": "microsoft.graph.automaticRepliesSetting"},
  "language": {"@odata.type": "microsoft.graph.localeInfo"},
  "timeZone": "string",
  "workingHours": {"@odata.type": "microsoft.graph.workingHours"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailboxSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
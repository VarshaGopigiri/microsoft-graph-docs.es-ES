# <a name="automaticrepliesmailtips-resource-type"></a><span data-ttu-id="a6658-101">Tipo de recurso automaticRepliesMailTips</span><span class="sxs-lookup"><span data-stu-id="a6658-101">automaticRepliesMailTips resource type</span></span>


<span data-ttu-id="a6658-102">[Sugerencias de correo electrónico](../resources/mailtips.md) acerca de las respuestas automáticas que se han configurado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a6658-102">[MailTips](../resources/mailtips.md) about any automatic replies that have been set up on a mailbox.</span></span>

## <a name="properties"></a><span data-ttu-id="a6658-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a6658-103">Properties</span></span>
| <span data-ttu-id="a6658-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a6658-104">Property</span></span>     | <span data-ttu-id="a6658-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6658-105">Type</span></span>   |<span data-ttu-id="a6658-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6658-106">Description</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a6658-107">message</span><span class="sxs-lookup"><span data-stu-id="a6658-107">message</span></span> | <span data-ttu-id="a6658-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="a6658-108">String</span></span> | <span data-ttu-id="a6658-109">El mensaje de respuesta automática.</span><span class="sxs-lookup"><span data-stu-id="a6658-109">The automatic reply message.</span></span> |
| <span data-ttu-id="a6658-110">messageLanguage</span><span class="sxs-lookup"><span data-stu-id="a6658-110">messageLanguage</span></span> | [<span data-ttu-id="a6658-111">localeInfo</span><span class="sxs-lookup"><span data-stu-id="a6658-111">localeInfo</span></span>](../resources/localeinfo.md) | <span data-ttu-id="a6658-112">El idioma en el que se encuentra el mensaje de respuesta automática.</span><span class="sxs-lookup"><span data-stu-id="a6658-112">The language that the automatic reply message is in.</span></span> |
| <span data-ttu-id="a6658-113">scheduledEndTime</span><span class="sxs-lookup"><span data-stu-id="a6658-113">ScheduledEndTime</span></span> | [<span data-ttu-id="a6658-114">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="a6658-114">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md) | <span data-ttu-id="a6658-115">La fecha y la hora en que las respuestas automáticas se configuran para finalizar.</span><span class="sxs-lookup"><span data-stu-id="a6658-115">The date and time that automatic replies are set to end, if Status is set to .</span></span> |
| <span data-ttu-id="a6658-116">scheduledStartTime</span><span class="sxs-lookup"><span data-stu-id="a6658-116">ScheduledStartTime</span></span> | [<span data-ttu-id="a6658-117">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="a6658-117">dateTimeTimeZone</span></span>](../resources/datetimetimezone.md) | <span data-ttu-id="a6658-118">La fecha y la hora en que las respuestas automáticas están configuradas para comenzar.</span><span class="sxs-lookup"><span data-stu-id="a6658-118">The date and time that automatic replies are set to begin, if Status is set to .</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a6658-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a6658-119">JSON representation</span></span>

<span data-ttu-id="a6658-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a6658-120">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "messageLanguage",
    "scheduledEndTime",
    "scheduledStartTime"
  ],
  "@odata.type": "microsoft.graph.automaticRepliesMailTips"
}-->

```json
{
  "message": "string",
  "messageLanguage": {"@odata.type": "microsoft.graph.localeInfo"},
  "scheduledEndTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "scheduledStartTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "automaticRepliesMailTips resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
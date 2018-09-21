# <a name="get-outlook-events-in-a-shared-or-delegated-calendar"></a><span data-ttu-id="09761-101">Obtener eventos de Outlook en un calendario compartido o delegado</span><span class="sxs-lookup"><span data-stu-id="09761-101">Get Outlook events in a shared or delegated calendar</span></span>

<span data-ttu-id="09761-102">En Outlook, los clientes pueden compartir un calendario con otros usuarios y permitirles ver o modificar los eventos de ese calendario.</span><span class="sxs-lookup"><span data-stu-id="09761-102">In Outlook, customers can share a calendar with other users and let them view or modify events in that calendar.</span></span> <span data-ttu-id="09761-103">Los clientes también pueden conceder un delegado para que actúe en su nombre, para recibir o responder a convocatorias de reunión, o crear o cambiar elementos en el calendario.</span><span class="sxs-lookup"><span data-stu-id="09761-103">Customers can also grant a delegate to act on their  behalf, to receive or respond to meeting requests, or create or change items in the calendar.</span></span>

<span data-ttu-id="09761-104">Mediante programación, Microsoft Graph permite obtener eventos de los calendarios que se han compartido por otros usuarios, así como los propios calendarios compartidos.</span><span class="sxs-lookup"><span data-stu-id="09761-104">Programmatically, Microsoft Graph supports getting messages in mail folders that have been shared by other users, as well as getting the shared folders themselves.</span></span> <span data-ttu-id="09761-105">La compatibilidad también se aplica a las carpetas que se han delegado.</span><span class="sxs-lookup"><span data-stu-id="09761-105">The support also applies to calendars that have been delegated.</span></span>

<span data-ttu-id="09761-106">Por ejemplo, Garth tiene compartido con John su calendario predeterminado y ha concedido a John acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="09761-106">As an example, Garth has shared with John his default calendar and given John read access.</span></span> <span data-ttu-id="09761-107">Si John ha iniciado sesión en su aplicación y ha proporcionado los permisos delegados (Calendars.Read.Shared o Calendars.ReadWrite.Shared), la aplicación podrá obtener acceso al calendario predeterminado de Garth y a eventos de ese calendario tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="09761-107">If John has signed in your app and provided delegated permissions (Mail.Read.Shared or Mail.ReadWrite.Shared), your app will be able to access Garth's mail and Garth's Inbox as described below.</span></span>

## <a name="get-an-event-in-the-shared-calendar"></a><span data-ttu-id="09761-108">Obtener un evento del calendario compartido</span><span class="sxs-lookup"><span data-stu-id="09761-108">Get an event in the shared calendar</span></span>

<span data-ttu-id="09761-109">Puede obtener un evento específico del calendario predeterminado compartido de Garth:</span><span class="sxs-lookup"><span data-stu-id="09761-109">You can get a specific event in Garth's shared default calendar:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar/events/{id}
```

<span data-ttu-id="09761-110">Si esto se completa correctamente, obtendrá HTTP 200 OK y la instancia de [evento](../api-reference/v1.0/resources/event.md) identificada por `{id}` del calendario predeterminado de Garth.</span><span class="sxs-lookup"><span data-stu-id="09761-110">On successful completion, you'll get HTTP 200 OK and the [message](../api-reference/v1.0/resources/event.md) instance identified by `{id}` from Garth's Inbox.</span></span>

## <a name="get-all-the-events-in-the-shared-calendar"></a><span data-ttu-id="09761-111">Obtener todos los eventos del calendario compartido</span><span class="sxs-lookup"><span data-stu-id="09761-111">Get all the events in the shared calendar</span></span>

<span data-ttu-id="09761-112">Obtenga todos los eventos del calendario predeterminado que Garth ha compartido con John:</span><span class="sxs-lookup"><span data-stu-id="09761-112">Get all the events in the default calendar that Garth has shared with John:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar/events
```

<span data-ttu-id="09761-113">Si esto se completa correctamente, obtendrá HTTP 200 OK y una colección de instancias de [evento](../api-reference/v1.0/resources/event.md) en el calendario de predeterminado de Garth.</span><span class="sxs-lookup"><span data-stu-id="09761-113">On successful completion, you'll get HTTP 200 OK and a collection of [message](../api-reference/v1.0/resources/event.md) instances in Garth's Inbox.</span></span>

## <a name="get-the-shared-calendar"></a><span data-ttu-id="09761-114">Obtener el calendario compartido</span><span class="sxs-lookup"><span data-stu-id="09761-114">Get the shared folder</span></span>

<span data-ttu-id="09761-115">Obtenga el calendario predeterminado que Garth ha compartido con John.</span><span class="sxs-lookup"><span data-stu-id="09761-115">Get the folder (Inbox) that Garth has shared with John.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar
```

<span data-ttu-id="09761-116">Si esto se completa correctamente, obtendrá HTTP 200 OK y una instancia de [calendario](../api-reference/v1.0/resources/calendar.md) que representa la carpeta predeterminada de Garth.</span><span class="sxs-lookup"><span data-stu-id="09761-116">On successful completion, you'll get HTTP 200 OK and a [mailFolder](../api-reference/v1.0/resources/calendar.md) instance that represents Garth's Inbox folder.</span></span>

<span data-ttu-id="09761-117">Se aplicarían las mismas funciones de GET si Garth hubiera delegado a John acceso su calendario predeterminado, o si hubiera delegado a John todo su buzón.</span><span class="sxs-lookup"><span data-stu-id="09761-117">The same GET capabilities apply if Garth had delegated John further access to Garth's Inbox, or if Garth had delegated John his entire mailbox.</span></span>

<span data-ttu-id="09761-118">Si Garth no ha compartido su calendario predeterminado con John ni ha delegado su buzón a John, especificar el Id. de usuario o el nombre principal de usuario de Garth en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="09761-118">If Garth has not shared his calendar with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="09761-119">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="09761-119">Next steps</span></span>

<span data-ttu-id="09761-120">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="09761-120">Find out more about:</span></span>

- [<span data-ttu-id="09761-121">¿Por qué debería realizar la integración con el calendario de Outlook?</span><span class="sxs-lookup"><span data-stu-id="09761-121">Why integrate with Outlook calendar?</span></span>](outlook-calendar-concept-overview.md)
- <span data-ttu-id="09761-122">[API de calendario](../api-reference/v1.0/resources/calendar.md) en Microsoft Graph v1.0.</span><span class="sxs-lookup"><span data-stu-id="09761-122">The [calendar API](../api-reference/v1.0/resources/calendar.md) in Microsoft Graph v1.0.</span></span>
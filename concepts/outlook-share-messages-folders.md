# <a name="get-outlook-messages-in-a-shared-or-delegated-folder"></a><span data-ttu-id="611cc-101">Obtener los mensajes de Outlook en una carpeta compartida o delegada</span><span class="sxs-lookup"><span data-stu-id="611cc-101">Get Outlook messages in a shared or delegated folder</span></span>

<!-- remove similar content in other topics when ready to publish - list messages, get message, get mail folder.
These topics also have similar section - list events, get event, get calendar, list contacts, get contact, get contact folder.
-->

<span data-ttu-id="611cc-102">Outlook permite a los clientes compartir las carpetas de correo entre sí y proporcionar diferentes tipos de acceso a las carpetas individuales como "leer", "crear", "modificar" o "eliminar".</span><span class="sxs-lookup"><span data-stu-id="611cc-102">Outlook lets customers share folders with one another and provide "read", "create", or "modify" access to individual folders or the entire mailbox.</span></span> <span data-ttu-id="611cc-103">Además, Outlook permite que un cliente elija a otro usuario para que actúe en su nombre y para que tenga acceso a carpetas de correo concretas o a todo su buzón. En Outlook, esto también se denomina "delegación".</span><span class="sxs-lookup"><span data-stu-id="611cc-103">Outlook also allows a customer to delegate another user to act on the customer's behalf, and access specific mail folders or the customer's entire mailbox; this is also known as "delegation" in Outlook.</span></span>

<span data-ttu-id="611cc-104">Mediante programación, Microsoft Graph admite la recepción de mensajes en carpetas de correo que se han compartido con otros usuarios, así como obtener esas carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="611cc-104">Programmatically, Microsoft Graph supports getting messages in mail folders that have been shared by other users, as well as getting the shared folders themselves.</span></span> <span data-ttu-id="611cc-105">La compatibilidad también se aplica a las carpetas que se han delegado.</span><span class="sxs-lookup"><span data-stu-id="611cc-105">The support also applies to folders that have been delegated.</span></span>

<span data-ttu-id="611cc-106">Por ejemplo, Jorge ha compartido con Juan su bandeja de entrada y le ha dado acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="611cc-106">As an example, Garth has shared with John read access to Garth's Inbox.</span></span> <span data-ttu-id="611cc-107">Si Juan ha iniciado sesión en la aplicación y proporciona permisos delegados (Mail.Read.Shared o Mail.ReadWrite.Shared), la aplicación podrá acceder al correo de Jorge y a su bandeja de entrada, tal como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="611cc-107">If John has signed in your app and provided delegated permissions (Mail.Read.Shared or Mail.ReadWrite.Shared), your app will be able to access Garth's mail and Garth's Inbox as described below.</span></span>

## <a name="get-a-message-in-the-shared-folder"></a><span data-ttu-id="611cc-108">Obtener un mensaje en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="611cc-108">Get a message in the shared folder</span></span>

<span data-ttu-id="611cc-109">Puede obtener un mensaje específico en la Bandeja de entrada de Jorge:</span><span class="sxs-lookup"><span data-stu-id="611cc-109">You can get a specific message in Garth's Inbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages/{id}
```

<span data-ttu-id="611cc-110">Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [mensaje](../api-reference/v1.0/resources/message.md) identificada por `{id}` de la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="611cc-110">On successful completion, you'll get HTTP 200 OK and the [message](../api-reference/v1.0/resources/message.md) instance identified by `{id}` from Garth's Inbox.</span></span>

## <a name="get-all-messages-in-the-shared-folder"></a><span data-ttu-id="611cc-111">Obtener todos los mensajes en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="611cc-111">Get all messages in the shared folder</span></span>

<span data-ttu-id="611cc-112">Obtenga todos los mensajes en la Bandeja de entrada de Jorge:</span><span class="sxs-lookup"><span data-stu-id="611cc-112">Get all the messages in Garth's Inbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages
```

<span data-ttu-id="611cc-113">Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias de [mensajes](../api-reference/v1.0/resources/message.md) en la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="611cc-113">On successful completion, you'll get HTTP 200 OK and a collection of [message](../api-reference/v1.0/resources/message.md) instances in Garth's Inbox.</span></span>

## <a name="get-the-shared-folder"></a><span data-ttu-id="611cc-114">Obtener la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="611cc-114">Get the shared folder</span></span>

<span data-ttu-id="611cc-115">Obtenga la carpeta (Bandeja de entrada) que compartió Jorge con Juan.</span><span class="sxs-lookup"><span data-stu-id="611cc-115">Get the folder (Inbox) that Garth has shared with John.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')
```

<span data-ttu-id="611cc-116">Cuando se complete correctamente, verá HTTP 200 OK y la instancia [mailFolder](../api-reference/v1.0/resources/mailfolder.md) que representa la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="611cc-116">On successful completion, you'll get HTTP 200 OK and a [mailFolder](../api-reference/v1.0/resources/mailfolder.md) instance that represents Garth's Inbox folder.</span></span>

<span data-ttu-id="611cc-117">Se aplican las mismas capacidades de GET si Jorge había delegado a Juan acceso a la Bandeja de entrada de Jorge o había delegado Juan todo su buzón.</span><span class="sxs-lookup"><span data-stu-id="611cc-117">The same GET capabilities apply if Garth had delegated John further access to Garth's Inbox, or if Garth had delegated John his entire mailbox.</span></span>

<span data-ttu-id="611cc-118">Si Jorge no ha compartido su bandeja de entrada con Juan ni le ha delegado su buzón, especificar el ID de usuario de Jorge o el nombre principal de usuario en esas operaciones GET producirá un error.</span><span class="sxs-lookup"><span data-stu-id="611cc-118">If Garth has not shared his message folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="611cc-119">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="611cc-119">Next steps</span></span>

<span data-ttu-id="611cc-120">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="611cc-120">Find out more about:</span></span>

- [<span data-ttu-id="611cc-121">¿Por qué debería realizar la integración con Correo de Outlook?</span><span class="sxs-lookup"><span data-stu-id="611cc-121">Why integrate with Outlook mail</span></span>](outlook-mail-concept-overview.md)
- <span data-ttu-id="611cc-122">[Usar la API de correo](../api-reference/v1.0/resources/mail_api_overview.md) y sus [casos de uso](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases) en la versión 1.0 de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="611cc-122">[Using the mail API](../api-reference/v1.0/resources/mail_api_overview.md) and its [use cases](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases) in Microsoft Graph v1.0.</span></span>
# <a name="share-outlook-message-folders-between-users"></a><span data-ttu-id="7fd30-101">Compartir las carpetas de mensajes de Outlook entre los usuarios</span><span class="sxs-lookup"><span data-stu-id="7fd30-101">Share Outlook message folders between users</span></span>

<!-- remove similar content in other topics when ready to publish - list messages, get message, get mail folder.
These topics also have similar section - list events, get event, get calendar, list contacts, get contact, get contact folder.
-->

<span data-ttu-id="7fd30-102">Outlook permite a los clientes compartir carpetas entre ellos y proporcionar acceso de "lectura", "creación" o "edición" a las carpetas individuales o a todo el buzón.</span><span class="sxs-lookup"><span data-stu-id="7fd30-102">Outlook lets customers share folders with one another and provide "read", "create", or "modify" access to individual folders or the entire mailbox.</span></span> <span data-ttu-id="7fd30-103">Esta es también se denominan "delegación" en Outlook.</span><span class="sxs-lookup"><span data-stu-id="7fd30-103">This is also known as "delegation" in Outlook.</span></span>

<span data-ttu-id="7fd30-104">Mediante programación, Microsoft Graph admite la recepción de mensajes en carpetas de correo que se han compartido con otros usuarios, así como obtener esas carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="7fd30-104">Programmatically, Microsoft Graph supports getting messages in mail folders that have been shared by other users, as well as getting the shared folders themselves.</span></span>

<span data-ttu-id="7fd30-105">Por ejemplo, Jorge ha compartido con Juan el acceso de lectura a la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="7fd30-105">As an example, Garth has shared with John read access to Garth's Inbox.</span></span> <span data-ttu-id="7fd30-106">Si Juan ha iniciado sesión en la aplicación y proporciona permisos delegados (Mail.Read.Shared o Mail.ReadWrite.Shared), la aplicación podrá acceder al correo de Jorge y a su Bandeja de entrada tal como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="7fd30-106">If John has signed in your app and provided delegated permissions (Mail.Read.Shared or Mail.ReadWrite.Shared), your app will be able to access Garth's mail and Garth's Inbox as described below.</span></span>

## <a name="get-a-message-in-the-shared-folder"></a><span data-ttu-id="7fd30-107">Obtener un mensaje en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="7fd30-107">Get a message in the shared folder</span></span>

<span data-ttu-id="7fd30-108">Puede obtener un mensaje específico en la Bandeja de entrada de Jorge:</span><span class="sxs-lookup"><span data-stu-id="7fd30-108">You can get a specific message in Garth's Inbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages/{id}
```

<span data-ttu-id="7fd30-109">Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [mensaje](../api-reference/v1.0/resources/message.md) identificada por `{id}` de la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="7fd30-109">On successful completion, you'll get HTTP 200 OK and the [message](../api-reference/v1.0/resources/message.md) instance identified by `{id}` from Garth's Inbox.</span></span>

## <a name="get-all-messages-in-the-shared-folder"></a><span data-ttu-id="7fd30-110">Obtener todos los mensajes en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="7fd30-110">Get all messages in the shared folder</span></span>

<span data-ttu-id="7fd30-111">Obtenga todos los mensajes en la Bandeja de entrada de Jorge:</span><span class="sxs-lookup"><span data-stu-id="7fd30-111">Get all the messages in Garth's Inbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages
```

<span data-ttu-id="7fd30-112">Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias de [mensajes](../api-reference/v1.0/resources/message.md) en la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="7fd30-112">On successful completion, you'll get HTTP 200 OK and a collection of [message](../api-reference/v1.0/resources/message.md) instances in Garth's Inbox.</span></span>

## <a name="get-the-shared-folder"></a><span data-ttu-id="7fd30-113">Obtener la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="7fd30-113">Get the shared folder</span></span>

<span data-ttu-id="7fd30-114">Obtenga la carpeta (Bandeja de entrada) que compartió Jorge con Juan.</span><span class="sxs-lookup"><span data-stu-id="7fd30-114">Get the folder (Inbox) that Garth has shared with John.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')
```

<span data-ttu-id="7fd30-115">Cuando se complete correctamente, verá HTTP 200 OK y la instancia [mailFolder](../api-reference/v1.0/resources/mailfolder.md) que representa la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="7fd30-115">On successful completion, you'll get HTTP 200 OK and a [mailFolder](../api-reference/v1.0/resources/mailfolder.md) instance that represents Garth's Inbox folder.</span></span>

<span data-ttu-id="7fd30-116">Se aplican las mismas capacidades de GET si Jorge había delegado a Juan acceso a la Bandeja de entrada de Jorge o había delegado Juan todo su buzón.</span><span class="sxs-lookup"><span data-stu-id="7fd30-116">The same GET capabilities apply if Garth had delegated John further access to Garth's Inbox, or if Garth had delegated John his entire mailbox.</span></span>

<span data-ttu-id="7fd30-117">Si Garth no ha compartido su carpeta de mensajes con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="7fd30-117">If Garth has not shared his message folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="7fd30-118">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="7fd30-118">Next steps</span></span>

<span data-ttu-id="7fd30-119">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="7fd30-119">Find out more about:</span></span>

- [<span data-ttu-id="7fd30-120">¿Por qué debería realizar la integración con Correo de Outlook?</span><span class="sxs-lookup"><span data-stu-id="7fd30-120">Why integrate with Outlook mail</span></span>](outlook-mail-concept-overview.md)
- <span data-ttu-id="7fd30-121">[Usar la API de correo](../api-reference/v1.0/resources/mail_api_overview.md) y sus [casos de uso](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases) en la versión 1.0 de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="7fd30-121">[Using the mail API](../api-reference/v1.0/resources/mail_api_overview.md) and its [use cases](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases) in Microsoft Graph v1.0.</span></span>
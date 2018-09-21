# <a name="get-outlook-contacts-in-a-shared-folder"></a><span data-ttu-id="fac98-101">Obtener los contactos de Outlook en una carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="fac98-101">Get Outlook contacts in a shared folder</span></span>

<span data-ttu-id="fac98-102">Outlook permite a los clientes compartir las carpetas entre sí y proporcionar diferentes tipos de acceso como "leer", "crear", "modificar" o "eliminar" a las carpetas de contactos individuales.</span><span class="sxs-lookup"><span data-stu-id="fac98-102">Outlook lets customers share folders with one another and provide "read", "create", or "modify" access to individual folders or the entire mailbox.</span></span> <span data-ttu-id="fac98-103">Además, Outlook permite que un cliente elija a otro usuario para que actúe en su nombre y para que tenga acceso a carpetas de correo concretas o a todo su buzón. En Outlook, esto también se denomina "delegación".</span><span class="sxs-lookup"><span data-stu-id="fac98-103">Outlook also allows a customer to delegate another user to act on the customer's behalf, and access specific folders or the customer's entire mailbox; this is also known as "delegation" in Outlook.</span></span>

<span data-ttu-id="fac98-104">Mediante programación, Microsoft Graph permite obtener los contactos de las carpetas de contactos compartidas por otros usuarios, así como las propias carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="fac98-104">Programmatically, Microsoft Graph supports getting messages in mail folders that have been shared by other users, as well as getting the shared folders themselves.</span></span> <span data-ttu-id="fac98-105">La compatibilidad también se aplica a las carpetas de un buzón delegado.</span><span class="sxs-lookup"><span data-stu-id="fac98-105">The support also applies to folders in a delegated mailbox.</span></span>

<span data-ttu-id="fac98-106">Por ejemplo, Garth tiene compartida con John una carpeta de contactos personalizada y concede a John acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="fac98-106">As an example, Garth has shared with John a custom contact folder and given John read access.</span></span> <span data-ttu-id="fac98-107">Si John ha iniciado sesión en su aplicación y ha proporcionado permisos delegados (Contacts.Read.Shared o Contacts.ReadWrite.Shared), la aplicación podrá obtener acceso a carpeta de contactos personalizada de Garth y a los contactos de esa carpeta, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="fac98-107">If John has signed in your app and provided delegated permissions (Mail.Read.Shared or Mail.ReadWrite.Shared), your app will be able to access Garth's mail and Garth's Inbox as described below.</span></span>

## <a name="get-a-contact-in-the-shared-folder"></a><span data-ttu-id="fac98-108">Obtener un contacto de la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="fac98-108">Get a message in the shared folder</span></span>

<span data-ttu-id="fac98-109">Puede obtener un contacto específico de la carpeta de contactos personalizada que Garth ha compartido con John:</span><span class="sxs-lookup"><span data-stu-id="fac98-109">You can get a specific contact in the custom contact folder that Garth has shared with John:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts/{id}
```

<span data-ttu-id="fac98-110">Si esto se completa correctamente, obtendrá HTTP 200 OK y la instancia de [contacto](../api-reference/v1.0/resources/contact.md) identificada por `{id}` de la carpeta de contactos compartida del Garth.</span><span class="sxs-lookup"><span data-stu-id="fac98-110">On successful completion, you'll get HTTP 200 OK and the [message](../api-reference/v1.0/resources/contact.md) instance identified by `{id}` from Garth's Inbox.</span></span>

## <a name="get-all-contacts-in-the-shared-folder"></a><span data-ttu-id="fac98-111">Obtener todos los contactos de la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="fac98-111">Get all messages in the shared folder</span></span>

<span data-ttu-id="fac98-112">Obtenga todos los contactos de la carpeta de contactos compartida de Garth:</span><span class="sxs-lookup"><span data-stu-id="fac98-112">Get all the contacts in Garth's shared contact folder:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts
```

<span data-ttu-id="fac98-113">Si esto se completa correctamente, obtendrá HTTP 200 OK y una colección de instancias de [contacto](../api-reference/v1.0/resources/contact.md) de la carpeta de contactos compartida de Garth.</span><span class="sxs-lookup"><span data-stu-id="fac98-113">On successful completion, you'll get HTTP 200 OK and a collection of [message](../api-reference/v1.0/resources/contact.md) instances in Garth's Inbox.</span></span>

## <a name="get-the-shared-folder"></a><span data-ttu-id="fac98-114">Obtener la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="fac98-114">Get the shared folder</span></span>

<span data-ttu-id="fac98-115">Obtenga la carpeta de contactos que Garth ha compartido con John.</span><span class="sxs-lookup"><span data-stu-id="fac98-115">Get the folder (Inbox) that Garth has shared with John.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}
```

<span data-ttu-id="fac98-116">Si esto se completa correctamente, obtendrá HTTP 200 OK y una instancia de [contactFolder](../api-reference/v1.0/resources/contactfolder.md) que representa la carpeta de contactos compartida de Garth.</span><span class="sxs-lookup"><span data-stu-id="fac98-116">On successful completion, you'll get HTTP 200 OK and a [mailFolder](../api-reference/v1.0/resources/contactfolder.md) instance that represents Garth's Inbox folder.</span></span>

<span data-ttu-id="fac98-117">Se aplicarían las mismas funciones de GET si Garth hubiera delegado a John todo su buzón.</span><span class="sxs-lookup"><span data-stu-id="fac98-117">The same GET capabilities apply if Garth had delegated John further access to Garth's Inbox, or if Garth had delegated John his entire mailbox.</span></span>

<span data-ttu-id="fac98-118">Si Garth no ha compartido su carpeta de contactos con John ni ha delegado su buzón a John, especificar el ID. de usuario o el nombre principal de usuario de Garth en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="fac98-118">If Garth has not shared his contact folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="fac98-119">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="fac98-119">Next steps</span></span>

<span data-ttu-id="fac98-120">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="fac98-120">Find out more about:</span></span>

- [<span data-ttu-id="fac98-121">¿Por qué integrar con contactos personales de Outlook?</span><span class="sxs-lookup"><span data-stu-id="fac98-121">Why integrate with Outlook personal contacts?</span></span>](outlook-contacts-concept-overview.md)
- <span data-ttu-id="fac98-122">[API de contactos](../api-reference/v1.0/resources/contact.md) en Microsoft Graph v1.0.</span><span class="sxs-lookup"><span data-stu-id="fac98-122">The [contacts API](../api-reference/v1.0/resources/contact.md) in Microsoft Graph v1.0.</span></span>
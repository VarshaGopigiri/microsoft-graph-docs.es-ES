---
title: Obtener mensajes de Outlook en una carpeta compartida o delegada
description: 'Estos temas también tienen sección similar: lista de eventos, obtener evento, obtener calendario, lista de contactos, obtener contactos, obtener la carpeta de contactos.'
ms.openlocfilehash: d9e04527879cb32f14dc8d74a814a54150c5b2d0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092862"
---
# <a name="get-outlook-messages-in-a-shared-or-delegated-folder"></a><span data-ttu-id="58334-103">Obtener mensajes de Outlook en una carpeta compartida o delegada</span><span class="sxs-lookup"><span data-stu-id="58334-103">Get Outlook messages in a shared or delegated folder</span></span>

<!-- remove similar content in other topics when ready to publish - list messages, get message, get mail folder.
These topics also have similar section - list events, get event, get calendar, list contacts, get contact, get contact folder.
-->

<span data-ttu-id="58334-104">Outlook permite a los clientes compartir carpetas entre ellos y proporcionar acceso de "lectura", "creación", "edición" o "eliminación" a las carpetas individuales.</span><span class="sxs-lookup"><span data-stu-id="58334-104">Outlook lets customers share folders with one another and provide "read", "create", or "modify" access to individual folders or the entire mailbox.</span></span> <span data-ttu-id="58334-105">Outlook también permite a un cliente delegar en otro usuario en nombre del cliente y tener acceso a carpetas de correo específico o a todo buzón del cliente; esto también se denomina "delegación" en Outlook.</span><span class="sxs-lookup"><span data-stu-id="58334-105">Outlook also allows a customer to delegate another user to act on the customer's behalf, and access specific mail folders or the customer's entire mailbox; this is also known as "delegation" in Outlook.</span></span>

<span data-ttu-id="58334-106">Mediante programación, Microsoft Graph admite la recepción de mensajes en carpetas de correo que se han compartido con otros usuarios, así como obtener esas carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="58334-106">Programmatically, Microsoft Graph supports getting messages in mail folders that have been shared by other users, as well as getting the shared folders themselves.</span></span> <span data-ttu-id="58334-107">El soporte también se aplica a los calendarios que se han delegado.</span><span class="sxs-lookup"><span data-stu-id="58334-107">The support also applies to folders that have been delegated.</span></span>

<span data-ttu-id="58334-108">Por ejemplo, Jorge ha compartido con Juan y se le ha dado acceso de lectura a la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="58334-108">As an example, Garth has shared with John read access to Garth's Inbox.</span></span> <span data-ttu-id="58334-109">Si Juan ha iniciado sesión en la aplicación y proporciona permisos delegados (Mail.Read.Shared o Mail.ReadWrite.Shared), la aplicación podrá acceder al correo de Jorge y a su Bandeja de entrada tal como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="58334-109">If John has signed in your app and provided delegated permissions (Mail.Read.Shared or Mail.ReadWrite.Shared), your app will be able to access Garth's mail and Garth's Inbox as described below.</span></span>

## <a name="get-a-message-in-the-shared-folder"></a><span data-ttu-id="58334-110">Obtener un mensaje en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="58334-110">Get a message in the shared folder</span></span>

<span data-ttu-id="58334-111">Puede obtener un mensaje específico en la Bandeja de entrada de Jorge:</span><span class="sxs-lookup"><span data-stu-id="58334-111">You can get a specific message in Garth's Inbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages/{id}
```

<span data-ttu-id="58334-112">Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [mensaje](/graph/api/resources/message?view=graph-rest-1.0) identificada por `{id}` de la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="58334-112">On successful completion, you'll get HTTP 200 OK and the [message](/graph/api/resources/message?view=graph-rest-1.0) instance identified by `{id}` from Garth's Inbox.</span></span>

## <a name="get-all-messages-in-the-shared-folder"></a><span data-ttu-id="58334-113">Obtener todos los mensajes en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="58334-113">Get all messages in the shared folder</span></span>

<span data-ttu-id="58334-114">Obtenga todos los mensajes en la Bandeja de entrada de Jorge:</span><span class="sxs-lookup"><span data-stu-id="58334-114">Get all the messages in Garth's Inbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages
```

<span data-ttu-id="58334-115">Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias de [mensajes](/graph/api/resources/message?view=graph-rest-1.0) en la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="58334-115">On successful completion, you'll get HTTP 200 OK and a collection of [message](/graph/api/resources/message?view=graph-rest-1.0) instances in Garth's Inbox.</span></span>

## <a name="get-the-shared-folder"></a><span data-ttu-id="58334-116">Obtener la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="58334-116">Get the shared folder</span></span>

<span data-ttu-id="58334-117">Obtenga la carpeta (Bandeja de entrada) que compartió Jorge con Juan.</span><span class="sxs-lookup"><span data-stu-id="58334-117">Get the folder (Inbox) that Garth has shared with John.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')
```

<span data-ttu-id="58334-118">Cuando se complete correctamente, verá HTTP 200 OK y la instancia [mailFolder](/graph/api/resources/mailfolder?view=graph-rest-1.0) que representa la Bandeja de entrada de Jorge.</span><span class="sxs-lookup"><span data-stu-id="58334-118">On successful completion, you'll get HTTP 200 OK and a [mailFolder](/graph/api/resources/mailfolder?view=graph-rest-1.0) instance that represents Garth's Inbox folder.</span></span>

<span data-ttu-id="58334-119">Se aplican las mismas capacidades de GET si Jorge había delegado a Juan acceso a la Bandeja de entrada de Jorge o había delegado Juan todo su buzón.</span><span class="sxs-lookup"><span data-stu-id="58334-119">The same GET capabilities apply if Garth had delegated John further access to Garth's Inbox, or if Garth had delegated John his entire mailbox.</span></span>

<span data-ttu-id="58334-120">Si Jorge no ha compartido su Bandeja de entrada con John ni ha delegado su buzón a Juan, especificar el identificador de usuario de Jorge o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="58334-120">If Garth has not shared his message folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="58334-121">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="58334-121">Next steps</span></span>

<span data-ttu-id="58334-122">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="58334-122">Find out more about:</span></span>

- [<span data-ttu-id="58334-123">¿Por qué integrar con el correo de Outlook?</span><span class="sxs-lookup"><span data-stu-id="58334-123">Why integrate with Outlook mail</span></span>](outlook-mail-concept-overview.md)
- <span data-ttu-id="58334-124">[Usar la API de correo](/graph/api/resources/mail-api-overview?view=graph-rest-1.0) y sus [casos de uso](/graph/api/resources/mail-api-overview?view=graph-rest-1.0#common-use-cases) en Microsoft Graph v1.0.</span><span class="sxs-lookup"><span data-stu-id="58334-124">[Using the mail API](/graph/api/resources/mail-api-overview?view=graph-rest-1.0) and its [use cases](/graph/api/resources/mail-api-overview?view=graph-rest-1.0#common-use-cases) in Microsoft Graph v1.0.</span></span>
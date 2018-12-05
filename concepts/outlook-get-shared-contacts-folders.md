---
title: Obtener contactos de Outlook en una carpeta compartida
description: " También es esto "
ms.openlocfilehash: c8c5b3a2eac49153826113af036146cc4475d9e5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092812"
---
# <a name="get-outlook-contacts-in-a-shared-folder"></a><span data-ttu-id="4ea71-103">Obtener contactos de Outlook en una carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="4ea71-103">Get Outlook contacts in a shared folder</span></span>

<span data-ttu-id="4ea71-104">Outlook permite a los clientes compartir carpetas entre ellos y proporcionar acceso de "lectura", "creación", "edición" o "eliminación" a las carpetas de contactos individuales.</span><span class="sxs-lookup"><span data-stu-id="4ea71-104">Outlook lets customers share folders with one another and provide "read", "create", or "modify" access to individual folders or the entire mailbox.</span></span> <span data-ttu-id="4ea71-105">Outlook también permite a un cliente delegar en otro usuario en nombre del cliente y tener acceso a carpetas de correo específico o a todo buzón del cliente; esto también se denomina "delegación" en Outlook.</span><span class="sxs-lookup"><span data-stu-id="4ea71-105">Outlook also allows a customer to delegate another user to act on the customer's behalf, and access specific folders or the customer's entire mailbox; this is also known as "delegation" in Outlook.</span></span>

<span data-ttu-id="4ea71-106">Mediante programación, Microsoft Graph admite la recepción de mensajes en carpetas de correo que han compartido otros usuarios, así como obtener esas carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="4ea71-106">Programmatically, Microsoft Graph supports getting messages in mail folders that have been shared by other users, as well as getting the shared folders themselves.</span></span> <span data-ttu-id="4ea71-107">El soporte también se aplica a los archivos en un buzón de correo delegado.</span><span class="sxs-lookup"><span data-stu-id="4ea71-107">The support also applies to folders in a delegated mailbox.</span></span>

<span data-ttu-id="4ea71-108">Por ejemplo, Juan ha compartido con Miguel una carpeta de contactos personalizada y le ha concedido el acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="4ea71-108">As an example, Garth has shared with John a custom contact folder and given John read access.</span></span> <span data-ttu-id="4ea71-109">Si Miguel ha iniciado sesión en la aplicación y ha proporcionado permisos delegados (Contacts.Read.Shared o Contacts.ReadWrite.Shared), la aplicación podrá acceder a la carpeta de contactos personalizada de Juan y a los contactos en dicha carpeta, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="4ea71-109">If John has signed in your app and provided delegated permissions (Mail.Read.Shared or Mail.ReadWrite.Shared), your app will be able to access Garth's mail and Garth's Inbox as described below.</span></span>

## <a name="get-a-contact-in-the-shared-folder"></a><span data-ttu-id="4ea71-110">Obtener un contacto en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="4ea71-110">Get a message in the shared folder</span></span>

<span data-ttu-id="4ea71-111">Puede obtener un contacto específico en la carpeta de contactos personalizada que Juan ha compartido con Miguel:</span><span class="sxs-lookup"><span data-stu-id="4ea71-111">You can get a specific contact in the custom contact folder that Garth has shared with John:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts/{id}
```

<span data-ttu-id="4ea71-112">Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [contacto](/graph/api/resources/contact?view=graph-rest-1.0) identificada por `{id}` desde la carpeta de contactos que ha compartido Juan.</span><span class="sxs-lookup"><span data-stu-id="4ea71-112">On successful completion, you'll get HTTP 200 OK and the [message](/graph/api/resources/contact?view=graph-rest-1.0) instance identified by `{id}` from Garth's Inbox.</span></span>

## <a name="get-all-contacts-in-the-shared-folder"></a><span data-ttu-id="4ea71-113">Obtener todos los contactos en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="4ea71-113">Get all messages in the shared folder</span></span>

<span data-ttu-id="4ea71-114">Obtener todos los contactos en la carpeta de contactos que ha compartido Juan:</span><span class="sxs-lookup"><span data-stu-id="4ea71-114">Get all the contacts in Garth's shared contact folder:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts
```

<span data-ttu-id="4ea71-115">Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias [contacto](/graph/api/resources/contact?view=graph-rest-1.0) en la carpeta de contactos que ha compartido Juan.</span><span class="sxs-lookup"><span data-stu-id="4ea71-115">On successful completion, you'll get HTTP 200 OK and a collection of [message](/graph/api/resources/contact?view=graph-rest-1.0) instances in Garth's Inbox.</span></span>

## <a name="get-the-shared-folder"></a><span data-ttu-id="4ea71-116">Obtener la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="4ea71-116">Get the shared folder</span></span>

<span data-ttu-id="4ea71-117">Obtener la carpeta que Juan ha compartido con Miguel.</span><span class="sxs-lookup"><span data-stu-id="4ea71-117">Get the folder (Inbox) that Garth has shared with John.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}
```

<span data-ttu-id="4ea71-118">Cuando se complete correctamente, verá HTTP 200 OK y la instancia [contactFolder](/graph/api/resources/contactfolder?view=graph-rest-1.0) que representa la carpeta de contactos que ha compartido Juan.</span><span class="sxs-lookup"><span data-stu-id="4ea71-118">On successful completion, you'll get HTTP 200 OK and a [mailFolder](/graph/api/resources/contactfolder?view=graph-rest-1.0) instance that represents Garth's Inbox folder.</span></span>

<span data-ttu-id="4ea71-119">Las mismas capacidades de "obtener" aplican si Jorge hubiera delegado en Juan todo su buzón.</span><span class="sxs-lookup"><span data-stu-id="4ea71-119">The same GET capabilities apply if Garth had delegated John further access to Garth's Inbox, or if Garth had delegated John his entire mailbox.</span></span>

<span data-ttu-id="4ea71-120">Si Juan no ha compartido su carpeta de contactos con Miguel ni ha delegado su buzón en él, especificar el identificador de usuario del Juan o el nombre principal de usuario en esas operaciones "obtener" devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="4ea71-120">If Garth has not shared his contact folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="4ea71-121">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="4ea71-121">Next steps</span></span>

<span data-ttu-id="4ea71-122">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="4ea71-122">Find out more about:</span></span>

- [<span data-ttu-id="4ea71-123">¿Por qué integrar con contactos personales de Outlook?</span><span class="sxs-lookup"><span data-stu-id="4ea71-123">Why integrate with Outlook personal contacts?</span></span>](outlook-contacts-concept-overview.md)
- <span data-ttu-id="4ea71-124">La [API de contactos](/graph/api/resources/contact?view=graph-rest-1.0) en la versión 1.0 de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="4ea71-124">The [contacts API](/graph/api/resources/contact?view=graph-rest-1.0) in Microsoft Graph v1.0.</span></span>
---
title: Obtener contactos de Outlook en una carpeta compartida
description: Outlook permite a los clientes compartir carpetas entre ellos y proporcionar acceso de lectura, creación, edición o eliminación a las carpetas de contactos individuales. Outlook también permite a un cliente delegar en otro usuario para actuar en nombre del cliente.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 86533a28c0af206458b63fd19f32f01c5b68710b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932157"
---
# <a name="get-outlook-contacts-in-a-shared-folder"></a><span data-ttu-id="cf54b-104">Obtener contactos de Outlook en una carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="cf54b-104">Get Outlook contacts in a shared folder</span></span>

<span data-ttu-id="cf54b-105">Outlook permite a los clientes compartir carpetas entre ellos y proporcionar acceso de "lectura", "creación", "edición" o "eliminación" a las carpetas de contactos individuales.</span><span class="sxs-lookup"><span data-stu-id="cf54b-105">Outlook lets customers share folders with one another and provide "read", "create", "modify", or "delete" access to individual contact folders.</span></span> <span data-ttu-id="cf54b-106">Outlook también permite a un cliente delegar en otro usuario en nombre del cliente y tener acceso a carpetas de correo específico o a todo buzón del cliente; esto también se denomina "delegación" en Outlook.</span><span class="sxs-lookup"><span data-stu-id="cf54b-106">Outlook also allows a customer to delegate another user to act on the customer's behalf, and access specific folders or the customer's entire mailbox; this is also known as "delegation" in Outlook.</span></span>

<span data-ttu-id="cf54b-107">Mediante programación, Microsoft Graph admite la recepción de mensajes en carpetas de correo que han compartido otros usuarios, así como obtener esas carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="cf54b-107">Programmatically, Microsoft Graph supports getting contacts in contact folders that have been shared by other users, as well as getting the shared folders themselves.</span></span> <span data-ttu-id="cf54b-108">El soporte también se aplica a los archivos en un buzón de correo delegado.</span><span class="sxs-lookup"><span data-stu-id="cf54b-108">The support also applies to folders in a delegated mailbox.</span></span>

<span data-ttu-id="cf54b-109">Por ejemplo, Juan ha compartido con Miguel una carpeta de contactos personalizada y le ha concedido el acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="cf54b-109">As an example, Garth has shared with John a custom contact folder and given John read access.</span></span> <span data-ttu-id="cf54b-110">Si Miguel ha iniciado sesión en la aplicación y ha proporcionado permisos delegados (Contacts.Read.Shared o Contacts.ReadWrite.Shared), la aplicación podrá acceder a la carpeta de contactos personalizada de Juan y a los contactos en dicha carpeta, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="cf54b-110">If John has signed into your app and provided delegated permissions (Contacts.Read.Shared or Contacts.ReadWrite.Shared), your app will be able to access Garth's custom contact folder and contacts in that folder as described below.</span></span>

> <span data-ttu-id="cf54b-111">**Nota** Los permisos de uso compartidos (Contacts.Read.Shared o Contacts.ReadWrite.Shared) le permiten leer o escribir contactos en una carpeta compartida o delegada.</span><span class="sxs-lookup"><span data-stu-id="cf54b-111">**Note** The sharing permissions (Contacts.Read.Shared or Contacts.ReadWrite.Shared) allow you to read or write contacts in a shared or delegated folder.</span></span> <span data-ttu-id="cf54b-112">No admiten la [suscripción a notificaciones de cambios](webhooks.md) en elementos de dichas carpetas.</span><span class="sxs-lookup"><span data-stu-id="cf54b-112">They do not support [subscribing to change notifications](webhooks.md) on items in such folders.</span></span> <span data-ttu-id="cf54b-113">Para configurar las suscripciones de notificación de cambios a los contactos en una carpeta compartida o delegada, o cualquier otra carpeta de contactos de un usuario en el espacio empresarial, use los permisos de aplicación Contacts.Read.</span><span class="sxs-lookup"><span data-stu-id="cf54b-113">To set up change notification subscriptions on contacts in a shared, delegated, or any other user's contact folder in the tenant, use the application permission, Contacts.Read.</span></span>

## <a name="get-a-contact-in-the-shared-folder"></a><span data-ttu-id="cf54b-114">Obtener un contacto en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="cf54b-114">Get a contact in the shared folder</span></span>

<span data-ttu-id="cf54b-115">Puede obtener un contacto específico en la carpeta de contactos personalizada que Juan ha compartido con Miguel:</span><span class="sxs-lookup"><span data-stu-id="cf54b-115">You can get a specific contact in the custom contact folder that Garth has shared with John:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts/{id}
```

<span data-ttu-id="cf54b-116">Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [contacto](/graph/api/resources/contact?view=graph-rest-1.0) identificada por `{id}` desde la carpeta de contactos que ha compartido Juan.</span><span class="sxs-lookup"><span data-stu-id="cf54b-116">On successful completion, you'll get HTTP 200 OK and the [contact](/graph/api/resources/contact?view=graph-rest-1.0) instance identified by `{id}` from Garth's shared contact folder.</span></span>

## <a name="get-all-contacts-in-the-shared-folder"></a><span data-ttu-id="cf54b-117">Obtener todos los contactos en la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="cf54b-117">Get all contacts in the shared folder</span></span>

<span data-ttu-id="cf54b-118">Obtener todos los contactos en la carpeta de contactos que ha compartido Juan:</span><span class="sxs-lookup"><span data-stu-id="cf54b-118">Get all the contacts in Garth's shared contact folder:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts
```

<span data-ttu-id="cf54b-119">Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias [contacto](/graph/api/resources/contact?view=graph-rest-1.0) en la carpeta de contactos que ha compartido Juan.</span><span class="sxs-lookup"><span data-stu-id="cf54b-119">On successful completion, you'll get HTTP 200 OK and a collection of [contact](/graph/api/resources/contact?view=graph-rest-1.0) instances in Garth's shared contact folder.</span></span>

## <a name="get-the-shared-folder"></a><span data-ttu-id="cf54b-120">Obtener la carpeta compartida</span><span class="sxs-lookup"><span data-stu-id="cf54b-120">Get the shared folder</span></span>

<span data-ttu-id="cf54b-121">Obtener la carpeta que Juan ha compartido con Miguel.</span><span class="sxs-lookup"><span data-stu-id="cf54b-121">Get the contact folder that Garth has shared with John.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}
```

<span data-ttu-id="cf54b-122">Cuando se complete correctamente, verá HTTP 200 OK y la instancia [contactFolder](/graph/api/resources/contactfolder?view=graph-rest-1.0) que representa la carpeta de contactos que ha compartido Juan.</span><span class="sxs-lookup"><span data-stu-id="cf54b-122">On successful completion, you'll get HTTP 200 OK and a [contactFolder](/graph/api/resources/contactfolder?view=graph-rest-1.0) instance that represents Garth's shared contact folder.</span></span>

<span data-ttu-id="cf54b-123">Las mismas capacidades de "obtener" aplican si Jorge hubiera delegado en Juan todo su buzón.</span><span class="sxs-lookup"><span data-stu-id="cf54b-123">The same GET capabilities apply if Garth had delegated John his entire mailbox.</span></span>

<span data-ttu-id="cf54b-124">Si Juan no ha compartido su carpeta de contactos con Miguel ni ha delegado su buzón en él, especificar el identificador de usuario del Juan o el nombre principal de usuario en esas operaciones "obtener" devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="cf54b-124">If Garth has not shared the contact folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="cf54b-125">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="cf54b-125">Next steps</span></span>

<span data-ttu-id="cf54b-126">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="cf54b-126">Find out more about:</span></span>

- [<span data-ttu-id="cf54b-127">¿Por qué integrar con contactos personales de Outlook?</span><span class="sxs-lookup"><span data-stu-id="cf54b-127">Why integrate with Outlook personal contacts</span></span>](outlook-contacts-concept-overview.md)
- <span data-ttu-id="cf54b-128">La [API de contactos](/graph/api/resources/contact?view=graph-rest-1.0) en la versión 1.0 de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="cf54b-128">The [contacts API](/graph/api/resources/contact?view=graph-rest-1.0) in Microsoft Graph v1.0.</span></span>

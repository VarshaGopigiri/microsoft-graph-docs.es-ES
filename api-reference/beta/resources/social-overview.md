---
title: Usar la API de gráfico de Microsoft para integrar inteligencia sociales en una aplicación
description: Microsoft Graph admite gestos sociales en contexto social de un usuario y proporciona acceso a personas útiles y datos de contenido social.
localization_priority: Priority
ms.openlocfilehash: b3b71cf1bad0d860978c75c88f0b77a32eab1a0c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862492"
---
# <a name="use-the-microsoft-graph-api-to-integrate-social-intelligence-in-an-app"></a><span data-ttu-id="58ee4-103">Usar la API de gráfico de Microsoft para integrar inteligencia sociales en una aplicación</span><span class="sxs-lookup"><span data-stu-id="58ee4-103">Use the Microsoft Graph API to integrate social intelligence in an app</span></span>

> <span data-ttu-id="58ee4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="58ee4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="58ee4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="58ee4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="58ee4-106">Microsoft Graph admite gestos sociales en contexto social de un usuario y proporciona acceso a personas útiles y datos de contenido social.</span><span class="sxs-lookup"><span data-stu-id="58ee4-106">Microsoft Graph supports social gestures in a user's social context, and provides access to useful people and social data.</span></span>

## <a name="aggregate-and-extract-specific-information-about-people"></a><span data-ttu-id="58ee4-107">Agregar y extraer información específica acerca de las personas</span><span class="sxs-lookup"><span data-stu-id="58ee4-107">Aggregate and extract specific information about people</span></span>

<span data-ttu-id="58ee4-108">Utilice el recurso de [persona](../resources/person.md) y agregar información acerca de una persona de la API de personas a través de correo, contactos y las redes sociales.</span><span class="sxs-lookup"><span data-stu-id="58ee4-108">Use the [person](../resources/person.md) resource and the People API to aggregate information about a person from across mail, contacts, and social networks.</span></span> <span data-ttu-id="58ee4-109">Los resultados se ordenan por su importancia en función de varias relaciones empresariales, colaboración y comunicación.</span><span class="sxs-lookup"><span data-stu-id="58ee4-109">The results are ordered by their relevance based on multiple communication, collaboration, and business relationships.</span></span> <span data-ttu-id="58ee4-110">La API permite a examinar, ordenar, seleccionar, filtrar o búsqueda de personas en función de los criterios.</span><span class="sxs-lookup"><span data-stu-id="58ee4-110">The API lets you browse, sort, select, filter, or search for persons based on your criteria.</span></span>

- [<span data-ttu-id="58ee4-111">List people</span><span class="sxs-lookup"><span data-stu-id="58ee4-111">List people</span></span>](../api/user-list-people.md)

## <a name="manage--mentions"></a><span data-ttu-id="58ee4-112">Administrar @ menciones</span><span class="sxs-lookup"><span data-stu-id="58ee4-112">Manage @-Mentions</span></span>

<span data-ttu-id="58ee4-113">Realizar llamadas a un destinatario notificar y obtener atención del destinatario de un mensaje es un gesto social comunes.</span><span class="sxs-lookup"><span data-stu-id="58ee4-113">Calling out a recipient to notify and get the recipient's attention in a message is a common social gesture.</span></span>
<span data-ttu-id="58ee4-114">El recurso [mencione](../resources/mention.md) y la API de menciones proporcionan un mecanismo ligero para llamar a un destinatario de un [mensaje](../resources/message.md), obtener todos los mensajes en el que un usuario recibe una notificación mediante una mención @, u obtener cada mención en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="58ee4-114">The [mention](../resources/mention.md) resource and the Mentions API provide a light-weight mechanism to call out a recipient in a [message](../resources/message.md), get all the messages in which a user is notified using an @-mention, or get each mention in a message.</span></span>

<!--
Include the next sentence when supporting events.

**Mention** is also supported by [Event](../resources/event.md).

-->

- <span data-ttu-id="58ee4-115">Crear menciones en un mensaje nuevo</span><span class="sxs-lookup"><span data-stu-id="58ee4-115">Create mentions in a new message</span></span>

  - [<span data-ttu-id="58ee4-116">Crear y enviar menciones como parte de un nuevo mensaje</span><span class="sxs-lookup"><span data-stu-id="58ee4-116">Create and send mentions as part of a new message</span></span>](../api/user-sendmail.md#request-2)
  - [<span data-ttu-id="58ee4-117">Crear menciones como parte de un borrador de mensaje</span><span class="sxs-lookup"><span data-stu-id="58ee4-117">Create mentions as part of a message draft</span></span>](../api/user-post-messages.md#request-2)

- <span data-ttu-id="58ee4-118">Obtener información acerca de menciones en un mensaje</span><span class="sxs-lookup"><span data-stu-id="58ee4-118">Get information about mentions in a message</span></span>

  - [<span data-ttu-id="58ee4-119">Obtener todos los mensajes en el buzón del usuario que ha iniciado sesión que indiquen el usuario</span><span class="sxs-lookup"><span data-stu-id="58ee4-119">Get all the messages in the signed-in user's mailbox that mention the user</span></span>](../api/user-list-messages.md#request-2)
  - [<span data-ttu-id="58ee4-120">Obtener detalles de cada mención en un mensaje</span><span class="sxs-lookup"><span data-stu-id="58ee4-120">Get details of each mention in a message</span></span>](../api/message-get.md#request-2)

- <span data-ttu-id="58ee4-121">[Eliminar una mención](../api/message-delete.md#request-2) en un mensaje</span><span class="sxs-lookup"><span data-stu-id="58ee4-121">[Delete a mention](../api/message-delete.md#request-2) in a message</span></span>

## <a name="access-social-data-around-and-about-a-user"></a><span data-ttu-id="58ee4-122">Datos de contenido social acceso alrededor y acerca de un usuario</span><span class="sxs-lookup"><span data-stu-id="58ee4-122">Access social data around and about a user</span></span>

<span data-ttu-id="58ee4-123">Gráfico de Office encapsula las relaciones entre las distintas entidades en Office 365.</span><span class="sxs-lookup"><span data-stu-id="58ee4-123">Office Graph encapsulates the relationships between different entities in Office 365.</span></span> <span data-ttu-id="58ee4-124">Utilice el gráfico de Office para obtener perspectivas sociales a usuarios individuales a través de Office 365.</span><span class="sxs-lookup"><span data-stu-id="58ee4-124">Use Office Graph to get social insights into individual users across Office 365.</span></span>

- <span data-ttu-id="58ee4-125">Lista de los elementos [tendencias alrededor de](../api/insights-list-trending.md) un usuario</span><span class="sxs-lookup"><span data-stu-id="58ee4-125">List the items [trending around](../api/insights-list-trending.md) a user</span></span>
- <span data-ttu-id="58ee4-126">Los usuarios que han sido [trabajar con](../api/user-list-people.md) la lista de un usuario</span><span class="sxs-lookup"><span data-stu-id="58ee4-126">List users who have been [working with](../api/user-list-people.md) a user</span></span>

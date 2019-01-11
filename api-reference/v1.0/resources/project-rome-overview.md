---
title: Usar la API de Microsoft Graph para trabajar con Project Roma
description: Roma de proyecto es una iniciativa de Microsoft para crear un dispositivo entre experiencias de plataforma. Proyecto Roma permite a una aplicación en un cliente local o el servicio para interactuar con las aplicaciones y servicios en un host remoto cuando el usuario inicia sesión con la misma cuenta de Microsoft que se utilizan para iniciar sesión en el dispositivo de cliente. Esto le permite a las experiencias de entre el dispositivo y multiplataforma de programa que se centran en las tareas de usuario en lugar de dispositivos.
localization_priority: Normal
ms.openlocfilehash: d103bb68560a39cc4491460969a36bb81bb6da44
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840967"
---
# <a name="use-the-microsoft-graph-api-to-work-with-project-rome"></a><span data-ttu-id="5f899-105">Usar la API de Microsoft Graph para trabajar con Project Roma</span><span class="sxs-lookup"><span data-stu-id="5f899-105">Use the Microsoft Graph API to work with Project Rome</span></span>

<span data-ttu-id="5f899-106">[Roma de proyecto](https://developer.microsoft.com/en-us/windows/project-rome) es una iniciativa de Microsoft para crear un dispositivo entre experiencias de plataforma.</span><span class="sxs-lookup"><span data-stu-id="5f899-106">[Project Rome](https://developer.microsoft.com/en-us/windows/project-rome) is a Microsoft initiative to build a cross-device experiences platform.</span></span> <span data-ttu-id="5f899-107">Proyecto Roma permite a una aplicación en un cliente local o el servicio para interactuar con las aplicaciones y servicios en un host remoto cuando el usuario inicia sesión con la misma cuenta de Microsoft que se utilizan para iniciar sesión en el dispositivo de cliente.</span><span class="sxs-lookup"><span data-stu-id="5f899-107">Project Rome enables an app on a local client or service to interact with apps and services on a remote host when the user signs in with the same Microsoft account that they use to sign in on the client device.</span></span> <span data-ttu-id="5f899-108">Esto le permite a las experiencias de entre el dispositivo y multiplataforma de programa que se centran en las tareas de usuario en lugar de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5f899-108">This allows you to program cross-device and cross-platform experiences that are centered around user tasks rather than devices.</span></span>

<span data-ttu-id="5f899-109">Un componente clave se expone a través de Microsoft Graph para habilitar estas evaluaciones: actividades.</span><span class="sxs-lookup"><span data-stu-id="5f899-109">A key component is exposed via Microsoft Graph to enable these experiences: activities.</span></span>

## <a name="activities"></a><span data-ttu-id="5f899-110">Actividades</span><span class="sxs-lookup"><span data-stu-id="5f899-110">Activities</span></span>

<span data-ttu-id="5f899-111">Actividades en Microsoft Graph habilitar compromiso de usuario de unidad con sus aplicaciones en dispositivos y plataformas.</span><span class="sxs-lookup"><span data-stu-id="5f899-111">Activities in Microsoft Graph enable you to drive user engagement with your apps across devices and platforms.</span></span> <span data-ttu-id="5f899-112">Una actividad es la unidad de contratación de usuario y se compone de tres componentes:</span><span class="sxs-lookup"><span data-stu-id="5f899-112">An activity is the unit of user engagement, and consists of three components:</span></span>

- <span data-ttu-id="5f899-113">Un vínculo profundo</span><span class="sxs-lookup"><span data-stu-id="5f899-113">A deep link</span></span>
- <span data-ttu-id="5f899-114">Una representación visual</span><span class="sxs-lookup"><span data-stu-id="5f899-114">A visual representation</span></span>
- <span data-ttu-id="5f899-115">Los metadatos de contenido que describe la actividad, con el [https://schema.org/](https://schema.org/) shared vocabulario</span><span class="sxs-lookup"><span data-stu-id="5f899-115">Content metadata that describes the activity, using the [https://schema.org/](https://schema.org/) shared vocabulary</span></span>

<span data-ttu-id="5f899-116">Cuando se crea una sesión de una aplicación, se agrega un elemento de historial a la actividad para reflejar el período de contratación de usuario.</span><span class="sxs-lookup"><span data-stu-id="5f899-116">When a session is created by an application, a history item is added to the activity to reflect the period of user engagement.</span></span> <span data-ttu-id="5f899-117">Cada vez que un usuario reengages con una actividad, se agrega un nuevo elemento de historial a la actividad para acumular compromiso de usuario.</span><span class="sxs-lookup"><span data-stu-id="5f899-117">Each time a user reengages with an activity, a new history item is added to the activity to accrue user engagement.</span></span>

<span data-ttu-id="5f899-118">Cuando una aplicación publica los objetos de actividad de usuario, el objeto se mostrará en algunas de las nuevas superficies de la interfaz de usuario de Windows; Por ejemplo, las notificaciones de Cortana y escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5f899-118">When an application publishes user activity objects, the object will show up in some of the new UI surfaces in Windows; for example, Cortana Notifications and Timeline.</span></span> <span data-ttu-id="5f899-119">Puede especificar metadatos enriquecidos (para permitir actividades se presenten en el contexto de derecho) y elementos visuales enriquecidos (con el marcado de la [Tarjeta de adaptable](https://adaptivecards.io/) ) en los objetos de actividad.</span><span class="sxs-lookup"><span data-stu-id="5f899-119">You can specify both rich metadata (to allow activities to be presented in just the right context) and rich visuals (using [Adaptive Card](https://adaptivecards.io/) markup) in your activity objects.</span></span>

<span data-ttu-id="5f899-120">Puede usar las siguientes API de gráfico de Microsoft para crear y recuperar las actividades del usuario:</span><span class="sxs-lookup"><span data-stu-id="5f899-120">You can use the following Microsoft Graph APIs to create and retrieve user activities:</span></span>

- [<span data-ttu-id="5f899-121">Crear o reemplazar la actividad</span><span class="sxs-lookup"><span data-stu-id="5f899-121">Create or replace activity</span></span>](../api/projectrome-put-activity.md)
- [<span data-ttu-id="5f899-122">Obtener las actividades</span><span class="sxs-lookup"><span data-stu-id="5f899-122">Get activities</span></span>](../api/projectrome-get-activities.md)
- [<span data-ttu-id="5f899-123">Obtener actividades recientes</span><span class="sxs-lookup"><span data-stu-id="5f899-123">Get recent activities</span></span>](../api/projectrome-get-recent-activities.md)
- [<span data-ttu-id="5f899-124">Eliminar una actividad</span><span class="sxs-lookup"><span data-stu-id="5f899-124">Delete an activity</span></span>](../api/projectrome-delete-activity.md)
- [<span data-ttu-id="5f899-125">Crear o reemplazar un elemento de historial</span><span class="sxs-lookup"><span data-stu-id="5f899-125">Create or replace a history item</span></span>](../api/projectrome-put-historyitem.md)
- [<span data-ttu-id="5f899-126">Eliminar un elemento de historial</span><span class="sxs-lookup"><span data-stu-id="5f899-126">Delete a history item</span></span>](../api/projectrome-delete-historyitem.md)


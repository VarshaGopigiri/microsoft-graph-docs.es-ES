---
title: Crear y enviar una notificación
description: 'Crear y enviar una notificación de identificación de un usuario a través de Microsoft Graph. La notificación se almacena en la notificación de Microsoft Graph fuente almacén y se envía a todos los clientes de la aplicación en todos los extremos de dispositivo que el usuario ha iniciado sesión en.  '
ms.openlocfilehash: 7855d8b369a2efc6dada33c66c12ae76384a2760
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088502"
---
# <a name="create-and-send-a-notification"></a><span data-ttu-id="5a70c-104">Crear y enviar una notificación</span><span class="sxs-lookup"><span data-stu-id="5a70c-104">Create and send a notification</span></span>
> <span data-ttu-id="5a70c-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5a70c-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5a70c-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5a70c-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5a70c-107">Crear y enviar una notificación de identificación de un usuario a través de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="5a70c-107">Create and send a notification targeting a user through Microsoft Graph.</span></span> <span data-ttu-id="5a70c-108">La notificación se almacena en la notificación de Microsoft Graph fuente almacén y se envía a todos los clientes de la aplicación en todos los extremos de dispositivo que el usuario ha iniciado sesión en.</span><span class="sxs-lookup"><span data-stu-id="5a70c-108">The notification is stored in the Microsoft Graph notification feed store, and is sent to all app clients on all device endpoints that the user is signed in to.</span></span>  
## <a name="permissions"></a><span data-ttu-id="5a70c-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="5a70c-109">Permissions</span></span>
<span data-ttu-id="5a70c-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5a70c-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5a70c-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5a70c-112">Permission type</span></span>      | <span data-ttu-id="5a70c-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5a70c-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5a70c-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5a70c-114">Delegated (work or school account)</span></span> | <span data-ttu-id="5a70c-115">Notifications.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="5a70c-115">Notifications.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="5a70c-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5a70c-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5a70c-117">Notifications.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="5a70c-117">Notifications.ReadWrite.CreatedByApp</span></span>    |

## <a name="http-request"></a><span data-ttu-id="5a70c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5a70c-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/notifications/
```
## <a name="request-headers"></a><span data-ttu-id="5a70c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5a70c-119">Request headers</span></span>
|<span data-ttu-id="5a70c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5a70c-120">Name</span></span> | <span data-ttu-id="5a70c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a70c-121">Type</span></span> | <span data-ttu-id="5a70c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a70c-122">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="5a70c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5a70c-123">Authorization</span></span> | <span data-ttu-id="5a70c-124">string</span><span class="sxs-lookup"><span data-stu-id="5a70c-124">string</span></span> |<span data-ttu-id="5a70c-125">El encabezado authorization se utiliza para pasar las credenciales del usuario que realiza llamada.</span><span class="sxs-lookup"><span data-stu-id="5a70c-125">The authorization header is used to pass the credentials of the calling party.</span></span> <span data-ttu-id="5a70c-126">Bearer {token}.</span><span class="sxs-lookup"><span data-stu-id="5a70c-126">Bearer {token}.</span></span> <span data-ttu-id="5a70c-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5a70c-127">Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="5a70c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5a70c-128">Request body</span></span>
<span data-ttu-id="5a70c-129">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [notificación](../resources/projectrome-notification.md) .</span><span class="sxs-lookup"><span data-stu-id="5a70c-129">In the request body, supply a JSON representation of a [notification](../resources/projectrome-notification.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="5a70c-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a70c-130">Response</span></span>
<span data-ttu-id="5a70c-131">Si tiene éxito, este método devuelve el `201 Created` código de respuesta que indica que la notificación se ha creado y almacenados correctamente.</span><span class="sxs-lookup"><span data-stu-id="5a70c-131">If successful, this method returns the `201 Created` response code that indicates that the notification was successfully created and stored.</span></span> 
## <a name="example"></a><span data-ttu-id="5a70c-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5a70c-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="5a70c-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5a70c-133">Request</span></span>
<span data-ttu-id="5a70c-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5a70c-134">The following is an example of the request.</span></span>

```http
POST https://graph.microsoft.com/beta/me/notifications/
Content-type: application/json

{
    "targetHostName": "graphnotifications.sample.windows.com",
    "appNotificationId": "testDirectToastNotification",
    "expirationDateTime": "2018-08-29T23:51:33.000Z",
    "payload": {
        "visualContent": {
            "title": "Hello World!",
            "body": "Notifications are Great!"
        }
    },
    "targetPolicy": {
        "platformTypes": [
        "windows",
        "android"
        ]
    },
    "priority": "High",
    "groupName": "TestGroup",
    "displayTimeToLive": "23"
}
```

#### <a name="response"></a><span data-ttu-id="5a70c-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a70c-135">Response</span></span>
<span data-ttu-id="5a70c-136">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a70c-136">The following is an example of the response.</span></span>

```http
HTTP/1.1 201
Content-Type: application/json
location: https://graph.microsoft.com/beta/me/notifications/518c4fb1-c565-4d67-95c4-bcc3eb8eda1b

{
    "@odata.context": "https://graph.microsoft.com/test872018/$metadata#users('graphNotificationsUser%40contoso.com')/notifications/$entity",
    "appNotificationId": "testDirectToastNotification",
    "displayTimeToLive": 23,
    "expirationDateTime": "2018-08-24T12:31:53.858Z",
    "groupName": "TestGroup",
    "id": "cd5c5e6a-99ce-470a-9982-c47635e73620",
    "priority": "1",
    "payload": {
        "visualContent": {
            "title": "Hello World!",
            "body": "Notifications are Great!"
        }
    }
}
```



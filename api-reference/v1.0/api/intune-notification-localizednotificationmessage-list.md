---
title: Enumerar localizedNotificationMessages
description: Enumere las propiedades y las relaciones de los objetos localizedNotificationMessage.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ffccd0f496c8096e06371f14cdadf7a1a12e08a5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963685"
---
# <a name="list-localizednotificationmessages"></a><span data-ttu-id="fab74-103">Enumerar localizedNotificationMessages</span><span class="sxs-lookup"><span data-stu-id="fab74-103">List localizedNotificationMessages</span></span>

> <span data-ttu-id="fab74-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fab74-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fab74-105">Enumere las propiedades y las relaciones de los objetos [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="fab74-105">List properties and relationships of the [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fab74-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fab74-106">Prerequisites</span></span>
<span data-ttu-id="fab74-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fab74-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fab74-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fab74-109">Permission type</span></span>|<span data-ttu-id="fab74-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fab74-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fab74-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fab74-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fab74-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="fab74-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="fab74-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fab74-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fab74-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fab74-114">Not supported.</span></span>|
|<span data-ttu-id="fab74-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fab74-115">Application</span></span>|<span data-ttu-id="fab74-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fab74-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fab74-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fab74-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages
```

## <a name="request-headers"></a><span data-ttu-id="fab74-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fab74-118">Request headers</span></span>
|<span data-ttu-id="fab74-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fab74-119">Header</span></span>|<span data-ttu-id="fab74-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fab74-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fab74-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fab74-121">Authorization</span></span>|<span data-ttu-id="fab74-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fab74-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fab74-123">Accept</span><span class="sxs-lookup"><span data-stu-id="fab74-123">Accept</span></span>|<span data-ttu-id="fab74-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fab74-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fab74-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fab74-125">Request body</span></span>
<span data-ttu-id="fab74-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fab74-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fab74-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fab74-127">Response</span></span>
<span data-ttu-id="fab74-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fab74-128">If successful, this method returns a `200 OK` response code and a collection of [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fab74-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fab74-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="fab74-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fab74-130">Request</span></span>
<span data-ttu-id="fab74-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fab74-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages
```

### <a name="response"></a><span data-ttu-id="fab74-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fab74-132">Response</span></span>
<span data-ttu-id="fab74-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fab74-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 374

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.localizedNotificationMessage",
      "id": "7a777708-7708-7a77-0877-777a0877777a",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "locale": "Locale value",
      "subject": "Subject value",
      "messageTemplate": "Message Template value",
      "isDefault": true
    }
  ]
}
```




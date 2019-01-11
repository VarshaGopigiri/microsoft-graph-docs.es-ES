---
title: Obtener localizedNotificationMessage
description: Lea las propiedades y las relaciones del objeto localizedNotificationMessage.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: dd341a2bf506d8d17c0bdb604604243c7789ad7e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885354"
---
# <a name="get-localizednotificationmessage"></a><span data-ttu-id="8a8c8-103">Obtener localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="8a8c8-103">Get localizedNotificationMessage</span></span>

> <span data-ttu-id="8a8c8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8a8c8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8a8c8-105">Lea las propiedades y las relaciones del objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="8a8c8-105">Read properties and relationships of the [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8a8c8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8a8c8-106">Prerequisites</span></span>
<span data-ttu-id="8a8c8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8a8c8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8a8c8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a8c8-109">Permission type</span></span>|<span data-ttu-id="8a8c8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a8c8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8a8c8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a8c8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8a8c8-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="8a8c8-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="8a8c8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a8c8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8a8c8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a8c8-114">Not supported.</span></span>|
|<span data-ttu-id="8a8c8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a8c8-115">Application</span></span>|<span data-ttu-id="8a8c8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a8c8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8a8c8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a8c8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages/{localizedNotificationMessageId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8a8c8-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8a8c8-118">Optional query parameters</span></span>
<span data-ttu-id="8a8c8-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a8c8-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="8a8c8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a8c8-120">Request headers</span></span>
|<span data-ttu-id="8a8c8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a8c8-121">Header</span></span>|<span data-ttu-id="8a8c8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8a8c8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8a8c8-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8a8c8-123">Authorization</span></span>|<span data-ttu-id="8a8c8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8a8c8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8a8c8-125">Accept</span><span class="sxs-lookup"><span data-stu-id="8a8c8-125">Accept</span></span>|<span data-ttu-id="8a8c8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8a8c8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8a8c8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a8c8-127">Request body</span></span>
<span data-ttu-id="8a8c8-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8a8c8-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8a8c8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a8c8-129">Response</span></span>
<span data-ttu-id="8a8c8-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a8c8-130">If successful, this method returns a `200 OK` response code and [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a8c8-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a8c8-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="8a8c8-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a8c8-132">Request</span></span>
<span data-ttu-id="8a8c8-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a8c8-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages/{localizedNotificationMessageId}
```

### <a name="response"></a><span data-ttu-id="8a8c8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a8c8-134">Response</span></span>
<span data-ttu-id="8a8c8-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a8c8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 346

{
  "value": {
    "@odata.type": "#microsoft.graph.localizedNotificationMessage",
    "id": "7a777708-7708-7a77-0877-777a0877777a",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "locale": "Locale value",
    "subject": "Subject value",
    "messageTemplate": "Message Template value",
    "isDefault": true
  }
}
```




---
title: Crear localizedNotificationMessage
description: Cree un objeto localizedNotificationMessage.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cd9b2568ccf80d2000271d597baf0a6ace6bf9ca
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968067"
---
# <a name="create-localizednotificationmessage"></a><span data-ttu-id="2d5df-103">Crear localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="2d5df-103">Create localizedNotificationMessage</span></span>

> <span data-ttu-id="2d5df-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2d5df-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2d5df-105">Cree un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="2d5df-105">Create a new [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2d5df-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2d5df-106">Prerequisites</span></span>
<span data-ttu-id="2d5df-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2d5df-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2d5df-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2d5df-109">Permission type</span></span>|<span data-ttu-id="2d5df-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2d5df-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2d5df-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2d5df-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2d5df-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2d5df-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="2d5df-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d5df-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2d5df-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d5df-114">Not supported.</span></span>|
|<span data-ttu-id="2d5df-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2d5df-115">Application</span></span>|<span data-ttu-id="2d5df-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d5df-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2d5df-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d5df-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages
```

## <a name="request-headers"></a><span data-ttu-id="2d5df-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2d5df-118">Request headers</span></span>
|<span data-ttu-id="2d5df-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d5df-119">Header</span></span>|<span data-ttu-id="2d5df-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2d5df-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2d5df-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2d5df-121">Authorization</span></span>|<span data-ttu-id="2d5df-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2d5df-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2d5df-123">Accept</span><span class="sxs-lookup"><span data-stu-id="2d5df-123">Accept</span></span>|<span data-ttu-id="2d5df-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2d5df-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2d5df-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d5df-125">Request body</span></span>
<span data-ttu-id="2d5df-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto localizedNotificationMessage.</span><span class="sxs-lookup"><span data-stu-id="2d5df-126">In the request body, supply a JSON representation for the localizedNotificationMessage object.</span></span>

<span data-ttu-id="2d5df-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto localizedNotificationMessage.</span><span class="sxs-lookup"><span data-stu-id="2d5df-127">The following table shows the properties that are required when you create the localizedNotificationMessage.</span></span>

|<span data-ttu-id="2d5df-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2d5df-128">Property</span></span>|<span data-ttu-id="2d5df-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d5df-129">Type</span></span>|<span data-ttu-id="2d5df-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d5df-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2d5df-131">id</span><span class="sxs-lookup"><span data-stu-id="2d5df-131">id</span></span>|<span data-ttu-id="2d5df-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="2d5df-132">String</span></span>|<span data-ttu-id="2d5df-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2d5df-133">Key of the entity.</span></span>|
|<span data-ttu-id="2d5df-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2d5df-134">lastModifiedDateTime</span></span>|<span data-ttu-id="2d5df-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2d5df-135">DateTimeOffset</span></span>|<span data-ttu-id="2d5df-136">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="2d5df-136">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="2d5df-137">configuración regional</span><span class="sxs-lookup"><span data-stu-id="2d5df-137">locale</span></span>|<span data-ttu-id="2d5df-138">String</span><span class="sxs-lookup"><span data-stu-id="2d5df-138">String</span></span>|<span data-ttu-id="2d5df-139">La configuración regional para la que se destina este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2d5df-139">The Locale for which this message is destined.</span></span>|
|<span data-ttu-id="2d5df-140">subject</span><span class="sxs-lookup"><span data-stu-id="2d5df-140">subject</span></span>|<span data-ttu-id="2d5df-141">String</span><span class="sxs-lookup"><span data-stu-id="2d5df-141">String</span></span>|<span data-ttu-id="2d5df-142">El asunto de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="2d5df-142">The Message Template Subject.</span></span>|
|<span data-ttu-id="2d5df-143">messageTemplate</span><span class="sxs-lookup"><span data-stu-id="2d5df-143">messageTemplate</span></span>|<span data-ttu-id="2d5df-144">String</span><span class="sxs-lookup"><span data-stu-id="2d5df-144">String</span></span>|<span data-ttu-id="2d5df-145">El contenido de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="2d5df-145">The Message Template content.</span></span>|
|<span data-ttu-id="2d5df-146">isDefault</span><span class="sxs-lookup"><span data-stu-id="2d5df-146">isDefault</span></span>|<span data-ttu-id="2d5df-147">Booleano</span><span class="sxs-lookup"><span data-stu-id="2d5df-147">Boolean</span></span>|<span data-ttu-id="2d5df-148">Marca para indicar si se trata de la configuración regional predeterminada para la reserva del idioma.</span><span class="sxs-lookup"><span data-stu-id="2d5df-148">Flag to indicate whether or not this is the default locale for language fallback.</span></span> <span data-ttu-id="2d5df-149">Solo se puede establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="2d5df-149">This flag can only be set.</span></span> <span data-ttu-id="2d5df-150">Para eliminarla, establezca esta propiedad en true en otro mensaje de notificación localizado.</span><span class="sxs-lookup"><span data-stu-id="2d5df-150">To unset, set this property to true on another Localized Notification Message.</span></span>|



## <a name="response"></a><span data-ttu-id="2d5df-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d5df-151">Response</span></span>
<span data-ttu-id="2d5df-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d5df-152">If successful, this method returns a `201 Created` response code and a [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2d5df-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d5df-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="2d5df-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d5df-154">Request</span></span>
<span data-ttu-id="2d5df-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2d5df-155">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages
Content-type: application/json
Content-length: 200

{
  "@odata.type": "#microsoft.graph.localizedNotificationMessage",
  "locale": "Locale value",
  "subject": "Subject value",
  "messageTemplate": "Message Template value",
  "isDefault": true
}
```

### <a name="response"></a><span data-ttu-id="2d5df-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d5df-156">Response</span></span>
<span data-ttu-id="2d5df-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2d5df-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 313

{
  "@odata.type": "#microsoft.graph.localizedNotificationMessage",
  "id": "7a777708-7708-7a77-0877-777a0877777a",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "locale": "Locale value",
  "subject": "Subject value",
  "messageTemplate": "Message Template value",
  "isDefault": true
}
```




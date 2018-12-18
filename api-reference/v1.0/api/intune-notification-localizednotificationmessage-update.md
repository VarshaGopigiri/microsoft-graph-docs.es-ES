---
title: Actualizar localizedNotificationMessage
description: Actualice las propiedades de un objeto localizedNotificationMessage.
author: tfitzmac
ms.openlocfilehash: 117f648b2e8d8172338f00878cc715beac938525
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348828"
---
# <a name="update-localizednotificationmessage"></a><span data-ttu-id="a32f8-103">Actualizar localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="a32f8-103">Update localizedNotificationMessage</span></span>

> <span data-ttu-id="a32f8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a32f8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a32f8-105">Actualice las propiedades de un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="a32f8-105">Update the properties of a [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a32f8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a32f8-106">Prerequisites</span></span>
<span data-ttu-id="a32f8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a32f8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a32f8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a32f8-109">Permission type</span></span>|<span data-ttu-id="a32f8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a32f8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a32f8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a32f8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a32f8-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a32f8-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="a32f8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a32f8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a32f8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a32f8-114">Not supported.</span></span>|
|<span data-ttu-id="a32f8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a32f8-115">Application</span></span>|<span data-ttu-id="a32f8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a32f8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a32f8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a32f8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages/{localizedNotificationMessageId}
```

## <a name="request-headers"></a><span data-ttu-id="a32f8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a32f8-118">Request headers</span></span>
|<span data-ttu-id="a32f8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a32f8-119">Header</span></span>|<span data-ttu-id="a32f8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a32f8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a32f8-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="a32f8-121">Authorization</span></span>|<span data-ttu-id="a32f8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a32f8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a32f8-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a32f8-123">Accept</span></span>|<span data-ttu-id="a32f8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a32f8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a32f8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a32f8-125">Request body</span></span>
<span data-ttu-id="a32f8-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="a32f8-126">In the request body, supply a JSON representation for the [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object.</span></span>

<span data-ttu-id="a32f8-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="a32f8-127">The following table shows the properties that are required when you create the [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span></span>

|<span data-ttu-id="a32f8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a32f8-128">Property</span></span>|<span data-ttu-id="a32f8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a32f8-129">Type</span></span>|<span data-ttu-id="a32f8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a32f8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a32f8-131">id</span><span class="sxs-lookup"><span data-stu-id="a32f8-131">id</span></span>|<span data-ttu-id="a32f8-132">String</span><span class="sxs-lookup"><span data-stu-id="a32f8-132">String</span></span>|<span data-ttu-id="a32f8-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a32f8-133">Key of the entity.</span></span>|
|<span data-ttu-id="a32f8-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a32f8-134">lastModifiedDateTime</span></span>|<span data-ttu-id="a32f8-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a32f8-135">DateTimeOffset</span></span>|<span data-ttu-id="a32f8-136">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a32f8-136">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="a32f8-137">configuración regional</span><span class="sxs-lookup"><span data-stu-id="a32f8-137">locale</span></span>|<span data-ttu-id="a32f8-138">String</span><span class="sxs-lookup"><span data-stu-id="a32f8-138">String</span></span>|<span data-ttu-id="a32f8-139">La configuración regional para la que se destina este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a32f8-139">The Locale for which this message is destined.</span></span>|
|<span data-ttu-id="a32f8-140">subject</span><span class="sxs-lookup"><span data-stu-id="a32f8-140">subject</span></span>|<span data-ttu-id="a32f8-141">String</span><span class="sxs-lookup"><span data-stu-id="a32f8-141">String</span></span>|<span data-ttu-id="a32f8-142">El asunto de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a32f8-142">The Message Template Subject.</span></span>|
|<span data-ttu-id="a32f8-143">messageTemplate</span><span class="sxs-lookup"><span data-stu-id="a32f8-143">messageTemplate</span></span>|<span data-ttu-id="a32f8-144">String</span><span class="sxs-lookup"><span data-stu-id="a32f8-144">String</span></span>|<span data-ttu-id="a32f8-145">El contenido de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a32f8-145">The Message Template content.</span></span>|
|<span data-ttu-id="a32f8-146">isDefault</span><span class="sxs-lookup"><span data-stu-id="a32f8-146">isDefault</span></span>|<span data-ttu-id="a32f8-147">Boolean</span><span class="sxs-lookup"><span data-stu-id="a32f8-147">Boolean</span></span>|<span data-ttu-id="a32f8-148">Marca para indicar si se trata de la configuración regional predeterminada para la reserva del idioma.</span><span class="sxs-lookup"><span data-stu-id="a32f8-148">Flag to indicate whether or not this is the default locale for language fallback.</span></span> <span data-ttu-id="a32f8-149">Solo se puede establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="a32f8-149">This flag can only be set.</span></span> <span data-ttu-id="a32f8-150">Para eliminarla, establezca esta propiedad en true en otro mensaje de notificación localizado.</span><span class="sxs-lookup"><span data-stu-id="a32f8-150">To unset, set this property to true on another Localized Notification Message.</span></span>|



## <a name="response"></a><span data-ttu-id="a32f8-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a32f8-151">Response</span></span>
<span data-ttu-id="a32f8-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a32f8-152">If successful, this method returns a `200 OK` response code and an updated [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a32f8-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a32f8-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="a32f8-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a32f8-154">Request</span></span>
<span data-ttu-id="a32f8-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a32f8-155">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages/{localizedNotificationMessageId}
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

### <a name="response"></a><span data-ttu-id="a32f8-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a32f8-156">Response</span></span>
<span data-ttu-id="a32f8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a32f8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




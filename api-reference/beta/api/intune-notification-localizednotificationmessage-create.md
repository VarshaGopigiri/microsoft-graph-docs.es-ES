---
title: Crear localizedNotificationMessage
description: Cree un objeto localizedNotificationMessage.
ms.openlocfilehash: b894055804104c61c9991066f273f4c9bce34629
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085506"
---
# <a name="create-localizednotificationmessage"></a><span data-ttu-id="7aab1-103">Crear localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="7aab1-103">Create localizedNotificationMessage</span></span>

> <span data-ttu-id="7aab1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7aab1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7aab1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7aab1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7aab1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7aab1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7aab1-107">Cree un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="7aab1-107">Create a new [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7aab1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7aab1-108">Prerequisites</span></span>
<span data-ttu-id="7aab1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7aab1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7aab1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7aab1-111">Permission type</span></span>|<span data-ttu-id="7aab1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7aab1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7aab1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7aab1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7aab1-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7aab1-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="7aab1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7aab1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7aab1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7aab1-116">Not supported.</span></span>|
|<span data-ttu-id="7aab1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7aab1-117">Application</span></span>|<span data-ttu-id="7aab1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7aab1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7aab1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7aab1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages
```

## <a name="request-headers"></a><span data-ttu-id="7aab1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7aab1-120">Request headers</span></span>
|<span data-ttu-id="7aab1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7aab1-121">Header</span></span>|<span data-ttu-id="7aab1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7aab1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7aab1-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7aab1-123">Authorization</span></span>|<span data-ttu-id="7aab1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7aab1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7aab1-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7aab1-125">Accept</span></span>|<span data-ttu-id="7aab1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7aab1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7aab1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7aab1-127">Request body</span></span>
<span data-ttu-id="7aab1-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto localizedNotificationMessage.</span><span class="sxs-lookup"><span data-stu-id="7aab1-128">In the request body, supply a JSON representation for the localizedNotificationMessage object.</span></span>

<span data-ttu-id="7aab1-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto localizedNotificationMessage.</span><span class="sxs-lookup"><span data-stu-id="7aab1-129">The following table shows the properties that are required when you create the localizedNotificationMessage.</span></span>

|<span data-ttu-id="7aab1-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7aab1-130">Property</span></span>|<span data-ttu-id="7aab1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7aab1-131">Type</span></span>|<span data-ttu-id="7aab1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7aab1-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7aab1-133">id</span><span class="sxs-lookup"><span data-stu-id="7aab1-133">id</span></span>|<span data-ttu-id="7aab1-134">String</span><span class="sxs-lookup"><span data-stu-id="7aab1-134">String</span></span>|<span data-ttu-id="7aab1-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7aab1-135">Key of the entity.</span></span>|
|<span data-ttu-id="7aab1-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7aab1-136">lastModifiedDateTime</span></span>|<span data-ttu-id="7aab1-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7aab1-137">DateTimeOffset</span></span>|<span data-ttu-id="7aab1-138">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="7aab1-138">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="7aab1-139">configuración regional</span><span class="sxs-lookup"><span data-stu-id="7aab1-139">locale</span></span>|<span data-ttu-id="7aab1-140">String</span><span class="sxs-lookup"><span data-stu-id="7aab1-140">String</span></span>|<span data-ttu-id="7aab1-141">La configuración regional para la que se destina este mensaje.</span><span class="sxs-lookup"><span data-stu-id="7aab1-141">The Locale for which this message is destined.</span></span>|
|<span data-ttu-id="7aab1-142">subject</span><span class="sxs-lookup"><span data-stu-id="7aab1-142">subject</span></span>|<span data-ttu-id="7aab1-143">String</span><span class="sxs-lookup"><span data-stu-id="7aab1-143">String</span></span>|<span data-ttu-id="7aab1-144">El asunto de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="7aab1-144">The Message Template Subject.</span></span>|
|<span data-ttu-id="7aab1-145">messageTemplate</span><span class="sxs-lookup"><span data-stu-id="7aab1-145">messageTemplate</span></span>|<span data-ttu-id="7aab1-146">String</span><span class="sxs-lookup"><span data-stu-id="7aab1-146">String</span></span>|<span data-ttu-id="7aab1-147">El contenido de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="7aab1-147">The Message Template content.</span></span>|
|<span data-ttu-id="7aab1-148">isDefault</span><span class="sxs-lookup"><span data-stu-id="7aab1-148">isDefault</span></span>|<span data-ttu-id="7aab1-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="7aab1-149">Boolean</span></span>|<span data-ttu-id="7aab1-150">Marca para indicar si se trata de la configuración regional predeterminada para la reserva del idioma.</span><span class="sxs-lookup"><span data-stu-id="7aab1-150">Flag to indicate whether or not this is the default locale for language fallback.</span></span> <span data-ttu-id="7aab1-151">Solo se puede establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="7aab1-151">This flag can only be set.</span></span> <span data-ttu-id="7aab1-152">Para eliminarla, establezca esta propiedad en true en otro mensaje de notificación localizado.</span><span class="sxs-lookup"><span data-stu-id="7aab1-152">To unset, set this property to true on another Localized Notification Message.</span></span>|



## <a name="response"></a><span data-ttu-id="7aab1-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7aab1-153">Response</span></span>
<span data-ttu-id="7aab1-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7aab1-154">If successful, this method returns a `201 Created` response code and a [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7aab1-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7aab1-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="7aab1-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7aab1-156">Request</span></span>
<span data-ttu-id="7aab1-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7aab1-157">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages
Content-type: application/json
Content-length: 264

{
  "@odata.type": "#microsoft.graph.localizedNotificationMessage",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "locale": "Locale value",
  "subject": "Subject value",
  "messageTemplate": "Message Template value",
  "isDefault": true
}
```

### <a name="response"></a><span data-ttu-id="7aab1-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7aab1-158">Response</span></span>
<span data-ttu-id="7aab1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7aab1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





# <a name="update-localizednotificationmessage"></a><span data-ttu-id="52f29-101">Actualizar localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="52f29-101">Update localizedNotificationMessage</span></span>

> <span data-ttu-id="52f29-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="52f29-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="52f29-103">Actualice las propiedades de un objeto [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="52f29-103">Update the properties of a [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="52f29-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="52f29-104">Prerequisites</span></span>
<span data-ttu-id="52f29-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="52f29-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="52f29-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="52f29-107">Permission type</span></span>|<span data-ttu-id="52f29-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="52f29-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="52f29-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="52f29-109">Delegated (work or school account)</span></span>|<span data-ttu-id="52f29-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="52f29-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="52f29-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="52f29-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="52f29-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52f29-112">Not supported.</span></span>|
|<span data-ttu-id="52f29-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="52f29-113">Application</span></span>|<span data-ttu-id="52f29-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52f29-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="52f29-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52f29-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages/{localizedNotificationMessageId}
```

## <a name="request-headers"></a><span data-ttu-id="52f29-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52f29-116">Request headers</span></span>
|<span data-ttu-id="52f29-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52f29-117">Header</span></span>|<span data-ttu-id="52f29-118">Valor</span><span class="sxs-lookup"><span data-stu-id="52f29-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="52f29-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="52f29-119">Authorization</span></span>|<span data-ttu-id="52f29-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="52f29-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="52f29-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="52f29-121">Accept</span></span>|<span data-ttu-id="52f29-122">application/json</span><span class="sxs-lookup"><span data-stu-id="52f29-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="52f29-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52f29-123">Request body</span></span>
<span data-ttu-id="52f29-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="52f29-124">In the request body, supply a JSON representation for the [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md) object.</span></span>

<span data-ttu-id="52f29-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="52f29-125">The following table shows the properties that are required when you create the [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md).</span></span>

|<span data-ttu-id="52f29-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="52f29-126">Property</span></span>|<span data-ttu-id="52f29-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="52f29-127">Type</span></span>|<span data-ttu-id="52f29-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="52f29-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="52f29-129">id</span><span class="sxs-lookup"><span data-stu-id="52f29-129">id</span></span>|<span data-ttu-id="52f29-130">String</span><span class="sxs-lookup"><span data-stu-id="52f29-130">String</span></span>|<span data-ttu-id="52f29-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="52f29-131">Key of the entity.</span></span>|
|<span data-ttu-id="52f29-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="52f29-132">lastModifiedDateTime</span></span>|<span data-ttu-id="52f29-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="52f29-133">DateTimeOffset</span></span>|<span data-ttu-id="52f29-134">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="52f29-134">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="52f29-135">configuración regional</span><span class="sxs-lookup"><span data-stu-id="52f29-135">locale</span></span>|<span data-ttu-id="52f29-136">String</span><span class="sxs-lookup"><span data-stu-id="52f29-136">String</span></span>|<span data-ttu-id="52f29-137">La configuración regional para la que se destina este mensaje.</span><span class="sxs-lookup"><span data-stu-id="52f29-137">The Locale for which this message is destined.</span></span>|
|<span data-ttu-id="52f29-138">subject</span><span class="sxs-lookup"><span data-stu-id="52f29-138">subject</span></span>|<span data-ttu-id="52f29-139">String</span><span class="sxs-lookup"><span data-stu-id="52f29-139">String</span></span>|<span data-ttu-id="52f29-140">El asunto de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="52f29-140">The Message Template Subject.</span></span>|
|<span data-ttu-id="52f29-141">messageTemplate</span><span class="sxs-lookup"><span data-stu-id="52f29-141">messageTemplate</span></span>|<span data-ttu-id="52f29-142">String</span><span class="sxs-lookup"><span data-stu-id="52f29-142">String</span></span>|<span data-ttu-id="52f29-143">El contenido de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="52f29-143">The Message Template content.</span></span>|
|<span data-ttu-id="52f29-144">isDefault</span><span class="sxs-lookup"><span data-stu-id="52f29-144">isDefault</span></span>|<span data-ttu-id="52f29-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="52f29-145">Boolean</span></span>|<span data-ttu-id="52f29-146">Marca para indicar si se trata de la configuración regional predeterminada para la reserva del idioma.</span><span class="sxs-lookup"><span data-stu-id="52f29-146">Flag to indicate whether or not this is the default locale for language fallback.</span></span> <span data-ttu-id="52f29-147">Solo se puede establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="52f29-147">This flag can only be set.</span></span> <span data-ttu-id="52f29-148">Para eliminarla, establezca esta propiedad en true en otro mensaje de notificación localizado.</span><span class="sxs-lookup"><span data-stu-id="52f29-148">To unset, set this property to true on another Localized Notification Message.</span></span>|



## <a name="response"></a><span data-ttu-id="52f29-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52f29-149">Response</span></span>
<span data-ttu-id="52f29-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52f29-150">If successful, this method returns a `200 OK` response code and an updated [localizedNotificationMessage](../resources/intune_notification_localizednotificationmessage.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="52f29-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52f29-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="52f29-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52f29-152">Request</span></span>
<span data-ttu-id="52f29-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52f29-153">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="52f29-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52f29-154">Response</span></span>
<span data-ttu-id="52f29-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52f29-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




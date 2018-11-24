# <a name="update-notificationmessagetemplate"></a><span data-ttu-id="97814-101">Actualizar notificationMessageTemplate</span><span class="sxs-lookup"><span data-stu-id="97814-101">Update notificationMessageTemplate</span></span>

> <span data-ttu-id="97814-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="97814-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="97814-103">Actualice las propiedades de un objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="97814-103">Update the properties of a [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="97814-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="97814-104">Prerequisites</span></span>
<span data-ttu-id="97814-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="97814-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="97814-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="97814-107">Permission type</span></span>|<span data-ttu-id="97814-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="97814-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="97814-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="97814-109">Delegated (work or school account)</span></span>|<span data-ttu-id="97814-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="97814-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="97814-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="97814-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="97814-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97814-112">Not supported.</span></span>|
|<span data-ttu-id="97814-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="97814-113">Application</span></span>|<span data-ttu-id="97814-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97814-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="97814-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="97814-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}
```

## <a name="request-headers"></a><span data-ttu-id="97814-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="97814-116">Request headers</span></span>
|<span data-ttu-id="97814-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97814-117">Header</span></span>|<span data-ttu-id="97814-118">Valor</span><span class="sxs-lookup"><span data-stu-id="97814-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="97814-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="97814-119">Authorization</span></span>|<span data-ttu-id="97814-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="97814-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="97814-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="97814-121">Accept</span></span>|<span data-ttu-id="97814-122">application/json</span><span class="sxs-lookup"><span data-stu-id="97814-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="97814-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="97814-123">Request body</span></span>
<span data-ttu-id="97814-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="97814-124">In the request body, supply a JSON representation for the [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md) object.</span></span>

<span data-ttu-id="97814-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="97814-125">The following table shows the properties that are required when you create the [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).</span></span>

|<span data-ttu-id="97814-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="97814-126">Property</span></span>|<span data-ttu-id="97814-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="97814-127">Type</span></span>|<span data-ttu-id="97814-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="97814-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="97814-129">id</span><span class="sxs-lookup"><span data-stu-id="97814-129">id</span></span>|<span data-ttu-id="97814-130">String</span><span class="sxs-lookup"><span data-stu-id="97814-130">String</span></span>|<span data-ttu-id="97814-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="97814-131">Key of the entity.</span></span>|
|<span data-ttu-id="97814-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="97814-132">lastModifiedDateTime</span></span>|<span data-ttu-id="97814-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="97814-133">DateTimeOffset</span></span>|<span data-ttu-id="97814-134">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="97814-134">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="97814-135">displayName</span><span class="sxs-lookup"><span data-stu-id="97814-135">displayName</span></span>|<span data-ttu-id="97814-136">String</span><span class="sxs-lookup"><span data-stu-id="97814-136">String</span></span>|<span data-ttu-id="97814-137">Nombre para mostrar de la plantilla de mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="97814-137">Display name for the Notification Message Template.</span></span>|
|<span data-ttu-id="97814-138">defaultLocale</span><span class="sxs-lookup"><span data-stu-id="97814-138">defaultLocale</span></span>|<span data-ttu-id="97814-139">String</span><span class="sxs-lookup"><span data-stu-id="97814-139">String</span></span>|<span data-ttu-id="97814-140">La configuración regional predeterminada de reserva para los casos en que la configuración regional solicitada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="97814-140">The default locale to fallback onto when the requested locale is not available.</span></span>|
|<span data-ttu-id="97814-141">brandingOptions</span><span class="sxs-lookup"><span data-stu-id="97814-141">brandingOptions</span></span>|[<span data-ttu-id="97814-142">notificationTemplateBrandingOptions</span><span class="sxs-lookup"><span data-stu-id="97814-142">notificationTemplateBrandingOptions</span></span>](../resources/intune_notification_notificationtemplatebrandingoptions.md)|<span data-ttu-id="97814-143">Las opciones de personalización de marca de la plantilla de mensaje.</span><span class="sxs-lookup"><span data-stu-id="97814-143">The Message Template Branding Options.</span></span> <span data-ttu-id="97814-144">La personalización de marca está definida en la consola de administración de Intune.</span><span class="sxs-lookup"><span data-stu-id="97814-144">Branding is defined in the Intune Admin Console.</span></span> <span data-ttu-id="97814-145">Los valores posibles son: `none`, `includeCompanyLogo`, `includeCompanyName` y `includeContactInformation`.</span><span class="sxs-lookup"><span data-stu-id="97814-145">Possible values are: `none`, `includeCompanyLogo`, `includeCompanyName`, `includeContactInformation`.</span></span>|



## <a name="response"></a><span data-ttu-id="97814-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97814-146">Response</span></span>
<span data-ttu-id="97814-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="97814-147">If successful, this method returns a `200 OK` response code and an updated [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="97814-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97814-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="97814-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="97814-149">Request</span></span>
<span data-ttu-id="97814-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97814-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}
Content-type: application/json
Content-length: 197

{
  "@odata.type": "#microsoft.graph.notificationMessageTemplate",
  "displayName": "Display Name value",
  "defaultLocale": "Default Locale value",
  "brandingOptions": "includeCompanyLogo"
}
```

### <a name="response"></a><span data-ttu-id="97814-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97814-151">Response</span></span>
<span data-ttu-id="97814-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="97814-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 310

{
  "@odata.type": "#microsoft.graph.notificationMessageTemplate",
  "id": "e1db399b-399b-e1db-9b39-dbe19b39dbe1",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "defaultLocale": "Default Locale value",
  "brandingOptions": "includeCompanyLogo"
}
```




# <a name="update-notificationmessagetemplate"></a><span data-ttu-id="9c72e-101">Actualizar notificationMessageTemplate</span><span class="sxs-lookup"><span data-stu-id="9c72e-101">Update notificationMessageTemplate</span></span>

> <span data-ttu-id="9c72e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9c72e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9c72e-103">Actualice las propiedades de un objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="9c72e-103">Update the properties of a [calendar](../resources/intune_notification_notificationmessagetemplate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9c72e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9c72e-104">Prerequisites</span></span>
<span data-ttu-id="9c72e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9c72e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9c72e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9c72e-107">Permission type</span></span>|<span data-ttu-id="9c72e-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9c72e-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9c72e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9c72e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="9c72e-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9c72e-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="9c72e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9c72e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9c72e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9c72e-112">Not supported.</span></span>|
|<span data-ttu-id="9c72e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9c72e-113">Application</span></span>|<span data-ttu-id="9c72e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9c72e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9c72e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9c72e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}
```

## <a name="request-headers"></a><span data-ttu-id="9c72e-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9c72e-116">Request headers</span></span>
|<span data-ttu-id="9c72e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c72e-117">Header</span></span>|<span data-ttu-id="9c72e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9c72e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9c72e-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="9c72e-119">Authorization</span></span>|<span data-ttu-id="9c72e-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9c72e-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="9c72e-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9c72e-121">Accept</span></span>|<span data-ttu-id="9c72e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="9c72e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9c72e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9c72e-123">Request body</span></span>
<span data-ttu-id="9c72e-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="9c72e-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_notification_notificationmessagetemplate.md) object.</span></span>

<span data-ttu-id="9c72e-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="9c72e-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="9c72e-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9c72e-126">Property</span></span>|<span data-ttu-id="9c72e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c72e-127">Type</span></span>|<span data-ttu-id="9c72e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c72e-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9c72e-129">id</span><span class="sxs-lookup"><span data-stu-id="9c72e-129">id</span></span>|<span data-ttu-id="9c72e-130">String</span><span class="sxs-lookup"><span data-stu-id="9c72e-130">String</span></span>|<span data-ttu-id="9c72e-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9c72e-131">Key of the setting.</span></span>|
|<span data-ttu-id="9c72e-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9c72e-132">lastModifiedDateTime</span></span>|<span data-ttu-id="9c72e-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9c72e-133">DateTimeOffset</span></span>|<span data-ttu-id="9c72e-134">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="9c72e-134">Indicates the date the object was last modified.</span></span>|
|<span data-ttu-id="9c72e-135">displayName</span><span class="sxs-lookup"><span data-stu-id="9c72e-135">displayName</span></span>|<span data-ttu-id="9c72e-136">String</span><span class="sxs-lookup"><span data-stu-id="9c72e-136">String</span></span>|<span data-ttu-id="9c72e-137">Nombre para mostrar de la plantilla de mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="9c72e-137">Display name for the Notification Message Template.</span></span>|
|<span data-ttu-id="9c72e-138">defaultLocale</span><span class="sxs-lookup"><span data-stu-id="9c72e-138">DefaultLocale</span></span>|<span data-ttu-id="9c72e-139">String</span><span class="sxs-lookup"><span data-stu-id="9c72e-139">String</span></span>|<span data-ttu-id="9c72e-140">La configuración regional predeterminada de reserva para los casos en que la configuración regional solicitada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9c72e-140">The default locale to fallback onto when the requested locale is not available.</span></span>|
|<span data-ttu-id="9c72e-141">brandingOptions</span><span class="sxs-lookup"><span data-stu-id="9c72e-141">brandingOptions</span></span>|<span data-ttu-id="9c72e-142">String</span><span class="sxs-lookup"><span data-stu-id="9c72e-142">String</span></span>|<span data-ttu-id="9c72e-143">Las opciones de personalización de marca de la plantilla de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9c72e-143">The Message Template Branding Options.</span></span> <span data-ttu-id="9c72e-144">La personalización de marca está definida en la consola de administración de Intune.</span><span class="sxs-lookup"><span data-stu-id="9c72e-144">Branding is defined in the Intune Admin Console.</span></span> <span data-ttu-id="9c72e-145">Los valores posibles son: `none`, `includeCompanyLogo`, `includeCompanyName` y `includeContactInformation`.</span><span class="sxs-lookup"><span data-stu-id="9c72e-145">Possible values are: `none`, `includeCompanyLogo`, `includeCompanyName`, `includeContactInformation`.</span></span>|



## <a name="response"></a><span data-ttu-id="9c72e-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c72e-146">Response</span></span>
<span data-ttu-id="9c72e-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c72e-147">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_notification_notificationmessagetemplate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9c72e-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9c72e-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="9c72e-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9c72e-149">Request</span></span>
<span data-ttu-id="9c72e-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c72e-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}
Content-type: application/json
Content-length: 195

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "defaultLocale": "Default Locale value",
  "brandingOptions": "includeCompanyLogo"
}
```

### <a name="response"></a><span data-ttu-id="9c72e-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9c72e-151">Response</span></span>
<span data-ttu-id="9c72e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9c72e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




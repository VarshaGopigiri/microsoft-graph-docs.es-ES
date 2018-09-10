# <a name="update-applepushnotificationcertificate"></a><span data-ttu-id="53503-101">Actualizar applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="53503-101">Update applePushNotificationCertificate</span></span>

> <span data-ttu-id="53503-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53503-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53503-103">Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="53503-103">Update the properties of a [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="53503-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="53503-104">Prerequisites</span></span>
<span data-ttu-id="53503-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="53503-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="53503-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53503-107">Permission type</span></span>|<span data-ttu-id="53503-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53503-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="53503-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53503-109">Delegated (work or school account)</span></span>|<span data-ttu-id="53503-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="53503-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="53503-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53503-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="53503-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53503-112">Not supported.</span></span>|
|<span data-ttu-id="53503-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53503-113">Application</span></span>|<span data-ttu-id="53503-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53503-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="53503-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53503-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/applePushNotificationCertificate
```

## <a name="request-headers"></a><span data-ttu-id="53503-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53503-116">Request headers</span></span>
|<span data-ttu-id="53503-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53503-117">Header</span></span>|<span data-ttu-id="53503-118">Valor</span><span class="sxs-lookup"><span data-stu-id="53503-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="53503-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="53503-119">Authorization</span></span>|<span data-ttu-id="53503-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="53503-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="53503-121">Accept</span><span class="sxs-lookup"><span data-stu-id="53503-121">Accept</span></span>|<span data-ttu-id="53503-122">application/json</span><span class="sxs-lookup"><span data-stu-id="53503-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="53503-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53503-123">Request body</span></span>
<span data-ttu-id="53503-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="53503-124">In the request body, supply a JSON representation for the [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md) object.</span></span>

<span data-ttu-id="53503-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="53503-125">The following table shows the properties that are required when you create the [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span></span>

|<span data-ttu-id="53503-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53503-126">Property</span></span>|<span data-ttu-id="53503-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="53503-127">Type</span></span>|<span data-ttu-id="53503-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="53503-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53503-129">id</span><span class="sxs-lookup"><span data-stu-id="53503-129">id</span></span>|<span data-ttu-id="53503-130">String</span><span class="sxs-lookup"><span data-stu-id="53503-130">String</span></span>|<span data-ttu-id="53503-131">Identificador único del certificado</span><span class="sxs-lookup"><span data-stu-id="53503-131">Unique Identifier for the certificate</span></span>|
|<span data-ttu-id="53503-132">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="53503-132">appleIdentifier</span></span>|<span data-ttu-id="53503-133">String</span><span class="sxs-lookup"><span data-stu-id="53503-133">String</span></span>|<span data-ttu-id="53503-134">Id. de Apple de la cuenta que se usó para crear el certificado push MDM.</span><span class="sxs-lookup"><span data-stu-id="53503-134">Apple Id of the account used to create the MDM push certificate.</span></span>|
|<span data-ttu-id="53503-135">topicIdentifier</span><span class="sxs-lookup"><span data-stu-id="53503-135">topicIdentifier</span></span>|<span data-ttu-id="53503-136">String</span><span class="sxs-lookup"><span data-stu-id="53503-136">String</span></span>|<span data-ttu-id="53503-137">Id. del tema</span><span class="sxs-lookup"><span data-stu-id="53503-137">Topic Id.</span></span>|
|<span data-ttu-id="53503-138">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="53503-138">lastModifiedDateTime</span></span>|<span data-ttu-id="53503-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53503-139">DateTimeOffset</span></span>|<span data-ttu-id="53503-140">Fecha y hora de la última modificación del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="53503-140">Last modified date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="53503-141">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="53503-141">expirationDateTime</span></span>|<span data-ttu-id="53503-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53503-142">DateTimeOffset</span></span>|<span data-ttu-id="53503-143">Fecha y hora de la expiración del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="53503-143">The expiration date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="53503-144">certificado</span><span class="sxs-lookup"><span data-stu-id="53503-144">certificate</span></span>|<span data-ttu-id="53503-145">String</span><span class="sxs-lookup"><span data-stu-id="53503-145">String</span></span>|<span data-ttu-id="53503-146">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="53503-146">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="53503-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53503-147">Response</span></span>
<span data-ttu-id="53503-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53503-148">If successful, this method returns a `200 OK` response code and an updated [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53503-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53503-149">Example</span></span>
### <a name="request"></a><span data-ttu-id="53503-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53503-150">Request</span></span>
<span data-ttu-id="53503-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53503-151">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/applePushNotificationCertificate
Content-type: application/json
Content-length: 264

{
  "appleIdentifier": "Apple Identifier value",
  "topicIdentifier": "Topic Identifier value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "certificate": "Certificate value"
}
```

### <a name="response"></a><span data-ttu-id="53503-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53503-152">Response</span></span>
<span data-ttu-id="53503-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="53503-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 384

{
  "@odata.type": "#microsoft.graph.applePushNotificationCertificate",
  "id": "c4c8f047-f047-c4c8-47f0-c8c447f0c8c4",
  "appleIdentifier": "Apple Identifier value",
  "topicIdentifier": "Topic Identifier value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "certificate": "Certificate value"
}
```









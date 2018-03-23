# <a name="update-applepushnotificationcertificate"></a><span data-ttu-id="cbb2b-101">Actualizar applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="cbb2b-101">Update applePushNotificationCertificate</span></span>

> <span data-ttu-id="cbb2b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cbb2b-103">Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="cbb2b-103">Update the properties of a [calendar](../resources/intune_devices_applepushnotificationcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cbb2b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cbb2b-104">Prerequisites</span></span>
<span data-ttu-id="cbb2b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cbb2b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cbb2b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cbb2b-107">Permission type</span></span>|<span data-ttu-id="cbb2b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cbb2b-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cbb2b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cbb2b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="cbb2b-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cbb2b-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="cbb2b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cbb2b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cbb2b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-112">Not supported.</span></span>|
|<span data-ttu-id="cbb2b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cbb2b-113">Application</span></span>|<span data-ttu-id="cbb2b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cbb2b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cbb2b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/applePushNotificationCertificate
```

## <a name="request-headers"></a><span data-ttu-id="cbb2b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cbb2b-116">Request headers</span></span>
|<span data-ttu-id="cbb2b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbb2b-117">Header</span></span>|<span data-ttu-id="cbb2b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cbb2b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cbb2b-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="cbb2b-119">Authorization</span></span>|<span data-ttu-id="cbb2b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="cbb2b-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cbb2b-121">Accept</span></span>|<span data-ttu-id="cbb2b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="cbb2b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cbb2b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cbb2b-123">Request body</span></span>
<span data-ttu-id="cbb2b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="cbb2b-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_devices_applepushnotificationcertificate.md) object.</span></span>

<span data-ttu-id="cbb2b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="cbb2b-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="cbb2b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cbb2b-126">Property</span></span>|<span data-ttu-id="cbb2b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbb2b-127">Type</span></span>|<span data-ttu-id="cbb2b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb2b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cbb2b-129">id</span><span class="sxs-lookup"><span data-stu-id="cbb2b-129">id</span></span>|<span data-ttu-id="cbb2b-130">String</span><span class="sxs-lookup"><span data-stu-id="cbb2b-130">String</span></span>|<span data-ttu-id="cbb2b-131">Identificador único del certificado</span><span class="sxs-lookup"><span data-stu-id="cbb2b-131">Unique Identifier for the certificate</span></span>|
|<span data-ttu-id="cbb2b-132">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="cbb2b-132">appleIdentifier</span></span>|<span data-ttu-id="cbb2b-133">String</span><span class="sxs-lookup"><span data-stu-id="cbb2b-133">String</span></span>|<span data-ttu-id="cbb2b-134">Id. de Apple de la cuenta que se usó para crear el certificado push MDM.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-134">Apple Id of the account used to create the MDM push certificate.</span></span>|
|<span data-ttu-id="cbb2b-135">topicIdentifier</span><span class="sxs-lookup"><span data-stu-id="cbb2b-135">topicIdentifier</span></span>|<span data-ttu-id="cbb2b-136">String</span><span class="sxs-lookup"><span data-stu-id="cbb2b-136">String</span></span>|<span data-ttu-id="cbb2b-137">Id. del tema</span><span class="sxs-lookup"><span data-stu-id="cbb2b-137">Topic Id.</span></span>|
|<span data-ttu-id="cbb2b-138">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cbb2b-138">lastModifiedDateTime</span></span>|<span data-ttu-id="cbb2b-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cbb2b-139">DateTimeOffset</span></span>|<span data-ttu-id="cbb2b-140">Fecha y hora de la última modificación del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-140">Last modified date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="cbb2b-141">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="cbb2b-141">expirationDateTime</span></span>|<span data-ttu-id="cbb2b-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cbb2b-142">DateTimeOffset</span></span>|<span data-ttu-id="cbb2b-143">Fecha y hora de la expiración del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-143">The expiration date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="cbb2b-144">certificado</span><span class="sxs-lookup"><span data-stu-id="cbb2b-144">ACS, certificate</span></span>|<span data-ttu-id="cbb2b-145">String</span><span class="sxs-lookup"><span data-stu-id="cbb2b-145">String</span></span>|<span data-ttu-id="cbb2b-146">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cbb2b-146">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="cbb2b-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbb2b-147">Response</span></span>
<span data-ttu-id="cbb2b-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-148">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_devices_applepushnotificationcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cbb2b-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cbb2b-149">Example</span></span>
### <a name="request"></a><span data-ttu-id="cbb2b-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cbb2b-150">Request</span></span>
<span data-ttu-id="cbb2b-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-151">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="cbb2b-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbb2b-152">Response</span></span>
<span data-ttu-id="cbb2b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cbb2b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




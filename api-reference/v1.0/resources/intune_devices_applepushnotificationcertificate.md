# <a name="applepushnotificationcertificate-resource-type"></a><span data-ttu-id="df42e-101">Tipo de recurso applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="df42e-101">applePushNotificationCertificate resource type</span></span>

> <span data-ttu-id="df42e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="df42e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="df42e-103">Certificado de notificación de inserción de Apple.</span><span class="sxs-lookup"><span data-stu-id="df42e-103">Apple push notification certificate.</span></span>
## <a name="methods"></a><span data-ttu-id="df42e-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="df42e-104">Methods</span></span>
|<span data-ttu-id="df42e-105">Método</span><span class="sxs-lookup"><span data-stu-id="df42e-105">Method</span></span>|<span data-ttu-id="df42e-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df42e-106">Return Type</span></span>|<span data-ttu-id="df42e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="df42e-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="df42e-108">Obtener applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="df42e-108">Get applePushNotificationCertificate</span></span>](../api/intune_devices_applepushnotificationcertificate_get.md)|[<span data-ttu-id="df42e-109">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="df42e-109">applePushNotificationCertificate</span></span>](../resources/intune_devices_applepushnotificationcertificate.md)|<span data-ttu-id="df42e-110">Lea las propiedades y las relaciones del objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="df42e-110">Read properties and relationships of [plannerPlanDetails](../resources/intune_devices_applepushnotificationcertificate.md) object.</span></span>|
|[<span data-ttu-id="df42e-111">Actualizar applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="df42e-111">Update applePushNotificationCertificate</span></span>](../api/intune_devices_applepushnotificationcertificate_update.md)|[<span data-ttu-id="df42e-112">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="df42e-112">applePushNotificationCertificate</span></span>](../resources/intune_devices_applepushnotificationcertificate.md)|<span data-ttu-id="df42e-113">Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="df42e-113">Update the properties of a [calendar](../resources/intune_devices_applepushnotificationcertificate.md) object.</span></span>|
|[<span data-ttu-id="df42e-114">Función downloadApplePushNotificationCertificateSigningRequest</span><span class="sxs-lookup"><span data-stu-id="df42e-114">downloadApplePushNotificationCertificateSigningRequest function</span></span>](../api/intune_devices_applepushnotificationcertificate_downloadapplepushnotificationcertificatesigningrequest.md)|<span data-ttu-id="df42e-115">cadena</span><span class="sxs-lookup"><span data-stu-id="df42e-115">String</span></span>|<span data-ttu-id="df42e-116">Descargar solicitud de firma de certificado de notificación de inserción de Apple</span><span class="sxs-lookup"><span data-stu-id="df42e-116">Download Apple push notification certificate signing request</span></span>|

## <a name="properties"></a><span data-ttu-id="df42e-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df42e-117">Properties</span></span>
|<span data-ttu-id="df42e-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="df42e-118">Property</span></span>|<span data-ttu-id="df42e-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="df42e-119">Type</span></span>|<span data-ttu-id="df42e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="df42e-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="df42e-121">id</span><span class="sxs-lookup"><span data-stu-id="df42e-121">id</span></span>|<span data-ttu-id="df42e-122">cadena</span><span class="sxs-lookup"><span data-stu-id="df42e-122">String</span></span>|<span data-ttu-id="df42e-123">Identificador único del certificado</span><span class="sxs-lookup"><span data-stu-id="df42e-123">Unique Identifier for the certificate</span></span>|
|<span data-ttu-id="df42e-124">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="df42e-124">appleIdentifier</span></span>|<span data-ttu-id="df42e-125">cadena</span><span class="sxs-lookup"><span data-stu-id="df42e-125">String</span></span>|<span data-ttu-id="df42e-126">Id. de Apple de la cuenta que se usó para crear el certificado push MDM.</span><span class="sxs-lookup"><span data-stu-id="df42e-126">Apple Id of the account used to create the MDM push certificate.</span></span>|
|<span data-ttu-id="df42e-127">topicIdentifier</span><span class="sxs-lookup"><span data-stu-id="df42e-127">topicIdentifier</span></span>|<span data-ttu-id="df42e-128">cadena</span><span class="sxs-lookup"><span data-stu-id="df42e-128">String</span></span>|<span data-ttu-id="df42e-129">Id. del tema</span><span class="sxs-lookup"><span data-stu-id="df42e-129">Topic Id.</span></span>|
|<span data-ttu-id="df42e-130">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="df42e-130">lastModifiedDateTime</span></span>|<span data-ttu-id="df42e-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="df42e-131">DateTimeOffset</span></span>|<span data-ttu-id="df42e-132">Fecha y hora de la última modificación del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="df42e-132">Last modified date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="df42e-133">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="df42e-133">expirationDateTime</span></span>|<span data-ttu-id="df42e-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="df42e-134">DateTimeOffset</span></span>|<span data-ttu-id="df42e-135">Fecha y hora de la expiración del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="df42e-135">The expiration date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="df42e-136">certificado</span><span class="sxs-lookup"><span data-stu-id="df42e-136">ACS, certificate</span></span>|<span data-ttu-id="df42e-137">cadena</span><span class="sxs-lookup"><span data-stu-id="df42e-137">String</span></span>|<span data-ttu-id="df42e-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="df42e-138">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="df42e-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="df42e-139">Relationships</span></span>
<span data-ttu-id="df42e-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="df42e-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="df42e-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="df42e-141">JSON Representation</span></span>
<span data-ttu-id="df42e-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="df42e-142">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.applePushNotificationCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.applePushNotificationCertificate",
  "id": "String (identifier)",
  "appleIdentifier": "String",
  "topicIdentifier": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "expirationDateTime": "String (timestamp)",
  "certificate": "String"
}
```




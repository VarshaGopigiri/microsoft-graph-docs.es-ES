# <a name="applepushnotificationcertificate-resource-type"></a><span data-ttu-id="c8bdf-101">Tipo de recurso applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8bdf-101">applePushNotificationCertificate resource type</span></span>

> <span data-ttu-id="c8bdf-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c8bdf-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c8bdf-103">Certificado de notificación de inserción de Apple.</span><span class="sxs-lookup"><span data-stu-id="c8bdf-103">Apple push notification certificate.</span></span>
## <a name="methods"></a><span data-ttu-id="c8bdf-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8bdf-104">Methods</span></span>
|<span data-ttu-id="c8bdf-105">Método</span><span class="sxs-lookup"><span data-stu-id="c8bdf-105">Method</span></span>|<span data-ttu-id="c8bdf-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8bdf-106">Return Type</span></span>|<span data-ttu-id="c8bdf-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8bdf-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="c8bdf-108">Obtener applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8bdf-108">Get applePushNotificationCertificate</span></span>](../api/intune_devices_applepushnotificationcertificate_get.md)|[<span data-ttu-id="c8bdf-109">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8bdf-109">applePushNotificationCertificate</span></span>](../resources/intune_devices_applepushnotificationcertificate.md)|<span data-ttu-id="c8bdf-110">Lea las propiedades y las relaciones del objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="c8bdf-110">Read properties and relationships of the [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md) object.</span></span>|
|[<span data-ttu-id="c8bdf-111">Actualizar applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8bdf-111">Update applePushNotificationCertificate</span></span>](../api/intune_devices_applepushnotificationcertificate_update.md)|[<span data-ttu-id="c8bdf-112">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="c8bdf-112">applePushNotificationCertificate</span></span>](../resources/intune_devices_applepushnotificationcertificate.md)|<span data-ttu-id="c8bdf-113">Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="c8bdf-113">Update the properties of a [applePushNotificationCertificate](../resources/intune_devices_applepushnotificationcertificate.md) object.</span></span>|
|[<span data-ttu-id="c8bdf-114">Función downloadApplePushNotificationCertificateSigningRequest</span><span class="sxs-lookup"><span data-stu-id="c8bdf-114">downloadApplePushNotificationCertificateSigningRequest function</span></span>](../api/intune_devices_applepushnotificationcertificate_downloadapplepushnotificationcertificatesigningrequest.md)|<span data-ttu-id="c8bdf-115">cadena</span><span class="sxs-lookup"><span data-stu-id="c8bdf-115">String</span></span>|<span data-ttu-id="c8bdf-116">Descargar solicitud de firma de certificado de notificación de inserción de Apple</span><span class="sxs-lookup"><span data-stu-id="c8bdf-116">Download Apple push notification certificate signing request</span></span>|

## <a name="properties"></a><span data-ttu-id="c8bdf-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8bdf-117">Properties</span></span>
|<span data-ttu-id="c8bdf-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8bdf-118">Property</span></span>|<span data-ttu-id="c8bdf-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8bdf-119">Type</span></span>|<span data-ttu-id="c8bdf-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8bdf-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c8bdf-121">id</span><span class="sxs-lookup"><span data-stu-id="c8bdf-121">id</span></span>|<span data-ttu-id="c8bdf-122">String</span><span class="sxs-lookup"><span data-stu-id="c8bdf-122">String</span></span>|<span data-ttu-id="c8bdf-123">Identificador único del certificado</span><span class="sxs-lookup"><span data-stu-id="c8bdf-123">Unique Identifier for the certificate</span></span>|
|<span data-ttu-id="c8bdf-124">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="c8bdf-124">appleIdentifier</span></span>|<span data-ttu-id="c8bdf-125">String</span><span class="sxs-lookup"><span data-stu-id="c8bdf-125">String</span></span>|<span data-ttu-id="c8bdf-126">Id. de Apple de la cuenta que se usó para crear el certificado push MDM.</span><span class="sxs-lookup"><span data-stu-id="c8bdf-126">Apple Id of the account used to create the MDM push certificate.</span></span>|
|<span data-ttu-id="c8bdf-127">topicIdentifier</span><span class="sxs-lookup"><span data-stu-id="c8bdf-127">topicIdentifier</span></span>|<span data-ttu-id="c8bdf-128">String</span><span class="sxs-lookup"><span data-stu-id="c8bdf-128">String</span></span>|<span data-ttu-id="c8bdf-129">Id. del tema</span><span class="sxs-lookup"><span data-stu-id="c8bdf-129">Topic Id.</span></span>|
|<span data-ttu-id="c8bdf-130">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c8bdf-130">lastModifiedDateTime</span></span>|<span data-ttu-id="c8bdf-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8bdf-131">DateTimeOffset</span></span>|<span data-ttu-id="c8bdf-132">Fecha y hora de la última modificación del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="c8bdf-132">Last modified date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="c8bdf-133">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="c8bdf-133">expirationDateTime</span></span>|<span data-ttu-id="c8bdf-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8bdf-134">DateTimeOffset</span></span>|<span data-ttu-id="c8bdf-135">Fecha y hora de la expiración del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="c8bdf-135">The expiration date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="c8bdf-136">certificado</span><span class="sxs-lookup"><span data-stu-id="c8bdf-136">certificate</span></span>|<span data-ttu-id="c8bdf-137">String</span><span class="sxs-lookup"><span data-stu-id="c8bdf-137">String</span></span>|<span data-ttu-id="c8bdf-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c8bdf-138">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="c8bdf-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c8bdf-139">Relationships</span></span>
<span data-ttu-id="c8bdf-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c8bdf-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c8bdf-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c8bdf-141">JSON Representation</span></span>
<span data-ttu-id="c8bdf-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c8bdf-142">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.applePushNotificationCertificate"
}-->
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









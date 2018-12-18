---
title: Tipo de recurso applePushNotificationCertificate
description: Certificado de notificación de inserción de Apple.
author: tfitzmac
ms.openlocfilehash: b5be59f1a6318e07fff981fd32ec6461cb530798
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305442"
---
# <a name="applepushnotificationcertificate-resource-type"></a><span data-ttu-id="baf0c-103">Tipo de recurso applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="baf0c-103">applePushNotificationCertificate resource type</span></span>

> <span data-ttu-id="baf0c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="baf0c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="baf0c-105">Certificado de notificación de inserción de Apple.</span><span class="sxs-lookup"><span data-stu-id="baf0c-105">Apple push notification certificate.</span></span>
## <a name="methods"></a><span data-ttu-id="baf0c-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="baf0c-106">Methods</span></span>
|<span data-ttu-id="baf0c-107">Método</span><span class="sxs-lookup"><span data-stu-id="baf0c-107">Method</span></span>|<span data-ttu-id="baf0c-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="baf0c-108">Return Type</span></span>|<span data-ttu-id="baf0c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="baf0c-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="baf0c-110">Obtener applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="baf0c-110">Get applePushNotificationCertificate</span></span>](../api/intune-devices-applepushnotificationcertificate-get.md)|[<span data-ttu-id="baf0c-111">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="baf0c-111">applePushNotificationCertificate</span></span>](../resources/intune-devices-applepushnotificationcertificate.md)|<span data-ttu-id="baf0c-112">Lea las propiedades y las relaciones del objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="baf0c-112">Read properties and relationships of the [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object.</span></span>|
|[<span data-ttu-id="baf0c-113">Actualizar applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="baf0c-113">Update applePushNotificationCertificate</span></span>](../api/intune-devices-applepushnotificationcertificate-update.md)|[<span data-ttu-id="baf0c-114">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="baf0c-114">applePushNotificationCertificate</span></span>](../resources/intune-devices-applepushnotificationcertificate.md)|<span data-ttu-id="baf0c-115">Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="baf0c-115">Update the properties of a [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object.</span></span>|
|[<span data-ttu-id="baf0c-116">Función downloadApplePushNotificationCertificateSigningRequest</span><span class="sxs-lookup"><span data-stu-id="baf0c-116">downloadApplePushNotificationCertificateSigningRequest function</span></span>](../api/intune-devices-applepushnotificationcertificate-downloadapplepushnotificationcertificatesigningrequest.md)|<span data-ttu-id="baf0c-117">cadena</span><span class="sxs-lookup"><span data-stu-id="baf0c-117">String</span></span>|<span data-ttu-id="baf0c-118">Descargar solicitud de firma de certificado de notificación de inserción de Apple</span><span class="sxs-lookup"><span data-stu-id="baf0c-118">Download Apple push notification certificate signing request</span></span>|

## <a name="properties"></a><span data-ttu-id="baf0c-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="baf0c-119">Properties</span></span>
|<span data-ttu-id="baf0c-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="baf0c-120">Property</span></span>|<span data-ttu-id="baf0c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="baf0c-121">Type</span></span>|<span data-ttu-id="baf0c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="baf0c-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="baf0c-123">id</span><span class="sxs-lookup"><span data-stu-id="baf0c-123">id</span></span>|<span data-ttu-id="baf0c-124">String</span><span class="sxs-lookup"><span data-stu-id="baf0c-124">String</span></span>|<span data-ttu-id="baf0c-125">Identificador único del certificado</span><span class="sxs-lookup"><span data-stu-id="baf0c-125">Unique Identifier for the certificate</span></span>|
|<span data-ttu-id="baf0c-126">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="baf0c-126">appleIdentifier</span></span>|<span data-ttu-id="baf0c-127">String</span><span class="sxs-lookup"><span data-stu-id="baf0c-127">String</span></span>|<span data-ttu-id="baf0c-128">Id. de Apple de la cuenta que se usó para crear el certificado push MDM.</span><span class="sxs-lookup"><span data-stu-id="baf0c-128">Apple Id of the account used to create the MDM push certificate.</span></span>|
|<span data-ttu-id="baf0c-129">topicIdentifier</span><span class="sxs-lookup"><span data-stu-id="baf0c-129">topicIdentifier</span></span>|<span data-ttu-id="baf0c-130">String</span><span class="sxs-lookup"><span data-stu-id="baf0c-130">String</span></span>|<span data-ttu-id="baf0c-131">Id. del tema</span><span class="sxs-lookup"><span data-stu-id="baf0c-131">Topic Id.</span></span>|
|<span data-ttu-id="baf0c-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="baf0c-132">lastModifiedDateTime</span></span>|<span data-ttu-id="baf0c-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="baf0c-133">DateTimeOffset</span></span>|<span data-ttu-id="baf0c-134">Fecha y hora de la última modificación del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="baf0c-134">Last modified date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="baf0c-135">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="baf0c-135">expirationDateTime</span></span>|<span data-ttu-id="baf0c-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="baf0c-136">DateTimeOffset</span></span>|<span data-ttu-id="baf0c-137">Fecha y hora de la expiración del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="baf0c-137">The expiration date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="baf0c-138">certificado</span><span class="sxs-lookup"><span data-stu-id="baf0c-138">certificate</span></span>|<span data-ttu-id="baf0c-139">String</span><span class="sxs-lookup"><span data-stu-id="baf0c-139">String</span></span>|<span data-ttu-id="baf0c-140">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="baf0c-140">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="baf0c-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="baf0c-141">Relationships</span></span>
<span data-ttu-id="baf0c-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="baf0c-142">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="baf0c-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="baf0c-143">JSON Representation</span></span>
<span data-ttu-id="baf0c-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="baf0c-144">Here is a JSON representation of the resource.</span></span>
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




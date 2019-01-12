---
title: Tipo de recurso applePushNotificationCertificate
description: Certificado de notificación de inserción de Apple.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8f07561029d35d945eca118f095496891c73a25a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941740"
---
# <a name="applepushnotificationcertificate-resource-type"></a><span data-ttu-id="74498-103">Tipo de recurso applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="74498-103">applePushNotificationCertificate resource type</span></span>

> <span data-ttu-id="74498-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74498-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74498-105">Certificado de notificación de inserción de Apple.</span><span class="sxs-lookup"><span data-stu-id="74498-105">Apple push notification certificate.</span></span>
## <a name="methods"></a><span data-ttu-id="74498-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="74498-106">Methods</span></span>
|<span data-ttu-id="74498-107">Método</span><span class="sxs-lookup"><span data-stu-id="74498-107">Method</span></span>|<span data-ttu-id="74498-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74498-108">Return Type</span></span>|<span data-ttu-id="74498-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="74498-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="74498-110">Obtener applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="74498-110">Get applePushNotificationCertificate</span></span>](../api/intune-devices-applepushnotificationcertificate-get.md)|[<span data-ttu-id="74498-111">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="74498-111">applePushNotificationCertificate</span></span>](../resources/intune-devices-applepushnotificationcertificate.md)|<span data-ttu-id="74498-112">Lea las propiedades y las relaciones del objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="74498-112">Read properties and relationships of the [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object.</span></span>|
|[<span data-ttu-id="74498-113">Actualizar applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="74498-113">Update applePushNotificationCertificate</span></span>](../api/intune-devices-applepushnotificationcertificate-update.md)|[<span data-ttu-id="74498-114">applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="74498-114">applePushNotificationCertificate</span></span>](../resources/intune-devices-applepushnotificationcertificate.md)|<span data-ttu-id="74498-115">Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="74498-115">Update the properties of a [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object.</span></span>|
|[<span data-ttu-id="74498-116">Función downloadApplePushNotificationCertificateSigningRequest</span><span class="sxs-lookup"><span data-stu-id="74498-116">downloadApplePushNotificationCertificateSigningRequest function</span></span>](../api/intune-devices-applepushnotificationcertificate-downloadapplepushnotificationcertificatesigningrequest.md)|<span data-ttu-id="74498-117">cadena</span><span class="sxs-lookup"><span data-stu-id="74498-117">String</span></span>|<span data-ttu-id="74498-118">Descargar solicitud de firma de certificado de notificación de inserción de Apple</span><span class="sxs-lookup"><span data-stu-id="74498-118">Download Apple push notification certificate signing request</span></span>|

## <a name="properties"></a><span data-ttu-id="74498-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="74498-119">Properties</span></span>
|<span data-ttu-id="74498-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="74498-120">Property</span></span>|<span data-ttu-id="74498-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="74498-121">Type</span></span>|<span data-ttu-id="74498-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="74498-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="74498-123">id</span><span class="sxs-lookup"><span data-stu-id="74498-123">id</span></span>|<span data-ttu-id="74498-124">String</span><span class="sxs-lookup"><span data-stu-id="74498-124">String</span></span>|<span data-ttu-id="74498-125">Identificador único del certificado</span><span class="sxs-lookup"><span data-stu-id="74498-125">Unique Identifier for the certificate</span></span>|
|<span data-ttu-id="74498-126">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="74498-126">appleIdentifier</span></span>|<span data-ttu-id="74498-127">String</span><span class="sxs-lookup"><span data-stu-id="74498-127">String</span></span>|<span data-ttu-id="74498-128">Id. de Apple de la cuenta que se usó para crear el certificado push MDM.</span><span class="sxs-lookup"><span data-stu-id="74498-128">Apple Id of the account used to create the MDM push certificate.</span></span>|
|<span data-ttu-id="74498-129">topicIdentifier</span><span class="sxs-lookup"><span data-stu-id="74498-129">topicIdentifier</span></span>|<span data-ttu-id="74498-130">String</span><span class="sxs-lookup"><span data-stu-id="74498-130">String</span></span>|<span data-ttu-id="74498-131">Id. del tema</span><span class="sxs-lookup"><span data-stu-id="74498-131">Topic Id.</span></span>|
|<span data-ttu-id="74498-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="74498-132">lastModifiedDateTime</span></span>|<span data-ttu-id="74498-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="74498-133">DateTimeOffset</span></span>|<span data-ttu-id="74498-134">Fecha y hora de la última modificación del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="74498-134">Last modified date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="74498-135">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="74498-135">expirationDateTime</span></span>|<span data-ttu-id="74498-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="74498-136">DateTimeOffset</span></span>|<span data-ttu-id="74498-137">Fecha y hora de la expiración del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="74498-137">The expiration date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="74498-138">certificado</span><span class="sxs-lookup"><span data-stu-id="74498-138">certificate</span></span>|<span data-ttu-id="74498-139">String</span><span class="sxs-lookup"><span data-stu-id="74498-139">String</span></span>|<span data-ttu-id="74498-140">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="74498-140">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="74498-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="74498-141">Relationships</span></span>
<span data-ttu-id="74498-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="74498-142">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="74498-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="74498-143">JSON Representation</span></span>
<span data-ttu-id="74498-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="74498-144">Here is a JSON representation of the resource.</span></span>
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




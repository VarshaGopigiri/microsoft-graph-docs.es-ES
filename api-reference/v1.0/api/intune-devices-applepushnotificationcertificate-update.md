---
title: Actualizar applePushNotificationCertificate
description: Actualice las propiedades de un objeto applePushNotificationCertificate.
ms.openlocfilehash: 640fae8367813682f890ee41e11614c44d933412
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030874"
---
# <a name="update-applepushnotificationcertificate"></a><span data-ttu-id="cf938-103">Actualizar applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="cf938-103">Update applePushNotificationCertificate</span></span>

> <span data-ttu-id="cf938-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf938-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf938-105">Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="cf938-105">Update the properties of a [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cf938-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cf938-106">Prerequisites</span></span>
<span data-ttu-id="cf938-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cf938-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cf938-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf938-109">Permission type</span></span>|<span data-ttu-id="cf938-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf938-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cf938-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf938-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cf938-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf938-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="cf938-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf938-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cf938-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf938-114">Not supported.</span></span>|
|<span data-ttu-id="cf938-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf938-115">Application</span></span>|<span data-ttu-id="cf938-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf938-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cf938-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf938-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/applePushNotificationCertificate
```

## <a name="request-headers"></a><span data-ttu-id="cf938-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf938-118">Request headers</span></span>
|<span data-ttu-id="cf938-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf938-119">Header</span></span>|<span data-ttu-id="cf938-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cf938-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cf938-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="cf938-121">Authorization</span></span>|<span data-ttu-id="cf938-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cf938-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cf938-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cf938-123">Accept</span></span>|<span data-ttu-id="cf938-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cf938-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cf938-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf938-125">Request body</span></span>
<span data-ttu-id="cf938-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="cf938-126">In the request body, supply a JSON representation for the [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object.</span></span>

<span data-ttu-id="cf938-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="cf938-127">The following table shows the properties that are required when you create the [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span></span>

|<span data-ttu-id="cf938-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf938-128">Property</span></span>|<span data-ttu-id="cf938-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf938-129">Type</span></span>|<span data-ttu-id="cf938-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf938-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf938-131">id</span><span class="sxs-lookup"><span data-stu-id="cf938-131">id</span></span>|<span data-ttu-id="cf938-132">String</span><span class="sxs-lookup"><span data-stu-id="cf938-132">String</span></span>|<span data-ttu-id="cf938-133">Identificador único del certificado</span><span class="sxs-lookup"><span data-stu-id="cf938-133">Unique Identifier for the certificate</span></span>|
|<span data-ttu-id="cf938-134">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="cf938-134">appleIdentifier</span></span>|<span data-ttu-id="cf938-135">String</span><span class="sxs-lookup"><span data-stu-id="cf938-135">String</span></span>|<span data-ttu-id="cf938-136">Id. de Apple de la cuenta que se usó para crear el certificado push MDM.</span><span class="sxs-lookup"><span data-stu-id="cf938-136">Apple Id of the account used to create the MDM push certificate.</span></span>|
|<span data-ttu-id="cf938-137">topicIdentifier</span><span class="sxs-lookup"><span data-stu-id="cf938-137">topicIdentifier</span></span>|<span data-ttu-id="cf938-138">String</span><span class="sxs-lookup"><span data-stu-id="cf938-138">String</span></span>|<span data-ttu-id="cf938-139">Id. del tema</span><span class="sxs-lookup"><span data-stu-id="cf938-139">Topic Id.</span></span>|
|<span data-ttu-id="cf938-140">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cf938-140">lastModifiedDateTime</span></span>|<span data-ttu-id="cf938-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf938-141">DateTimeOffset</span></span>|<span data-ttu-id="cf938-142">Fecha y hora de la última modificación del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="cf938-142">Last modified date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="cf938-143">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="cf938-143">expirationDateTime</span></span>|<span data-ttu-id="cf938-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf938-144">DateTimeOffset</span></span>|<span data-ttu-id="cf938-145">Fecha y hora de la expiración del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="cf938-145">The expiration date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="cf938-146">certificado</span><span class="sxs-lookup"><span data-stu-id="cf938-146">certificate</span></span>|<span data-ttu-id="cf938-147">String</span><span class="sxs-lookup"><span data-stu-id="cf938-147">String</span></span>|<span data-ttu-id="cf938-148">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf938-148">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="cf938-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf938-149">Response</span></span>
<span data-ttu-id="cf938-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf938-150">If successful, this method returns a `200 OK` response code and an updated [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf938-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf938-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="cf938-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf938-152">Request</span></span>
<span data-ttu-id="cf938-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf938-153">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/applePushNotificationCertificate
Content-type: application/json
Content-length: 271

{
  "@odata.type": "#microsoft.graph.applePushNotificationCertificate",
  "appleIdentifier": "Apple Identifier value",
  "topicIdentifier": "Topic Identifier value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "certificate": "Certificate value"
}
```

### <a name="response"></a><span data-ttu-id="cf938-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf938-154">Response</span></span>
<span data-ttu-id="cf938-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf938-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




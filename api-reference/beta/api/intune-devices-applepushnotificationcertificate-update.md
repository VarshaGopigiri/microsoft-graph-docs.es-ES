---
title: Actualizar applePushNotificationCertificate
description: Actualice las propiedades de un objeto applePushNotificationCertificate.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b6cc1b113b964dbc2f2ffdaae1e52639ec2463f7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964840"
---
# <a name="update-applepushnotificationcertificate"></a><span data-ttu-id="9622c-103">Actualizar applePushNotificationCertificate</span><span class="sxs-lookup"><span data-stu-id="9622c-103">Update applePushNotificationCertificate</span></span>

> <span data-ttu-id="9622c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9622c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9622c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9622c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9622c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9622c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9622c-107">Actualice las propiedades de un objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="9622c-107">Update the properties of a [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9622c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9622c-108">Prerequisites</span></span>
<span data-ttu-id="9622c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9622c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9622c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9622c-111">Permission type</span></span>|<span data-ttu-id="9622c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9622c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9622c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9622c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9622c-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9622c-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="9622c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9622c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9622c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9622c-116">Not supported.</span></span>|
|<span data-ttu-id="9622c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9622c-117">Application</span></span>|<span data-ttu-id="9622c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9622c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9622c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9622c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/applePushNotificationCertificate
```

## <a name="request-headers"></a><span data-ttu-id="9622c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9622c-120">Request headers</span></span>
|<span data-ttu-id="9622c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9622c-121">Header</span></span>|<span data-ttu-id="9622c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9622c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9622c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9622c-123">Authorization</span></span>|<span data-ttu-id="9622c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9622c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9622c-125">Accept</span><span class="sxs-lookup"><span data-stu-id="9622c-125">Accept</span></span>|<span data-ttu-id="9622c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9622c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9622c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9622c-127">Request body</span></span>
<span data-ttu-id="9622c-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="9622c-128">In the request body, supply a JSON representation for the [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object.</span></span>

<span data-ttu-id="9622c-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="9622c-129">The following table shows the properties that are required when you create the [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md).</span></span>

|<span data-ttu-id="9622c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9622c-130">Property</span></span>|<span data-ttu-id="9622c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9622c-131">Type</span></span>|<span data-ttu-id="9622c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9622c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9622c-133">id</span><span class="sxs-lookup"><span data-stu-id="9622c-133">id</span></span>|<span data-ttu-id="9622c-134">String</span><span class="sxs-lookup"><span data-stu-id="9622c-134">String</span></span>|<span data-ttu-id="9622c-135">Identificador único del certificado</span><span class="sxs-lookup"><span data-stu-id="9622c-135">Unique Identifier for the certificate</span></span>|
|<span data-ttu-id="9622c-136">appleIdentifier</span><span class="sxs-lookup"><span data-stu-id="9622c-136">appleIdentifier</span></span>|<span data-ttu-id="9622c-137">String</span><span class="sxs-lookup"><span data-stu-id="9622c-137">String</span></span>|<span data-ttu-id="9622c-138">Id. de Apple de la cuenta que se usó para crear el certificado push MDM.</span><span class="sxs-lookup"><span data-stu-id="9622c-138">Apple Id of the account used to create the MDM push certificate.</span></span>|
|<span data-ttu-id="9622c-139">topicIdentifier</span><span class="sxs-lookup"><span data-stu-id="9622c-139">topicIdentifier</span></span>|<span data-ttu-id="9622c-140">String</span><span class="sxs-lookup"><span data-stu-id="9622c-140">String</span></span>|<span data-ttu-id="9622c-141">Id. del tema</span><span class="sxs-lookup"><span data-stu-id="9622c-141">Topic Id.</span></span>|
|<span data-ttu-id="9622c-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9622c-142">lastModifiedDateTime</span></span>|<span data-ttu-id="9622c-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9622c-143">DateTimeOffset</span></span>|<span data-ttu-id="9622c-144">Fecha y hora de la última modificación del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="9622c-144">Last modified date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="9622c-145">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="9622c-145">expirationDateTime</span></span>|<span data-ttu-id="9622c-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9622c-146">DateTimeOffset</span></span>|<span data-ttu-id="9622c-147">Fecha y hora de la expiración del certificado de notificación push de Apple.</span><span class="sxs-lookup"><span data-stu-id="9622c-147">The expiration date and time for Apple push notification certificate.</span></span>|
|<span data-ttu-id="9622c-148">certificateUploadStatus</span><span class="sxs-lookup"><span data-stu-id="9622c-148">certificateUploadStatus</span></span>|<span data-ttu-id="9622c-149">String</span><span class="sxs-lookup"><span data-stu-id="9622c-149">String</span></span>|<span data-ttu-id="9622c-150">El estado de carga del certificado.</span><span class="sxs-lookup"><span data-stu-id="9622c-150">The certificate upload status.</span></span>|
|<span data-ttu-id="9622c-151">certificateUploadFailureReason</span><span class="sxs-lookup"><span data-stu-id="9622c-151">certificateUploadFailureReason</span></span>|<span data-ttu-id="9622c-152">String</span><span class="sxs-lookup"><span data-stu-id="9622c-152">String</span></span>|<span data-ttu-id="9622c-153">No se pudo la razón por la carga de certificado.</span><span class="sxs-lookup"><span data-stu-id="9622c-153">The reason the certificate upload failed.</span></span>|
|<span data-ttu-id="9622c-154">certificado</span><span class="sxs-lookup"><span data-stu-id="9622c-154">certificate</span></span>|<span data-ttu-id="9622c-155">String</span><span class="sxs-lookup"><span data-stu-id="9622c-155">String</span></span>|<span data-ttu-id="9622c-156">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9622c-156">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="9622c-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9622c-157">Response</span></span>
<span data-ttu-id="9622c-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9622c-158">If successful, this method returns a `200 OK` response code and an updated [applePushNotificationCertificate](../resources/intune-devices-applepushnotificationcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9622c-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9622c-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="9622c-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9622c-160">Request</span></span>
<span data-ttu-id="9622c-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9622c-161">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/applePushNotificationCertificate
Content-type: application/json
Content-length: 409

{
  "appleIdentifier": "Apple Identifier value",
  "topicIdentifier": "Topic Identifier value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "certificateUploadStatus": "Certificate Upload Status value",
  "certificateUploadFailureReason": "Certificate Upload Failure Reason value",
  "certificate": "Certificate value"
}
```

### <a name="response"></a><span data-ttu-id="9622c-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9622c-162">Response</span></span>
<span data-ttu-id="9622c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9622c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 529

{
  "@odata.type": "#microsoft.graph.applePushNotificationCertificate",
  "id": "c4c8f047-f047-c4c8-47f0-c8c447f0c8c4",
  "appleIdentifier": "Apple Identifier value",
  "topicIdentifier": "Topic Identifier value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "certificateUploadStatus": "Certificate Upload Status value",
  "certificateUploadFailureReason": "Certificate Upload Failure Reason value",
  "certificate": "Certificate value"
}
```






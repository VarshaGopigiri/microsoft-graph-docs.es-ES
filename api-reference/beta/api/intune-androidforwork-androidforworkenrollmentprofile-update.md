---
title: Actualizar androidForWorkEnrollmentProfile
description: Actualice las propiedades de un objeto androidForWorkEnrollmentProfile.
ms.openlocfilehash: f0af5db7115de09657d08d093836527e3198cad0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089103"
---
# <a name="update-androidforworkenrollmentprofile"></a><span data-ttu-id="16296-103">Actualizar androidForWorkEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="16296-103">Update androidForWorkEnrollmentProfile</span></span>

> <span data-ttu-id="16296-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16296-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16296-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16296-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="16296-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16296-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16296-107">Actualice las propiedades de un objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="16296-107">Update the properties of a [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="16296-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="16296-108">Prerequisites</span></span>
<span data-ttu-id="16296-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="16296-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="16296-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16296-111">Permission type</span></span>|<span data-ttu-id="16296-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="16296-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="16296-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16296-113">Delegated (work or school account)</span></span>|<span data-ttu-id="16296-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="16296-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="16296-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16296-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="16296-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16296-116">Not supported.</span></span>|
|<span data-ttu-id="16296-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16296-117">Application</span></span>|<span data-ttu-id="16296-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16296-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="16296-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16296-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/androidForWorkEnrollmentProfiles/{androidForWorkEnrollmentProfileId}
```

## <a name="request-headers"></a><span data-ttu-id="16296-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16296-120">Request headers</span></span>
|<span data-ttu-id="16296-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16296-121">Header</span></span>|<span data-ttu-id="16296-122">Valor</span><span class="sxs-lookup"><span data-stu-id="16296-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="16296-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="16296-123">Authorization</span></span>|<span data-ttu-id="16296-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="16296-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="16296-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="16296-125">Accept</span></span>|<span data-ttu-id="16296-126">application/json</span><span class="sxs-lookup"><span data-stu-id="16296-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="16296-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16296-127">Request body</span></span>
<span data-ttu-id="16296-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="16296-128">In the request body, supply a JSON representation for the [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) object.</span></span>

<span data-ttu-id="16296-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="16296-129">The following table shows the properties that are required when you create the [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).</span></span>

|<span data-ttu-id="16296-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16296-130">Property</span></span>|<span data-ttu-id="16296-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="16296-131">Type</span></span>|<span data-ttu-id="16296-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="16296-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16296-133">accountId</span><span class="sxs-lookup"><span data-stu-id="16296-133">accountId</span></span>|<span data-ttu-id="16296-134">String</span><span class="sxs-lookup"><span data-stu-id="16296-134">String</span></span>|<span data-ttu-id="16296-135">GUID del espacio empresarial al que pertenece el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="16296-135">Tenant GUID the enrollment profile belongs to.</span></span>|
|<span data-ttu-id="16296-136">id</span><span class="sxs-lookup"><span data-stu-id="16296-136">id</span></span>|<span data-ttu-id="16296-137">String</span><span class="sxs-lookup"><span data-stu-id="16296-137">String</span></span>|<span data-ttu-id="16296-138">GUID único del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="16296-138">Unique GUID for the enrollment profile.</span></span>|
|<span data-ttu-id="16296-139">displayName</span><span class="sxs-lookup"><span data-stu-id="16296-139">displayName</span></span>|<span data-ttu-id="16296-140">String</span><span class="sxs-lookup"><span data-stu-id="16296-140">String</span></span>|<span data-ttu-id="16296-141">Nombre para mostrar del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="16296-141">Display name for the enrollment profile.</span></span>|
|<span data-ttu-id="16296-142">descripción</span><span class="sxs-lookup"><span data-stu-id="16296-142">description</span></span>|<span data-ttu-id="16296-143">String</span><span class="sxs-lookup"><span data-stu-id="16296-143">String</span></span>|<span data-ttu-id="16296-144">Descripción del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="16296-144">Description for the enrollment profile.</span></span>|
|<span data-ttu-id="16296-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="16296-145">createdDateTime</span></span>|<span data-ttu-id="16296-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16296-146">DateTimeOffset</span></span>|<span data-ttu-id="16296-147">Fecha y hora en que se creó el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="16296-147">Date time the enrollment profile was created.</span></span>|
|<span data-ttu-id="16296-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="16296-148">lastModifiedDateTime</span></span>|<span data-ttu-id="16296-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16296-149">DateTimeOffset</span></span>|<span data-ttu-id="16296-150">Fecha y hora en que se modificó el perfil de inscripción por última vez.</span><span class="sxs-lookup"><span data-stu-id="16296-150">Date time the enrollment profile was last modified.</span></span>|
|<span data-ttu-id="16296-151">tokenValue</span><span class="sxs-lookup"><span data-stu-id="16296-151">tokenValue</span></span>|<span data-ttu-id="16296-152">String</span><span class="sxs-lookup"><span data-stu-id="16296-152">String</span></span>|<span data-ttu-id="16296-153">Valor del token creado más recientemente para este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="16296-153">Value of the most recently created token for this enrollment profile.</span></span>|
|<span data-ttu-id="16296-154">tokenExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="16296-154">tokenExpirationDateTime</span></span>|<span data-ttu-id="16296-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16296-155">DateTimeOffset</span></span>|<span data-ttu-id="16296-156">Fecha y hora en que expirará el token creado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="16296-156">Date time the most recently created token will expire.</span></span>|
|<span data-ttu-id="16296-157">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="16296-157">enrolledDeviceCount</span></span>|<span data-ttu-id="16296-158">Int32</span><span class="sxs-lookup"><span data-stu-id="16296-158">Int32</span></span>|<span data-ttu-id="16296-159">Número total de dispositivos Android que se han inscrito con este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="16296-159">Total number of Android devices that have enrolled using this enrollment profile.</span></span>|
|<span data-ttu-id="16296-160">qrCodeContent</span><span class="sxs-lookup"><span data-stu-id="16296-160">qrCodeContent</span></span>|<span data-ttu-id="16296-161">String</span><span class="sxs-lookup"><span data-stu-id="16296-161">String</span></span>|<span data-ttu-id="16296-162">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="16296-162">String used to generate a QR code for the token.</span></span>|
|<span data-ttu-id="16296-163">qrCodeImage</span><span class="sxs-lookup"><span data-stu-id="16296-163">qrCodeImage</span></span>|[<span data-ttu-id="16296-164">mimeContent</span><span class="sxs-lookup"><span data-stu-id="16296-164">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="16296-165">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="16296-165">String used to generate a QR code for the token.</span></span>|



## <a name="response"></a><span data-ttu-id="16296-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16296-166">Response</span></span>
<span data-ttu-id="16296-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16296-167">If successful, this method returns a `200 OK` response code and an updated [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="16296-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16296-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="16296-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16296-169">Request</span></span>
<span data-ttu-id="16296-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16296-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/androidForWorkEnrollmentProfiles/{androidForWorkEnrollmentProfileId}
Content-type: application/json
Content-length: 490

{
  "accountId": "Account Id value",
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "tokenValue": "Token Value value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "enrolledDeviceCount": 3,
  "qrCodeContent": "Qr Code Content value",
  "qrCodeImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```

### <a name="response"></a><span data-ttu-id="16296-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16296-171">Response</span></span>
<span data-ttu-id="16296-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="16296-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 668

{
  "@odata.type": "#microsoft.graph.androidForWorkEnrollmentProfile",
  "accountId": "Account Id value",
  "id": "e6742553-2553-e674-5325-74e6532574e6",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "tokenValue": "Token Value value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "enrolledDeviceCount": 3,
  "qrCodeContent": "Qr Code Content value",
  "qrCodeImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```






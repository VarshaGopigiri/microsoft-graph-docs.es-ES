---
title: Crear androidDeviceOwnerEnrollmentProfile
description: Crear un nuevo objeto androidDeviceOwnerEnrollmentProfile.
ms.openlocfilehash: da59eaf01dea9208540b7116b6309af754980157
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084260"
---
# <a name="create-androiddeviceownerenrollmentprofile"></a><span data-ttu-id="4deef-103">Crear androidDeviceOwnerEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="4deef-103">Create androidDeviceOwnerEnrollmentProfile</span></span>

> <span data-ttu-id="4deef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4deef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4deef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4deef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4deef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4deef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4deef-107">Crear un nuevo objeto [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="4deef-107">Create a new [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4deef-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4deef-108">Prerequisites</span></span>
<span data-ttu-id="4deef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4deef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4deef-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4deef-111">Permission type</span></span>|<span data-ttu-id="4deef-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4deef-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4deef-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4deef-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4deef-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4deef-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4deef-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4deef-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4deef-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4deef-116">Not supported.</span></span>|
|<span data-ttu-id="4deef-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4deef-117">Application</span></span>|<span data-ttu-id="4deef-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4deef-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4deef-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4deef-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/androidDeviceOwnerEnrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="4deef-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4deef-120">Request headers</span></span>
|<span data-ttu-id="4deef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4deef-121">Header</span></span>|<span data-ttu-id="4deef-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4deef-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4deef-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4deef-123">Authorization</span></span>|<span data-ttu-id="4deef-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4deef-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4deef-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4deef-125">Accept</span></span>|<span data-ttu-id="4deef-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4deef-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4deef-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4deef-127">Request body</span></span>
<span data-ttu-id="4deef-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidDeviceOwnerEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="4deef-128">In the request body, supply a JSON representation for the androidDeviceOwnerEnrollmentProfile object.</span></span>

<span data-ttu-id="4deef-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidDeviceOwnerEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="4deef-129">The following table shows the properties that are required when you create the androidDeviceOwnerEnrollmentProfile.</span></span>

|<span data-ttu-id="4deef-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4deef-130">Property</span></span>|<span data-ttu-id="4deef-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4deef-131">Type</span></span>|<span data-ttu-id="4deef-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4deef-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4deef-133">accountId</span><span class="sxs-lookup"><span data-stu-id="4deef-133">accountId</span></span>|<span data-ttu-id="4deef-134">String</span><span class="sxs-lookup"><span data-stu-id="4deef-134">String</span></span>|<span data-ttu-id="4deef-135">GUID del espacio empresarial al que pertenece el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="4deef-135">Tenant GUID the enrollment profile belongs to.</span></span>|
|<span data-ttu-id="4deef-136">id</span><span class="sxs-lookup"><span data-stu-id="4deef-136">id</span></span>|<span data-ttu-id="4deef-137">String</span><span class="sxs-lookup"><span data-stu-id="4deef-137">String</span></span>|<span data-ttu-id="4deef-138">GUID único del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="4deef-138">Unique GUID for the enrollment profile.</span></span>|
|<span data-ttu-id="4deef-139">displayName</span><span class="sxs-lookup"><span data-stu-id="4deef-139">displayName</span></span>|<span data-ttu-id="4deef-140">String</span><span class="sxs-lookup"><span data-stu-id="4deef-140">String</span></span>|<span data-ttu-id="4deef-141">Nombre para mostrar del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="4deef-141">Display name for the enrollment profile.</span></span>|
|<span data-ttu-id="4deef-142">descripción</span><span class="sxs-lookup"><span data-stu-id="4deef-142">description</span></span>|<span data-ttu-id="4deef-143">String</span><span class="sxs-lookup"><span data-stu-id="4deef-143">String</span></span>|<span data-ttu-id="4deef-144">Descripción del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="4deef-144">Description for the enrollment profile.</span></span>|
|<span data-ttu-id="4deef-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4deef-145">createdDateTime</span></span>|<span data-ttu-id="4deef-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4deef-146">DateTimeOffset</span></span>|<span data-ttu-id="4deef-147">Fecha y hora en que se creó el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="4deef-147">Date time the enrollment profile was created.</span></span>|
|<span data-ttu-id="4deef-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4deef-148">lastModifiedDateTime</span></span>|<span data-ttu-id="4deef-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4deef-149">DateTimeOffset</span></span>|<span data-ttu-id="4deef-150">Fecha y hora en que se modificó el perfil de inscripción por última vez.</span><span class="sxs-lookup"><span data-stu-id="4deef-150">Date time the enrollment profile was last modified.</span></span>|
|<span data-ttu-id="4deef-151">tokenValue</span><span class="sxs-lookup"><span data-stu-id="4deef-151">tokenValue</span></span>|<span data-ttu-id="4deef-152">String</span><span class="sxs-lookup"><span data-stu-id="4deef-152">String</span></span>|<span data-ttu-id="4deef-153">Valor del token creado más recientemente para este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="4deef-153">Value of the most recently created token for this enrollment profile.</span></span>|
|<span data-ttu-id="4deef-154">tokenCreationDateTime</span><span class="sxs-lookup"><span data-stu-id="4deef-154">tokenCreationDateTime</span></span>|<span data-ttu-id="4deef-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4deef-155">DateTimeOffset</span></span>|<span data-ttu-id="4deef-156">Fecha hora en que se creó el token creado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="4deef-156">Date time the most recently created token was created.</span></span>|
|<span data-ttu-id="4deef-157">tokenExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="4deef-157">tokenExpirationDateTime</span></span>|<span data-ttu-id="4deef-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4deef-158">DateTimeOffset</span></span>|<span data-ttu-id="4deef-159">Fecha y hora en que expirará el token creado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="4deef-159">Date time the most recently created token will expire.</span></span>|
|<span data-ttu-id="4deef-160">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4deef-160">enrolledDeviceCount</span></span>|<span data-ttu-id="4deef-161">Int32</span><span class="sxs-lookup"><span data-stu-id="4deef-161">Int32</span></span>|<span data-ttu-id="4deef-162">Número total de dispositivos Android que se han inscrito con este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="4deef-162">Total number of Android devices that have enrolled using this enrollment profile.</span></span>|
|<span data-ttu-id="4deef-163">qrCodeContent</span><span class="sxs-lookup"><span data-stu-id="4deef-163">qrCodeContent</span></span>|<span data-ttu-id="4deef-164">String</span><span class="sxs-lookup"><span data-stu-id="4deef-164">String</span></span>|<span data-ttu-id="4deef-165">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="4deef-165">String used to generate a QR code for the token.</span></span>|
|<span data-ttu-id="4deef-166">qrCodeImage</span><span class="sxs-lookup"><span data-stu-id="4deef-166">qrCodeImage</span></span>|[<span data-ttu-id="4deef-167">mimeContent</span><span class="sxs-lookup"><span data-stu-id="4deef-167">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="4deef-168">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="4deef-168">String used to generate a QR code for the token.</span></span>|



## <a name="response"></a><span data-ttu-id="4deef-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4deef-169">Response</span></span>
<span data-ttu-id="4deef-170">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4deef-170">If successful, this method returns a `201 Created` response code and a [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4deef-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4deef-171">Example</span></span>
### <a name="request"></a><span data-ttu-id="4deef-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4deef-172">Request</span></span>
<span data-ttu-id="4deef-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4deef-173">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/androidDeviceOwnerEnrollmentProfiles
Content-type: application/json
Content-length: 629

{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerEnrollmentProfile",
  "accountId": "Account Id value",
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "tokenValue": "Token Value value",
  "tokenCreationDateTime": "2017-01-01T00:01:38.5314127-08:00",
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

### <a name="response"></a><span data-ttu-id="4deef-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4deef-174">Response</span></span>
<span data-ttu-id="4deef-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4deef-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 737

{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerEnrollmentProfile",
  "accountId": "Account Id value",
  "id": "a8d0245e-245e-a8d0-5e24-d0a85e24d0a8",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "tokenValue": "Token Value value",
  "tokenCreationDateTime": "2017-01-01T00:01:38.5314127-08:00",
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






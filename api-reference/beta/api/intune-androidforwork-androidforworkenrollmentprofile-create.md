---
title: Crear androidForWorkEnrollmentProfile
description: Cree un objeto androidForWorkEnrollmentProfile.
author: tfitzmac
ms.openlocfilehash: 794179968afc4f39c809373b3425c076f7a591a3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27355981"
---
# <a name="create-androidforworkenrollmentprofile"></a><span data-ttu-id="83f21-103">Crear androidForWorkEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="83f21-103">Create androidForWorkEnrollmentProfile</span></span>

> <span data-ttu-id="83f21-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="83f21-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="83f21-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="83f21-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="83f21-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="83f21-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="83f21-107">Cree un objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="83f21-107">Create a new [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="83f21-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="83f21-108">Prerequisites</span></span>
<span data-ttu-id="83f21-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="83f21-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="83f21-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="83f21-111">Permission type</span></span>|<span data-ttu-id="83f21-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="83f21-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="83f21-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="83f21-113">Delegated (work or school account)</span></span>|<span data-ttu-id="83f21-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="83f21-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="83f21-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="83f21-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="83f21-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="83f21-116">Not supported.</span></span>|
|<span data-ttu-id="83f21-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="83f21-117">Application</span></span>|<span data-ttu-id="83f21-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="83f21-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="83f21-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="83f21-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/androidForWorkEnrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="83f21-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="83f21-120">Request headers</span></span>
|<span data-ttu-id="83f21-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83f21-121">Header</span></span>|<span data-ttu-id="83f21-122">Valor</span><span class="sxs-lookup"><span data-stu-id="83f21-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="83f21-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="83f21-123">Authorization</span></span>|<span data-ttu-id="83f21-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="83f21-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="83f21-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="83f21-125">Accept</span></span>|<span data-ttu-id="83f21-126">application/json</span><span class="sxs-lookup"><span data-stu-id="83f21-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="83f21-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="83f21-127">Request body</span></span>
<span data-ttu-id="83f21-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidForWorkEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="83f21-128">In the request body, supply a JSON representation for the androidForWorkEnrollmentProfile object.</span></span>

<span data-ttu-id="83f21-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidForWorkEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="83f21-129">The following table shows the properties that are required when you create the androidForWorkEnrollmentProfile.</span></span>

|<span data-ttu-id="83f21-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="83f21-130">Property</span></span>|<span data-ttu-id="83f21-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="83f21-131">Type</span></span>|<span data-ttu-id="83f21-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="83f21-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="83f21-133">accountId</span><span class="sxs-lookup"><span data-stu-id="83f21-133">accountId</span></span>|<span data-ttu-id="83f21-134">String</span><span class="sxs-lookup"><span data-stu-id="83f21-134">String</span></span>|<span data-ttu-id="83f21-135">GUID del espacio empresarial al que pertenece el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="83f21-135">Tenant GUID the enrollment profile belongs to.</span></span>|
|<span data-ttu-id="83f21-136">id</span><span class="sxs-lookup"><span data-stu-id="83f21-136">id</span></span>|<span data-ttu-id="83f21-137">String</span><span class="sxs-lookup"><span data-stu-id="83f21-137">String</span></span>|<span data-ttu-id="83f21-138">GUID único del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="83f21-138">Unique GUID for the enrollment profile.</span></span>|
|<span data-ttu-id="83f21-139">displayName</span><span class="sxs-lookup"><span data-stu-id="83f21-139">displayName</span></span>|<span data-ttu-id="83f21-140">String</span><span class="sxs-lookup"><span data-stu-id="83f21-140">String</span></span>|<span data-ttu-id="83f21-141">Nombre para mostrar del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="83f21-141">Display name for the enrollment profile.</span></span>|
|<span data-ttu-id="83f21-142">descripción</span><span class="sxs-lookup"><span data-stu-id="83f21-142">description</span></span>|<span data-ttu-id="83f21-143">String</span><span class="sxs-lookup"><span data-stu-id="83f21-143">String</span></span>|<span data-ttu-id="83f21-144">Descripción del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="83f21-144">Description for the enrollment profile.</span></span>|
|<span data-ttu-id="83f21-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="83f21-145">createdDateTime</span></span>|<span data-ttu-id="83f21-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="83f21-146">DateTimeOffset</span></span>|<span data-ttu-id="83f21-147">Fecha y hora en que se creó el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="83f21-147">Date time the enrollment profile was created.</span></span>|
|<span data-ttu-id="83f21-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="83f21-148">lastModifiedDateTime</span></span>|<span data-ttu-id="83f21-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="83f21-149">DateTimeOffset</span></span>|<span data-ttu-id="83f21-150">Fecha y hora en que se modificó el perfil de inscripción por última vez.</span><span class="sxs-lookup"><span data-stu-id="83f21-150">Date time the enrollment profile was last modified.</span></span>|
|<span data-ttu-id="83f21-151">tokenValue</span><span class="sxs-lookup"><span data-stu-id="83f21-151">tokenValue</span></span>|<span data-ttu-id="83f21-152">String</span><span class="sxs-lookup"><span data-stu-id="83f21-152">String</span></span>|<span data-ttu-id="83f21-153">Valor del token creado más recientemente para este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="83f21-153">Value of the most recently created token for this enrollment profile.</span></span>|
|<span data-ttu-id="83f21-154">tokenExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="83f21-154">tokenExpirationDateTime</span></span>|<span data-ttu-id="83f21-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="83f21-155">DateTimeOffset</span></span>|<span data-ttu-id="83f21-156">Fecha y hora en que expirará el token creado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="83f21-156">Date time the most recently created token will expire.</span></span>|
|<span data-ttu-id="83f21-157">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="83f21-157">enrolledDeviceCount</span></span>|<span data-ttu-id="83f21-158">Int32</span><span class="sxs-lookup"><span data-stu-id="83f21-158">Int32</span></span>|<span data-ttu-id="83f21-159">Número total de dispositivos Android que se han inscrito con este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="83f21-159">Total number of Android devices that have enrolled using this enrollment profile.</span></span>|
|<span data-ttu-id="83f21-160">qrCodeContent</span><span class="sxs-lookup"><span data-stu-id="83f21-160">qrCodeContent</span></span>|<span data-ttu-id="83f21-161">String</span><span class="sxs-lookup"><span data-stu-id="83f21-161">String</span></span>|<span data-ttu-id="83f21-162">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="83f21-162">String used to generate a QR code for the token.</span></span>|
|<span data-ttu-id="83f21-163">qrCodeImage</span><span class="sxs-lookup"><span data-stu-id="83f21-163">qrCodeImage</span></span>|[<span data-ttu-id="83f21-164">mimeContent</span><span class="sxs-lookup"><span data-stu-id="83f21-164">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="83f21-165">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="83f21-165">String used to generate a QR code for the token.</span></span>|



## <a name="response"></a><span data-ttu-id="83f21-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83f21-166">Response</span></span>
<span data-ttu-id="83f21-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="83f21-167">If successful, this method returns a `201 Created` response code and a [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="83f21-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="83f21-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="83f21-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="83f21-169">Request</span></span>
<span data-ttu-id="83f21-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="83f21-170">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/androidForWorkEnrollmentProfiles
Content-type: application/json
Content-length: 560

{
  "@odata.type": "#microsoft.graph.androidForWorkEnrollmentProfile",
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

### <a name="response"></a><span data-ttu-id="83f21-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83f21-171">Response</span></span>
<span data-ttu-id="83f21-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="83f21-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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






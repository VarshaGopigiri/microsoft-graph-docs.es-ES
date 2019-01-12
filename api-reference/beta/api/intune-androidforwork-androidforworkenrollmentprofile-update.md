---
title: Actualizar androidForWorkEnrollmentProfile
description: Actualice las propiedades de un objeto androidForWorkEnrollmentProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5c65c01996ce482d7456396fd831a9ab2aa465b4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916211"
---
# <a name="update-androidforworkenrollmentprofile"></a><span data-ttu-id="d7656-103">Actualizar androidForWorkEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="d7656-103">Update androidForWorkEnrollmentProfile</span></span>

> <span data-ttu-id="d7656-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7656-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7656-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7656-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d7656-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d7656-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d7656-107">Actualice las propiedades de un objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="d7656-107">Update the properties of a [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d7656-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d7656-108">Prerequisites</span></span>
<span data-ttu-id="d7656-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d7656-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d7656-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7656-111">Permission type</span></span>|<span data-ttu-id="d7656-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7656-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d7656-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7656-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d7656-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d7656-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d7656-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7656-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d7656-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7656-116">Not supported.</span></span>|
|<span data-ttu-id="d7656-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7656-117">Application</span></span>|<span data-ttu-id="d7656-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7656-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d7656-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7656-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/androidForWorkEnrollmentProfiles/{androidForWorkEnrollmentProfileId}
```

## <a name="request-headers"></a><span data-ttu-id="d7656-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7656-120">Request headers</span></span>
|<span data-ttu-id="d7656-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7656-121">Header</span></span>|<span data-ttu-id="d7656-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d7656-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d7656-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d7656-123">Authorization</span></span>|<span data-ttu-id="d7656-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d7656-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d7656-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d7656-125">Accept</span></span>|<span data-ttu-id="d7656-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d7656-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d7656-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7656-127">Request body</span></span>
<span data-ttu-id="d7656-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="d7656-128">In the request body, supply a JSON representation for the [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) object.</span></span>

<span data-ttu-id="d7656-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="d7656-129">The following table shows the properties that are required when you create the [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md).</span></span>

|<span data-ttu-id="d7656-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7656-130">Property</span></span>|<span data-ttu-id="d7656-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7656-131">Type</span></span>|<span data-ttu-id="d7656-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7656-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d7656-133">accountId</span><span class="sxs-lookup"><span data-stu-id="d7656-133">accountId</span></span>|<span data-ttu-id="d7656-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7656-134">String</span></span>|<span data-ttu-id="d7656-135">GUID del espacio empresarial al que pertenece el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d7656-135">Tenant GUID the enrollment profile belongs to.</span></span>|
|<span data-ttu-id="d7656-136">id</span><span class="sxs-lookup"><span data-stu-id="d7656-136">id</span></span>|<span data-ttu-id="d7656-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7656-137">String</span></span>|<span data-ttu-id="d7656-138">GUID único del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d7656-138">Unique GUID for the enrollment profile.</span></span>|
|<span data-ttu-id="d7656-139">displayName</span><span class="sxs-lookup"><span data-stu-id="d7656-139">displayName</span></span>|<span data-ttu-id="d7656-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7656-140">String</span></span>|<span data-ttu-id="d7656-141">Nombre para mostrar del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d7656-141">Display name for the enrollment profile.</span></span>|
|<span data-ttu-id="d7656-142">descripción</span><span class="sxs-lookup"><span data-stu-id="d7656-142">description</span></span>|<span data-ttu-id="d7656-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7656-143">String</span></span>|<span data-ttu-id="d7656-144">Descripción del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d7656-144">Description for the enrollment profile.</span></span>|
|<span data-ttu-id="d7656-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d7656-145">createdDateTime</span></span>|<span data-ttu-id="d7656-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d7656-146">DateTimeOffset</span></span>|<span data-ttu-id="d7656-147">Fecha y hora en que se creó el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d7656-147">Date time the enrollment profile was created.</span></span>|
|<span data-ttu-id="d7656-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d7656-148">lastModifiedDateTime</span></span>|<span data-ttu-id="d7656-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d7656-149">DateTimeOffset</span></span>|<span data-ttu-id="d7656-150">Fecha y hora en que se modificó el perfil de inscripción por última vez.</span><span class="sxs-lookup"><span data-stu-id="d7656-150">Date time the enrollment profile was last modified.</span></span>|
|<span data-ttu-id="d7656-151">tokenValue</span><span class="sxs-lookup"><span data-stu-id="d7656-151">tokenValue</span></span>|<span data-ttu-id="d7656-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7656-152">String</span></span>|<span data-ttu-id="d7656-153">Valor del token creado más recientemente para este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d7656-153">Value of the most recently created token for this enrollment profile.</span></span>|
|<span data-ttu-id="d7656-154">tokenExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="d7656-154">tokenExpirationDateTime</span></span>|<span data-ttu-id="d7656-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d7656-155">DateTimeOffset</span></span>|<span data-ttu-id="d7656-156">Fecha y hora en que expirará el token creado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="d7656-156">Date time the most recently created token will expire.</span></span>|
|<span data-ttu-id="d7656-157">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d7656-157">enrolledDeviceCount</span></span>|<span data-ttu-id="d7656-158">Int32</span><span class="sxs-lookup"><span data-stu-id="d7656-158">Int32</span></span>|<span data-ttu-id="d7656-159">Número total de dispositivos Android que se han inscrito con este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="d7656-159">Total number of Android devices that have enrolled using this enrollment profile.</span></span>|
|<span data-ttu-id="d7656-160">qrCodeContent</span><span class="sxs-lookup"><span data-stu-id="d7656-160">qrCodeContent</span></span>|<span data-ttu-id="d7656-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7656-161">String</span></span>|<span data-ttu-id="d7656-162">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="d7656-162">String used to generate a QR code for the token.</span></span>|
|<span data-ttu-id="d7656-163">qrCodeImage</span><span class="sxs-lookup"><span data-stu-id="d7656-163">qrCodeImage</span></span>|[<span data-ttu-id="d7656-164">mimeContent</span><span class="sxs-lookup"><span data-stu-id="d7656-164">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="d7656-165">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="d7656-165">String used to generate a QR code for the token.</span></span>|



## <a name="response"></a><span data-ttu-id="d7656-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7656-166">Response</span></span>
<span data-ttu-id="d7656-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7656-167">If successful, this method returns a `200 OK` response code and an updated [androidForWorkEnrollmentProfile](../resources/intune-androidforwork-androidforworkenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d7656-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7656-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="d7656-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7656-169">Request</span></span>
<span data-ttu-id="d7656-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7656-170">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="d7656-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7656-171">Response</span></span>
<span data-ttu-id="d7656-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d7656-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






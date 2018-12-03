---
title: Actualizar userPFXCertificate
description: Actualizar las propiedades de un objeto userPFXCertificate.
ms.openlocfilehash: 9fde1e8ff073df7acf76119ace0848616424951a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082929"
---
# <a name="update-userpfxcertificate"></a><span data-ttu-id="c89ca-103">Actualizar userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="c89ca-103">Update userPFXCertificate</span></span>

> <span data-ttu-id="c89ca-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c89ca-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c89ca-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c89ca-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c89ca-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c89ca-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c89ca-107">Actualizar las propiedades de un objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="c89ca-107">Update the properties of a [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c89ca-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c89ca-108">Prerequisites</span></span>
<span data-ttu-id="c89ca-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c89ca-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c89ca-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c89ca-111">Permission type</span></span>|<span data-ttu-id="c89ca-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c89ca-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c89ca-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c89ca-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c89ca-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c89ca-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="c89ca-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c89ca-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c89ca-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c89ca-116">Not supported.</span></span>|
|<span data-ttu-id="c89ca-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c89ca-117">Application</span></span>|<span data-ttu-id="c89ca-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c89ca-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c89ca-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c89ca-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/userPfxCertificates/{userPFXCertificateId}
```

## <a name="request-headers"></a><span data-ttu-id="c89ca-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c89ca-120">Request headers</span></span>
|<span data-ttu-id="c89ca-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c89ca-121">Header</span></span>|<span data-ttu-id="c89ca-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c89ca-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c89ca-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c89ca-123">Authorization</span></span>|<span data-ttu-id="c89ca-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c89ca-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c89ca-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c89ca-125">Accept</span></span>|<span data-ttu-id="c89ca-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c89ca-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c89ca-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c89ca-127">Request body</span></span>
<span data-ttu-id="c89ca-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="c89ca-128">In the request body, supply a JSON representation for the [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) object.</span></span>

<span data-ttu-id="c89ca-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="c89ca-129">The following table shows the properties that are required when you create the [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md).</span></span>

|<span data-ttu-id="c89ca-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c89ca-130">Property</span></span>|<span data-ttu-id="c89ca-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c89ca-131">Type</span></span>|<span data-ttu-id="c89ca-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c89ca-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c89ca-133">id</span><span class="sxs-lookup"><span data-stu-id="c89ca-133">id</span></span>|<span data-ttu-id="c89ca-134">String</span><span class="sxs-lookup"><span data-stu-id="c89ca-134">String</span></span>|<span data-ttu-id="c89ca-135">Identificador único para el certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="c89ca-135">Unique identifier for the PFX certificate.</span></span>|
|<span data-ttu-id="c89ca-136">huella digital</span><span class="sxs-lookup"><span data-stu-id="c89ca-136">thumbprint</span></span>|<span data-ttu-id="c89ca-137">String</span><span class="sxs-lookup"><span data-stu-id="c89ca-137">String</span></span>|<span data-ttu-id="c89ca-138">SHA-1 huella digital del certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="c89ca-138">SHA-1 thumbprint of the PFX certificate.</span></span>|
|<span data-ttu-id="c89ca-139">intendedPurpose</span><span class="sxs-lookup"><span data-stu-id="c89ca-139">intendedPurpose</span></span>|[<span data-ttu-id="c89ca-140">userPfxIntendedPurpose</span><span class="sxs-lookup"><span data-stu-id="c89ca-140">userPfxIntendedPurpose</span></span>](../resources/intune-raimportcerts-userpfxintendedpurpose.md)|<span data-ttu-id="c89ca-141">Del certificado propósito desde el punto de vista de la implementación.</span><span class="sxs-lookup"><span data-stu-id="c89ca-141">Certificate's intended purpose from the point-of-view of deployment.</span></span> <span data-ttu-id="c89ca-142">Los valores posibles son: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn` y `wifi`.</span><span class="sxs-lookup"><span data-stu-id="c89ca-142">Possible values are: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn`, `wifi`.</span></span>|
|<span data-ttu-id="c89ca-143">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c89ca-143">userPrincipalName</span></span>|<span data-ttu-id="c89ca-144">String</span><span class="sxs-lookup"><span data-stu-id="c89ca-144">String</span></span>|<span data-ttu-id="c89ca-145">Nombre Principal de usuario del certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="c89ca-145">User Principal Name of the PFX certificate.</span></span>|
|<span data-ttu-id="c89ca-146">startDateTime</span><span class="sxs-lookup"><span data-stu-id="c89ca-146">startDateTime</span></span>|<span data-ttu-id="c89ca-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c89ca-147">DateTimeOffset</span></span>|<span data-ttu-id="c89ca-148">Fecha/hora de inicio de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="c89ca-148">Certificate's validity start date/time.</span></span>|
|<span data-ttu-id="c89ca-149">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="c89ca-149">expirationDateTime</span></span>|<span data-ttu-id="c89ca-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c89ca-150">DateTimeOffset</span></span>|<span data-ttu-id="c89ca-151">Fecha de expiración de validez y hora del certificado.</span><span class="sxs-lookup"><span data-stu-id="c89ca-151">Certificate's validity expiration date/time.</span></span>|
|<span data-ttu-id="c89ca-152">providerName</span><span class="sxs-lookup"><span data-stu-id="c89ca-152">providerName</span></span>|<span data-ttu-id="c89ca-153">String</span><span class="sxs-lookup"><span data-stu-id="c89ca-153">String</span></span>|<span data-ttu-id="c89ca-154">Proveedor de cifrado usado para cifrar este blob.</span><span class="sxs-lookup"><span data-stu-id="c89ca-154">Crypto provider used to encrypt this blob.</span></span>|
|<span data-ttu-id="c89ca-155">nombre de clave</span><span class="sxs-lookup"><span data-stu-id="c89ca-155">keyName</span></span>|<span data-ttu-id="c89ca-156">String</span><span class="sxs-lookup"><span data-stu-id="c89ca-156">String</span></span>|<span data-ttu-id="c89ca-157">Nombre de la clave (en el proveedor) utilizada para cifrar el blob.</span><span class="sxs-lookup"><span data-stu-id="c89ca-157">Name of the key (within the provider) used to encrypt the blob.</span></span>|
|<span data-ttu-id="c89ca-158">paddingScheme</span><span class="sxs-lookup"><span data-stu-id="c89ca-158">paddingScheme</span></span>|[<span data-ttu-id="c89ca-159">userPfxPaddingScheme</span><span class="sxs-lookup"><span data-stu-id="c89ca-159">userPfxPaddingScheme</span></span>](../resources/intune-raimportcerts-userpfxpaddingscheme.md)|<span data-ttu-id="c89ca-160">Espaciado interno utilizado por el proveedor durante el cifrado y descifrado de combinación.</span><span class="sxs-lookup"><span data-stu-id="c89ca-160">Padding scheme used by the provider during encryption/decryption.</span></span> <span data-ttu-id="c89ca-161">Los valores posibles son: `none`, `pkcs1`, `oaepSha1`, `oaepSha256`, `oaepSha384`, `oaepSha512`.</span><span class="sxs-lookup"><span data-stu-id="c89ca-161">Possible values are: `none`, `pkcs1`, `oaepSha1`, `oaepSha256`, `oaepSha384`, `oaepSha512`.</span></span>|
|<span data-ttu-id="c89ca-162">encryptedPfxBlob</span><span class="sxs-lookup"><span data-stu-id="c89ca-162">encryptedPfxBlob</span></span>|<span data-ttu-id="c89ca-163">Binario</span><span class="sxs-lookup"><span data-stu-id="c89ca-163">Binary</span></span>|<span data-ttu-id="c89ca-164">Blob PFX cifrado.</span><span class="sxs-lookup"><span data-stu-id="c89ca-164">Encrypted PFX blob.</span></span>|
|<span data-ttu-id="c89ca-165">encryptedPfxPassword</span><span class="sxs-lookup"><span data-stu-id="c89ca-165">encryptedPfxPassword</span></span>|<span data-ttu-id="c89ca-166">String</span><span class="sxs-lookup"><span data-stu-id="c89ca-166">String</span></span>|<span data-ttu-id="c89ca-167">Contraseña PFX cifrada.</span><span class="sxs-lookup"><span data-stu-id="c89ca-167">Encrypted PFX password.</span></span>|
|<span data-ttu-id="c89ca-168">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c89ca-168">createdDateTime</span></span>|<span data-ttu-id="c89ca-169">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c89ca-169">DateTimeOffset</span></span>|<span data-ttu-id="c89ca-170">Fecha y hora cuando se importó este certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="c89ca-170">Date/time when this PFX certificate was imported.</span></span>|
|<span data-ttu-id="c89ca-171">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c89ca-171">lastModifiedDateTime</span></span>|<span data-ttu-id="c89ca-172">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c89ca-172">DateTimeOffset</span></span>|<span data-ttu-id="c89ca-173">Fecha y hora cuando se modificó por última vez este certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="c89ca-173">Date/time when this PFX certificate was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="c89ca-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c89ca-174">Response</span></span>
<span data-ttu-id="c89ca-175">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c89ca-175">If successful, this method returns a `200 OK` response code and an updated [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c89ca-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c89ca-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="c89ca-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c89ca-177">Request</span></span>
<span data-ttu-id="c89ca-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c89ca-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/userPfxCertificates/{userPFXCertificateId}
Content-type: application/json
Content-length: 530

{
  "thumbprint": "Thumbprint value",
  "intendedPurpose": "smimeEncryption",
  "userPrincipalName": "User Principal Name value",
  "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "providerName": "Provider Name value",
  "keyName": "Key Name value",
  "paddingScheme": "pkcs1",
  "encryptedPfxBlob": "ZW5jcnlwdGVkUGZ4QmxvYg==",
  "encryptedPfxPassword": "Encrypted Pfx Password value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```

### <a name="response"></a><span data-ttu-id="c89ca-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c89ca-179">Response</span></span>
<span data-ttu-id="c89ca-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c89ca-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 695

{
  "@odata.type": "#microsoft.graph.userPFXCertificate",
  "id": "045c159b-159b-045c-9b15-5c049b155c04",
  "thumbprint": "Thumbprint value",
  "intendedPurpose": "smimeEncryption",
  "userPrincipalName": "User Principal Name value",
  "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "providerName": "Provider Name value",
  "keyName": "Key Name value",
  "paddingScheme": "pkcs1",
  "encryptedPfxBlob": "ZW5jcnlwdGVkUGZ4QmxvYg==",
  "encryptedPfxPassword": "Encrypted Pfx Password value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```





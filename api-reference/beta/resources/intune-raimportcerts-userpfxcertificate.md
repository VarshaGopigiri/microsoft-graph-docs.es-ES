---
title: tipo de recurso userPFXCertificate
description: Entidad que encapsula toda la información necesaria para los certificados PFX de un usuario.
ms.openlocfilehash: 89040cafa976c88ce84cb8f73bc8a68e2cdfbdf2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087589"
---
# <a name="userpfxcertificate-resource-type"></a><span data-ttu-id="8d279-103">tipo de recurso userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="8d279-103">userPFXCertificate resource type</span></span>

> <span data-ttu-id="8d279-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8d279-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8d279-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8d279-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8d279-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d279-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d279-107">Entidad que encapsula toda la información necesaria para los certificados PFX de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8d279-107">Entity that encapsulates all information required for a user's PFX certificates.</span></span>
## <a name="methods"></a><span data-ttu-id="8d279-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8d279-108">Methods</span></span>
|<span data-ttu-id="8d279-109">Método</span><span class="sxs-lookup"><span data-stu-id="8d279-109">Method</span></span>|<span data-ttu-id="8d279-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d279-110">Return Type</span></span>|<span data-ttu-id="8d279-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d279-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="8d279-112">Lista userPFXCertificates</span><span class="sxs-lookup"><span data-stu-id="8d279-112">List userPFXCertificates</span></span>](../api/intune-raimportcerts-userpfxcertificate-list.md)|<span data-ttu-id="8d279-113">colección de [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)</span><span class="sxs-lookup"><span data-stu-id="8d279-113">[userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) collection</span></span>|<span data-ttu-id="8d279-114">Propiedades de la lista y relaciones de los objetos [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="8d279-114">List properties and relationships of the [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) objects.</span></span>|
|[<span data-ttu-id="8d279-115">Obtener userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="8d279-115">Get userPFXCertificate</span></span>](../api/intune-raimportcerts-userpfxcertificate-get.md)|[<span data-ttu-id="8d279-116">userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="8d279-116">userPFXCertificate</span></span>](../resources/intune-raimportcerts-userpfxcertificate.md)|<span data-ttu-id="8d279-117">Leer las propiedades y las relaciones del objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="8d279-117">Read properties and relationships of the [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) object.</span></span>|
|[<span data-ttu-id="8d279-118">Crear userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="8d279-118">Create userPFXCertificate</span></span>](../api/intune-raimportcerts-userpfxcertificate-create.md)|[<span data-ttu-id="8d279-119">userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="8d279-119">userPFXCertificate</span></span>](../resources/intune-raimportcerts-userpfxcertificate.md)|<span data-ttu-id="8d279-120">Crear un nuevo objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="8d279-120">Create a new [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) object.</span></span>|
|[<span data-ttu-id="8d279-121">Eliminar userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="8d279-121">Delete userPFXCertificate</span></span>](../api/intune-raimportcerts-userpfxcertificate-delete.md)|<span data-ttu-id="8d279-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8d279-122">None</span></span>|<span data-ttu-id="8d279-123">Elimina un [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="8d279-123">Deletes a [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md).</span></span>|
|[<span data-ttu-id="8d279-124">Actualizar userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="8d279-124">Update userPFXCertificate</span></span>](../api/intune-raimportcerts-userpfxcertificate-update.md)|[<span data-ttu-id="8d279-125">userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="8d279-125">userPFXCertificate</span></span>](../resources/intune-raimportcerts-userpfxcertificate.md)|<span data-ttu-id="8d279-126">Actualizar las propiedades de un objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="8d279-126">Update the properties of a [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="8d279-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d279-127">Properties</span></span>
|<span data-ttu-id="8d279-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d279-128">Property</span></span>|<span data-ttu-id="8d279-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d279-129">Type</span></span>|<span data-ttu-id="8d279-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d279-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d279-131">id</span><span class="sxs-lookup"><span data-stu-id="8d279-131">id</span></span>|<span data-ttu-id="8d279-132">String</span><span class="sxs-lookup"><span data-stu-id="8d279-132">String</span></span>|<span data-ttu-id="8d279-133">Identificador único para el certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="8d279-133">Unique identifier for the PFX certificate.</span></span>|
|<span data-ttu-id="8d279-134">huella digital</span><span class="sxs-lookup"><span data-stu-id="8d279-134">thumbprint</span></span>|<span data-ttu-id="8d279-135">String</span><span class="sxs-lookup"><span data-stu-id="8d279-135">String</span></span>|<span data-ttu-id="8d279-136">SHA-1 huella digital del certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="8d279-136">SHA-1 thumbprint of the PFX certificate.</span></span>|
|<span data-ttu-id="8d279-137">intendedPurpose</span><span class="sxs-lookup"><span data-stu-id="8d279-137">intendedPurpose</span></span>|[<span data-ttu-id="8d279-138">userPfxIntendedPurpose</span><span class="sxs-lookup"><span data-stu-id="8d279-138">userPfxIntendedPurpose</span></span>](../resources/intune-raimportcerts-userpfxintendedpurpose.md)|<span data-ttu-id="8d279-139">Del certificado propósito desde el punto de vista de la implementación.</span><span class="sxs-lookup"><span data-stu-id="8d279-139">Certificate's intended purpose from the point-of-view of deployment.</span></span> <span data-ttu-id="8d279-140">Los valores posibles son: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn` y `wifi`.</span><span class="sxs-lookup"><span data-stu-id="8d279-140">Possible values are: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn`, `wifi`.</span></span>|
|<span data-ttu-id="8d279-141">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d279-141">userPrincipalName</span></span>|<span data-ttu-id="8d279-142">String</span><span class="sxs-lookup"><span data-stu-id="8d279-142">String</span></span>|<span data-ttu-id="8d279-143">Nombre Principal de usuario del certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="8d279-143">User Principal Name of the PFX certificate.</span></span>|
|<span data-ttu-id="8d279-144">startDateTime</span><span class="sxs-lookup"><span data-stu-id="8d279-144">startDateTime</span></span>|<span data-ttu-id="8d279-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8d279-145">DateTimeOffset</span></span>|<span data-ttu-id="8d279-146">Fecha/hora de inicio de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="8d279-146">Certificate's validity start date/time.</span></span>|
|<span data-ttu-id="8d279-147">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="8d279-147">expirationDateTime</span></span>|<span data-ttu-id="8d279-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8d279-148">DateTimeOffset</span></span>|<span data-ttu-id="8d279-149">Fecha de expiración de validez y hora del certificado.</span><span class="sxs-lookup"><span data-stu-id="8d279-149">Certificate's validity expiration date/time.</span></span>|
|<span data-ttu-id="8d279-150">providerName</span><span class="sxs-lookup"><span data-stu-id="8d279-150">providerName</span></span>|<span data-ttu-id="8d279-151">String</span><span class="sxs-lookup"><span data-stu-id="8d279-151">String</span></span>|<span data-ttu-id="8d279-152">Proveedor de cifrado usado para cifrar este blob.</span><span class="sxs-lookup"><span data-stu-id="8d279-152">Crypto provider used to encrypt this blob.</span></span>|
|<span data-ttu-id="8d279-153">nombre de clave</span><span class="sxs-lookup"><span data-stu-id="8d279-153">keyName</span></span>|<span data-ttu-id="8d279-154">String</span><span class="sxs-lookup"><span data-stu-id="8d279-154">String</span></span>|<span data-ttu-id="8d279-155">Nombre de la clave (en el proveedor) utilizada para cifrar el blob.</span><span class="sxs-lookup"><span data-stu-id="8d279-155">Name of the key (within the provider) used to encrypt the blob.</span></span>|
|<span data-ttu-id="8d279-156">paddingScheme</span><span class="sxs-lookup"><span data-stu-id="8d279-156">paddingScheme</span></span>|[<span data-ttu-id="8d279-157">userPfxPaddingScheme</span><span class="sxs-lookup"><span data-stu-id="8d279-157">userPfxPaddingScheme</span></span>](../resources/intune-raimportcerts-userpfxpaddingscheme.md)|<span data-ttu-id="8d279-158">Espaciado interno utilizado por el proveedor durante el cifrado y descifrado de combinación.</span><span class="sxs-lookup"><span data-stu-id="8d279-158">Padding scheme used by the provider during encryption/decryption.</span></span> <span data-ttu-id="8d279-159">Los valores posibles son: `none`, `pkcs1`, `oaepSha1`, `oaepSha256`, `oaepSha384`, `oaepSha512`.</span><span class="sxs-lookup"><span data-stu-id="8d279-159">Possible values are: `none`, `pkcs1`, `oaepSha1`, `oaepSha256`, `oaepSha384`, `oaepSha512`.</span></span>|
|<span data-ttu-id="8d279-160">encryptedPfxBlob</span><span class="sxs-lookup"><span data-stu-id="8d279-160">encryptedPfxBlob</span></span>|<span data-ttu-id="8d279-161">Binario</span><span class="sxs-lookup"><span data-stu-id="8d279-161">Binary</span></span>|<span data-ttu-id="8d279-162">Blob PFX cifrado.</span><span class="sxs-lookup"><span data-stu-id="8d279-162">Encrypted PFX blob.</span></span>|
|<span data-ttu-id="8d279-163">encryptedPfxPassword</span><span class="sxs-lookup"><span data-stu-id="8d279-163">encryptedPfxPassword</span></span>|<span data-ttu-id="8d279-164">String</span><span class="sxs-lookup"><span data-stu-id="8d279-164">String</span></span>|<span data-ttu-id="8d279-165">Contraseña PFX cifrada.</span><span class="sxs-lookup"><span data-stu-id="8d279-165">Encrypted PFX password.</span></span>|
|<span data-ttu-id="8d279-166">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8d279-166">createdDateTime</span></span>|<span data-ttu-id="8d279-167">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8d279-167">DateTimeOffset</span></span>|<span data-ttu-id="8d279-168">Fecha y hora cuando se importó este certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="8d279-168">Date/time when this PFX certificate was imported.</span></span>|
|<span data-ttu-id="8d279-169">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8d279-169">lastModifiedDateTime</span></span>|<span data-ttu-id="8d279-170">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8d279-170">DateTimeOffset</span></span>|<span data-ttu-id="8d279-171">Fecha y hora cuando se modificó por última vez este certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="8d279-171">Date/time when this PFX certificate was last modified.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8d279-172">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8d279-172">Relationships</span></span>
<span data-ttu-id="8d279-173">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8d279-173">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8d279-174">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d279-174">JSON Representation</span></span>
<span data-ttu-id="8d279-175">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d279-175">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userPFXCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userPFXCertificate",
  "id": "String (identifier)",
  "thumbprint": "String",
  "intendedPurpose": "String",
  "userPrincipalName": "String",
  "startDateTime": "String (timestamp)",
  "expirationDateTime": "String (timestamp)",
  "providerName": "String",
  "keyName": "String",
  "paddingScheme": "String",
  "encryptedPfxBlob": "binary",
  "encryptedPfxPassword": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)"
}
```






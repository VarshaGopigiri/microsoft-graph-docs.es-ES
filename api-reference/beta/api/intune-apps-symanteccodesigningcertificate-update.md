---
title: Actualizar symantecCodeSigningCertificate
description: Actualizar las propiedades de un objeto symantecCodeSigningCertificate.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7d95627e9a2c678097be0c3cb818a03906e8a06f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824741"
---
# <a name="update-symanteccodesigningcertificate"></a><span data-ttu-id="d0274-103">Actualizar symantecCodeSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="d0274-103">Update symantecCodeSigningCertificate</span></span>

> <span data-ttu-id="d0274-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0274-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0274-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0274-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d0274-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d0274-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d0274-107">Actualizar las propiedades de un objeto [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="d0274-107">Update the properties of a [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d0274-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d0274-108">Prerequisites</span></span>
<span data-ttu-id="d0274-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d0274-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d0274-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0274-111">Permission type</span></span>|<span data-ttu-id="d0274-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0274-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d0274-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0274-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d0274-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0274-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d0274-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0274-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d0274-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0274-116">Not supported.</span></span>|
|<span data-ttu-id="d0274-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0274-117">Application</span></span>|<span data-ttu-id="d0274-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0274-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d0274-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0274-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/symantecCodeSigningCertificate
```

## <a name="request-headers"></a><span data-ttu-id="d0274-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0274-120">Request headers</span></span>
|<span data-ttu-id="d0274-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0274-121">Header</span></span>|<span data-ttu-id="d0274-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d0274-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d0274-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d0274-123">Authorization</span></span>|<span data-ttu-id="d0274-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d0274-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d0274-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d0274-125">Accept</span></span>|<span data-ttu-id="d0274-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d0274-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d0274-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0274-127">Request body</span></span>
<span data-ttu-id="d0274-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="d0274-128">In the request body, supply a JSON representation for the [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) object.</span></span>

<span data-ttu-id="d0274-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="d0274-129">The following table shows the properties that are required when you create the [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md).</span></span>

|<span data-ttu-id="d0274-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0274-130">Property</span></span>|<span data-ttu-id="d0274-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0274-131">Type</span></span>|<span data-ttu-id="d0274-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0274-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d0274-133">id</span><span class="sxs-lookup"><span data-stu-id="d0274-133">id</span></span>|<span data-ttu-id="d0274-134">String</span><span class="sxs-lookup"><span data-stu-id="d0274-134">String</span></span>|<span data-ttu-id="d0274-135">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d0274-135">The key of the entity.</span></span>|
|<span data-ttu-id="d0274-136">content</span><span class="sxs-lookup"><span data-stu-id="d0274-136">content</span></span>|<span data-ttu-id="d0274-137">Binario</span><span class="sxs-lookup"><span data-stu-id="d0274-137">Binary</span></span>|<span data-ttu-id="d0274-138">El certificado de firma de código de Symantec de Windows en el formato de datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="d0274-138">The Windows Symantec Code-Signing Certificate in the raw data format.</span></span>|
|<span data-ttu-id="d0274-139">status</span><span class="sxs-lookup"><span data-stu-id="d0274-139">status</span></span>|[<span data-ttu-id="d0274-140">certificateStatus</span><span class="sxs-lookup"><span data-stu-id="d0274-140">certificateStatus</span></span>](../resources/intune-apps-certificatestatus.md)|<span data-ttu-id="d0274-141">El estado de Cert aprovisiona o no configurado.</span><span class="sxs-lookup"><span data-stu-id="d0274-141">The Cert Status Provisioned or not Provisioned.</span></span> <span data-ttu-id="d0274-142">Los valores posibles son: `notProvisioned` y `provisioned`.</span><span class="sxs-lookup"><span data-stu-id="d0274-142">Possible values are: `notProvisioned`, `provisioned`.</span></span>|
|<span data-ttu-id="d0274-143">password</span><span class="sxs-lookup"><span data-stu-id="d0274-143">password</span></span>|<span data-ttu-id="d0274-144">String</span><span class="sxs-lookup"><span data-stu-id="d0274-144">String</span></span>|<span data-ttu-id="d0274-145">La contraseña requerida para el archivo .pfx.</span><span class="sxs-lookup"><span data-stu-id="d0274-145">The Password required for .pfx file.</span></span>|
|<span data-ttu-id="d0274-146">subjectName</span><span class="sxs-lookup"><span data-stu-id="d0274-146">subjectName</span></span>|<span data-ttu-id="d0274-147">cadena</span><span class="sxs-lookup"><span data-stu-id="d0274-147">String</span></span>|<span data-ttu-id="d0274-148">El nombre de sujeto para el certificado.</span><span class="sxs-lookup"><span data-stu-id="d0274-148">The Subject Name for the cert.</span></span>|
|<span data-ttu-id="d0274-149">subject</span><span class="sxs-lookup"><span data-stu-id="d0274-149">subject</span></span>|<span data-ttu-id="d0274-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="d0274-150">String</span></span>|<span data-ttu-id="d0274-151">El valor de asunto para el certificado.</span><span class="sxs-lookup"><span data-stu-id="d0274-151">The Subject value for the cert.</span></span>|
|<span data-ttu-id="d0274-152">issuerName</span><span class="sxs-lookup"><span data-stu-id="d0274-152">issuerName</span></span>|<span data-ttu-id="d0274-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="d0274-153">String</span></span>|<span data-ttu-id="d0274-154">El nombre para el certificado del emisor.</span><span class="sxs-lookup"><span data-stu-id="d0274-154">The Issuer Name for the cert.</span></span>|
|<span data-ttu-id="d0274-155">emisor</span><span class="sxs-lookup"><span data-stu-id="d0274-155">issuer</span></span>|<span data-ttu-id="d0274-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="d0274-156">String</span></span>|<span data-ttu-id="d0274-157">El valor de emisor para el certificado.</span><span class="sxs-lookup"><span data-stu-id="d0274-157">The Issuer value for the cert.</span></span>|
|<span data-ttu-id="d0274-158">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="d0274-158">expirationDateTime</span></span>|<span data-ttu-id="d0274-159">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0274-159">DateTimeOffset</span></span>|<span data-ttu-id="d0274-160">La fecha de caducidad del certificado.</span><span class="sxs-lookup"><span data-stu-id="d0274-160">The Cert Expiration Date.</span></span>|
|<span data-ttu-id="d0274-161">uploadDateTime</span><span class="sxs-lookup"><span data-stu-id="d0274-161">uploadDateTime</span></span>|<span data-ttu-id="d0274-162">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0274-162">DateTimeOffset</span></span>|<span data-ttu-id="d0274-163">El tipo del certificado de firma de código como Symantec Cert.</span><span class="sxs-lookup"><span data-stu-id="d0274-163">The Type of the CodeSigning Cert as Symantec Cert.</span></span>|



## <a name="response"></a><span data-ttu-id="d0274-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0274-164">Response</span></span>
<span data-ttu-id="d0274-165">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0274-165">If successful, this method returns a `200 OK` response code and an updated [symantecCodeSigningCertificate](../resources/intune-apps-symanteccodesigningcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d0274-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0274-166">Example</span></span>
### <a name="request"></a><span data-ttu-id="d0274-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0274-167">Request</span></span>
<span data-ttu-id="d0274-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0274-168">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/symantecCodeSigningCertificate
Content-type: application/json
Content-length: 352

{
  "content": "Y29udGVudA==",
  "status": "provisioned",
  "password": "Password value",
  "subjectName": "Subject Name value",
  "subject": "Subject value",
  "issuerName": "Issuer Name value",
  "issuer": "Issuer value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "uploadDateTime": "2016-12-31T23:58:46.5747426-08:00"
}
```

### <a name="response"></a><span data-ttu-id="d0274-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0274-169">Response</span></span>
<span data-ttu-id="d0274-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0274-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 470

{
  "@odata.type": "#microsoft.graph.symantecCodeSigningCertificate",
  "id": "00ffe83e-e83e-00ff-3ee8-ff003ee8ff00",
  "content": "Y29udGVudA==",
  "status": "provisioned",
  "password": "Password value",
  "subjectName": "Subject Name value",
  "subject": "Subject value",
  "issuerName": "Issuer Name value",
  "issuer": "Issuer value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "uploadDateTime": "2016-12-31T23:58:46.5747426-08:00"
}
```






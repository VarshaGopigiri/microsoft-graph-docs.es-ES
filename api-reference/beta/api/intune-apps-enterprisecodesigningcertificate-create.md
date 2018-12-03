---
title: Crear enterpriseCodeSigningCertificate
description: Crear un nuevo objeto enterpriseCodeSigningCertificate.
ms.openlocfilehash: aa5d92c22a1cd4eb91a41b26ed92f76937ce9dcd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082999"
---
# <a name="create-enterprisecodesigningcertificate"></a><span data-ttu-id="f4950-103">Crear enterpriseCodeSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="f4950-103">Create enterpriseCodeSigningCertificate</span></span>

> <span data-ttu-id="f4950-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f4950-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f4950-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f4950-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f4950-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f4950-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f4950-107">Crear un nuevo objeto [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="f4950-107">Create a new [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f4950-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f4950-108">Prerequisites</span></span>
<span data-ttu-id="f4950-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f4950-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f4950-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4950-111">Permission type</span></span>|<span data-ttu-id="f4950-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4950-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f4950-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4950-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f4950-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f4950-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f4950-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4950-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f4950-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4950-116">Not supported.</span></span>|
|<span data-ttu-id="f4950-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4950-117">Application</span></span>|<span data-ttu-id="f4950-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4950-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f4950-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4950-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/enterpriseCodeSigningCertificates
```

## <a name="request-headers"></a><span data-ttu-id="f4950-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4950-120">Request headers</span></span>
|<span data-ttu-id="f4950-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4950-121">Header</span></span>|<span data-ttu-id="f4950-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f4950-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f4950-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f4950-123">Authorization</span></span>|<span data-ttu-id="f4950-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f4950-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f4950-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f4950-125">Accept</span></span>|<span data-ttu-id="f4950-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f4950-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f4950-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4950-127">Request body</span></span>
<span data-ttu-id="f4950-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto enterpriseCodeSigningCertificate.</span><span class="sxs-lookup"><span data-stu-id="f4950-128">In the request body, supply a JSON representation for the enterpriseCodeSigningCertificate object.</span></span>

<span data-ttu-id="f4950-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el enterpriseCodeSigningCertificate.</span><span class="sxs-lookup"><span data-stu-id="f4950-129">The following table shows the properties that are required when you create the enterpriseCodeSigningCertificate.</span></span>

|<span data-ttu-id="f4950-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4950-130">Property</span></span>|<span data-ttu-id="f4950-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4950-131">Type</span></span>|<span data-ttu-id="f4950-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4950-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f4950-133">id</span><span class="sxs-lookup"><span data-stu-id="f4950-133">id</span></span>|<span data-ttu-id="f4950-134">String</span><span class="sxs-lookup"><span data-stu-id="f4950-134">String</span></span>|<span data-ttu-id="f4950-135">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f4950-135">The key of the entity.</span></span>|
|<span data-ttu-id="f4950-136">content</span><span class="sxs-lookup"><span data-stu-id="f4950-136">content</span></span>|<span data-ttu-id="f4950-137">Binario</span><span class="sxs-lookup"><span data-stu-id="f4950-137">Binary</span></span>|<span data-ttu-id="f4950-138">El certificado de firma de código de empresa de Windows, en el formato de datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="f4950-138">The Windows Enterprise Code-Signing Certificate in the raw data format.</span></span>|
|<span data-ttu-id="f4950-139">status</span><span class="sxs-lookup"><span data-stu-id="f4950-139">status</span></span>|[<span data-ttu-id="f4950-140">certificateStatus</span><span class="sxs-lookup"><span data-stu-id="f4950-140">certificateStatus</span></span>](../resources/intune-apps-certificatestatus.md)|<span data-ttu-id="f4950-141">El estado del certificado aprovisiona o no configurado.</span><span class="sxs-lookup"><span data-stu-id="f4950-141">The Certificate Status Provisioned or not Provisioned.</span></span> <span data-ttu-id="f4950-142">Los valores posibles son: `notProvisioned` y `provisioned`.</span><span class="sxs-lookup"><span data-stu-id="f4950-142">Possible values are: `notProvisioned`, `provisioned`.</span></span>|
|<span data-ttu-id="f4950-143">subjectName</span><span class="sxs-lookup"><span data-stu-id="f4950-143">subjectName</span></span>|<span data-ttu-id="f4950-144">cadena</span><span class="sxs-lookup"><span data-stu-id="f4950-144">String</span></span>|<span data-ttu-id="f4950-145">El nombre de sujeto para el certificado.</span><span class="sxs-lookup"><span data-stu-id="f4950-145">The Subject Name for the cert.</span></span>|
|<span data-ttu-id="f4950-146">subject</span><span class="sxs-lookup"><span data-stu-id="f4950-146">subject</span></span>|<span data-ttu-id="f4950-147">String</span><span class="sxs-lookup"><span data-stu-id="f4950-147">String</span></span>|<span data-ttu-id="f4950-148">El valor de asunto para el certificado.</span><span class="sxs-lookup"><span data-stu-id="f4950-148">The Subject Value for the cert.</span></span>|
|<span data-ttu-id="f4950-149">issuerName</span><span class="sxs-lookup"><span data-stu-id="f4950-149">issuerName</span></span>|<span data-ttu-id="f4950-150">String</span><span class="sxs-lookup"><span data-stu-id="f4950-150">String</span></span>|<span data-ttu-id="f4950-151">El nombre para el certificado del emisor.</span><span class="sxs-lookup"><span data-stu-id="f4950-151">The Issuer Name for the cert.</span></span>|
|<span data-ttu-id="f4950-152">emisor</span><span class="sxs-lookup"><span data-stu-id="f4950-152">issuer</span></span>|<span data-ttu-id="f4950-153">String</span><span class="sxs-lookup"><span data-stu-id="f4950-153">String</span></span>|<span data-ttu-id="f4950-154">El valor de emisor para el certificado.</span><span class="sxs-lookup"><span data-stu-id="f4950-154">The Issuer value for the cert.</span></span>|
|<span data-ttu-id="f4950-155">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="f4950-155">expirationDateTime</span></span>|<span data-ttu-id="f4950-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4950-156">DateTimeOffset</span></span>|<span data-ttu-id="f4950-157">La fecha de caducidad del certificado.</span><span class="sxs-lookup"><span data-stu-id="f4950-157">The Cert Expiration Date.</span></span>|
|<span data-ttu-id="f4950-158">uploadDateTime</span><span class="sxs-lookup"><span data-stu-id="f4950-158">uploadDateTime</span></span>|<span data-ttu-id="f4950-159">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4950-159">DateTimeOffset</span></span>|<span data-ttu-id="f4950-160">La fecha de la hora del certificado de firma de código cuando se carga.</span><span class="sxs-lookup"><span data-stu-id="f4950-160">The date time of CodeSigning Cert when it is uploaded.</span></span>|



## <a name="response"></a><span data-ttu-id="f4950-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4950-161">Response</span></span>
<span data-ttu-id="f4950-162">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4950-162">If successful, this method returns a `201 Created` response code and a [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f4950-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4950-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="f4950-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4950-164">Request</span></span>
<span data-ttu-id="f4950-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4950-165">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/enterpriseCodeSigningCertificates
Content-type: application/json
Content-length: 390

{
  "@odata.type": "#microsoft.graph.enterpriseCodeSigningCertificate",
  "content": "Y29udGVudA==",
  "status": "provisioned",
  "subjectName": "Subject Name value",
  "subject": "Subject value",
  "issuerName": "Issuer Name value",
  "issuer": "Issuer value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "uploadDateTime": "2016-12-31T23:58:46.5747426-08:00"
}
```

### <a name="response"></a><span data-ttu-id="f4950-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4950-166">Response</span></span>
<span data-ttu-id="f4950-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f4950-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 439

{
  "@odata.type": "#microsoft.graph.enterpriseCodeSigningCertificate",
  "id": "b20d3703-3703-b20d-0337-0db203370db2",
  "content": "Y29udGVudA==",
  "status": "provisioned",
  "subjectName": "Subject Name value",
  "subject": "Subject value",
  "issuerName": "Issuer Name value",
  "issuer": "Issuer value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "uploadDateTime": "2016-12-31T23:58:46.5747426-08:00"
}
```





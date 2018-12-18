---
title: Crear enterpriseCodeSigningCertificate
description: Crear un nuevo objeto enterpriseCodeSigningCertificate.
author: tfitzmac
ms.openlocfilehash: 337513242ae653a1d18f3ed9460cf26210534ab8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341100"
---
# <a name="create-enterprisecodesigningcertificate"></a><span data-ttu-id="5a794-103">Crear enterpriseCodeSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="5a794-103">Create enterpriseCodeSigningCertificate</span></span>

> <span data-ttu-id="5a794-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5a794-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5a794-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5a794-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5a794-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5a794-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5a794-107">Crear un nuevo objeto [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="5a794-107">Create a new [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5a794-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5a794-108">Prerequisites</span></span>
<span data-ttu-id="5a794-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5a794-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5a794-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5a794-111">Permission type</span></span>|<span data-ttu-id="5a794-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5a794-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5a794-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5a794-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5a794-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5a794-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5a794-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5a794-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5a794-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a794-116">Not supported.</span></span>|
|<span data-ttu-id="5a794-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5a794-117">Application</span></span>|<span data-ttu-id="5a794-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a794-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5a794-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5a794-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/enterpriseCodeSigningCertificates
```

## <a name="request-headers"></a><span data-ttu-id="5a794-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5a794-120">Request headers</span></span>
|<span data-ttu-id="5a794-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a794-121">Header</span></span>|<span data-ttu-id="5a794-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5a794-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5a794-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5a794-123">Authorization</span></span>|<span data-ttu-id="5a794-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5a794-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5a794-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5a794-125">Accept</span></span>|<span data-ttu-id="5a794-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5a794-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5a794-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5a794-127">Request body</span></span>
<span data-ttu-id="5a794-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto enterpriseCodeSigningCertificate.</span><span class="sxs-lookup"><span data-stu-id="5a794-128">In the request body, supply a JSON representation for the enterpriseCodeSigningCertificate object.</span></span>

<span data-ttu-id="5a794-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el enterpriseCodeSigningCertificate.</span><span class="sxs-lookup"><span data-stu-id="5a794-129">The following table shows the properties that are required when you create the enterpriseCodeSigningCertificate.</span></span>

|<span data-ttu-id="5a794-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a794-130">Property</span></span>|<span data-ttu-id="5a794-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a794-131">Type</span></span>|<span data-ttu-id="5a794-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a794-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5a794-133">id</span><span class="sxs-lookup"><span data-stu-id="5a794-133">id</span></span>|<span data-ttu-id="5a794-134">String</span><span class="sxs-lookup"><span data-stu-id="5a794-134">String</span></span>|<span data-ttu-id="5a794-135">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5a794-135">The key of the entity.</span></span>|
|<span data-ttu-id="5a794-136">content</span><span class="sxs-lookup"><span data-stu-id="5a794-136">content</span></span>|<span data-ttu-id="5a794-137">Binario</span><span class="sxs-lookup"><span data-stu-id="5a794-137">Binary</span></span>|<span data-ttu-id="5a794-138">El certificado de firma de código de empresa de Windows, en el formato de datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="5a794-138">The Windows Enterprise Code-Signing Certificate in the raw data format.</span></span>|
|<span data-ttu-id="5a794-139">status</span><span class="sxs-lookup"><span data-stu-id="5a794-139">status</span></span>|[<span data-ttu-id="5a794-140">certificateStatus</span><span class="sxs-lookup"><span data-stu-id="5a794-140">certificateStatus</span></span>](../resources/intune-apps-certificatestatus.md)|<span data-ttu-id="5a794-141">El estado del certificado aprovisiona o no configurado.</span><span class="sxs-lookup"><span data-stu-id="5a794-141">The Certificate Status Provisioned or not Provisioned.</span></span> <span data-ttu-id="5a794-142">Los valores posibles son: `notProvisioned` y `provisioned`.</span><span class="sxs-lookup"><span data-stu-id="5a794-142">Possible values are: `notProvisioned`, `provisioned`.</span></span>|
|<span data-ttu-id="5a794-143">subjectName</span><span class="sxs-lookup"><span data-stu-id="5a794-143">subjectName</span></span>|<span data-ttu-id="5a794-144">cadena</span><span class="sxs-lookup"><span data-stu-id="5a794-144">String</span></span>|<span data-ttu-id="5a794-145">El nombre de sujeto para el certificado.</span><span class="sxs-lookup"><span data-stu-id="5a794-145">The Subject Name for the cert.</span></span>|
|<span data-ttu-id="5a794-146">subject</span><span class="sxs-lookup"><span data-stu-id="5a794-146">subject</span></span>|<span data-ttu-id="5a794-147">String</span><span class="sxs-lookup"><span data-stu-id="5a794-147">String</span></span>|<span data-ttu-id="5a794-148">El valor de asunto para el certificado.</span><span class="sxs-lookup"><span data-stu-id="5a794-148">The Subject Value for the cert.</span></span>|
|<span data-ttu-id="5a794-149">issuerName</span><span class="sxs-lookup"><span data-stu-id="5a794-149">issuerName</span></span>|<span data-ttu-id="5a794-150">String</span><span class="sxs-lookup"><span data-stu-id="5a794-150">String</span></span>|<span data-ttu-id="5a794-151">El nombre para el certificado del emisor.</span><span class="sxs-lookup"><span data-stu-id="5a794-151">The Issuer Name for the cert.</span></span>|
|<span data-ttu-id="5a794-152">emisor</span><span class="sxs-lookup"><span data-stu-id="5a794-152">issuer</span></span>|<span data-ttu-id="5a794-153">String</span><span class="sxs-lookup"><span data-stu-id="5a794-153">String</span></span>|<span data-ttu-id="5a794-154">El valor de emisor para el certificado.</span><span class="sxs-lookup"><span data-stu-id="5a794-154">The Issuer value for the cert.</span></span>|
|<span data-ttu-id="5a794-155">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="5a794-155">expirationDateTime</span></span>|<span data-ttu-id="5a794-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5a794-156">DateTimeOffset</span></span>|<span data-ttu-id="5a794-157">La fecha de caducidad del certificado.</span><span class="sxs-lookup"><span data-stu-id="5a794-157">The Cert Expiration Date.</span></span>|
|<span data-ttu-id="5a794-158">uploadDateTime</span><span class="sxs-lookup"><span data-stu-id="5a794-158">uploadDateTime</span></span>|<span data-ttu-id="5a794-159">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5a794-159">DateTimeOffset</span></span>|<span data-ttu-id="5a794-160">La fecha de la hora del certificado de firma de código cuando se carga.</span><span class="sxs-lookup"><span data-stu-id="5a794-160">The date time of CodeSigning Cert when it is uploaded.</span></span>|



## <a name="response"></a><span data-ttu-id="5a794-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a794-161">Response</span></span>
<span data-ttu-id="5a794-162">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a794-162">If successful, this method returns a `201 Created` response code and a [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5a794-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5a794-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="5a794-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5a794-164">Request</span></span>
<span data-ttu-id="5a794-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5a794-165">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="5a794-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a794-166">Response</span></span>
<span data-ttu-id="5a794-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5a794-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






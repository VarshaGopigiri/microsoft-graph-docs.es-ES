---
title: Crear iosVppEBook
description: Cree un objeto iosVppEBook.
ms.openlocfilehash: 403093fa69cff503022ba6104f27a1f8ccd96849
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089073"
---
# <a name="create-iosvppebook"></a><span data-ttu-id="36310-103">Crear iosVppEBook</span><span class="sxs-lookup"><span data-stu-id="36310-103">Create iosVppEBook</span></span>

> <span data-ttu-id="36310-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="36310-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="36310-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="36310-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="36310-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="36310-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="36310-107">Cree un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="36310-107">Create a new [iosVppEBook](../resources/intune-books-iosvppebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="36310-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="36310-108">Prerequisites</span></span>
<span data-ttu-id="36310-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="36310-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="36310-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="36310-111">Permission type</span></span>|<span data-ttu-id="36310-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="36310-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="36310-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="36310-113">Delegated (work or school account)</span></span>|<span data-ttu-id="36310-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="36310-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="36310-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="36310-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="36310-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36310-116">Not supported.</span></span>|
|<span data-ttu-id="36310-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="36310-117">Application</span></span>|<span data-ttu-id="36310-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36310-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="36310-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="36310-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks
```

## <a name="request-headers"></a><span data-ttu-id="36310-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="36310-120">Request headers</span></span>
|<span data-ttu-id="36310-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36310-121">Header</span></span>|<span data-ttu-id="36310-122">Valor</span><span class="sxs-lookup"><span data-stu-id="36310-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="36310-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="36310-123">Authorization</span></span>|<span data-ttu-id="36310-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="36310-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="36310-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="36310-125">Accept</span></span>|<span data-ttu-id="36310-126">application/json</span><span class="sxs-lookup"><span data-stu-id="36310-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="36310-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="36310-127">Request body</span></span>
<span data-ttu-id="36310-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppEBook.</span><span class="sxs-lookup"><span data-stu-id="36310-128">In the request body, supply a JSON representation for the iosVppEBook object.</span></span>

<span data-ttu-id="36310-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppEBook.</span><span class="sxs-lookup"><span data-stu-id="36310-129">The following table shows the properties that are required when you create the iosVppEBook.</span></span>

|<span data-ttu-id="36310-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="36310-130">Property</span></span>|<span data-ttu-id="36310-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="36310-131">Type</span></span>|<span data-ttu-id="36310-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="36310-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="36310-133">id</span><span class="sxs-lookup"><span data-stu-id="36310-133">id</span></span>|<span data-ttu-id="36310-134">String</span><span class="sxs-lookup"><span data-stu-id="36310-134">String</span></span>|<span data-ttu-id="36310-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="36310-135">Key of the entity.</span></span> <span data-ttu-id="36310-136">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-136">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-137">displayName</span><span class="sxs-lookup"><span data-stu-id="36310-137">displayName</span></span>|<span data-ttu-id="36310-138">String</span><span class="sxs-lookup"><span data-stu-id="36310-138">String</span></span>|<span data-ttu-id="36310-139">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="36310-139">Name of the eBook.</span></span> <span data-ttu-id="36310-140">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-140">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-141">descripción</span><span class="sxs-lookup"><span data-stu-id="36310-141">description</span></span>|<span data-ttu-id="36310-142">String</span><span class="sxs-lookup"><span data-stu-id="36310-142">String</span></span>|<span data-ttu-id="36310-143">Descripción.</span><span class="sxs-lookup"><span data-stu-id="36310-143">Description.</span></span> <span data-ttu-id="36310-144">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-144">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-145">publicador</span><span class="sxs-lookup"><span data-stu-id="36310-145">publisher</span></span>|<span data-ttu-id="36310-146">String</span><span class="sxs-lookup"><span data-stu-id="36310-146">String</span></span>|<span data-ttu-id="36310-147">Publicador.</span><span class="sxs-lookup"><span data-stu-id="36310-147">Publisher.</span></span> <span data-ttu-id="36310-148">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-148">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-149">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="36310-149">publishedDateTime</span></span>|<span data-ttu-id="36310-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="36310-150">DateTimeOffset</span></span>|<span data-ttu-id="36310-151">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="36310-151">The date and time when the eBook was published.</span></span> <span data-ttu-id="36310-152">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-152">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-153">largeCover</span><span class="sxs-lookup"><span data-stu-id="36310-153">largeCover</span></span>|[<span data-ttu-id="36310-154">mimeContent</span><span class="sxs-lookup"><span data-stu-id="36310-154">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="36310-155">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="36310-155">Book cover.</span></span> <span data-ttu-id="36310-156">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-156">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-157">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="36310-157">createdDateTime</span></span>|<span data-ttu-id="36310-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="36310-158">DateTimeOffset</span></span>|<span data-ttu-id="36310-159">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="36310-159">The date and time when the eBook file was created.</span></span> <span data-ttu-id="36310-160">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-160">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-161">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="36310-161">lastModifiedDateTime</span></span>|<span data-ttu-id="36310-162">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="36310-162">DateTimeOffset</span></span>|<span data-ttu-id="36310-163">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="36310-163">The date and time when the eBook was last modified.</span></span> <span data-ttu-id="36310-164">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-164">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-165">informationUrl</span><span class="sxs-lookup"><span data-stu-id="36310-165">informationUrl</span></span>|<span data-ttu-id="36310-166">String</span><span class="sxs-lookup"><span data-stu-id="36310-166">String</span></span>|<span data-ttu-id="36310-167">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="36310-167">The more information Url.</span></span> <span data-ttu-id="36310-168">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-168">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-169">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="36310-169">privacyInformationUrl</span></span>|<span data-ttu-id="36310-170">String</span><span class="sxs-lookup"><span data-stu-id="36310-170">String</span></span>|<span data-ttu-id="36310-171">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="36310-171">The privacy statement Url.</span></span> <span data-ttu-id="36310-172">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="36310-172">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="36310-173">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="36310-173">vppTokenId</span></span>|<span data-ttu-id="36310-174">Guid</span><span class="sxs-lookup"><span data-stu-id="36310-174">Guid</span></span>|<span data-ttu-id="36310-175">El Id. de token de VPP.</span><span class="sxs-lookup"><span data-stu-id="36310-175">The Vpp token ID.</span></span>|
|<span data-ttu-id="36310-176">appleId</span><span class="sxs-lookup"><span data-stu-id="36310-176">appleId</span></span>|<span data-ttu-id="36310-177">String</span><span class="sxs-lookup"><span data-stu-id="36310-177">String</span></span>|<span data-ttu-id="36310-178">El ID de Apple asociado a un token de VPP.</span><span class="sxs-lookup"><span data-stu-id="36310-178">The Apple ID associated with Vpp token.</span></span>|
|<span data-ttu-id="36310-179">vppOrganizationName</span><span class="sxs-lookup"><span data-stu-id="36310-179">vppOrganizationName</span></span>|<span data-ttu-id="36310-180">String</span><span class="sxs-lookup"><span data-stu-id="36310-180">String</span></span>|<span data-ttu-id="36310-181">El nombre de la organización del token de VPP.</span><span class="sxs-lookup"><span data-stu-id="36310-181">The Vpp token's organization name.</span></span>|
|<span data-ttu-id="36310-182">géneros</span><span class="sxs-lookup"><span data-stu-id="36310-182">genres</span></span>|<span data-ttu-id="36310-183">Colección string</span><span class="sxs-lookup"><span data-stu-id="36310-183">String collection</span></span>|<span data-ttu-id="36310-184">Géneros.</span><span class="sxs-lookup"><span data-stu-id="36310-184">Genres.</span></span>|
|<span data-ttu-id="36310-185">language</span><span class="sxs-lookup"><span data-stu-id="36310-185">language</span></span>|<span data-ttu-id="36310-186">String</span><span class="sxs-lookup"><span data-stu-id="36310-186">String</span></span>|<span data-ttu-id="36310-187">Idioma.</span><span class="sxs-lookup"><span data-stu-id="36310-187">Language.</span></span>|
|<span data-ttu-id="36310-188">vendedor</span><span class="sxs-lookup"><span data-stu-id="36310-188">seller</span></span>|<span data-ttu-id="36310-189">String</span><span class="sxs-lookup"><span data-stu-id="36310-189">String</span></span>|<span data-ttu-id="36310-190">Vendedor.</span><span class="sxs-lookup"><span data-stu-id="36310-190">Seller.</span></span>|
|<span data-ttu-id="36310-191">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="36310-191">totalLicenseCount</span></span>|<span data-ttu-id="36310-192">Int32</span><span class="sxs-lookup"><span data-stu-id="36310-192">Int32</span></span>|<span data-ttu-id="36310-193">Número total de licencias.</span><span class="sxs-lookup"><span data-stu-id="36310-193">Total license count.</span></span>|
|<span data-ttu-id="36310-194">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="36310-194">usedLicenseCount</span></span>|<span data-ttu-id="36310-195">Int32</span><span class="sxs-lookup"><span data-stu-id="36310-195">Int32</span></span>|<span data-ttu-id="36310-196">Número de licencias usadas.</span><span class="sxs-lookup"><span data-stu-id="36310-196">Used license count.</span></span>|



## <a name="response"></a><span data-ttu-id="36310-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36310-197">Response</span></span>
<span data-ttu-id="36310-198">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36310-198">If successful, this method returns a `201 Created` response code and a [iosVppEBook](../resources/intune-books-iosvppebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="36310-199">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36310-199">Example</span></span>
### <a name="request"></a><span data-ttu-id="36310-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="36310-200">Request</span></span>
<span data-ttu-id="36310-201">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="36310-201">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks
Content-type: application/json
Content-length: 856

{
  "@odata.type": "#microsoft.graph.iosVppEBook",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "informationUrl": "https://example.com/informationUrl/",
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "vppTokenId": "9148ac60-ac60-9148-60ac-489160ac4891",
  "appleId": "Apple Id value",
  "vppOrganizationName": "Vpp Organization Name value",
  "genres": [
    "Genres value"
  ],
  "language": "Language value",
  "seller": "Seller value",
  "totalLicenseCount": 1,
  "usedLicenseCount": 0
}
```

### <a name="response"></a><span data-ttu-id="36310-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36310-202">Response</span></span>
<span data-ttu-id="36310-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="36310-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 964

{
  "@odata.type": "#microsoft.graph.iosVppEBook",
  "id": "3b9f627e-627e-3b9f-7e62-9f3b7e629f3b",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "informationUrl": "https://example.com/informationUrl/",
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "vppTokenId": "9148ac60-ac60-9148-60ac-489160ac4891",
  "appleId": "Apple Id value",
  "vppOrganizationName": "Vpp Organization Name value",
  "genres": [
    "Genres value"
  ],
  "language": "Language value",
  "seller": "Seller value",
  "totalLicenseCount": 1,
  "usedLicenseCount": 0
}
```





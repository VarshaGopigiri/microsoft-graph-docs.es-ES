---
title: Crear iosVppEBook
description: Cree un objeto iosVppEBook.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1c8946efab803393c349fb011b714b78a075dd69
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815872"
---
# <a name="create-iosvppebook"></a><span data-ttu-id="6ae7a-103">Crear iosVppEBook</span><span class="sxs-lookup"><span data-stu-id="6ae7a-103">Create iosVppEBook</span></span>

> <span data-ttu-id="6ae7a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6ae7a-105">Cree un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="6ae7a-105">Create a new [iosVppEBook](../resources/intune-books-iosvppebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6ae7a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ae7a-106">Prerequisites</span></span>
<span data-ttu-id="6ae7a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6ae7a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6ae7a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ae7a-109">Permission type</span></span>|<span data-ttu-id="6ae7a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6ae7a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6ae7a-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6ae7a-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6ae7a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6ae7a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-114">Not supported.</span></span>|
|<span data-ttu-id="6ae7a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ae7a-115">Application</span></span>|<span data-ttu-id="6ae7a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6ae7a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ae7a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks
```

## <a name="request-headers"></a><span data-ttu-id="6ae7a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ae7a-118">Request headers</span></span>
|<span data-ttu-id="6ae7a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ae7a-119">Header</span></span>|<span data-ttu-id="6ae7a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6ae7a-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6ae7a-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="6ae7a-121">Authorization</span></span>|<span data-ttu-id="6ae7a-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6ae7a-123">Accept</span><span class="sxs-lookup"><span data-stu-id="6ae7a-123">Accept</span></span>|<span data-ttu-id="6ae7a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6ae7a-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ae7a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ae7a-125">Request body</span></span>
<span data-ttu-id="6ae7a-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppEBook.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-126">In the request body, supply a JSON representation for the iosVppEBook object.</span></span>

<span data-ttu-id="6ae7a-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppEBook.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-127">The following table shows the properties that are required when you create the iosVppEBook.</span></span>

|<span data-ttu-id="6ae7a-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ae7a-128">Property</span></span>|<span data-ttu-id="6ae7a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ae7a-129">Type</span></span>|<span data-ttu-id="6ae7a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ae7a-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6ae7a-131">id</span><span class="sxs-lookup"><span data-stu-id="6ae7a-131">id</span></span>|<span data-ttu-id="6ae7a-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-132">String</span></span>|<span data-ttu-id="6ae7a-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-133">Key of the entity.</span></span> <span data-ttu-id="6ae7a-134">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-134">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-135">displayName</span><span class="sxs-lookup"><span data-stu-id="6ae7a-135">displayName</span></span>|<span data-ttu-id="6ae7a-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-136">String</span></span>|<span data-ttu-id="6ae7a-137">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="6ae7a-137">Name of the eBook.</span></span> <span data-ttu-id="6ae7a-138">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-138">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-139">descripción</span><span class="sxs-lookup"><span data-stu-id="6ae7a-139">description</span></span>|<span data-ttu-id="6ae7a-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-140">String</span></span>|<span data-ttu-id="6ae7a-141">Descripción.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-141">Description.</span></span> <span data-ttu-id="6ae7a-142">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-142">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-143">publicador</span><span class="sxs-lookup"><span data-stu-id="6ae7a-143">publisher</span></span>|<span data-ttu-id="6ae7a-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-144">String</span></span>|<span data-ttu-id="6ae7a-145">Publicador.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-145">Publisher.</span></span> <span data-ttu-id="6ae7a-146">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-146">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-147">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="6ae7a-147">publishedDateTime</span></span>|<span data-ttu-id="6ae7a-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6ae7a-148">DateTimeOffset</span></span>|<span data-ttu-id="6ae7a-149">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-149">The date and time when the eBook was published.</span></span> <span data-ttu-id="6ae7a-150">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-150">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-151">largeCover</span><span class="sxs-lookup"><span data-stu-id="6ae7a-151">largeCover</span></span>|[<span data-ttu-id="6ae7a-152">mimeContent</span><span class="sxs-lookup"><span data-stu-id="6ae7a-152">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="6ae7a-153">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-153">Book cover.</span></span> <span data-ttu-id="6ae7a-154">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-154">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-155">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6ae7a-155">createdDateTime</span></span>|<span data-ttu-id="6ae7a-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6ae7a-156">DateTimeOffset</span></span>|<span data-ttu-id="6ae7a-157">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-157">The date and time when the eBook file was created.</span></span> <span data-ttu-id="6ae7a-158">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-158">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-159">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6ae7a-159">lastModifiedDateTime</span></span>|<span data-ttu-id="6ae7a-160">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6ae7a-160">DateTimeOffset</span></span>|<span data-ttu-id="6ae7a-161">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-161">The date and time when the eBook was last modified.</span></span> <span data-ttu-id="6ae7a-162">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-162">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-163">informationUrl</span><span class="sxs-lookup"><span data-stu-id="6ae7a-163">informationUrl</span></span>|<span data-ttu-id="6ae7a-164">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-164">String</span></span>|<span data-ttu-id="6ae7a-165">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-165">The more information Url.</span></span> <span data-ttu-id="6ae7a-166">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-166">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-167">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="6ae7a-167">privacyInformationUrl</span></span>|<span data-ttu-id="6ae7a-168">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-168">String</span></span>|<span data-ttu-id="6ae7a-169">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-169">The privacy statement Url.</span></span> <span data-ttu-id="6ae7a-170">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="6ae7a-170">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="6ae7a-171">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="6ae7a-171">vppTokenId</span></span>|<span data-ttu-id="6ae7a-172">Guid</span><span class="sxs-lookup"><span data-stu-id="6ae7a-172">Guid</span></span>|<span data-ttu-id="6ae7a-173">El Id. de token de VPP.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-173">The Vpp token ID.</span></span>|
|<span data-ttu-id="6ae7a-174">appleId</span><span class="sxs-lookup"><span data-stu-id="6ae7a-174">appleId</span></span>|<span data-ttu-id="6ae7a-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-175">String</span></span>|<span data-ttu-id="6ae7a-176">El ID de Apple asociado a un token de VPP.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-176">The Apple ID associated with Vpp token.</span></span>|
|<span data-ttu-id="6ae7a-177">vppOrganizationName</span><span class="sxs-lookup"><span data-stu-id="6ae7a-177">vppOrganizationName</span></span>|<span data-ttu-id="6ae7a-178">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-178">String</span></span>|<span data-ttu-id="6ae7a-179">El nombre de la organización del token de VPP.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-179">The Vpp token's organization name.</span></span>|
|<span data-ttu-id="6ae7a-180">géneros</span><span class="sxs-lookup"><span data-stu-id="6ae7a-180">genres</span></span>|<span data-ttu-id="6ae7a-181">Colección string</span><span class="sxs-lookup"><span data-stu-id="6ae7a-181">String collection</span></span>|<span data-ttu-id="6ae7a-182">Géneros.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-182">Genres.</span></span>|
|<span data-ttu-id="6ae7a-183">language</span><span class="sxs-lookup"><span data-stu-id="6ae7a-183">language</span></span>|<span data-ttu-id="6ae7a-184">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-184">String</span></span>|<span data-ttu-id="6ae7a-185">Idioma.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-185">Language.</span></span>|
|<span data-ttu-id="6ae7a-186">vendedor</span><span class="sxs-lookup"><span data-stu-id="6ae7a-186">seller</span></span>|<span data-ttu-id="6ae7a-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ae7a-187">String</span></span>|<span data-ttu-id="6ae7a-188">Vendedor.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-188">Seller.</span></span>|
|<span data-ttu-id="6ae7a-189">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="6ae7a-189">totalLicenseCount</span></span>|<span data-ttu-id="6ae7a-190">Int32</span><span class="sxs-lookup"><span data-stu-id="6ae7a-190">Int32</span></span>|<span data-ttu-id="6ae7a-191">Número total de licencias.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-191">Total license count.</span></span>|
|<span data-ttu-id="6ae7a-192">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="6ae7a-192">usedLicenseCount</span></span>|<span data-ttu-id="6ae7a-193">Int32</span><span class="sxs-lookup"><span data-stu-id="6ae7a-193">Int32</span></span>|<span data-ttu-id="6ae7a-194">Número de licencias usadas.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-194">Used license count.</span></span>|



## <a name="response"></a><span data-ttu-id="6ae7a-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ae7a-195">Response</span></span>
<span data-ttu-id="6ae7a-196">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-196">If successful, this method returns a `201 Created` response code and a [iosVppEBook](../resources/intune-books-iosvppebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ae7a-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ae7a-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="6ae7a-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ae7a-198">Request</span></span>
<span data-ttu-id="6ae7a-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-199">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks
Content-type: application/json
Content-length: 792

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

### <a name="response"></a><span data-ttu-id="6ae7a-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ae7a-200">Response</span></span>
<span data-ttu-id="6ae7a-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ae7a-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




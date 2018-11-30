---
title: Actualizar iosVppEBook
description: Actualice las propiedades de un objeto iosVppEBook.
ms.openlocfilehash: cc642b6abffe7a813e3b3a2e663db639cd60f119
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029509"
---
# <a name="update-iosvppebook"></a><span data-ttu-id="09fbf-103">Actualizar iosVppEBook</span><span class="sxs-lookup"><span data-stu-id="09fbf-103">Update iosVppEBook</span></span>

> <span data-ttu-id="09fbf-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="09fbf-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="09fbf-105">Actualice las propiedades de un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="09fbf-105">Update the properties of a [iosVppEBook](../resources/intune-books-iosvppebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="09fbf-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="09fbf-106">Prerequisites</span></span>
<span data-ttu-id="09fbf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="09fbf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="09fbf-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="09fbf-109">Permission type</span></span>|<span data-ttu-id="09fbf-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="09fbf-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="09fbf-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="09fbf-111">Delegated (work or school account)</span></span>|<span data-ttu-id="09fbf-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="09fbf-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="09fbf-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="09fbf-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="09fbf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="09fbf-114">Not supported.</span></span>|
|<span data-ttu-id="09fbf-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="09fbf-115">Application</span></span>|<span data-ttu-id="09fbf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="09fbf-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="09fbf-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="09fbf-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}
```

## <a name="request-headers"></a><span data-ttu-id="09fbf-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="09fbf-118">Request headers</span></span>
|<span data-ttu-id="09fbf-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09fbf-119">Header</span></span>|<span data-ttu-id="09fbf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="09fbf-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="09fbf-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="09fbf-121">Authorization</span></span>|<span data-ttu-id="09fbf-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="09fbf-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="09fbf-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="09fbf-123">Accept</span></span>|<span data-ttu-id="09fbf-124">application/json</span><span class="sxs-lookup"><span data-stu-id="09fbf-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="09fbf-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="09fbf-125">Request body</span></span>
<span data-ttu-id="09fbf-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="09fbf-126">In the request body, supply a JSON representation for the [iosVppEBook](../resources/intune-books-iosvppebook.md) object.</span></span>

<span data-ttu-id="09fbf-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="09fbf-127">The following table shows the properties that are required when you create the [iosVppEBook](../resources/intune-books-iosvppebook.md).</span></span>

|<span data-ttu-id="09fbf-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09fbf-128">Property</span></span>|<span data-ttu-id="09fbf-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="09fbf-129">Type</span></span>|<span data-ttu-id="09fbf-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="09fbf-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="09fbf-131">id</span><span class="sxs-lookup"><span data-stu-id="09fbf-131">id</span></span>|<span data-ttu-id="09fbf-132">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-132">String</span></span>|<span data-ttu-id="09fbf-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="09fbf-133">Key of the entity.</span></span> <span data-ttu-id="09fbf-134">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-134">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-135">displayName</span><span class="sxs-lookup"><span data-stu-id="09fbf-135">displayName</span></span>|<span data-ttu-id="09fbf-136">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-136">String</span></span>|<span data-ttu-id="09fbf-137">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="09fbf-137">Name of the eBook.</span></span> <span data-ttu-id="09fbf-138">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-138">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-139">descripción</span><span class="sxs-lookup"><span data-stu-id="09fbf-139">description</span></span>|<span data-ttu-id="09fbf-140">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-140">String</span></span>|<span data-ttu-id="09fbf-141">Descripción.</span><span class="sxs-lookup"><span data-stu-id="09fbf-141">Description.</span></span> <span data-ttu-id="09fbf-142">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-142">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-143">publicador</span><span class="sxs-lookup"><span data-stu-id="09fbf-143">publisher</span></span>|<span data-ttu-id="09fbf-144">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-144">String</span></span>|<span data-ttu-id="09fbf-145">Publicador.</span><span class="sxs-lookup"><span data-stu-id="09fbf-145">Publisher.</span></span> <span data-ttu-id="09fbf-146">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-146">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-147">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="09fbf-147">publishedDateTime</span></span>|<span data-ttu-id="09fbf-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="09fbf-148">DateTimeOffset</span></span>|<span data-ttu-id="09fbf-149">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="09fbf-149">The date and time when the eBook was published.</span></span> <span data-ttu-id="09fbf-150">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-150">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-151">largeCover</span><span class="sxs-lookup"><span data-stu-id="09fbf-151">largeCover</span></span>|[<span data-ttu-id="09fbf-152">mimeContent</span><span class="sxs-lookup"><span data-stu-id="09fbf-152">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="09fbf-153">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="09fbf-153">Book cover.</span></span> <span data-ttu-id="09fbf-154">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-154">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-155">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="09fbf-155">createdDateTime</span></span>|<span data-ttu-id="09fbf-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="09fbf-156">DateTimeOffset</span></span>|<span data-ttu-id="09fbf-157">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="09fbf-157">The date and time when the eBook file was created.</span></span> <span data-ttu-id="09fbf-158">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-158">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-159">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="09fbf-159">lastModifiedDateTime</span></span>|<span data-ttu-id="09fbf-160">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="09fbf-160">DateTimeOffset</span></span>|<span data-ttu-id="09fbf-161">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="09fbf-161">The date and time when the eBook was last modified.</span></span> <span data-ttu-id="09fbf-162">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-162">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-163">informationUrl</span><span class="sxs-lookup"><span data-stu-id="09fbf-163">informationUrl</span></span>|<span data-ttu-id="09fbf-164">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-164">String</span></span>|<span data-ttu-id="09fbf-165">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="09fbf-165">The more information Url.</span></span> <span data-ttu-id="09fbf-166">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-166">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-167">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="09fbf-167">privacyInformationUrl</span></span>|<span data-ttu-id="09fbf-168">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-168">String</span></span>|<span data-ttu-id="09fbf-169">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="09fbf-169">The privacy statement Url.</span></span> <span data-ttu-id="09fbf-170">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="09fbf-170">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="09fbf-171">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="09fbf-171">vppTokenId</span></span>|<span data-ttu-id="09fbf-172">Guid</span><span class="sxs-lookup"><span data-stu-id="09fbf-172">Guid</span></span>|<span data-ttu-id="09fbf-173">El Id. de token de VPP.</span><span class="sxs-lookup"><span data-stu-id="09fbf-173">The Vpp token ID.</span></span>|
|<span data-ttu-id="09fbf-174">appleId</span><span class="sxs-lookup"><span data-stu-id="09fbf-174">appleId</span></span>|<span data-ttu-id="09fbf-175">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-175">String</span></span>|<span data-ttu-id="09fbf-176">El ID de Apple asociado a un token de VPP.</span><span class="sxs-lookup"><span data-stu-id="09fbf-176">The Apple ID associated with Vpp token.</span></span>|
|<span data-ttu-id="09fbf-177">vppOrganizationName</span><span class="sxs-lookup"><span data-stu-id="09fbf-177">vppOrganizationName</span></span>|<span data-ttu-id="09fbf-178">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-178">String</span></span>|<span data-ttu-id="09fbf-179">El nombre de la organización del token de VPP.</span><span class="sxs-lookup"><span data-stu-id="09fbf-179">The Vpp token's organization name.</span></span>|
|<span data-ttu-id="09fbf-180">géneros</span><span class="sxs-lookup"><span data-stu-id="09fbf-180">genres</span></span>|<span data-ttu-id="09fbf-181">Colección string</span><span class="sxs-lookup"><span data-stu-id="09fbf-181">String collection</span></span>|<span data-ttu-id="09fbf-182">Géneros.</span><span class="sxs-lookup"><span data-stu-id="09fbf-182">Genres.</span></span>|
|<span data-ttu-id="09fbf-183">language</span><span class="sxs-lookup"><span data-stu-id="09fbf-183">language</span></span>|<span data-ttu-id="09fbf-184">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-184">String</span></span>|<span data-ttu-id="09fbf-185">Idioma.</span><span class="sxs-lookup"><span data-stu-id="09fbf-185">Language.</span></span>|
|<span data-ttu-id="09fbf-186">vendedor</span><span class="sxs-lookup"><span data-stu-id="09fbf-186">seller</span></span>|<span data-ttu-id="09fbf-187">String</span><span class="sxs-lookup"><span data-stu-id="09fbf-187">String</span></span>|<span data-ttu-id="09fbf-188">Vendedor.</span><span class="sxs-lookup"><span data-stu-id="09fbf-188">Seller.</span></span>|
|<span data-ttu-id="09fbf-189">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="09fbf-189">totalLicenseCount</span></span>|<span data-ttu-id="09fbf-190">Int32</span><span class="sxs-lookup"><span data-stu-id="09fbf-190">Int32</span></span>|<span data-ttu-id="09fbf-191">Número total de licencias.</span><span class="sxs-lookup"><span data-stu-id="09fbf-191">Total license count.</span></span>|
|<span data-ttu-id="09fbf-192">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="09fbf-192">usedLicenseCount</span></span>|<span data-ttu-id="09fbf-193">Int32</span><span class="sxs-lookup"><span data-stu-id="09fbf-193">Int32</span></span>|<span data-ttu-id="09fbf-194">Número de licencias usadas.</span><span class="sxs-lookup"><span data-stu-id="09fbf-194">Used license count.</span></span>|



## <a name="response"></a><span data-ttu-id="09fbf-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09fbf-195">Response</span></span>
<span data-ttu-id="09fbf-196">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09fbf-196">If successful, this method returns a `200 OK` response code and an updated [iosVppEBook](../resources/intune-books-iosvppebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="09fbf-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="09fbf-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="09fbf-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="09fbf-198">Request</span></span>
<span data-ttu-id="09fbf-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="09fbf-199">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}
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

### <a name="response"></a><span data-ttu-id="09fbf-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09fbf-200">Response</span></span>
<span data-ttu-id="09fbf-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="09fbf-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




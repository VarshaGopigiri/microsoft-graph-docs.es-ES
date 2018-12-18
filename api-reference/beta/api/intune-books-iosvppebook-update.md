---
title: Actualizar iosVppEBook
description: Actualice las propiedades de un objeto iosVppEBook.
author: tfitzmac
ms.openlocfilehash: 275b8fa6f1c60b0381df09716da8ccf5985611df
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358383"
---
# <a name="update-iosvppebook"></a><span data-ttu-id="e270d-103">Actualizar iosVppEBook</span><span class="sxs-lookup"><span data-stu-id="e270d-103">Update iosVppEBook</span></span>

> <span data-ttu-id="e270d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e270d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e270d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e270d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e270d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e270d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e270d-107">Actualice las propiedades de un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="e270d-107">Update the properties of a [iosVppEBook](../resources/intune-books-iosvppebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e270d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e270d-108">Prerequisites</span></span>
<span data-ttu-id="e270d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e270d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e270d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e270d-111">Permission type</span></span>|<span data-ttu-id="e270d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e270d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e270d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e270d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e270d-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e270d-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e270d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e270d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e270d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e270d-116">Not supported.</span></span>|
|<span data-ttu-id="e270d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e270d-117">Application</span></span>|<span data-ttu-id="e270d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e270d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e270d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e270d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}
```

## <a name="request-headers"></a><span data-ttu-id="e270d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e270d-120">Request headers</span></span>
|<span data-ttu-id="e270d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e270d-121">Header</span></span>|<span data-ttu-id="e270d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e270d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e270d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e270d-123">Authorization</span></span>|<span data-ttu-id="e270d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e270d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e270d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e270d-125">Accept</span></span>|<span data-ttu-id="e270d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e270d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e270d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e270d-127">Request body</span></span>
<span data-ttu-id="e270d-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="e270d-128">In the request body, supply a JSON representation for the [iosVppEBook](../resources/intune-books-iosvppebook.md) object.</span></span>

<span data-ttu-id="e270d-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppEBook](../resources/intune-books-iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="e270d-129">The following table shows the properties that are required when you create the [iosVppEBook](../resources/intune-books-iosvppebook.md).</span></span>

|<span data-ttu-id="e270d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e270d-130">Property</span></span>|<span data-ttu-id="e270d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e270d-131">Type</span></span>|<span data-ttu-id="e270d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e270d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e270d-133">id</span><span class="sxs-lookup"><span data-stu-id="e270d-133">id</span></span>|<span data-ttu-id="e270d-134">String</span><span class="sxs-lookup"><span data-stu-id="e270d-134">String</span></span>|<span data-ttu-id="e270d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e270d-135">Key of the entity.</span></span> <span data-ttu-id="e270d-136">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-136">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-137">displayName</span><span class="sxs-lookup"><span data-stu-id="e270d-137">displayName</span></span>|<span data-ttu-id="e270d-138">String</span><span class="sxs-lookup"><span data-stu-id="e270d-138">String</span></span>|<span data-ttu-id="e270d-139">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="e270d-139">Name of the eBook.</span></span> <span data-ttu-id="e270d-140">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-140">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-141">descripción</span><span class="sxs-lookup"><span data-stu-id="e270d-141">description</span></span>|<span data-ttu-id="e270d-142">String</span><span class="sxs-lookup"><span data-stu-id="e270d-142">String</span></span>|<span data-ttu-id="e270d-143">Descripción.</span><span class="sxs-lookup"><span data-stu-id="e270d-143">Description.</span></span> <span data-ttu-id="e270d-144">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-144">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-145">publicador</span><span class="sxs-lookup"><span data-stu-id="e270d-145">publisher</span></span>|<span data-ttu-id="e270d-146">String</span><span class="sxs-lookup"><span data-stu-id="e270d-146">String</span></span>|<span data-ttu-id="e270d-147">Publicador.</span><span class="sxs-lookup"><span data-stu-id="e270d-147">Publisher.</span></span> <span data-ttu-id="e270d-148">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-148">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-149">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="e270d-149">publishedDateTime</span></span>|<span data-ttu-id="e270d-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e270d-150">DateTimeOffset</span></span>|<span data-ttu-id="e270d-151">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="e270d-151">The date and time when the eBook was published.</span></span> <span data-ttu-id="e270d-152">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-152">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-153">largeCover</span><span class="sxs-lookup"><span data-stu-id="e270d-153">largeCover</span></span>|[<span data-ttu-id="e270d-154">mimeContent</span><span class="sxs-lookup"><span data-stu-id="e270d-154">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="e270d-155">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="e270d-155">Book cover.</span></span> <span data-ttu-id="e270d-156">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-156">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-157">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e270d-157">createdDateTime</span></span>|<span data-ttu-id="e270d-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e270d-158">DateTimeOffset</span></span>|<span data-ttu-id="e270d-159">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="e270d-159">The date and time when the eBook file was created.</span></span> <span data-ttu-id="e270d-160">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-160">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-161">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e270d-161">lastModifiedDateTime</span></span>|<span data-ttu-id="e270d-162">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e270d-162">DateTimeOffset</span></span>|<span data-ttu-id="e270d-163">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="e270d-163">The date and time when the eBook was last modified.</span></span> <span data-ttu-id="e270d-164">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-164">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-165">informationUrl</span><span class="sxs-lookup"><span data-stu-id="e270d-165">informationUrl</span></span>|<span data-ttu-id="e270d-166">String</span><span class="sxs-lookup"><span data-stu-id="e270d-166">String</span></span>|<span data-ttu-id="e270d-167">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e270d-167">The more information Url.</span></span> <span data-ttu-id="e270d-168">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-168">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-169">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="e270d-169">privacyInformationUrl</span></span>|<span data-ttu-id="e270d-170">String</span><span class="sxs-lookup"><span data-stu-id="e270d-170">String</span></span>|<span data-ttu-id="e270d-171">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="e270d-171">The privacy statement Url.</span></span> <span data-ttu-id="e270d-172">Heredado de [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="e270d-172">Inherited from [managedEBook](../resources/intune-books-managedebook.md)</span></span>|
|<span data-ttu-id="e270d-173">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="e270d-173">vppTokenId</span></span>|<span data-ttu-id="e270d-174">Guid</span><span class="sxs-lookup"><span data-stu-id="e270d-174">Guid</span></span>|<span data-ttu-id="e270d-175">El Id. de token de VPP.</span><span class="sxs-lookup"><span data-stu-id="e270d-175">The Vpp token ID.</span></span>|
|<span data-ttu-id="e270d-176">appleId</span><span class="sxs-lookup"><span data-stu-id="e270d-176">appleId</span></span>|<span data-ttu-id="e270d-177">String</span><span class="sxs-lookup"><span data-stu-id="e270d-177">String</span></span>|<span data-ttu-id="e270d-178">El ID de Apple asociado a un token de VPP.</span><span class="sxs-lookup"><span data-stu-id="e270d-178">The Apple ID associated with Vpp token.</span></span>|
|<span data-ttu-id="e270d-179">vppOrganizationName</span><span class="sxs-lookup"><span data-stu-id="e270d-179">vppOrganizationName</span></span>|<span data-ttu-id="e270d-180">String</span><span class="sxs-lookup"><span data-stu-id="e270d-180">String</span></span>|<span data-ttu-id="e270d-181">El nombre de la organización del token de VPP.</span><span class="sxs-lookup"><span data-stu-id="e270d-181">The Vpp token's organization name.</span></span>|
|<span data-ttu-id="e270d-182">géneros</span><span class="sxs-lookup"><span data-stu-id="e270d-182">genres</span></span>|<span data-ttu-id="e270d-183">Colección string</span><span class="sxs-lookup"><span data-stu-id="e270d-183">String collection</span></span>|<span data-ttu-id="e270d-184">Géneros.</span><span class="sxs-lookup"><span data-stu-id="e270d-184">Genres.</span></span>|
|<span data-ttu-id="e270d-185">language</span><span class="sxs-lookup"><span data-stu-id="e270d-185">language</span></span>|<span data-ttu-id="e270d-186">String</span><span class="sxs-lookup"><span data-stu-id="e270d-186">String</span></span>|<span data-ttu-id="e270d-187">Idioma.</span><span class="sxs-lookup"><span data-stu-id="e270d-187">Language.</span></span>|
|<span data-ttu-id="e270d-188">vendedor</span><span class="sxs-lookup"><span data-stu-id="e270d-188">seller</span></span>|<span data-ttu-id="e270d-189">String</span><span class="sxs-lookup"><span data-stu-id="e270d-189">String</span></span>|<span data-ttu-id="e270d-190">Vendedor.</span><span class="sxs-lookup"><span data-stu-id="e270d-190">Seller.</span></span>|
|<span data-ttu-id="e270d-191">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="e270d-191">totalLicenseCount</span></span>|<span data-ttu-id="e270d-192">Int32</span><span class="sxs-lookup"><span data-stu-id="e270d-192">Int32</span></span>|<span data-ttu-id="e270d-193">Número total de licencias.</span><span class="sxs-lookup"><span data-stu-id="e270d-193">Total license count.</span></span>|
|<span data-ttu-id="e270d-194">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="e270d-194">usedLicenseCount</span></span>|<span data-ttu-id="e270d-195">Int32</span><span class="sxs-lookup"><span data-stu-id="e270d-195">Int32</span></span>|<span data-ttu-id="e270d-196">Número de licencias usadas.</span><span class="sxs-lookup"><span data-stu-id="e270d-196">Used license count.</span></span>|



## <a name="response"></a><span data-ttu-id="e270d-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e270d-197">Response</span></span>
<span data-ttu-id="e270d-198">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBook](../resources/intune-books-iosvppebook.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e270d-198">If successful, this method returns a `200 OK` response code and an updated [iosVppEBook](../resources/intune-books-iosvppebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e270d-199">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e270d-199">Example</span></span>
### <a name="request"></a><span data-ttu-id="e270d-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e270d-200">Request</span></span>
<span data-ttu-id="e270d-201">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e270d-201">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}
Content-type: application/json
Content-length: 806

{
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

### <a name="response"></a><span data-ttu-id="e270d-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e270d-202">Response</span></span>
<span data-ttu-id="e270d-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e270d-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






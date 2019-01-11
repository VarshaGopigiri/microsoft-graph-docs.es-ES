---
title: Crear macOSOfficeSuiteApp
description: Cree un objeto macOSOfficeSuiteApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bf65f879832e4687ad3e784d0b09d7234c8920b8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840477"
---
# <a name="create-macosofficesuiteapp"></a><span data-ttu-id="59430-103">Crear macOSOfficeSuiteApp</span><span class="sxs-lookup"><span data-stu-id="59430-103">Create macOSOfficeSuiteApp</span></span>

> <span data-ttu-id="59430-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="59430-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="59430-105">Cree un objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-105">Create a new [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="59430-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="59430-106">Prerequisites</span></span>
<span data-ttu-id="59430-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="59430-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="59430-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59430-109">Permission type</span></span>|<span data-ttu-id="59430-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59430-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="59430-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59430-111">Delegated (work or school account)</span></span>|<span data-ttu-id="59430-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59430-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="59430-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59430-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="59430-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59430-114">Not supported.</span></span>|
|<span data-ttu-id="59430-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59430-115">Application</span></span>|<span data-ttu-id="59430-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59430-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="59430-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59430-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="59430-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59430-118">Request headers</span></span>
|<span data-ttu-id="59430-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59430-119">Header</span></span>|<span data-ttu-id="59430-120">Valor</span><span class="sxs-lookup"><span data-stu-id="59430-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="59430-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="59430-121">Authorization</span></span>|<span data-ttu-id="59430-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="59430-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="59430-123">Accept</span><span class="sxs-lookup"><span data-stu-id="59430-123">Accept</span></span>|<span data-ttu-id="59430-124">application/json</span><span class="sxs-lookup"><span data-stu-id="59430-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="59430-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59430-125">Request body</span></span>
<span data-ttu-id="59430-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto macOSOfficeSuiteApp.</span><span class="sxs-lookup"><span data-stu-id="59430-126">In the request body, supply a JSON representation for the macOSOfficeSuiteApp object.</span></span>

<span data-ttu-id="59430-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto macOSOfficeSuiteApp.</span><span class="sxs-lookup"><span data-stu-id="59430-127">The following table shows the properties that are required when you create the macOSOfficeSuiteApp.</span></span>

|<span data-ttu-id="59430-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59430-128">Property</span></span>|<span data-ttu-id="59430-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="59430-129">Type</span></span>|<span data-ttu-id="59430-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="59430-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="59430-131">id</span><span class="sxs-lookup"><span data-stu-id="59430-131">id</span></span>|<span data-ttu-id="59430-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="59430-132">String</span></span>|<span data-ttu-id="59430-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="59430-133">Key of the entity.</span></span> <span data-ttu-id="59430-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-135">displayName</span><span class="sxs-lookup"><span data-stu-id="59430-135">displayName</span></span>|<span data-ttu-id="59430-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="59430-136">String</span></span>|<span data-ttu-id="59430-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="59430-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="59430-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-139">descripción</span><span class="sxs-lookup"><span data-stu-id="59430-139">description</span></span>|<span data-ttu-id="59430-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="59430-140">String</span></span>|<span data-ttu-id="59430-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59430-141">The description of the app.</span></span> <span data-ttu-id="59430-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-143">publicador</span><span class="sxs-lookup"><span data-stu-id="59430-143">publisher</span></span>|<span data-ttu-id="59430-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="59430-144">String</span></span>|<span data-ttu-id="59430-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59430-145">The publisher of the app.</span></span> <span data-ttu-id="59430-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="59430-147">largeIcon</span></span>|[<span data-ttu-id="59430-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="59430-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="59430-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="59430-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="59430-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="59430-151">createdDateTime</span></span>|<span data-ttu-id="59430-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="59430-152">DateTimeOffset</span></span>|<span data-ttu-id="59430-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59430-153">The date and time the app was created.</span></span> <span data-ttu-id="59430-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="59430-155">lastModifiedDateTime</span></span>|<span data-ttu-id="59430-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="59430-156">DateTimeOffset</span></span>|<span data-ttu-id="59430-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59430-157">The date and time the app was last modified.</span></span> <span data-ttu-id="59430-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="59430-159">isFeatured</span></span>|<span data-ttu-id="59430-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="59430-160">Boolean</span></span>|<span data-ttu-id="59430-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="59430-162">privacyInformationUrl</span></span>|<span data-ttu-id="59430-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="59430-163">String</span></span>|<span data-ttu-id="59430-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="59430-164">The privacy statement Url.</span></span> <span data-ttu-id="59430-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="59430-166">informationUrl</span></span>|<span data-ttu-id="59430-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="59430-167">String</span></span>|<span data-ttu-id="59430-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="59430-168">The more information Url.</span></span> <span data-ttu-id="59430-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-170">owner</span><span class="sxs-lookup"><span data-stu-id="59430-170">owner</span></span>|<span data-ttu-id="59430-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="59430-171">String</span></span>|<span data-ttu-id="59430-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59430-172">The owner of the app.</span></span> <span data-ttu-id="59430-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-174">developer</span><span class="sxs-lookup"><span data-stu-id="59430-174">developer</span></span>|<span data-ttu-id="59430-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="59430-175">String</span></span>|<span data-ttu-id="59430-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59430-176">The developer of the app.</span></span> <span data-ttu-id="59430-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-178">notas</span><span class="sxs-lookup"><span data-stu-id="59430-178">notes</span></span>|<span data-ttu-id="59430-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="59430-179">String</span></span>|<span data-ttu-id="59430-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59430-180">Notes for the app.</span></span> <span data-ttu-id="59430-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="59430-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="59430-182">publishingState</span></span>|[<span data-ttu-id="59430-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="59430-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="59430-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59430-184">The publishing state for the app.</span></span> <span data-ttu-id="59430-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="59430-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="59430-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="59430-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="59430-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="59430-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|



## <a name="response"></a><span data-ttu-id="59430-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59430-188">Response</span></span>
<span data-ttu-id="59430-189">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59430-189">If successful, this method returns a `201 Created` response code and a [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="59430-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59430-190">Example</span></span>
### <a name="request"></a><span data-ttu-id="59430-191">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59430-191">Request</span></span>
<span data-ttu-id="59430-192">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59430-192">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 584

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing"
}
```

### <a name="response"></a><span data-ttu-id="59430-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59430-193">Response</span></span>
<span data-ttu-id="59430-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="59430-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 756

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
  "id": "bf39e35d-e35d-bf39-5de3-39bf5de339bf",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing"
}
```




---
title: Actualizar macOSOfficeSuiteApp
description: Actualice las propiedades de un objeto macOSOfficeSuiteApp.
author: tfitzmac
ms.openlocfilehash: ae4dea6f9e7bc1740d2677e61c5ed24532c6111e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331482"
---
# <a name="update-macosofficesuiteapp"></a><span data-ttu-id="b2ffa-103">Actualizar macOSOfficeSuiteApp</span><span class="sxs-lookup"><span data-stu-id="b2ffa-103">Update macOSOfficeSuiteApp</span></span>

> <span data-ttu-id="b2ffa-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b2ffa-105">Actualice las propiedades de un objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-105">Update the properties of a [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b2ffa-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b2ffa-106">Prerequisites</span></span>
<span data-ttu-id="b2ffa-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b2ffa-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2ffa-109">Permission type</span></span>|<span data-ttu-id="b2ffa-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2ffa-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b2ffa-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2ffa-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b2ffa-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b2ffa-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b2ffa-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2ffa-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b2ffa-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-114">Not supported.</span></span>|
|<span data-ttu-id="b2ffa-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2ffa-115">Application</span></span>|<span data-ttu-id="b2ffa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b2ffa-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2ffa-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="b2ffa-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2ffa-118">Request headers</span></span>
|<span data-ttu-id="b2ffa-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2ffa-119">Header</span></span>|<span data-ttu-id="b2ffa-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b2ffa-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b2ffa-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b2ffa-121">Authorization</span></span>|<span data-ttu-id="b2ffa-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b2ffa-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b2ffa-123">Accept</span></span>|<span data-ttu-id="b2ffa-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b2ffa-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b2ffa-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b2ffa-125">Request body</span></span>
<span data-ttu-id="b2ffa-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-126">In the request body, supply a JSON representation for the [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object.</span></span>

<span data-ttu-id="b2ffa-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-127">The following table shows the properties that are required when you create the [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span></span>

|<span data-ttu-id="b2ffa-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b2ffa-128">Property</span></span>|<span data-ttu-id="b2ffa-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2ffa-129">Type</span></span>|<span data-ttu-id="b2ffa-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2ffa-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b2ffa-131">id</span><span class="sxs-lookup"><span data-stu-id="b2ffa-131">id</span></span>|<span data-ttu-id="b2ffa-132">String</span><span class="sxs-lookup"><span data-stu-id="b2ffa-132">String</span></span>|<span data-ttu-id="b2ffa-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-133">Key of the entity.</span></span> <span data-ttu-id="b2ffa-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-135">displayName</span><span class="sxs-lookup"><span data-stu-id="b2ffa-135">displayName</span></span>|<span data-ttu-id="b2ffa-136">String</span><span class="sxs-lookup"><span data-stu-id="b2ffa-136">String</span></span>|<span data-ttu-id="b2ffa-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="b2ffa-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-139">descripción</span><span class="sxs-lookup"><span data-stu-id="b2ffa-139">description</span></span>|<span data-ttu-id="b2ffa-140">String</span><span class="sxs-lookup"><span data-stu-id="b2ffa-140">String</span></span>|<span data-ttu-id="b2ffa-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-141">The description of the app.</span></span> <span data-ttu-id="b2ffa-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-143">publicador</span><span class="sxs-lookup"><span data-stu-id="b2ffa-143">publisher</span></span>|<span data-ttu-id="b2ffa-144">String</span><span class="sxs-lookup"><span data-stu-id="b2ffa-144">String</span></span>|<span data-ttu-id="b2ffa-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-145">The publisher of the app.</span></span> <span data-ttu-id="b2ffa-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="b2ffa-147">largeIcon</span></span>|[<span data-ttu-id="b2ffa-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="b2ffa-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="b2ffa-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="b2ffa-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b2ffa-151">createdDateTime</span></span>|<span data-ttu-id="b2ffa-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b2ffa-152">DateTimeOffset</span></span>|<span data-ttu-id="b2ffa-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-153">The date and time the app was created.</span></span> <span data-ttu-id="b2ffa-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b2ffa-155">lastModifiedDateTime</span></span>|<span data-ttu-id="b2ffa-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b2ffa-156">DateTimeOffset</span></span>|<span data-ttu-id="b2ffa-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-157">The date and time the app was last modified.</span></span> <span data-ttu-id="b2ffa-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="b2ffa-159">isFeatured</span></span>|<span data-ttu-id="b2ffa-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="b2ffa-160">Boolean</span></span>|<span data-ttu-id="b2ffa-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="b2ffa-162">privacyInformationUrl</span></span>|<span data-ttu-id="b2ffa-163">String</span><span class="sxs-lookup"><span data-stu-id="b2ffa-163">String</span></span>|<span data-ttu-id="b2ffa-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-164">The privacy statement Url.</span></span> <span data-ttu-id="b2ffa-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="b2ffa-166">informationUrl</span></span>|<span data-ttu-id="b2ffa-167">String</span><span class="sxs-lookup"><span data-stu-id="b2ffa-167">String</span></span>|<span data-ttu-id="b2ffa-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-168">The more information Url.</span></span> <span data-ttu-id="b2ffa-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-170">owner</span><span class="sxs-lookup"><span data-stu-id="b2ffa-170">owner</span></span>|<span data-ttu-id="b2ffa-171">String</span><span class="sxs-lookup"><span data-stu-id="b2ffa-171">String</span></span>|<span data-ttu-id="b2ffa-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-172">The owner of the app.</span></span> <span data-ttu-id="b2ffa-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-174">developer</span><span class="sxs-lookup"><span data-stu-id="b2ffa-174">developer</span></span>|<span data-ttu-id="b2ffa-175">String</span><span class="sxs-lookup"><span data-stu-id="b2ffa-175">String</span></span>|<span data-ttu-id="b2ffa-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-176">The developer of the app.</span></span> <span data-ttu-id="b2ffa-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-178">notas</span><span class="sxs-lookup"><span data-stu-id="b2ffa-178">notes</span></span>|<span data-ttu-id="b2ffa-179">String</span><span class="sxs-lookup"><span data-stu-id="b2ffa-179">String</span></span>|<span data-ttu-id="b2ffa-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-180">Notes for the app.</span></span> <span data-ttu-id="b2ffa-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="b2ffa-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="b2ffa-182">publishingState</span></span>|[<span data-ttu-id="b2ffa-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="b2ffa-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="b2ffa-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-184">The publishing state for the app.</span></span> <span data-ttu-id="b2ffa-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="b2ffa-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="b2ffa-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="b2ffa-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|



## <a name="response"></a><span data-ttu-id="b2ffa-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2ffa-188">Response</span></span>
<span data-ttu-id="b2ffa-189">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-189">If successful, this method returns a `200 OK` response code and an updated [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b2ffa-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2ffa-190">Example</span></span>
### <a name="request"></a><span data-ttu-id="b2ffa-191">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2ffa-191">Request</span></span>
<span data-ttu-id="b2ffa-192">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-192">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
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

### <a name="response"></a><span data-ttu-id="b2ffa-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2ffa-193">Response</span></span>
<span data-ttu-id="b2ffa-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b2ffa-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




---
title: Actualizar webApp
description: Actualice las propiedades de un objeto webApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f1b2362a6a46d33d859ce0eb39f0a117a29aa8fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871095"
---
# <a name="update-webapp"></a><span data-ttu-id="cf367-103">Actualizar webApp</span><span class="sxs-lookup"><span data-stu-id="cf367-103">Update webApp</span></span>

> <span data-ttu-id="cf367-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf367-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf367-105">Actualice las propiedades de un objeto [webApp](../resources/intune-apps-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-105">Update the properties of a [webApp](../resources/intune-apps-webapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cf367-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cf367-106">Prerequisites</span></span>
<span data-ttu-id="cf367-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cf367-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cf367-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf367-109">Permission type</span></span>|<span data-ttu-id="cf367-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf367-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cf367-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf367-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cf367-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf367-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="cf367-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf367-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cf367-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf367-114">Not supported.</span></span>|
|<span data-ttu-id="cf367-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf367-115">Application</span></span>|<span data-ttu-id="cf367-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf367-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cf367-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf367-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="cf367-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf367-118">Request headers</span></span>
|<span data-ttu-id="cf367-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf367-119">Header</span></span>|<span data-ttu-id="cf367-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cf367-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cf367-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="cf367-121">Authorization</span></span>|<span data-ttu-id="cf367-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cf367-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cf367-123">Accept</span><span class="sxs-lookup"><span data-stu-id="cf367-123">Accept</span></span>|<span data-ttu-id="cf367-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cf367-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cf367-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf367-125">Request body</span></span>
<span data-ttu-id="cf367-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [webApp](../resources/intune-apps-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-126">In the request body, supply a JSON representation for the [webApp](../resources/intune-apps-webapp.md) object.</span></span>

<span data-ttu-id="cf367-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [webApp](../resources/intune-apps-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-127">The following table shows the properties that are required when you create the [webApp](../resources/intune-apps-webapp.md).</span></span>

|<span data-ttu-id="cf367-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf367-128">Property</span></span>|<span data-ttu-id="cf367-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf367-129">Type</span></span>|<span data-ttu-id="cf367-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf367-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf367-131">id</span><span class="sxs-lookup"><span data-stu-id="cf367-131">id</span></span>|<span data-ttu-id="cf367-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-132">String</span></span>|<span data-ttu-id="cf367-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="cf367-133">Key of the entity.</span></span> <span data-ttu-id="cf367-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-135">displayName</span><span class="sxs-lookup"><span data-stu-id="cf367-135">displayName</span></span>|<span data-ttu-id="cf367-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-136">String</span></span>|<span data-ttu-id="cf367-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="cf367-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="cf367-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-139">descripción</span><span class="sxs-lookup"><span data-stu-id="cf367-139">description</span></span>|<span data-ttu-id="cf367-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-140">String</span></span>|<span data-ttu-id="cf367-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf367-141">The description of the app.</span></span> <span data-ttu-id="cf367-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-143">publicador</span><span class="sxs-lookup"><span data-stu-id="cf367-143">publisher</span></span>|<span data-ttu-id="cf367-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-144">String</span></span>|<span data-ttu-id="cf367-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf367-145">The publisher of the app.</span></span> <span data-ttu-id="cf367-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="cf367-147">largeIcon</span></span>|[<span data-ttu-id="cf367-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="cf367-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="cf367-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="cf367-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="cf367-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cf367-151">createdDateTime</span></span>|<span data-ttu-id="cf367-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf367-152">DateTimeOffset</span></span>|<span data-ttu-id="cf367-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf367-153">The date and time the app was created.</span></span> <span data-ttu-id="cf367-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cf367-155">lastModifiedDateTime</span></span>|<span data-ttu-id="cf367-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf367-156">DateTimeOffset</span></span>|<span data-ttu-id="cf367-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf367-157">The date and time the app was last modified.</span></span> <span data-ttu-id="cf367-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="cf367-159">isFeatured</span></span>|<span data-ttu-id="cf367-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf367-160">Boolean</span></span>|<span data-ttu-id="cf367-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="cf367-162">privacyInformationUrl</span></span>|<span data-ttu-id="cf367-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-163">String</span></span>|<span data-ttu-id="cf367-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="cf367-164">The privacy statement Url.</span></span> <span data-ttu-id="cf367-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="cf367-166">informationUrl</span></span>|<span data-ttu-id="cf367-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-167">String</span></span>|<span data-ttu-id="cf367-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cf367-168">The more information Url.</span></span> <span data-ttu-id="cf367-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-170">owner</span><span class="sxs-lookup"><span data-stu-id="cf367-170">owner</span></span>|<span data-ttu-id="cf367-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-171">String</span></span>|<span data-ttu-id="cf367-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf367-172">The owner of the app.</span></span> <span data-ttu-id="cf367-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-174">developer</span><span class="sxs-lookup"><span data-stu-id="cf367-174">developer</span></span>|<span data-ttu-id="cf367-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-175">String</span></span>|<span data-ttu-id="cf367-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf367-176">The developer of the app.</span></span> <span data-ttu-id="cf367-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-178">notas</span><span class="sxs-lookup"><span data-stu-id="cf367-178">notes</span></span>|<span data-ttu-id="cf367-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-179">String</span></span>|<span data-ttu-id="cf367-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf367-180">Notes for the app.</span></span> <span data-ttu-id="cf367-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf367-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="cf367-182">publishingState</span></span>|[<span data-ttu-id="cf367-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="cf367-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="cf367-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf367-184">The publishing state for the app.</span></span> <span data-ttu-id="cf367-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="cf367-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="cf367-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf367-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="cf367-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="cf367-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="cf367-188">appUrl</span><span class="sxs-lookup"><span data-stu-id="cf367-188">appUrl</span></span>|<span data-ttu-id="cf367-189">Cadena</span><span class="sxs-lookup"><span data-stu-id="cf367-189">String</span></span>|<span data-ttu-id="cf367-190">Dirección URL de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="cf367-190">The web app URL.</span></span>|
|<span data-ttu-id="cf367-191">useManagedBrowser</span><span class="sxs-lookup"><span data-stu-id="cf367-191">useManagedBrowser</span></span>|<span data-ttu-id="cf367-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf367-192">Boolean</span></span>|<span data-ttu-id="cf367-193">Indica si se va a usar el explorador administrado.</span><span class="sxs-lookup"><span data-stu-id="cf367-193">Whether or not to use managed browser.</span></span> <span data-ttu-id="cf367-194">Esta propiedad solo es aplicable a iOS y Android.</span><span class="sxs-lookup"><span data-stu-id="cf367-194">This property is only applicable for Android and IOS.</span></span>|



## <a name="response"></a><span data-ttu-id="cf367-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf367-195">Response</span></span>
<span data-ttu-id="cf367-196">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [webApp](../resources/intune-apps-webapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf367-196">If successful, this method returns a `200 OK` response code and an updated [webApp](../resources/intune-apps-webapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf367-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf367-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="cf367-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf367-198">Request</span></span>
<span data-ttu-id="cf367-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf367-199">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 645

{
  "@odata.type": "#microsoft.graph.webApp",
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
  "publishingState": "processing",
  "appUrl": "https://example.com/appUrl/",
  "useManagedBrowser": true
}
```

### <a name="response"></a><span data-ttu-id="cf367-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf367-200">Response</span></span>
<span data-ttu-id="cf367-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf367-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 817

{
  "@odata.type": "#microsoft.graph.webApp",
  "id": "4bdc5d30-5d30-4bdc-305d-dc4b305ddc4b",
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
  "publishingState": "processing",
  "appUrl": "https://example.com/appUrl/",
  "useManagedBrowser": true
}
```




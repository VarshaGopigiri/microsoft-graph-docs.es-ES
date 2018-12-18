---
title: Crear windowsPhone81StoreApp
description: Crear un nuevo objeto windowsPhone81StoreApp.
author: tfitzmac
ms.openlocfilehash: 2fe6f1bc2ee2884b5e9ab6251d63a30d2972ef2c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345923"
---
# <a name="create-windowsphone81storeapp"></a><span data-ttu-id="65d06-103">Crear windowsPhone81StoreApp</span><span class="sxs-lookup"><span data-stu-id="65d06-103">Create windowsPhone81StoreApp</span></span>

> <span data-ttu-id="65d06-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="65d06-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="65d06-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="65d06-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="65d06-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="65d06-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="65d06-107">Crear un nuevo objeto [windowsPhone81StoreApp](../resources/intune-apps-windowsphone81storeapp.md) .</span><span class="sxs-lookup"><span data-stu-id="65d06-107">Create a new [windowsPhone81StoreApp](../resources/intune-apps-windowsphone81storeapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="65d06-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="65d06-108">Prerequisites</span></span>
<span data-ttu-id="65d06-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="65d06-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="65d06-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65d06-111">Permission type</span></span>|<span data-ttu-id="65d06-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65d06-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="65d06-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="65d06-113">Delegated (work or school account)</span></span>|<span data-ttu-id="65d06-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="65d06-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="65d06-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="65d06-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="65d06-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65d06-116">Not supported.</span></span>|
|<span data-ttu-id="65d06-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="65d06-117">Application</span></span>|<span data-ttu-id="65d06-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65d06-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="65d06-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65d06-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="65d06-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="65d06-120">Request headers</span></span>
|<span data-ttu-id="65d06-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65d06-121">Header</span></span>|<span data-ttu-id="65d06-122">Valor</span><span class="sxs-lookup"><span data-stu-id="65d06-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="65d06-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="65d06-123">Authorization</span></span>|<span data-ttu-id="65d06-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="65d06-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="65d06-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="65d06-125">Accept</span></span>|<span data-ttu-id="65d06-126">application/json</span><span class="sxs-lookup"><span data-stu-id="65d06-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="65d06-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="65d06-127">Request body</span></span>
<span data-ttu-id="65d06-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsPhone81StoreApp.</span><span class="sxs-lookup"><span data-stu-id="65d06-128">In the request body, supply a JSON representation for the windowsPhone81StoreApp object.</span></span>

<span data-ttu-id="65d06-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsPhone81StoreApp.</span><span class="sxs-lookup"><span data-stu-id="65d06-129">The following table shows the properties that are required when you create the windowsPhone81StoreApp.</span></span>

|<span data-ttu-id="65d06-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="65d06-130">Property</span></span>|<span data-ttu-id="65d06-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="65d06-131">Type</span></span>|<span data-ttu-id="65d06-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="65d06-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="65d06-133">id</span><span class="sxs-lookup"><span data-stu-id="65d06-133">id</span></span>|<span data-ttu-id="65d06-134">String</span><span class="sxs-lookup"><span data-stu-id="65d06-134">String</span></span>|<span data-ttu-id="65d06-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="65d06-135">Key of the entity.</span></span> <span data-ttu-id="65d06-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-137">displayName</span><span class="sxs-lookup"><span data-stu-id="65d06-137">displayName</span></span>|<span data-ttu-id="65d06-138">String</span><span class="sxs-lookup"><span data-stu-id="65d06-138">String</span></span>|<span data-ttu-id="65d06-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="65d06-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="65d06-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-141">descripción</span><span class="sxs-lookup"><span data-stu-id="65d06-141">description</span></span>|<span data-ttu-id="65d06-142">String</span><span class="sxs-lookup"><span data-stu-id="65d06-142">String</span></span>|<span data-ttu-id="65d06-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65d06-143">The description of the app.</span></span> <span data-ttu-id="65d06-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-145">publicador</span><span class="sxs-lookup"><span data-stu-id="65d06-145">publisher</span></span>|<span data-ttu-id="65d06-146">String</span><span class="sxs-lookup"><span data-stu-id="65d06-146">String</span></span>|<span data-ttu-id="65d06-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65d06-147">The publisher of the app.</span></span> <span data-ttu-id="65d06-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="65d06-149">largeIcon</span></span>|[<span data-ttu-id="65d06-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="65d06-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="65d06-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="65d06-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="65d06-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="65d06-153">createdDateTime</span></span>|<span data-ttu-id="65d06-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="65d06-154">DateTimeOffset</span></span>|<span data-ttu-id="65d06-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65d06-155">The date and time the app was created.</span></span> <span data-ttu-id="65d06-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="65d06-157">lastModifiedDateTime</span></span>|<span data-ttu-id="65d06-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="65d06-158">DateTimeOffset</span></span>|<span data-ttu-id="65d06-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65d06-159">The date and time the app was last modified.</span></span> <span data-ttu-id="65d06-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="65d06-161">isFeatured</span></span>|<span data-ttu-id="65d06-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="65d06-162">Boolean</span></span>|<span data-ttu-id="65d06-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="65d06-164">privacyInformationUrl</span></span>|<span data-ttu-id="65d06-165">String</span><span class="sxs-lookup"><span data-stu-id="65d06-165">String</span></span>|<span data-ttu-id="65d06-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="65d06-166">The privacy statement Url.</span></span> <span data-ttu-id="65d06-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="65d06-168">informationUrl</span></span>|<span data-ttu-id="65d06-169">String</span><span class="sxs-lookup"><span data-stu-id="65d06-169">String</span></span>|<span data-ttu-id="65d06-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="65d06-170">The more information Url.</span></span> <span data-ttu-id="65d06-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-172">owner</span><span class="sxs-lookup"><span data-stu-id="65d06-172">owner</span></span>|<span data-ttu-id="65d06-173">String</span><span class="sxs-lookup"><span data-stu-id="65d06-173">String</span></span>|<span data-ttu-id="65d06-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65d06-174">The owner of the app.</span></span> <span data-ttu-id="65d06-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-176">developer</span><span class="sxs-lookup"><span data-stu-id="65d06-176">developer</span></span>|<span data-ttu-id="65d06-177">String</span><span class="sxs-lookup"><span data-stu-id="65d06-177">String</span></span>|<span data-ttu-id="65d06-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65d06-178">The developer of the app.</span></span> <span data-ttu-id="65d06-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-180">notas</span><span class="sxs-lookup"><span data-stu-id="65d06-180">notes</span></span>|<span data-ttu-id="65d06-181">String</span><span class="sxs-lookup"><span data-stu-id="65d06-181">String</span></span>|<span data-ttu-id="65d06-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65d06-182">Notes for the app.</span></span> <span data-ttu-id="65d06-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="65d06-184">uploadState</span></span>|<span data-ttu-id="65d06-185">Int32</span><span class="sxs-lookup"><span data-stu-id="65d06-185">Int32</span></span>|<span data-ttu-id="65d06-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="65d06-186">The upload state.</span></span> <span data-ttu-id="65d06-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="65d06-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="65d06-188">publishingState</span></span>|[<span data-ttu-id="65d06-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="65d06-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="65d06-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65d06-190">The publishing state for the app.</span></span> <span data-ttu-id="65d06-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="65d06-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="65d06-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="65d06-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="65d06-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="65d06-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="65d06-194">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="65d06-194">appStoreUrl</span></span>|<span data-ttu-id="65d06-195">String</span><span class="sxs-lookup"><span data-stu-id="65d06-195">String</span></span>|<span data-ttu-id="65d06-196">URL de la tienda de aplicación de Windows Phone 8.1.</span><span class="sxs-lookup"><span data-stu-id="65d06-196">The Windows Phone 8.1 app store URL.</span></span>|



## <a name="response"></a><span data-ttu-id="65d06-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65d06-197">Response</span></span>
<span data-ttu-id="65d06-198">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsPhone81StoreApp](../resources/intune-apps-windowsphone81storeapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65d06-198">If successful, this method returns a `201 Created` response code and a [windowsPhone81StoreApp](../resources/intune-apps-windowsphone81storeapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="65d06-199">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65d06-199">Example</span></span>
### <a name="request"></a><span data-ttu-id="65d06-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="65d06-200">Request</span></span>
<span data-ttu-id="65d06-201">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="65d06-201">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 727

{
  "@odata.type": "#microsoft.graph.windowsPhone81StoreApp",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "uploadState": 11,
  "publishingState": "processing",
  "appStoreUrl": "https://example.com/appStoreUrl/"
}
```

### <a name="response"></a><span data-ttu-id="65d06-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65d06-202">Response</span></span>
<span data-ttu-id="65d06-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="65d06-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 835

{
  "@odata.type": "#microsoft.graph.windowsPhone81StoreApp",
  "id": "f68ce6a1-e6a1-f68c-a1e6-8cf6a1e68cf6",
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
  "uploadState": 11,
  "publishingState": "processing",
  "appStoreUrl": "https://example.com/appStoreUrl/"
}
```






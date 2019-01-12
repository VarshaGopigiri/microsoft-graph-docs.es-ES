---
title: Actualizar windowsPhoneXAP
description: Actualizar las propiedades de un objeto windowsPhoneXAP.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 55bd6c3df68dbe76b0ce36e94f49e2a7c8d50f10
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944337"
---
# <a name="update-windowsphonexap"></a><span data-ttu-id="4e112-103">Actualizar windowsPhoneXAP</span><span class="sxs-lookup"><span data-stu-id="4e112-103">Update windowsPhoneXAP</span></span>

> <span data-ttu-id="4e112-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4e112-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4e112-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4e112-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4e112-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4e112-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4e112-107">Actualizar las propiedades de un objeto [windowsPhoneXAP](../resources/intune-apps-windowsphonexap.md) .</span><span class="sxs-lookup"><span data-stu-id="4e112-107">Update the properties of a [windowsPhoneXAP](../resources/intune-apps-windowsphonexap.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4e112-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4e112-108">Prerequisites</span></span>
<span data-ttu-id="4e112-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4e112-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4e112-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4e112-111">Permission type</span></span>|<span data-ttu-id="4e112-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4e112-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4e112-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4e112-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4e112-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4e112-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="4e112-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4e112-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4e112-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4e112-116">Not supported.</span></span>|
|<span data-ttu-id="4e112-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4e112-117">Application</span></span>|<span data-ttu-id="4e112-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4e112-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4e112-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4e112-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="4e112-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4e112-120">Request headers</span></span>
|<span data-ttu-id="4e112-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e112-121">Header</span></span>|<span data-ttu-id="4e112-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4e112-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4e112-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="4e112-123">Authorization</span></span>|<span data-ttu-id="4e112-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4e112-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4e112-125">Accept</span><span class="sxs-lookup"><span data-stu-id="4e112-125">Accept</span></span>|<span data-ttu-id="4e112-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4e112-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4e112-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4e112-127">Request body</span></span>
<span data-ttu-id="4e112-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsPhoneXAP](../resources/intune-apps-windowsphonexap.md) .</span><span class="sxs-lookup"><span data-stu-id="4e112-128">In the request body, supply a JSON representation for the [windowsPhoneXAP](../resources/intune-apps-windowsphonexap.md) object.</span></span>

<span data-ttu-id="4e112-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsPhoneXAP](../resources/intune-apps-windowsphonexap.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-129">The following table shows the properties that are required when you create the [windowsPhoneXAP](../resources/intune-apps-windowsphonexap.md).</span></span>

|<span data-ttu-id="4e112-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4e112-130">Property</span></span>|<span data-ttu-id="4e112-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e112-131">Type</span></span>|<span data-ttu-id="4e112-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e112-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4e112-133">id</span><span class="sxs-lookup"><span data-stu-id="4e112-133">id</span></span>|<span data-ttu-id="4e112-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-134">String</span></span>|<span data-ttu-id="4e112-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4e112-135">Key of the entity.</span></span> <span data-ttu-id="4e112-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-137">displayName</span><span class="sxs-lookup"><span data-stu-id="4e112-137">displayName</span></span>|<span data-ttu-id="4e112-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-138">String</span></span>|<span data-ttu-id="4e112-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="4e112-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="4e112-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-141">descripción</span><span class="sxs-lookup"><span data-stu-id="4e112-141">description</span></span>|<span data-ttu-id="4e112-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-142">String</span></span>|<span data-ttu-id="4e112-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e112-143">The description of the app.</span></span> <span data-ttu-id="4e112-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-145">publicador</span><span class="sxs-lookup"><span data-stu-id="4e112-145">publisher</span></span>|<span data-ttu-id="4e112-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-146">String</span></span>|<span data-ttu-id="4e112-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e112-147">The publisher of the app.</span></span> <span data-ttu-id="4e112-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="4e112-149">largeIcon</span></span>|[<span data-ttu-id="4e112-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="4e112-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="4e112-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="4e112-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="4e112-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4e112-153">createdDateTime</span></span>|<span data-ttu-id="4e112-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4e112-154">DateTimeOffset</span></span>|<span data-ttu-id="4e112-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e112-155">The date and time the app was created.</span></span> <span data-ttu-id="4e112-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4e112-157">lastModifiedDateTime</span></span>|<span data-ttu-id="4e112-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4e112-158">DateTimeOffset</span></span>|<span data-ttu-id="4e112-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e112-159">The date and time the app was last modified.</span></span> <span data-ttu-id="4e112-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="4e112-161">isFeatured</span></span>|<span data-ttu-id="4e112-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="4e112-162">Boolean</span></span>|<span data-ttu-id="4e112-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="4e112-164">privacyInformationUrl</span></span>|<span data-ttu-id="4e112-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-165">String</span></span>|<span data-ttu-id="4e112-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="4e112-166">The privacy statement Url.</span></span> <span data-ttu-id="4e112-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="4e112-168">informationUrl</span></span>|<span data-ttu-id="4e112-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-169">String</span></span>|<span data-ttu-id="4e112-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4e112-170">The more information Url.</span></span> <span data-ttu-id="4e112-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-172">owner</span><span class="sxs-lookup"><span data-stu-id="4e112-172">owner</span></span>|<span data-ttu-id="4e112-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-173">String</span></span>|<span data-ttu-id="4e112-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e112-174">The owner of the app.</span></span> <span data-ttu-id="4e112-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-176">developer</span><span class="sxs-lookup"><span data-stu-id="4e112-176">developer</span></span>|<span data-ttu-id="4e112-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-177">String</span></span>|<span data-ttu-id="4e112-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e112-178">The developer of the app.</span></span> <span data-ttu-id="4e112-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-180">notas</span><span class="sxs-lookup"><span data-stu-id="4e112-180">notes</span></span>|<span data-ttu-id="4e112-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-181">String</span></span>|<span data-ttu-id="4e112-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e112-182">Notes for the app.</span></span> <span data-ttu-id="4e112-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="4e112-184">uploadState</span></span>|<span data-ttu-id="4e112-185">Int32</span><span class="sxs-lookup"><span data-stu-id="4e112-185">Int32</span></span>|<span data-ttu-id="4e112-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="4e112-186">The upload state.</span></span> <span data-ttu-id="4e112-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4e112-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="4e112-188">publishingState</span></span>|[<span data-ttu-id="4e112-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="4e112-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="4e112-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e112-190">The publishing state for the app.</span></span> <span data-ttu-id="4e112-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="4e112-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="4e112-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="4e112-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="4e112-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="4e112-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="4e112-194">committedContentVersion</span></span>|<span data-ttu-id="4e112-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-195">String</span></span>|<span data-ttu-id="4e112-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="4e112-196">The internal committed content version.</span></span> <span data-ttu-id="4e112-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="4e112-198">fileName</span><span class="sxs-lookup"><span data-stu-id="4e112-198">fileName</span></span>|<span data-ttu-id="4e112-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-199">String</span></span>|<span data-ttu-id="4e112-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="4e112-200">The name of the main Lob application file.</span></span> <span data-ttu-id="4e112-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="4e112-202">size</span><span class="sxs-lookup"><span data-stu-id="4e112-202">size</span></span>|<span data-ttu-id="4e112-203">Int64</span><span class="sxs-lookup"><span data-stu-id="4e112-203">Int64</span></span>|<span data-ttu-id="4e112-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="4e112-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="4e112-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4e112-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="4e112-206">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4e112-206">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="4e112-207">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4e112-207">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="4e112-208">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="4e112-208">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="4e112-209">productIdentifier</span><span class="sxs-lookup"><span data-stu-id="4e112-209">productIdentifier</span></span>|<span data-ttu-id="4e112-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-210">String</span></span>|<span data-ttu-id="4e112-211">El identificador del producto.</span><span class="sxs-lookup"><span data-stu-id="4e112-211">The Product Identifier.</span></span>|
|<span data-ttu-id="4e112-212">identityVersion</span><span class="sxs-lookup"><span data-stu-id="4e112-212">identityVersion</span></span>|<span data-ttu-id="4e112-213">Cadena</span><span class="sxs-lookup"><span data-stu-id="4e112-213">String</span></span>|<span data-ttu-id="4e112-214">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="4e112-214">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="4e112-215">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e112-215">Response</span></span>
<span data-ttu-id="4e112-216">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsPhoneXAP](../resources/intune-apps-windowsphonexap.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4e112-216">If successful, this method returns a `200 OK` response code and an updated [windowsPhoneXAP](../resources/intune-apps-windowsphonexap.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4e112-217">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e112-217">Example</span></span>
### <a name="request"></a><span data-ttu-id="4e112-218">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4e112-218">Request</span></span>
<span data-ttu-id="4e112-219">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4e112-219">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1089

{
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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  },
  "productIdentifier": "Product Identifier value",
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="4e112-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e112-220">Response</span></span>
<span data-ttu-id="4e112-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4e112-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1251

{
  "@odata.type": "#microsoft.graph.windowsPhoneXAP",
  "id": "301ddc77-dc77-301d-77dc-1d3077dc1d30",
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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  },
  "productIdentifier": "Product Identifier value",
  "identityVersion": "Identity Version value"
}
```






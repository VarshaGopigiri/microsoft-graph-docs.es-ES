---
title: Actualizar windowsUniversalAppX
description: Actualice las propiedades de un objeto windowsUniversalAppX.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b47da8672b980b30471f87bbbe4d9cee14eb5089
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892522"
---
# <a name="update-windowsuniversalappx"></a><span data-ttu-id="74bdd-103">Actualizar windowsUniversalAppX</span><span class="sxs-lookup"><span data-stu-id="74bdd-103">Update windowsUniversalAppX</span></span>

> <span data-ttu-id="74bdd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="74bdd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="74bdd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="74bdd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="74bdd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74bdd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74bdd-107">Actualice las propiedades de un objeto [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-107">Update the properties of a [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="74bdd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="74bdd-108">Prerequisites</span></span>
<span data-ttu-id="74bdd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="74bdd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="74bdd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74bdd-111">Permission type</span></span>|<span data-ttu-id="74bdd-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74bdd-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="74bdd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74bdd-113">Delegated (work or school account)</span></span>|<span data-ttu-id="74bdd-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="74bdd-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="74bdd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74bdd-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="74bdd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74bdd-116">Not supported.</span></span>|
|<span data-ttu-id="74bdd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74bdd-117">Application</span></span>|<span data-ttu-id="74bdd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74bdd-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="74bdd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74bdd-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="74bdd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74bdd-120">Request headers</span></span>
|<span data-ttu-id="74bdd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74bdd-121">Header</span></span>|<span data-ttu-id="74bdd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="74bdd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="74bdd-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="74bdd-123">Authorization</span></span>|<span data-ttu-id="74bdd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="74bdd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="74bdd-125">Accept</span><span class="sxs-lookup"><span data-stu-id="74bdd-125">Accept</span></span>|<span data-ttu-id="74bdd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="74bdd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="74bdd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74bdd-127">Request body</span></span>
<span data-ttu-id="74bdd-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-128">In the request body, supply a JSON representation for the [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) object.</span></span>

<span data-ttu-id="74bdd-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-129">The following table shows the properties that are required when you create the [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md).</span></span>

|<span data-ttu-id="74bdd-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="74bdd-130">Property</span></span>|<span data-ttu-id="74bdd-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="74bdd-131">Type</span></span>|<span data-ttu-id="74bdd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="74bdd-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="74bdd-133">id</span><span class="sxs-lookup"><span data-stu-id="74bdd-133">id</span></span>|<span data-ttu-id="74bdd-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-134">String</span></span>|<span data-ttu-id="74bdd-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="74bdd-135">Key of the entity.</span></span> <span data-ttu-id="74bdd-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-137">displayName</span><span class="sxs-lookup"><span data-stu-id="74bdd-137">displayName</span></span>|<span data-ttu-id="74bdd-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-138">String</span></span>|<span data-ttu-id="74bdd-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="74bdd-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="74bdd-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-141">descripción</span><span class="sxs-lookup"><span data-stu-id="74bdd-141">description</span></span>|<span data-ttu-id="74bdd-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-142">String</span></span>|<span data-ttu-id="74bdd-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-143">The description of the app.</span></span> <span data-ttu-id="74bdd-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-145">publicador</span><span class="sxs-lookup"><span data-stu-id="74bdd-145">publisher</span></span>|<span data-ttu-id="74bdd-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-146">String</span></span>|<span data-ttu-id="74bdd-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-147">The publisher of the app.</span></span> <span data-ttu-id="74bdd-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="74bdd-149">largeIcon</span></span>|[<span data-ttu-id="74bdd-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="74bdd-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="74bdd-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="74bdd-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="74bdd-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="74bdd-153">createdDateTime</span></span>|<span data-ttu-id="74bdd-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="74bdd-154">DateTimeOffset</span></span>|<span data-ttu-id="74bdd-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-155">The date and time the app was created.</span></span> <span data-ttu-id="74bdd-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="74bdd-157">lastModifiedDateTime</span></span>|<span data-ttu-id="74bdd-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="74bdd-158">DateTimeOffset</span></span>|<span data-ttu-id="74bdd-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-159">The date and time the app was last modified.</span></span> <span data-ttu-id="74bdd-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="74bdd-161">isFeatured</span></span>|<span data-ttu-id="74bdd-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="74bdd-162">Boolean</span></span>|<span data-ttu-id="74bdd-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="74bdd-164">privacyInformationUrl</span></span>|<span data-ttu-id="74bdd-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-165">String</span></span>|<span data-ttu-id="74bdd-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="74bdd-166">The privacy statement Url.</span></span> <span data-ttu-id="74bdd-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="74bdd-168">informationUrl</span></span>|<span data-ttu-id="74bdd-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-169">String</span></span>|<span data-ttu-id="74bdd-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="74bdd-170">The more information Url.</span></span> <span data-ttu-id="74bdd-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-172">owner</span><span class="sxs-lookup"><span data-stu-id="74bdd-172">owner</span></span>|<span data-ttu-id="74bdd-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-173">String</span></span>|<span data-ttu-id="74bdd-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-174">The owner of the app.</span></span> <span data-ttu-id="74bdd-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-176">developer</span><span class="sxs-lookup"><span data-stu-id="74bdd-176">developer</span></span>|<span data-ttu-id="74bdd-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-177">String</span></span>|<span data-ttu-id="74bdd-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-178">The developer of the app.</span></span> <span data-ttu-id="74bdd-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-180">notas</span><span class="sxs-lookup"><span data-stu-id="74bdd-180">notes</span></span>|<span data-ttu-id="74bdd-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-181">String</span></span>|<span data-ttu-id="74bdd-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-182">Notes for the app.</span></span> <span data-ttu-id="74bdd-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="74bdd-184">uploadState</span></span>|<span data-ttu-id="74bdd-185">Int32</span><span class="sxs-lookup"><span data-stu-id="74bdd-185">Int32</span></span>|<span data-ttu-id="74bdd-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="74bdd-186">The upload state.</span></span> <span data-ttu-id="74bdd-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="74bdd-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="74bdd-188">publishingState</span></span>|[<span data-ttu-id="74bdd-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="74bdd-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="74bdd-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-190">The publishing state for the app.</span></span> <span data-ttu-id="74bdd-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="74bdd-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="74bdd-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="74bdd-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="74bdd-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="74bdd-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="74bdd-194">committedContentVersion</span></span>|<span data-ttu-id="74bdd-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-195">String</span></span>|<span data-ttu-id="74bdd-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="74bdd-196">The internal committed content version.</span></span> <span data-ttu-id="74bdd-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="74bdd-198">fileName</span><span class="sxs-lookup"><span data-stu-id="74bdd-198">fileName</span></span>|<span data-ttu-id="74bdd-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-199">String</span></span>|<span data-ttu-id="74bdd-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="74bdd-200">The name of the main Lob application file.</span></span> <span data-ttu-id="74bdd-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="74bdd-202">size</span><span class="sxs-lookup"><span data-stu-id="74bdd-202">size</span></span>|<span data-ttu-id="74bdd-203">Int64</span><span class="sxs-lookup"><span data-stu-id="74bdd-203">Int64</span></span>|<span data-ttu-id="74bdd-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="74bdd-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="74bdd-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="74bdd-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="74bdd-206">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="74bdd-206">applicableArchitectures</span></span>|[<span data-ttu-id="74bdd-207">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="74bdd-207">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="74bdd-208">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-208">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="74bdd-209">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="74bdd-209">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="74bdd-210">applicableDeviceTypes</span><span class="sxs-lookup"><span data-stu-id="74bdd-210">applicableDeviceTypes</span></span>|[<span data-ttu-id="74bdd-211">windowsDeviceType</span><span class="sxs-lookup"><span data-stu-id="74bdd-211">windowsDeviceType</span></span>](../resources/intune-apps-windowsdevicetype.md)|<span data-ttu-id="74bdd-212">Tipos de dispositivos Windows en los que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-212">The Windows device type(s) for which this app can run on.</span></span> <span data-ttu-id="74bdd-213">Los valores posibles son: `none`, `desktop`, `mobile`, `holographic` y `team`.</span><span class="sxs-lookup"><span data-stu-id="74bdd-213">Possible values are: `none`, `desktop`, `mobile`, `holographic`, `team`.</span></span>|
|<span data-ttu-id="74bdd-214">identityName</span><span class="sxs-lookup"><span data-stu-id="74bdd-214">identityName</span></span>|<span data-ttu-id="74bdd-215">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-215">String</span></span>|<span data-ttu-id="74bdd-216">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="74bdd-216">The Identity Name.</span></span>|
|<span data-ttu-id="74bdd-217">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="74bdd-217">identityPublisherHash</span></span>|<span data-ttu-id="74bdd-218">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-218">String</span></span>|<span data-ttu-id="74bdd-219">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="74bdd-219">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="74bdd-220">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="74bdd-220">identityResourceIdentifier</span></span>|<span data-ttu-id="74bdd-221">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-221">String</span></span>|<span data-ttu-id="74bdd-222">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="74bdd-222">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="74bdd-223">isBundle</span><span class="sxs-lookup"><span data-stu-id="74bdd-223">isBundle</span></span>|<span data-ttu-id="74bdd-224">Booleano</span><span class="sxs-lookup"><span data-stu-id="74bdd-224">Boolean</span></span>|<span data-ttu-id="74bdd-225">Indica si la aplicación es una agrupación.</span><span class="sxs-lookup"><span data-stu-id="74bdd-225">Whether or not the app is a bundle.</span></span>|
|<span data-ttu-id="74bdd-226">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="74bdd-226">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="74bdd-227">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="74bdd-227">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="74bdd-228">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="74bdd-228">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="74bdd-229">identityVersion</span><span class="sxs-lookup"><span data-stu-id="74bdd-229">identityVersion</span></span>|<span data-ttu-id="74bdd-230">Cadena</span><span class="sxs-lookup"><span data-stu-id="74bdd-230">String</span></span>|<span data-ttu-id="74bdd-231">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="74bdd-231">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="74bdd-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74bdd-232">Response</span></span>
<span data-ttu-id="74bdd-233">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74bdd-233">If successful, this method returns a `200 OK` response code and an updated [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74bdd-234">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74bdd-234">Example</span></span>
### <a name="request"></a><span data-ttu-id="74bdd-235">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74bdd-235">Request</span></span>
<span data-ttu-id="74bdd-236">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74bdd-236">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1308

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
  "applicableArchitectures": "x86",
  "applicableDeviceTypes": "desktop",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
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
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="74bdd-237">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74bdd-237">Response</span></span>
<span data-ttu-id="74bdd-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74bdd-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1475

{
  "@odata.type": "#microsoft.graph.windowsUniversalAppX",
  "id": "4bc47eba-7eba-4bc4-ba7e-c44bba7ec44b",
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
  "applicableArchitectures": "x86",
  "applicableDeviceTypes": "desktop",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
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
  "identityVersion": "Identity Version value"
}
```






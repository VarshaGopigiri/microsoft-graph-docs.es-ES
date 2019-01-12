---
title: Actualizar windowsPhone81AppXBundle
description: Actualizar las propiedades de un objeto windowsPhone81AppXBundle.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2902e95fc8b92a33f2b7e9597e8d96123e8eaef3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949097"
---
# <a name="update-windowsphone81appxbundle"></a><span data-ttu-id="1a33c-103">Actualizar windowsPhone81AppXBundle</span><span class="sxs-lookup"><span data-stu-id="1a33c-103">Update windowsPhone81AppXBundle</span></span>

> <span data-ttu-id="1a33c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1a33c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1a33c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1a33c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1a33c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1a33c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1a33c-107">Actualizar las propiedades de un objeto [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) .</span><span class="sxs-lookup"><span data-stu-id="1a33c-107">Update the properties of a [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1a33c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1a33c-108">Prerequisites</span></span>
<span data-ttu-id="1a33c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1a33c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1a33c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1a33c-111">Permission type</span></span>|<span data-ttu-id="1a33c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1a33c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1a33c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1a33c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1a33c-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1a33c-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1a33c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1a33c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1a33c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a33c-116">Not supported.</span></span>|
|<span data-ttu-id="1a33c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1a33c-117">Application</span></span>|<span data-ttu-id="1a33c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1a33c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1a33c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1a33c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="1a33c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1a33c-120">Request headers</span></span>
|<span data-ttu-id="1a33c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a33c-121">Header</span></span>|<span data-ttu-id="1a33c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1a33c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1a33c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1a33c-123">Authorization</span></span>|<span data-ttu-id="1a33c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1a33c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1a33c-125">Accept</span><span class="sxs-lookup"><span data-stu-id="1a33c-125">Accept</span></span>|<span data-ttu-id="1a33c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1a33c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1a33c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1a33c-127">Request body</span></span>
<span data-ttu-id="1a33c-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) .</span><span class="sxs-lookup"><span data-stu-id="1a33c-128">In the request body, supply a JSON representation for the [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) object.</span></span>

<span data-ttu-id="1a33c-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-129">The following table shows the properties that are required when you create the [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md).</span></span>

|<span data-ttu-id="1a33c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1a33c-130">Property</span></span>|<span data-ttu-id="1a33c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1a33c-131">Type</span></span>|<span data-ttu-id="1a33c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a33c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1a33c-133">id</span><span class="sxs-lookup"><span data-stu-id="1a33c-133">id</span></span>|<span data-ttu-id="1a33c-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-134">String</span></span>|<span data-ttu-id="1a33c-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1a33c-135">Key of the entity.</span></span> <span data-ttu-id="1a33c-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-137">displayName</span><span class="sxs-lookup"><span data-stu-id="1a33c-137">displayName</span></span>|<span data-ttu-id="1a33c-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-138">String</span></span>|<span data-ttu-id="1a33c-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="1a33c-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="1a33c-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-141">descripción</span><span class="sxs-lookup"><span data-stu-id="1a33c-141">description</span></span>|<span data-ttu-id="1a33c-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-142">String</span></span>|<span data-ttu-id="1a33c-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a33c-143">The description of the app.</span></span> <span data-ttu-id="1a33c-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-145">publicador</span><span class="sxs-lookup"><span data-stu-id="1a33c-145">publisher</span></span>|<span data-ttu-id="1a33c-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-146">String</span></span>|<span data-ttu-id="1a33c-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a33c-147">The publisher of the app.</span></span> <span data-ttu-id="1a33c-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="1a33c-149">largeIcon</span></span>|[<span data-ttu-id="1a33c-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="1a33c-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="1a33c-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="1a33c-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="1a33c-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1a33c-153">createdDateTime</span></span>|<span data-ttu-id="1a33c-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1a33c-154">DateTimeOffset</span></span>|<span data-ttu-id="1a33c-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a33c-155">The date and time the app was created.</span></span> <span data-ttu-id="1a33c-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1a33c-157">lastModifiedDateTime</span></span>|<span data-ttu-id="1a33c-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1a33c-158">DateTimeOffset</span></span>|<span data-ttu-id="1a33c-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a33c-159">The date and time the app was last modified.</span></span> <span data-ttu-id="1a33c-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="1a33c-161">isFeatured</span></span>|<span data-ttu-id="1a33c-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="1a33c-162">Boolean</span></span>|<span data-ttu-id="1a33c-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="1a33c-164">privacyInformationUrl</span></span>|<span data-ttu-id="1a33c-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-165">String</span></span>|<span data-ttu-id="1a33c-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="1a33c-166">The privacy statement Url.</span></span> <span data-ttu-id="1a33c-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="1a33c-168">informationUrl</span></span>|<span data-ttu-id="1a33c-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-169">String</span></span>|<span data-ttu-id="1a33c-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1a33c-170">The more information Url.</span></span> <span data-ttu-id="1a33c-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-172">owner</span><span class="sxs-lookup"><span data-stu-id="1a33c-172">owner</span></span>|<span data-ttu-id="1a33c-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-173">String</span></span>|<span data-ttu-id="1a33c-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a33c-174">The owner of the app.</span></span> <span data-ttu-id="1a33c-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-176">developer</span><span class="sxs-lookup"><span data-stu-id="1a33c-176">developer</span></span>|<span data-ttu-id="1a33c-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-177">String</span></span>|<span data-ttu-id="1a33c-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a33c-178">The developer of the app.</span></span> <span data-ttu-id="1a33c-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-180">notas</span><span class="sxs-lookup"><span data-stu-id="1a33c-180">notes</span></span>|<span data-ttu-id="1a33c-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-181">String</span></span>|<span data-ttu-id="1a33c-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a33c-182">Notes for the app.</span></span> <span data-ttu-id="1a33c-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="1a33c-184">uploadState</span></span>|<span data-ttu-id="1a33c-185">Int32</span><span class="sxs-lookup"><span data-stu-id="1a33c-185">Int32</span></span>|<span data-ttu-id="1a33c-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="1a33c-186">The upload state.</span></span> <span data-ttu-id="1a33c-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1a33c-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="1a33c-188">publishingState</span></span>|[<span data-ttu-id="1a33c-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="1a33c-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="1a33c-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a33c-190">The publishing state for the app.</span></span> <span data-ttu-id="1a33c-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="1a33c-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="1a33c-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="1a33c-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="1a33c-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="1a33c-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="1a33c-194">committedContentVersion</span></span>|<span data-ttu-id="1a33c-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-195">String</span></span>|<span data-ttu-id="1a33c-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="1a33c-196">The internal committed content version.</span></span> <span data-ttu-id="1a33c-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="1a33c-198">fileName</span><span class="sxs-lookup"><span data-stu-id="1a33c-198">fileName</span></span>|<span data-ttu-id="1a33c-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-199">String</span></span>|<span data-ttu-id="1a33c-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="1a33c-200">The name of the main Lob application file.</span></span> <span data-ttu-id="1a33c-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="1a33c-202">size</span><span class="sxs-lookup"><span data-stu-id="1a33c-202">size</span></span>|<span data-ttu-id="1a33c-203">Int64</span><span class="sxs-lookup"><span data-stu-id="1a33c-203">Int64</span></span>|<span data-ttu-id="1a33c-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="1a33c-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="1a33c-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="1a33c-206">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="1a33c-206">applicableArchitectures</span></span>|[<span data-ttu-id="1a33c-207">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="1a33c-207">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="1a33c-208">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a33c-208">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="1a33c-209">Se hereda de [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md).</span><span class="sxs-lookup"><span data-stu-id="1a33c-209">Inherited from [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md).</span></span> <span data-ttu-id="1a33c-210">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="1a33c-210">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="1a33c-211">identityName</span><span class="sxs-lookup"><span data-stu-id="1a33c-211">identityName</span></span>|<span data-ttu-id="1a33c-212">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-212">String</span></span>|<span data-ttu-id="1a33c-213">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="1a33c-213">The Identity Name.</span></span> <span data-ttu-id="1a33c-214">Se hereda de [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span><span class="sxs-lookup"><span data-stu-id="1a33c-214">Inherited from [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span></span>|
|<span data-ttu-id="1a33c-215">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="1a33c-215">identityPublisherHash</span></span>|<span data-ttu-id="1a33c-216">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-216">String</span></span>|<span data-ttu-id="1a33c-217">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="1a33c-217">The Identity Publisher Hash.</span></span> <span data-ttu-id="1a33c-218">Se hereda de [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span><span class="sxs-lookup"><span data-stu-id="1a33c-218">Inherited from [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span></span>|
|<span data-ttu-id="1a33c-219">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="1a33c-219">identityResourceIdentifier</span></span>|<span data-ttu-id="1a33c-220">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-220">String</span></span>|<span data-ttu-id="1a33c-221">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="1a33c-221">The Identity Resource Identifier.</span></span> <span data-ttu-id="1a33c-222">Se hereda de [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span><span class="sxs-lookup"><span data-stu-id="1a33c-222">Inherited from [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span></span>|
|<span data-ttu-id="1a33c-223">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="1a33c-223">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="1a33c-224">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="1a33c-224">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="1a33c-225">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="1a33c-225">The value for the minimum applicable operating system.</span></span> <span data-ttu-id="1a33c-226">Se hereda de [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span><span class="sxs-lookup"><span data-stu-id="1a33c-226">Inherited from [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span></span>|
|<span data-ttu-id="1a33c-227">phoneProductIdentifier</span><span class="sxs-lookup"><span data-stu-id="1a33c-227">phoneProductIdentifier</span></span>|<span data-ttu-id="1a33c-228">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-228">String</span></span>|<span data-ttu-id="1a33c-229">El identificador de producto del teléfono.</span><span class="sxs-lookup"><span data-stu-id="1a33c-229">The Phone Product Identifier.</span></span> <span data-ttu-id="1a33c-230">Se hereda de [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span><span class="sxs-lookup"><span data-stu-id="1a33c-230">Inherited from [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span></span>|
|<span data-ttu-id="1a33c-231">phonePublisherId</span><span class="sxs-lookup"><span data-stu-id="1a33c-231">phonePublisherId</span></span>|<span data-ttu-id="1a33c-232">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-232">String</span></span>|<span data-ttu-id="1a33c-233">El identificador del teléfono Publisher. se hereda de [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span><span class="sxs-lookup"><span data-stu-id="1a33c-233">The Phone Publisher Id. Inherited from [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span></span>|
|<span data-ttu-id="1a33c-234">identityVersion</span><span class="sxs-lookup"><span data-stu-id="1a33c-234">identityVersion</span></span>|<span data-ttu-id="1a33c-235">Cadena</span><span class="sxs-lookup"><span data-stu-id="1a33c-235">String</span></span>|<span data-ttu-id="1a33c-236">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="1a33c-236">The identity version.</span></span> <span data-ttu-id="1a33c-237">Se hereda de [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span><span class="sxs-lookup"><span data-stu-id="1a33c-237">Inherited from [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md)</span></span>|
|<span data-ttu-id="1a33c-238">appXPackageInformationList</span><span class="sxs-lookup"><span data-stu-id="1a33c-238">appXPackageInformationList</span></span>|<span data-ttu-id="1a33c-239">colección de [windowsPackageInformation](../resources/intune-apps-windowspackageinformation.md)</span><span class="sxs-lookup"><span data-stu-id="1a33c-239">[windowsPackageInformation](../resources/intune-apps-windowspackageinformation.md) collection</span></span>|<span data-ttu-id="1a33c-240">La lista de información del paquete AppX.</span><span class="sxs-lookup"><span data-stu-id="1a33c-240">The list of AppX Package Information.</span></span>|



## <a name="response"></a><span data-ttu-id="1a33c-241">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a33c-241">Response</span></span>
<span data-ttu-id="1a33c-242">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a33c-242">If successful, this method returns a `200 OK` response code and an updated [windowsPhone81AppXBundle](../resources/intune-apps-windowsphone81appxbundle.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1a33c-243">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a33c-243">Example</span></span>
### <a name="request"></a><span data-ttu-id="1a33c-244">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1a33c-244">Request</span></span>
<span data-ttu-id="1a33c-245">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a33c-245">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 2100

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
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
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
  "phoneProductIdentifier": "Phone Product Identifier value",
  "phonePublisherId": "Phone Publisher Id value",
  "identityVersion": "Identity Version value",
  "appXPackageInformationList": [
    {
      "@odata.type": "microsoft.graph.windowsPackageInformation",
      "applicableArchitecture": "x86",
      "displayName": "Display Name value",
      "identityName": "Identity Name value",
      "identityPublisher": "Identity Publisher value",
      "identityResourceIdentifier": "Identity Resource Identifier value",
      "identityVersion": "Identity Version value",
      "minimumSupportedOperatingSystem": {
        "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
        "v8_0": true,
        "v8_1": true,
        "v10_0": true,
        "v10_1607": true,
        "v10_1703": true,
        "v10_1709": true,
        "v10_1803": true
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="1a33c-246">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a33c-246">Response</span></span>
<span data-ttu-id="1a33c-p127">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1a33c-p127">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2271

{
  "@odata.type": "#microsoft.graph.windowsPhone81AppXBundle",
  "id": "2433be7c-be7c-2433-7cbe-33247cbe3324",
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
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
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
  "phoneProductIdentifier": "Phone Product Identifier value",
  "phonePublisherId": "Phone Publisher Id value",
  "identityVersion": "Identity Version value",
  "appXPackageInformationList": [
    {
      "@odata.type": "microsoft.graph.windowsPackageInformation",
      "applicableArchitecture": "x86",
      "displayName": "Display Name value",
      "identityName": "Identity Name value",
      "identityPublisher": "Identity Publisher value",
      "identityResourceIdentifier": "Identity Resource Identifier value",
      "identityVersion": "Identity Version value",
      "minimumSupportedOperatingSystem": {
        "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
        "v8_0": true,
        "v8_1": true,
        "v10_0": true,
        "v10_1607": true,
        "v10_1703": true,
        "v10_1709": true,
        "v10_1803": true
      }
    }
  ]
}
```






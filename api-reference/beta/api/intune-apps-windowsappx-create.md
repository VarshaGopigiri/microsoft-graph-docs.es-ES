---
title: Crear windowsAppX
description: Crear un nuevo objeto windowsAppX.
author: tfitzmac
ms.openlocfilehash: 9a7f2f0327fb8b0b8f2971efe58c6d3bdb5e03ba
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361953"
---
# <a name="create-windowsappx"></a><span data-ttu-id="2f1de-103">Crear windowsAppX</span><span class="sxs-lookup"><span data-stu-id="2f1de-103">Create windowsAppX</span></span>

> <span data-ttu-id="2f1de-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2f1de-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2f1de-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2f1de-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2f1de-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2f1de-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2f1de-107">Crear un nuevo objeto [windowsAppX](../resources/intune-apps-windowsappx.md) .</span><span class="sxs-lookup"><span data-stu-id="2f1de-107">Create a new [windowsAppX](../resources/intune-apps-windowsappx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2f1de-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2f1de-108">Prerequisites</span></span>
<span data-ttu-id="2f1de-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2f1de-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2f1de-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2f1de-111">Permission type</span></span>|<span data-ttu-id="2f1de-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2f1de-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2f1de-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2f1de-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2f1de-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2f1de-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="2f1de-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2f1de-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2f1de-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2f1de-116">Not supported.</span></span>|
|<span data-ttu-id="2f1de-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2f1de-117">Application</span></span>|<span data-ttu-id="2f1de-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2f1de-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2f1de-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2f1de-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="2f1de-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2f1de-120">Request headers</span></span>
|<span data-ttu-id="2f1de-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f1de-121">Header</span></span>|<span data-ttu-id="2f1de-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2f1de-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2f1de-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2f1de-123">Authorization</span></span>|<span data-ttu-id="2f1de-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2f1de-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2f1de-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2f1de-125">Accept</span></span>|<span data-ttu-id="2f1de-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2f1de-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2f1de-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2f1de-127">Request body</span></span>
<span data-ttu-id="2f1de-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsAppX.</span><span class="sxs-lookup"><span data-stu-id="2f1de-128">In the request body, supply a JSON representation for the windowsAppX object.</span></span>

<span data-ttu-id="2f1de-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsAppX.</span><span class="sxs-lookup"><span data-stu-id="2f1de-129">The following table shows the properties that are required when you create the windowsAppX.</span></span>

|<span data-ttu-id="2f1de-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2f1de-130">Property</span></span>|<span data-ttu-id="2f1de-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f1de-131">Type</span></span>|<span data-ttu-id="2f1de-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f1de-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2f1de-133">id</span><span class="sxs-lookup"><span data-stu-id="2f1de-133">id</span></span>|<span data-ttu-id="2f1de-134">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-134">String</span></span>|<span data-ttu-id="2f1de-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2f1de-135">Key of the entity.</span></span> <span data-ttu-id="2f1de-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-137">displayName</span><span class="sxs-lookup"><span data-stu-id="2f1de-137">displayName</span></span>|<span data-ttu-id="2f1de-138">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-138">String</span></span>|<span data-ttu-id="2f1de-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="2f1de-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="2f1de-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-141">descripción</span><span class="sxs-lookup"><span data-stu-id="2f1de-141">description</span></span>|<span data-ttu-id="2f1de-142">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-142">String</span></span>|<span data-ttu-id="2f1de-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-143">The description of the app.</span></span> <span data-ttu-id="2f1de-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-145">publicador</span><span class="sxs-lookup"><span data-stu-id="2f1de-145">publisher</span></span>|<span data-ttu-id="2f1de-146">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-146">String</span></span>|<span data-ttu-id="2f1de-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-147">The publisher of the app.</span></span> <span data-ttu-id="2f1de-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="2f1de-149">largeIcon</span></span>|[<span data-ttu-id="2f1de-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="2f1de-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="2f1de-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="2f1de-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="2f1de-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2f1de-153">createdDateTime</span></span>|<span data-ttu-id="2f1de-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2f1de-154">DateTimeOffset</span></span>|<span data-ttu-id="2f1de-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-155">The date and time the app was created.</span></span> <span data-ttu-id="2f1de-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2f1de-157">lastModifiedDateTime</span></span>|<span data-ttu-id="2f1de-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2f1de-158">DateTimeOffset</span></span>|<span data-ttu-id="2f1de-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-159">The date and time the app was last modified.</span></span> <span data-ttu-id="2f1de-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="2f1de-161">isFeatured</span></span>|<span data-ttu-id="2f1de-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="2f1de-162">Boolean</span></span>|<span data-ttu-id="2f1de-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="2f1de-164">privacyInformationUrl</span></span>|<span data-ttu-id="2f1de-165">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-165">String</span></span>|<span data-ttu-id="2f1de-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="2f1de-166">The privacy statement Url.</span></span> <span data-ttu-id="2f1de-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="2f1de-168">informationUrl</span></span>|<span data-ttu-id="2f1de-169">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-169">String</span></span>|<span data-ttu-id="2f1de-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2f1de-170">The more information Url.</span></span> <span data-ttu-id="2f1de-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-172">owner</span><span class="sxs-lookup"><span data-stu-id="2f1de-172">owner</span></span>|<span data-ttu-id="2f1de-173">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-173">String</span></span>|<span data-ttu-id="2f1de-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-174">The owner of the app.</span></span> <span data-ttu-id="2f1de-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-176">developer</span><span class="sxs-lookup"><span data-stu-id="2f1de-176">developer</span></span>|<span data-ttu-id="2f1de-177">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-177">String</span></span>|<span data-ttu-id="2f1de-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-178">The developer of the app.</span></span> <span data-ttu-id="2f1de-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-180">notas</span><span class="sxs-lookup"><span data-stu-id="2f1de-180">notes</span></span>|<span data-ttu-id="2f1de-181">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-181">String</span></span>|<span data-ttu-id="2f1de-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-182">Notes for the app.</span></span> <span data-ttu-id="2f1de-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="2f1de-184">uploadState</span></span>|<span data-ttu-id="2f1de-185">Int32</span><span class="sxs-lookup"><span data-stu-id="2f1de-185">Int32</span></span>|<span data-ttu-id="2f1de-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="2f1de-186">The upload state.</span></span> <span data-ttu-id="2f1de-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="2f1de-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="2f1de-188">publishingState</span></span>|[<span data-ttu-id="2f1de-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="2f1de-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="2f1de-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-190">The publishing state for the app.</span></span> <span data-ttu-id="2f1de-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="2f1de-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="2f1de-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="2f1de-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="2f1de-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="2f1de-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="2f1de-194">committedContentVersion</span></span>|<span data-ttu-id="2f1de-195">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-195">String</span></span>|<span data-ttu-id="2f1de-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="2f1de-196">The internal committed content version.</span></span> <span data-ttu-id="2f1de-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2f1de-198">fileName</span><span class="sxs-lookup"><span data-stu-id="2f1de-198">fileName</span></span>|<span data-ttu-id="2f1de-199">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-199">String</span></span>|<span data-ttu-id="2f1de-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="2f1de-200">The name of the main Lob application file.</span></span> <span data-ttu-id="2f1de-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2f1de-202">size</span><span class="sxs-lookup"><span data-stu-id="2f1de-202">size</span></span>|<span data-ttu-id="2f1de-203">Int64</span><span class="sxs-lookup"><span data-stu-id="2f1de-203">Int64</span></span>|<span data-ttu-id="2f1de-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="2f1de-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="2f1de-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="2f1de-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="2f1de-206">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="2f1de-206">applicableArchitectures</span></span>|[<span data-ttu-id="2f1de-207">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="2f1de-207">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="2f1de-208">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-208">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="2f1de-209">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="2f1de-209">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="2f1de-210">identityName</span><span class="sxs-lookup"><span data-stu-id="2f1de-210">identityName</span></span>|<span data-ttu-id="2f1de-211">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-211">String</span></span>|<span data-ttu-id="2f1de-212">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="2f1de-212">The Identity Name.</span></span>|
|<span data-ttu-id="2f1de-213">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="2f1de-213">identityPublisherHash</span></span>|<span data-ttu-id="2f1de-214">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-214">String</span></span>|<span data-ttu-id="2f1de-215">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="2f1de-215">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="2f1de-216">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="2f1de-216">identityResourceIdentifier</span></span>|<span data-ttu-id="2f1de-217">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-217">String</span></span>|<span data-ttu-id="2f1de-218">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="2f1de-218">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="2f1de-219">isBundle</span><span class="sxs-lookup"><span data-stu-id="2f1de-219">isBundle</span></span>|<span data-ttu-id="2f1de-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="2f1de-220">Boolean</span></span>|<span data-ttu-id="2f1de-221">Indica si la aplicación es una agrupación.</span><span class="sxs-lookup"><span data-stu-id="2f1de-221">Whether or not the app is a bundle.</span></span>|
|<span data-ttu-id="2f1de-222">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2f1de-222">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="2f1de-223">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2f1de-223">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="2f1de-224">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="2f1de-224">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="2f1de-225">identityVersion</span><span class="sxs-lookup"><span data-stu-id="2f1de-225">identityVersion</span></span>|<span data-ttu-id="2f1de-226">String</span><span class="sxs-lookup"><span data-stu-id="2f1de-226">String</span></span>|<span data-ttu-id="2f1de-227">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="2f1de-227">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="2f1de-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f1de-228">Response</span></span>
<span data-ttu-id="2f1de-229">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsAppX](../resources/intune-apps-windowsappx.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f1de-229">If successful, this method returns a `201 Created` response code and a [windowsAppX](../resources/intune-apps-windowsappx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2f1de-230">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f1de-230">Example</span></span>
### <a name="request"></a><span data-ttu-id="2f1de-231">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2f1de-231">Request</span></span>
<span data-ttu-id="2f1de-232">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f1de-232">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1319

{
  "@odata.type": "#microsoft.graph.windowsAppX",
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

### <a name="response"></a><span data-ttu-id="2f1de-233">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f1de-233">Response</span></span>
<span data-ttu-id="2f1de-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2f1de-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1427

{
  "@odata.type": "#microsoft.graph.windowsAppX",
  "id": "b5179a93-9a93-b517-939a-17b5939a17b5",
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






---
title: Crear vppToken
description: Crea un nuevo objeto vppToken.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 015cb03b806d3cd4fc79f690c4ad5e1aa11a072a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846924"
---
# <a name="create-vpptoken"></a><span data-ttu-id="237fe-103">Crear vppToken</span><span class="sxs-lookup"><span data-stu-id="237fe-103">Create vppToken</span></span>

> <span data-ttu-id="237fe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="237fe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="237fe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="237fe-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="237fe-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="237fe-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="237fe-107">Crea un nuevo objeto [vppToken](../resources/intune-onboarding-vpptoken.md).</span><span class="sxs-lookup"><span data-stu-id="237fe-107">Create a new [vppToken](../resources/intune-onboarding-vpptoken.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="237fe-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="237fe-108">Prerequisites</span></span>
<span data-ttu-id="237fe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="237fe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="237fe-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="237fe-111">Permission type</span></span>|<span data-ttu-id="237fe-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="237fe-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="237fe-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="237fe-113">Delegated (work or school account)</span></span>|<span data-ttu-id="237fe-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="237fe-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="237fe-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="237fe-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="237fe-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="237fe-116">Not supported.</span></span>|
|<span data-ttu-id="237fe-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="237fe-117">Application</span></span>|<span data-ttu-id="237fe-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="237fe-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="237fe-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="237fe-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/vppTokens
```

## <a name="request-headers"></a><span data-ttu-id="237fe-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="237fe-120">Request headers</span></span>
|<span data-ttu-id="237fe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="237fe-121">Header</span></span>|<span data-ttu-id="237fe-122">Valor</span><span class="sxs-lookup"><span data-stu-id="237fe-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="237fe-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="237fe-123">Authorization</span></span>|<span data-ttu-id="237fe-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="237fe-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="237fe-125">Accept</span><span class="sxs-lookup"><span data-stu-id="237fe-125">Accept</span></span>|<span data-ttu-id="237fe-126">application/json</span><span class="sxs-lookup"><span data-stu-id="237fe-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="237fe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="237fe-127">Request body</span></span>
<span data-ttu-id="237fe-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto vppToken.</span><span class="sxs-lookup"><span data-stu-id="237fe-128">In the request body, supply a JSON representation for the vppToken object.</span></span>

<span data-ttu-id="237fe-129">En la tabla siguiente se muestran las propiedades necesarias para crear el vppToken.</span><span class="sxs-lookup"><span data-stu-id="237fe-129">The following table shows the properties that are required when you create the vppToken.</span></span>

|<span data-ttu-id="237fe-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="237fe-130">Property</span></span>|<span data-ttu-id="237fe-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="237fe-131">Type</span></span>|<span data-ttu-id="237fe-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="237fe-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="237fe-133">id</span><span class="sxs-lookup"><span data-stu-id="237fe-133">id</span></span>|<span data-ttu-id="237fe-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="237fe-134">String</span></span>|<span data-ttu-id="237fe-135">Esto se genera automáticamente cuando se crea el appleVolumePurchaseProgramToken.</span><span class="sxs-lookup"><span data-stu-id="237fe-135">This is automatically generated when the appleVolumePurchaseProgramToken is created.</span></span> <span data-ttu-id="237fe-136">Es la clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="237fe-136">It is the Key of the entity.</span></span>|
|<span data-ttu-id="237fe-137">organizationName</span><span class="sxs-lookup"><span data-stu-id="237fe-137">organizationName</span></span>|<span data-ttu-id="237fe-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="237fe-138">String</span></span>|<span data-ttu-id="237fe-139">Organización asociada al token del Programa de Compras por Volumen de Apple</span><span class="sxs-lookup"><span data-stu-id="237fe-139">The organization associated with the Apple Volume Purchase Program Token</span></span>|
|<span data-ttu-id="237fe-140">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="237fe-140">vppTokenAccountType</span></span>|[<span data-ttu-id="237fe-141">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="237fe-141">vppTokenAccountType</span></span>](../resources/intune-shared-vpptokenaccounttype.md)|<span data-ttu-id="237fe-142">Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="237fe-142">The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with.</span></span> <span data-ttu-id="237fe-143">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="237fe-143">Possible values are: `business`, `education`.</span></span> <span data-ttu-id="237fe-144">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="237fe-144">Possible values are: `business`, `education`.</span></span>|
|<span data-ttu-id="237fe-145">Id. de Apple</span><span class="sxs-lookup"><span data-stu-id="237fe-145">appleId</span></span>|<span data-ttu-id="237fe-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="237fe-146">String</span></span>|<span data-ttu-id="237fe-147">Identificador de Apple asociado al token del Programa de compras por volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="237fe-147">The apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="237fe-148">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="237fe-148">expirationDateTime</span></span>|<span data-ttu-id="237fe-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="237fe-149">DateTimeOffset</span></span>|<span data-ttu-id="237fe-150">La fecha y hora de vencimiento del token del Programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="237fe-150">The expiration date time of the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="237fe-151">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="237fe-151">lastSyncDateTime</span></span>|<span data-ttu-id="237fe-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="237fe-152">DateTimeOffset</span></span>|<span data-ttu-id="237fe-153">La última vez que se realizó la sincronización de una aplicación con el servicio del programa de compras por volumen de Apple utilizando el token de ese programa de compras.</span><span class="sxs-lookup"><span data-stu-id="237fe-153">The last time when an application sync was done with the Apple volume purchase program service using the the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="237fe-154">token</span><span class="sxs-lookup"><span data-stu-id="237fe-154">token</span></span>|<span data-ttu-id="237fe-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="237fe-155">String</span></span>|<span data-ttu-id="237fe-156">La cadena del token del programa de compras por volumen de Apple descargada desde ese programa de compras.</span><span class="sxs-lookup"><span data-stu-id="237fe-156">The Apple Volume Purchase Program Token string downloaded from the Apple Volume Purchase Program.</span></span>|
|<span data-ttu-id="237fe-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="237fe-157">lastModifiedDateTime</span></span>|<span data-ttu-id="237fe-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="237fe-158">DateTimeOffset</span></span>|<span data-ttu-id="237fe-159">La fecha y hora de modificación asociada con el token del Programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="237fe-159">Last modification date time associated with the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="237fe-160">estado</span><span class="sxs-lookup"><span data-stu-id="237fe-160">state</span></span>|[<span data-ttu-id="237fe-161">vppTokenState</span><span class="sxs-lookup"><span data-stu-id="237fe-161">vppTokenState</span></span>](../resources/intune-onboarding-vpptokenstate.md)|<span data-ttu-id="237fe-162">Estado actual del token del Programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="237fe-162">Current state of the Apple Volume Purchase Program Token.</span></span> <span data-ttu-id="237fe-163">Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`.</span><span class="sxs-lookup"><span data-stu-id="237fe-163">Possible values are: `unknown`, `valid`, `expired`, `invalid`, `assignedToExternalMDM`.</span></span> <span data-ttu-id="237fe-164">Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`.</span><span class="sxs-lookup"><span data-stu-id="237fe-164">Possible values are: `unknown`, `valid`, `expired`, `invalid`, `assignedToExternalMDM`.</span></span>|
|<span data-ttu-id="237fe-165">tokenActionResults</span><span class="sxs-lookup"><span data-stu-id="237fe-165">tokenActionResults</span></span>|<span data-ttu-id="237fe-166">colección de [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="237fe-166">[vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md) collection</span></span>|<span data-ttu-id="237fe-167">La colección de Estados de las acciones que se realiza en el Token de programa de compra de Apple por volumen.</span><span class="sxs-lookup"><span data-stu-id="237fe-167">The collection of statuses of the actions performed on the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="237fe-168">lastSyncStatus</span><span class="sxs-lookup"><span data-stu-id="237fe-168">lastSyncStatus</span></span>|[<span data-ttu-id="237fe-169">vppTokenSyncStatus</span><span class="sxs-lookup"><span data-stu-id="237fe-169">vppTokenSyncStatus</span></span>](../resources/intune-onboarding-vpptokensyncstatus.md)|<span data-ttu-id="237fe-170">Estado de sincronización actual de la última sincronización de la aplicación que se activó con el Token del programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="237fe-170">Current sync status of the last application sync which was triggered using the Apple Volume Purchase Program Token.</span></span> <span data-ttu-id="237fe-171">Los valores posibles son: `none`, `inProgress`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="237fe-171">Possible values are: `none`, `inProgress`, `completed`, `failed`.</span></span> <span data-ttu-id="237fe-172">Los valores posibles son: `none`, `inProgress`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="237fe-172">Possible values are: `none`, `inProgress`, `completed`, `failed`.</span></span>|
|<span data-ttu-id="237fe-173">automaticallyUpdateApps</span><span class="sxs-lookup"><span data-stu-id="237fe-173">automaticallyUpdateApps</span></span>|<span data-ttu-id="237fe-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="237fe-174">Boolean</span></span>|<span data-ttu-id="237fe-175">Si las aplicaciones para el token VPP se actualizarán automáticamente o no.</span><span class="sxs-lookup"><span data-stu-id="237fe-175">Whether or not apps for the VPP token will be automatically updated.</span></span>|
|<span data-ttu-id="237fe-176">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="237fe-176">countryOrRegion</span></span>|<span data-ttu-id="237fe-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="237fe-177">String</span></span>|<span data-ttu-id="237fe-178">Si las aplicaciones para el token VPP se actualizarán automáticamente o no.</span><span class="sxs-lookup"><span data-stu-id="237fe-178">Whether or not apps for the VPP token will be automatically updated.</span></span>|
|<span data-ttu-id="237fe-179">dataSharingConsentGranted</span><span class="sxs-lookup"><span data-stu-id="237fe-179">dataSharingConsentGranted</span></span>|<span data-ttu-id="237fe-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="237fe-180">Boolean</span></span>|<span data-ttu-id="237fe-181">Concede de consentimiento para uso compartido con el programa de compra de Apple por volumen de datos.</span><span class="sxs-lookup"><span data-stu-id="237fe-181">Consent granted for data sharing with the Apple Volume Purchase Program.</span></span>|
|<span data-ttu-id="237fe-182">displayName</span><span class="sxs-lookup"><span data-stu-id="237fe-182">displayName</span></span>|<span data-ttu-id="237fe-183">Cadena</span><span class="sxs-lookup"><span data-stu-id="237fe-183">String</span></span>|<span data-ttu-id="237fe-184">Un administrador especifica el nombre descriptivo del token.</span><span class="sxs-lookup"><span data-stu-id="237fe-184">An admin specified token friendly name.</span></span>|
|<span data-ttu-id="237fe-185">locationName</span><span class="sxs-lookup"><span data-stu-id="237fe-185">locationName</span></span>|<span data-ttu-id="237fe-186">Cadena</span><span class="sxs-lookup"><span data-stu-id="237fe-186">String</span></span>|<span data-ttu-id="237fe-187">Ubicación de token devuelto desde VPP de Apple.</span><span class="sxs-lookup"><span data-stu-id="237fe-187">Token location returned from Apple VPP.</span></span>|
|<span data-ttu-id="237fe-188">claimTokenManagementFromExternalMdm</span><span class="sxs-lookup"><span data-stu-id="237fe-188">claimTokenManagementFromExternalMdm</span></span>|<span data-ttu-id="237fe-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="237fe-189">Boolean</span></span>|<span data-ttu-id="237fe-190">Administración de consentimiento para permitir que afirma token administración de MDM. externo</span><span class="sxs-lookup"><span data-stu-id="237fe-190">Admin consent to allow claiming token management from external MDM.</span></span>|



## <a name="response"></a><span data-ttu-id="237fe-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="237fe-191">Response</span></span>
<span data-ttu-id="237fe-192">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [vppToken](../resources/intune-onboarding-vpptoken.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="237fe-192">If successful, this method returns a `201 Created` response code and a [vppToken](../resources/intune-onboarding-vpptoken.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="237fe-193">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="237fe-193">Example</span></span>
### <a name="request"></a><span data-ttu-id="237fe-194">Solicitud</span><span class="sxs-lookup"><span data-stu-id="237fe-194">Request</span></span>
<span data-ttu-id="237fe-195">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="237fe-195">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/vppTokens
Content-type: application/json
Content-length: 1004

{
  "@odata.type": "#microsoft.graph.vppToken",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "valid",
  "tokenActionResults": [
    {
      "@odata.type": "microsoft.graph.vppTokenActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value",
  "dataSharingConsentGranted": true,
  "displayName": "Display Name value",
  "locationName": "Location Name value",
  "claimTokenManagementFromExternalMdm": true
}
```

### <a name="response"></a><span data-ttu-id="237fe-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="237fe-196">Response</span></span>
<span data-ttu-id="237fe-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="237fe-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1053

{
  "@odata.type": "#microsoft.graph.vppToken",
  "id": "9ceb2f92-2f92-9ceb-922f-eb9c922feb9c",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "valid",
  "tokenActionResults": [
    {
      "@odata.type": "microsoft.graph.vppTokenActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value",
  "dataSharingConsentGranted": true,
  "displayName": "Display Name value",
  "locationName": "Location Name value",
  "claimTokenManagementFromExternalMdm": true
}
```






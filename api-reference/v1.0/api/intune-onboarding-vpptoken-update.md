---
title: Actualizar vppToken
description: Actualiza las propiedades de un objeto vppToken.
ms.openlocfilehash: 15151f7d5dadfd7cbbdefa088c72f2c70c0bba65
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031758"
---
# <a name="update-vpptoken"></a><span data-ttu-id="39b72-103">Actualizar vppToken</span><span class="sxs-lookup"><span data-stu-id="39b72-103">Update vppToken</span></span>

> <span data-ttu-id="39b72-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39b72-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39b72-105">Actualiza las propiedades de un objeto [vppToken](../resources/intune-onboarding-vpptoken.md).</span><span class="sxs-lookup"><span data-stu-id="39b72-105">Update the properties of a [vppToken](../resources/intune-onboarding-vpptoken.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="39b72-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="39b72-106">Prerequisites</span></span>
<span data-ttu-id="39b72-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39b72-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39b72-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39b72-109">Permission type</span></span>|<span data-ttu-id="39b72-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39b72-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="39b72-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39b72-111">Delegated (work or school account)</span></span>|<span data-ttu-id="39b72-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39b72-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="39b72-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39b72-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="39b72-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39b72-114">Not supported.</span></span>|
|<span data-ttu-id="39b72-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39b72-115">Application</span></span>|<span data-ttu-id="39b72-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39b72-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="39b72-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39b72-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/vppTokens/{vppTokenId}
```

## <a name="request-headers"></a><span data-ttu-id="39b72-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39b72-118">Request headers</span></span>
|<span data-ttu-id="39b72-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39b72-119">Header</span></span>|<span data-ttu-id="39b72-120">Valor</span><span class="sxs-lookup"><span data-stu-id="39b72-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="39b72-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="39b72-121">Authorization</span></span>|<span data-ttu-id="39b72-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="39b72-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="39b72-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="39b72-123">Accept</span></span>|<span data-ttu-id="39b72-124">application/json</span><span class="sxs-lookup"><span data-stu-id="39b72-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="39b72-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39b72-125">Request body</span></span>
<span data-ttu-id="39b72-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [vppToken](../resources/intune-onboarding-vpptoken.md).</span><span class="sxs-lookup"><span data-stu-id="39b72-126">In the request body, supply a JSON representation for the [vppToken](../resources/intune-onboarding-vpptoken.md) object.</span></span>

<span data-ttu-id="39b72-127">En la tabla siguiente se muestran las propiedades necesarias para crear el [vppToken](../resources/intune-onboarding-vpptoken.md).</span><span class="sxs-lookup"><span data-stu-id="39b72-127">The following table shows the properties that are required when you create the [vppToken](../resources/intune-onboarding-vpptoken.md).</span></span>

|<span data-ttu-id="39b72-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39b72-128">Property</span></span>|<span data-ttu-id="39b72-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="39b72-129">Type</span></span>|<span data-ttu-id="39b72-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="39b72-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="39b72-131">id</span><span class="sxs-lookup"><span data-stu-id="39b72-131">id</span></span>|<span data-ttu-id="39b72-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="39b72-132">String</span></span>|<span data-ttu-id="39b72-133">Esto se genera automáticamente cuando se crea el appleVolumePurchaseProgramToken.</span><span class="sxs-lookup"><span data-stu-id="39b72-133">This is automatically generated when the appleVolumePurchaseProgramToken is created.</span></span> <span data-ttu-id="39b72-134">Es la clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="39b72-134">It is the Key of the entity.</span></span>|
|<span data-ttu-id="39b72-135">organizationName</span><span class="sxs-lookup"><span data-stu-id="39b72-135">organizationName</span></span>|<span data-ttu-id="39b72-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="39b72-136">String</span></span>|<span data-ttu-id="39b72-137">Organización asociada al token del Programa de Compras por Volumen de Apple</span><span class="sxs-lookup"><span data-stu-id="39b72-137">The organization associated with the Apple Volume Purchase Program Token</span></span>|
|<span data-ttu-id="39b72-138">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="39b72-138">vppTokenAccountType</span></span>|[<span data-ttu-id="39b72-139">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="39b72-139">vppTokenAccountType</span></span>](../resources/intune-shared-vpptokenaccounttype.md)|<span data-ttu-id="39b72-140">Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="39b72-140">The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with.</span></span> <span data-ttu-id="39b72-141">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="39b72-141">Possible values are: `business`, `education`.</span></span> <span data-ttu-id="39b72-142">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="39b72-142">Possible values are: `business`, `education`.</span></span>|
|<span data-ttu-id="39b72-143">Id. de Apple</span><span class="sxs-lookup"><span data-stu-id="39b72-143">appleId</span></span>|<span data-ttu-id="39b72-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="39b72-144">String</span></span>|<span data-ttu-id="39b72-145">Identificador de Apple asociado al token del Programa de compras por volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="39b72-145">The apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="39b72-146">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="39b72-146">expirationDateTime</span></span>|<span data-ttu-id="39b72-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39b72-147">DateTimeOffset</span></span>|<span data-ttu-id="39b72-148">La fecha y hora de vencimiento del token del Programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="39b72-148">The expiration date time of the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="39b72-149">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="39b72-149">lastSyncDateTime</span></span>|<span data-ttu-id="39b72-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39b72-150">DateTimeOffset</span></span>|<span data-ttu-id="39b72-151">La última vez que se realizó la sincronización de una aplicación con el servicio del programa de compras por volumen de Apple utilizando el token de ese programa de compras.</span><span class="sxs-lookup"><span data-stu-id="39b72-151">The last time when an application sync was done with the Apple volume purchase program service using the the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="39b72-152">token</span><span class="sxs-lookup"><span data-stu-id="39b72-152">token</span></span>|<span data-ttu-id="39b72-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="39b72-153">String</span></span>|<span data-ttu-id="39b72-154">La cadena del token del programa de compras por volumen de Apple descargada desde ese programa de compras.</span><span class="sxs-lookup"><span data-stu-id="39b72-154">The Apple Volume Purchase Program Token string downloaded from the Apple Volume Purchase Program.</span></span>|
|<span data-ttu-id="39b72-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="39b72-155">lastModifiedDateTime</span></span>|<span data-ttu-id="39b72-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39b72-156">DateTimeOffset</span></span>|<span data-ttu-id="39b72-157">La fecha y hora de modificación asociada con el token del Programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="39b72-157">Last modification date time associated with the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="39b72-158">estado</span><span class="sxs-lookup"><span data-stu-id="39b72-158">state</span></span>|[<span data-ttu-id="39b72-159">vppTokenState</span><span class="sxs-lookup"><span data-stu-id="39b72-159">vppTokenState</span></span>](../resources/intune-onboarding-vpptokenstate.md)|<span data-ttu-id="39b72-160">Estado actual del token del Programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="39b72-160">Current state of the Apple Volume Purchase Program Token.</span></span> <span data-ttu-id="39b72-161">Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`.</span><span class="sxs-lookup"><span data-stu-id="39b72-161">Possible values are: `unknown`, `valid`, `expired`, `invalid`, `assignedToExternalMDM`.</span></span> <span data-ttu-id="39b72-162">Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`.</span><span class="sxs-lookup"><span data-stu-id="39b72-162">Possible values are: `unknown`, `valid`, `expired`, `invalid`, `assignedToExternalMDM`.</span></span>|
|<span data-ttu-id="39b72-163">lastSyncStatus</span><span class="sxs-lookup"><span data-stu-id="39b72-163">lastSyncStatus</span></span>|[<span data-ttu-id="39b72-164">vppTokenSyncStatus</span><span class="sxs-lookup"><span data-stu-id="39b72-164">vppTokenSyncStatus</span></span>](../resources/intune-onboarding-vpptokensyncstatus.md)|<span data-ttu-id="39b72-165">Estado de sincronización actual de la última sincronización de la aplicación que se activó con el Token del programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="39b72-165">Current sync status of the last application sync which was triggered using the Apple Volume Purchase Program Token.</span></span> <span data-ttu-id="39b72-166">Los valores posibles son: `none`, `inProgress`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="39b72-166">Possible values are: `none`, `inProgress`, `completed`, `failed`.</span></span> <span data-ttu-id="39b72-167">Los valores posibles son: `none`, `inProgress`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="39b72-167">Possible values are: `none`, `inProgress`, `completed`, `failed`.</span></span>|
|<span data-ttu-id="39b72-168">automaticallyUpdateApps</span><span class="sxs-lookup"><span data-stu-id="39b72-168">automaticallyUpdateApps</span></span>|<span data-ttu-id="39b72-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="39b72-169">Boolean</span></span>|<span data-ttu-id="39b72-170">Si las aplicaciones para el token VPP se actualizarán automáticamente o no.</span><span class="sxs-lookup"><span data-stu-id="39b72-170">Whether or not apps for the VPP token will be automatically updated.</span></span>|
|<span data-ttu-id="39b72-171">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="39b72-171">countryOrRegion</span></span>|<span data-ttu-id="39b72-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="39b72-172">String</span></span>|<span data-ttu-id="39b72-173">Si las aplicaciones para el token VPP se actualizarán automáticamente o no.</span><span class="sxs-lookup"><span data-stu-id="39b72-173">Whether or not apps for the VPP token will be automatically updated.</span></span>|



## <a name="response"></a><span data-ttu-id="39b72-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39b72-174">Response</span></span>
<span data-ttu-id="39b72-175">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [vppToken](../resources/intune-onboarding-vpptoken.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39b72-175">If successful, this method returns a `200 OK` response code and an updated [vppToken](../resources/intune-onboarding-vpptoken.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="39b72-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39b72-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="39b72-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39b72-177">Request</span></span>
<span data-ttu-id="39b72-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39b72-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/vppTokens/{vppTokenId}
Content-type: application/json
Content-length: 461

{
  "@odata.type": "#microsoft.graph.vppToken",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "state": "valid",
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value"
}
```

### <a name="response"></a><span data-ttu-id="39b72-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39b72-179">Response</span></span>
<span data-ttu-id="39b72-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39b72-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 574

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
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value"
}
```




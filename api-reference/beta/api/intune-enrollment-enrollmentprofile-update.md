---
title: Actualizar enrollmentProfile
description: Actualizar las propiedades de un objeto enrollmentProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a642ab15427f29cec3a7535022135f9cc931856e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924254"
---
# <a name="update-enrollmentprofile"></a><span data-ttu-id="5f20b-103">Actualizar enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="5f20b-103">Update enrollmentProfile</span></span>

> <span data-ttu-id="5f20b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f20b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5f20b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f20b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5f20b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5f20b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5f20b-107">Actualizar las propiedades de un objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="5f20b-107">Update the properties of a [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5f20b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5f20b-108">Prerequisites</span></span>
<span data-ttu-id="5f20b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f20b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5f20b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f20b-111">Permission type</span></span>|<span data-ttu-id="5f20b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f20b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5f20b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f20b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5f20b-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f20b-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="5f20b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f20b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5f20b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f20b-116">Not supported.</span></span>|
|<span data-ttu-id="5f20b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f20b-117">Application</span></span>|<span data-ttu-id="5f20b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f20b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5f20b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f20b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}
```

## <a name="request-headers"></a><span data-ttu-id="5f20b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f20b-120">Request headers</span></span>
|<span data-ttu-id="5f20b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f20b-121">Header</span></span>|<span data-ttu-id="5f20b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5f20b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5f20b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5f20b-123">Authorization</span></span>|<span data-ttu-id="5f20b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5f20b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5f20b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="5f20b-125">Accept</span></span>|<span data-ttu-id="5f20b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5f20b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5f20b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f20b-127">Request body</span></span>
<span data-ttu-id="5f20b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="5f20b-128">In the request body, supply a JSON representation for the [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>

<span data-ttu-id="5f20b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="5f20b-129">The following table shows the properties that are required when you create the [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md).</span></span>

|<span data-ttu-id="5f20b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f20b-130">Property</span></span>|<span data-ttu-id="5f20b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f20b-131">Type</span></span>|<span data-ttu-id="5f20b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f20b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5f20b-133">id</span><span class="sxs-lookup"><span data-stu-id="5f20b-133">id</span></span>|<span data-ttu-id="5f20b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f20b-134">String</span></span>|<span data-ttu-id="5f20b-135">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="5f20b-135">The GUID for the object</span></span>|
|<span data-ttu-id="5f20b-136">displayName</span><span class="sxs-lookup"><span data-stu-id="5f20b-136">displayName</span></span>|<span data-ttu-id="5f20b-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f20b-137">String</span></span>|<span data-ttu-id="5f20b-138">Nombre del perfil</span><span class="sxs-lookup"><span data-stu-id="5f20b-138">Name of the profile</span></span>|
|<span data-ttu-id="5f20b-139">descripción</span><span class="sxs-lookup"><span data-stu-id="5f20b-139">description</span></span>|<span data-ttu-id="5f20b-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f20b-140">String</span></span>|<span data-ttu-id="5f20b-141">Descripción del perfil</span><span class="sxs-lookup"><span data-stu-id="5f20b-141">Description of the profile</span></span>|
|<span data-ttu-id="5f20b-142">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="5f20b-142">requiresUserAuthentication</span></span>|<span data-ttu-id="5f20b-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f20b-143">Boolean</span></span>|<span data-ttu-id="5f20b-144">Indica si el perfil requiere autenticación de usuario</span><span class="sxs-lookup"><span data-stu-id="5f20b-144">Indicates if the profile requires user authentication</span></span>|
|<span data-ttu-id="5f20b-145">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5f20b-145">configurationEndpointUrl</span></span>|<span data-ttu-id="5f20b-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f20b-146">String</span></span>|<span data-ttu-id="5f20b-147">Dirección url de extremo de configuración que se usará para inscripción</span><span class="sxs-lookup"><span data-stu-id="5f20b-147">Configuration endpoint url to use for Enrollment</span></span>|
|<span data-ttu-id="5f20b-148">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="5f20b-148">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="5f20b-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f20b-149">Boolean</span></span>|<span data-ttu-id="5f20b-150">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="5f20b-150">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span>|



## <a name="response"></a><span data-ttu-id="5f20b-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f20b-151">Response</span></span>
<span data-ttu-id="5f20b-152">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f20b-152">If successful, this method returns a `200 OK` response code and an updated [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5f20b-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f20b-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="5f20b-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f20b-154">Request</span></span>
<span data-ttu-id="5f20b-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f20b-155">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}
Content-type: application/json
Content-length: 250

{
  "displayName": "Display Name value",
  "description": "Description value",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
  "enableAuthenticationViaCompanyPortal": true
}
```

### <a name="response"></a><span data-ttu-id="5f20b-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f20b-156">Response</span></span>
<span data-ttu-id="5f20b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5f20b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 355

{
  "@odata.type": "#microsoft.graph.enrollmentProfile",
  "id": "012d8d5e-8d5e-012d-5e8d-2d015e8d2d01",
  "displayName": "Display Name value",
  "description": "Description value",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
  "enableAuthenticationViaCompanyPortal": true
}
```






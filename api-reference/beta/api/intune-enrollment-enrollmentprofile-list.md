---
title: Lista enrollmentProfiles
description: Propiedades de la lista y relaciones de los objetos enrollmentProfile.
ms.openlocfilehash: 8053cacd1f0f1e6f6335cc08675d8c38c5068ad5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090089"
---
# <a name="list-enrollmentprofiles"></a><span data-ttu-id="28878-103">Lista enrollmentProfiles</span><span class="sxs-lookup"><span data-stu-id="28878-103">List enrollmentProfiles</span></span>

> <span data-ttu-id="28878-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="28878-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="28878-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="28878-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="28878-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="28878-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="28878-107">Propiedades de la lista y relaciones de los objetos [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="28878-107">List properties and relationships of the [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="28878-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="28878-108">Prerequisites</span></span>
<span data-ttu-id="28878-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="28878-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="28878-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="28878-111">Permission type</span></span>|<span data-ttu-id="28878-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="28878-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="28878-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="28878-113">Delegated (work or school account)</span></span>|<span data-ttu-id="28878-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="28878-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="28878-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="28878-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="28878-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28878-116">Not supported.</span></span>|
|<span data-ttu-id="28878-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="28878-117">Application</span></span>|<span data-ttu-id="28878-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28878-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="28878-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="28878-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="28878-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="28878-120">Request headers</span></span>
|<span data-ttu-id="28878-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28878-121">Header</span></span>|<span data-ttu-id="28878-122">Valor</span><span class="sxs-lookup"><span data-stu-id="28878-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="28878-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="28878-123">Authorization</span></span>|<span data-ttu-id="28878-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="28878-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="28878-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="28878-125">Accept</span></span>|<span data-ttu-id="28878-126">application/json</span><span class="sxs-lookup"><span data-stu-id="28878-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="28878-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="28878-127">Request body</span></span>
<span data-ttu-id="28878-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="28878-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="28878-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28878-129">Response</span></span>
<span data-ttu-id="28878-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28878-130">If successful, this method returns a `200 OK` response code and a collection of [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="28878-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28878-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="28878-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="28878-132">Request</span></span>
<span data-ttu-id="28878-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="28878-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

### <a name="response"></a><span data-ttu-id="28878-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28878-134">Response</span></span>
<span data-ttu-id="28878-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="28878-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 416

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.enrollmentProfile",
      "id": "012d8d5e-8d5e-012d-5e8d-2d015e8d2d01",
      "displayName": "Display Name value",
      "description": "Description value",
      "requiresUserAuthentication": true,
      "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
      "enableAuthenticationViaCompanyPortal": true
    }
  ]
}
```





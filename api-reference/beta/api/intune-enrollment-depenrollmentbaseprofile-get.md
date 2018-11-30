---
title: Obtener depEnrollmentBaseProfile
description: Leer las propiedades y las relaciones del objeto depEnrollmentBaseProfile.
ms.openlocfilehash: 16c80005587691a819595672f2b4e0f104c8215f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086716"
---
# <a name="get-depenrollmentbaseprofile"></a><span data-ttu-id="a4247-103">Obtener depEnrollmentBaseProfile</span><span class="sxs-lookup"><span data-stu-id="a4247-103">Get depEnrollmentBaseProfile</span></span>

> <span data-ttu-id="a4247-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a4247-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a4247-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a4247-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a4247-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a4247-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a4247-107">Leer las propiedades y las relaciones del objeto [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a4247-107">Read properties and relationships of the [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a4247-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a4247-108">Prerequisites</span></span>
<span data-ttu-id="a4247-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a4247-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a4247-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4247-111">Permission type</span></span>|<span data-ttu-id="a4247-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4247-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a4247-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4247-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a4247-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="a4247-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="a4247-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4247-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a4247-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4247-116">Not supported.</span></span>|
|<span data-ttu-id="a4247-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4247-117">Application</span></span>|<span data-ttu-id="a4247-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4247-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a4247-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4247-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a4247-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a4247-120">Optional query parameters</span></span>
<span data-ttu-id="a4247-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4247-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a4247-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4247-122">Request headers</span></span>
|<span data-ttu-id="a4247-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4247-123">Header</span></span>|<span data-ttu-id="a4247-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a4247-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a4247-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="a4247-125">Authorization</span></span>|<span data-ttu-id="a4247-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a4247-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a4247-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a4247-127">Accept</span></span>|<span data-ttu-id="a4247-128">application/json</span><span class="sxs-lookup"><span data-stu-id="a4247-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a4247-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4247-129">Request body</span></span>
<span data-ttu-id="a4247-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a4247-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a4247-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4247-131">Response</span></span>
<span data-ttu-id="a4247-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4247-132">If successful, this method returns a `200 OK` response code and [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4247-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4247-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="a4247-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4247-134">Request</span></span>
<span data-ttu-id="a4247-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4247-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}
```

### <a name="response"></a><span data-ttu-id="a4247-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4247-136">Response</span></span>
<span data-ttu-id="a4247-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a4247-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 940

{
  "value": {
    "@odata.type": "#microsoft.graph.depEnrollmentBaseProfile",
    "id": "db378868-8868-db37-6888-37db688837db",
    "displayName": "Display Name value",
    "description": "Description value",
    "requiresUserAuthentication": true,
    "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
    "enableAuthenticationViaCompanyPortal": true,
    "isDefault": true,
    "supervisedModeEnabled": true,
    "supportDepartment": "Support Department value",
    "passCodeDisabled": true,
    "isMandatory": true,
    "locationDisabled": true,
    "supportPhoneNumber": "Support Phone Number value",
    "profileRemovalDisabled": true,
    "restoreBlocked": true,
    "appleIdDisabled": true,
    "termsAndConditionsDisabled": true,
    "touchIdDisabled": true,
    "applePayDisabled": true,
    "zoomDisabled": true,
    "siriDisabled": true,
    "diagnosticsDisabled": true
  }
}
```






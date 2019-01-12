---
title: Obtener windows10CompliancePolicy
description: Lea las propiedades y las relaciones del objeto windows10CompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fa842853be69fb932107f9e57906c149641246c1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920782"
---
# <a name="get-windows10compliancepolicy"></a><span data-ttu-id="1ff7d-103">Obtener windows10CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="1ff7d-103">Get windows10CompliancePolicy</span></span>

> <span data-ttu-id="1ff7d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1ff7d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1ff7d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1ff7d-107">Lea las propiedades y las relaciones del objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1ff7d-107">Read properties and relationships of the [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1ff7d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1ff7d-108">Prerequisites</span></span>
<span data-ttu-id="1ff7d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1ff7d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1ff7d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1ff7d-111">Permission type</span></span>|<span data-ttu-id="1ff7d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1ff7d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1ff7d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1ff7d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1ff7d-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1ff7d-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="1ff7d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1ff7d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1ff7d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-116">Not supported.</span></span>|
|<span data-ttu-id="1ff7d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1ff7d-117">Application</span></span>|<span data-ttu-id="1ff7d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1ff7d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ff7d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="1ff7d-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1ff7d-120">Optional query parameters</span></span>
<span data-ttu-id="1ff7d-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1ff7d-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ff7d-122">Request headers</span></span>
|<span data-ttu-id="1ff7d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ff7d-123">Header</span></span>|<span data-ttu-id="1ff7d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1ff7d-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1ff7d-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="1ff7d-125">Authorization</span></span>|<span data-ttu-id="1ff7d-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1ff7d-127">Accept</span><span class="sxs-lookup"><span data-stu-id="1ff7d-127">Accept</span></span>|<span data-ttu-id="1ff7d-128">application/json</span><span class="sxs-lookup"><span data-stu-id="1ff7d-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1ff7d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1ff7d-129">Request body</span></span>
<span data-ttu-id="1ff7d-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1ff7d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ff7d-131">Response</span></span>
<span data-ttu-id="1ff7d-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-132">If successful, this method returns a `200 OK` response code and [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1ff7d-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ff7d-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="1ff7d-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ff7d-134">Request</span></span>
<span data-ttu-id="1ff7d-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

### <a name="response"></a><span data-ttu-id="1ff7d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ff7d-136">Response</span></span>
<span data-ttu-id="1ff7d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1ff7d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1951

{
  "value": {
    "@odata.type": "#microsoft.graph.windows10CompliancePolicy",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "id": "2919ae62-ae62-2919-62ae-192962ae1929",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "version": 7,
    "passwordRequired": true,
    "passwordBlockSimple": true,
    "passwordRequiredToUnlockFromIdle": true,
    "passwordMinutesOfInactivityBeforeLock": 5,
    "passwordExpirationDays": 6,
    "passwordMinimumLength": 5,
    "passwordMinimumCharacterSetCount": 0,
    "passwordRequiredType": "alphanumeric",
    "passwordPreviousPasswordBlockCount": 2,
    "requireHealthyDeviceReport": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value",
    "mobileOsMinimumVersion": "Mobile Os Minimum Version value",
    "mobileOsMaximumVersion": "Mobile Os Maximum Version value",
    "earlyLaunchAntiMalwareDriverEnabled": true,
    "bitLockerEnabled": true,
    "secureBootEnabled": true,
    "codeIntegrityEnabled": true,
    "storageRequireEncryption": true,
    "activeFirewallRequired": true,
    "defenderEnabled": true,
    "defenderVersion": "Defender Version value",
    "signatureOutOfDate": true,
    "rtpEnabled": true,
    "antivirusRequired": true,
    "antiSpywareRequired": true,
    "validOperatingSystemBuildRanges": [
      {
        "@odata.type": "microsoft.graph.operatingSystemVersionRange",
        "description": "Description value",
        "lowestVersion": "Lowest Version value",
        "highestVersion": "Highest Version value"
      }
    ],
    "deviceThreatProtectionEnabled": true,
    "deviceThreatProtectionRequiredSecurityLevel": "secured",
    "configurationManagerComplianceRequired": true
  }
}
```






---
title: Obtener iosCompliancePolicy
description: Lea las propiedades y las relaciones del objeto iosCompliancePolicy.
ms.openlocfilehash: f78d3a123286bc6b49624c275c1901d030833fd2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087238"
---
# <a name="get-ioscompliancepolicy"></a><span data-ttu-id="5b4cc-103">Obtener iosCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="5b4cc-103">Get iosCompliancePolicy</span></span>

> <span data-ttu-id="5b4cc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5b4cc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5b4cc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5b4cc-107">Lea las propiedades y las relaciones del objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5b4cc-107">Read properties and relationships of the [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5b4cc-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5b4cc-108">Prerequisites</span></span>
<span data-ttu-id="5b4cc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5b4cc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5b4cc-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5b4cc-111">Permission type</span></span>|<span data-ttu-id="5b4cc-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5b4cc-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5b4cc-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5b4cc-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5b4cc-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="5b4cc-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="5b4cc-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5b4cc-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5b4cc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-116">Not supported.</span></span>|
|<span data-ttu-id="5b4cc-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5b4cc-117">Application</span></span>|<span data-ttu-id="5b4cc-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5b4cc-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5b4cc-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="5b4cc-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5b4cc-120">Optional query parameters</span></span>
<span data-ttu-id="5b4cc-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="5b4cc-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5b4cc-122">Request headers</span></span>
|<span data-ttu-id="5b4cc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b4cc-123">Header</span></span>|<span data-ttu-id="5b4cc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5b4cc-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5b4cc-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="5b4cc-125">Authorization</span></span>|<span data-ttu-id="5b4cc-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5b4cc-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5b4cc-127">Accept</span></span>|<span data-ttu-id="5b4cc-128">application/json</span><span class="sxs-lookup"><span data-stu-id="5b4cc-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5b4cc-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5b4cc-129">Request body</span></span>
<span data-ttu-id="5b4cc-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5b4cc-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b4cc-131">Response</span></span>
<span data-ttu-id="5b4cc-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-132">If successful, this method returns a `200 OK` response code and [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5b4cc-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b4cc-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="5b4cc-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5b4cc-134">Request</span></span>
<span data-ttu-id="5b4cc-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

### <a name="response"></a><span data-ttu-id="5b4cc-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b4cc-136">Response</span></span>
<span data-ttu-id="5b4cc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1376

{
  "value": {
    "@odata.type": "#microsoft.graph.iosCompliancePolicy",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "id": "4f501351-1351-4f50-5113-504f5113504f",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "version": 7,
    "passcodeBlockSimple": true,
    "passcodeExpirationDays": 6,
    "passcodeMinimumLength": 5,
    "passcodeMinutesOfInactivityBeforeLock": 5,
    "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
    "passcodePreviousPasscodeBlockCount": 2,
    "passcodeMinimumCharacterSetCount": 0,
    "passcodeRequiredType": "alphanumeric",
    "passcodeRequired": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value",
    "securityBlockJailbrokenDevices": true,
    "deviceThreatProtectionEnabled": true,
    "deviceThreatProtectionRequiredSecurityLevel": "secured",
    "managedEmailProfileRequired": true,
    "restrictedApps": [
      {
        "@odata.type": "microsoft.graph.appListItem",
        "name": "Name value",
        "publisher": "Publisher value",
        "appStoreUrl": "https://example.com/appStoreUrl/",
        "appId": "App Id value"
      }
    ]
  }
}
```





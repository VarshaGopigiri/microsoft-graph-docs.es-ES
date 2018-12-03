---
title: Enumerar windows81CompliancePolicies
description: Enumere las propiedades y las relaciones de los objetos windows81CompliancePolicy.
ms.openlocfilehash: 2bca199a6b87d300763cdf66a83c472e5fcfd950
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086736"
---
# <a name="list-windows81compliancepolicies"></a><span data-ttu-id="cff04-103">Enumerar windows81CompliancePolicies</span><span class="sxs-lookup"><span data-stu-id="cff04-103">List windows81CompliancePolicies</span></span>

> <span data-ttu-id="cff04-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cff04-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cff04-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cff04-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cff04-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cff04-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cff04-107">Enumere las propiedades y las relaciones de los objetos [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="cff04-107">List properties and relationships of the [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cff04-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cff04-108">Prerequisites</span></span>
<span data-ttu-id="cff04-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cff04-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cff04-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cff04-111">Permission type</span></span>|<span data-ttu-id="cff04-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cff04-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cff04-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cff04-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cff04-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="cff04-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="cff04-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cff04-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cff04-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cff04-116">Not supported.</span></span>|
|<span data-ttu-id="cff04-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cff04-117">Application</span></span>|<span data-ttu-id="cff04-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cff04-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cff04-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cff04-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="cff04-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cff04-120">Request headers</span></span>
|<span data-ttu-id="cff04-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cff04-121">Header</span></span>|<span data-ttu-id="cff04-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cff04-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cff04-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="cff04-123">Authorization</span></span>|<span data-ttu-id="cff04-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cff04-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cff04-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cff04-125">Accept</span></span>|<span data-ttu-id="cff04-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cff04-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cff04-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cff04-127">Request body</span></span>
<span data-ttu-id="cff04-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cff04-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cff04-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cff04-129">Response</span></span>
<span data-ttu-id="cff04-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cff04-130">If successful, this method returns a `200 OK` response code and a collection of [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cff04-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cff04-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="cff04-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cff04-132">Request</span></span>
<span data-ttu-id="cff04-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cff04-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies
```

### <a name="response"></a><span data-ttu-id="cff04-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cff04-134">Response</span></span>
<span data-ttu-id="cff04-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cff04-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 953

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windows81CompliancePolicy",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "id": "6bb4b7e0-b7e0-6bb4-e0b7-b46be0b7b46b",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "displayName": "Display Name value",
      "version": 7,
      "passwordRequired": true,
      "passwordBlockSimple": true,
      "passwordExpirationDays": 6,
      "passwordMinimumLength": 5,
      "passwordMinutesOfInactivityBeforeLock": 5,
      "passwordMinimumCharacterSetCount": 0,
      "passwordRequiredType": "alphanumeric",
      "passwordPreviousPasswordBlockCount": 2,
      "osMinimumVersion": "Os Minimum Version value",
      "osMaximumVersion": "Os Maximum Version value",
      "storageRequireEncryption": true
    }
  ]
}
```





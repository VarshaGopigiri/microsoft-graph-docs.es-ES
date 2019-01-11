---
title: Lista advancedThreatProtectionOnboardingDeviceSettingStates
description: Propiedades de la lista y relaciones de los objetos advancedThreatProtectionOnboardingDeviceSettingState.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d238b10cc9b40a6ae590617213521f067c3acc4b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854617"
---
# <a name="list-advancedthreatprotectiononboardingdevicesettingstates"></a><span data-ttu-id="2487b-103">Lista advancedThreatProtectionOnboardingDeviceSettingStates</span><span class="sxs-lookup"><span data-stu-id="2487b-103">List advancedThreatProtectionOnboardingDeviceSettingStates</span></span>

> <span data-ttu-id="2487b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2487b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2487b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2487b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2487b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2487b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2487b-107">Propiedades de la lista y relaciones de los objetos [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) .</span><span class="sxs-lookup"><span data-stu-id="2487b-107">List properties and relationships of the [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2487b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2487b-108">Prerequisites</span></span>
<span data-ttu-id="2487b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2487b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2487b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2487b-111">Permission type</span></span>|<span data-ttu-id="2487b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2487b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2487b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2487b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2487b-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="2487b-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="2487b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2487b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2487b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2487b-116">Not supported.</span></span>|
|<span data-ttu-id="2487b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2487b-117">Application</span></span>|<span data-ttu-id="2487b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2487b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2487b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2487b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/advancedThreatProtectionOnboardingStateSummary/advancedThreatProtectionOnboardingDeviceSettingStates
```

## <a name="request-headers"></a><span data-ttu-id="2487b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2487b-120">Request headers</span></span>
|<span data-ttu-id="2487b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2487b-121">Header</span></span>|<span data-ttu-id="2487b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2487b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2487b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2487b-123">Authorization</span></span>|<span data-ttu-id="2487b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2487b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2487b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="2487b-125">Accept</span></span>|<span data-ttu-id="2487b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2487b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2487b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2487b-127">Request body</span></span>
<span data-ttu-id="2487b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2487b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2487b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2487b-129">Response</span></span>
<span data-ttu-id="2487b-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2487b-130">If successful, this method returns a `200 OK` response code and a collection of [advancedThreatProtectionOnboardingDeviceSettingState](../resources/intune-deviceconfig-advancedthreatprotectiononboardingdevicesettingstate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2487b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2487b-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="2487b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2487b-132">Request</span></span>
<span data-ttu-id="2487b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2487b-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/advancedThreatProtectionOnboardingStateSummary/advancedThreatProtectionOnboardingDeviceSettingStates
```

### <a name="response"></a><span data-ttu-id="2487b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2487b-134">Response</span></span>
<span data-ttu-id="2487b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2487b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 711

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.advancedThreatProtectionOnboardingDeviceSettingState",
      "id": "63593fc6-3fc6-6359-c63f-5963c63f5963",
      "platformType": "windowsRT",
      "setting": "Setting value",
      "settingName": "Setting Name value",
      "deviceId": "Device Id value",
      "deviceName": "Device Name value",
      "userId": "User Id value",
      "userEmail": "User Email value",
      "userName": "User Name value",
      "userPrincipalName": "User Principal Name value",
      "deviceModel": "Device Model value",
      "state": "notApplicable",
      "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
    }
  ]
}
```






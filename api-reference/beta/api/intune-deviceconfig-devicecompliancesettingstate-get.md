---
title: Obtener deviceComplianceSettingState
description: Lea las propiedades y las relaciones del objeto deviceComplianceSettingState.
author: tfitzmac
ms.openlocfilehash: 2dca82a54cacb55e08dad5028377f53dba1204f9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307367"
---
# <a name="get-devicecompliancesettingstate"></a><span data-ttu-id="b391f-103">Obtener deviceComplianceSettingState</span><span class="sxs-lookup"><span data-stu-id="b391f-103">Get deviceComplianceSettingState</span></span>

> <span data-ttu-id="b391f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b391f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b391f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b391f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b391f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b391f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b391f-107">Lea las propiedades y las relaciones del objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="b391f-107">Read properties and relationships of the [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b391f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b391f-108">Prerequisites</span></span>
<span data-ttu-id="b391f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b391f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b391f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b391f-111">Permission type</span></span>|<span data-ttu-id="b391f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b391f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b391f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b391f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b391f-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="b391f-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="b391f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b391f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b391f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b391f-116">Not supported.</span></span>|
|<span data-ttu-id="b391f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b391f-117">Application</span></span>|<span data-ttu-id="b391f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b391f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b391f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b391f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates/{deviceComplianceSettingStateId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b391f-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b391f-120">Optional query parameters</span></span>
<span data-ttu-id="b391f-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b391f-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b391f-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b391f-122">Request headers</span></span>
|<span data-ttu-id="b391f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b391f-123">Header</span></span>|<span data-ttu-id="b391f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b391f-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b391f-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="b391f-125">Authorization</span></span>|<span data-ttu-id="b391f-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b391f-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b391f-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b391f-127">Accept</span></span>|<span data-ttu-id="b391f-128">application/json</span><span class="sxs-lookup"><span data-stu-id="b391f-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b391f-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b391f-129">Request body</span></span>
<span data-ttu-id="b391f-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b391f-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b391f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b391f-131">Response</span></span>
<span data-ttu-id="b391f-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b391f-132">If successful, this method returns a `200 OK` response code and [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b391f-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b391f-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="b391f-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b391f-134">Request</span></span>
<span data-ttu-id="b391f-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b391f-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates/{deviceComplianceSettingStateId}
```

### <a name="response"></a><span data-ttu-id="b391f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b391f-136">Response</span></span>
<span data-ttu-id="b391f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b391f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 645

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
    "id": "9905f955-f955-9905-55f9-059955f90599",
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
}
```






---
title: Obtener advancedThreatProtectionOnboardingStateSummary
description: Leer las propiedades y las relaciones del objeto advancedThreatProtectionOnboardingStateSummary.
author: tfitzmac
ms.openlocfilehash: 51cfc20a38e1b594b3fd983b481cf124e9e88455
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347554"
---
# <a name="get-advancedthreatprotectiononboardingstatesummary"></a><span data-ttu-id="0a401-103">Obtener advancedThreatProtectionOnboardingStateSummary</span><span class="sxs-lookup"><span data-stu-id="0a401-103">Get advancedThreatProtectionOnboardingStateSummary</span></span>

> <span data-ttu-id="0a401-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0a401-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0a401-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0a401-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0a401-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0a401-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0a401-107">Leer las propiedades y las relaciones del objeto [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) .</span><span class="sxs-lookup"><span data-stu-id="0a401-107">Read properties and relationships of the [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0a401-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0a401-108">Prerequisites</span></span>
<span data-ttu-id="0a401-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0a401-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0a401-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0a401-111">Permission type</span></span>|<span data-ttu-id="0a401-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0a401-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0a401-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0a401-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0a401-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="0a401-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="0a401-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0a401-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0a401-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a401-116">Not supported.</span></span>|
|<span data-ttu-id="0a401-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0a401-117">Application</span></span>|<span data-ttu-id="0a401-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a401-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0a401-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a401-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/advancedThreatProtectionOnboardingStateSummary
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0a401-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0a401-120">Optional query parameters</span></span>
<span data-ttu-id="0a401-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a401-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="0a401-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a401-122">Request headers</span></span>
|<span data-ttu-id="0a401-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a401-123">Header</span></span>|<span data-ttu-id="0a401-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0a401-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0a401-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="0a401-125">Authorization</span></span>|<span data-ttu-id="0a401-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0a401-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0a401-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0a401-127">Accept</span></span>|<span data-ttu-id="0a401-128">application/json</span><span class="sxs-lookup"><span data-stu-id="0a401-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0a401-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a401-129">Request body</span></span>
<span data-ttu-id="0a401-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0a401-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0a401-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a401-131">Response</span></span>
<span data-ttu-id="0a401-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a401-132">If successful, this method returns a `200 OK` response code and [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a401-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a401-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="0a401-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a401-134">Request</span></span>
<span data-ttu-id="0a401-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a401-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/advancedThreatProtectionOnboardingStateSummary
```

### <a name="response"></a><span data-ttu-id="0a401-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a401-136">Response</span></span>
<span data-ttu-id="0a401-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a401-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 419

{
  "value": {
    "@odata.type": "#microsoft.graph.advancedThreatProtectionOnboardingStateSummary",
    "id": "74089602-9602-7408-0296-087402960874",
    "unknownDeviceCount": 2,
    "notApplicableDeviceCount": 8,
    "compliantDeviceCount": 4,
    "remediatedDeviceCount": 5,
    "nonCompliantDeviceCount": 7,
    "errorDeviceCount": 0,
    "conflictDeviceCount": 3,
    "notAssignedDeviceCount": 6
  }
}
```






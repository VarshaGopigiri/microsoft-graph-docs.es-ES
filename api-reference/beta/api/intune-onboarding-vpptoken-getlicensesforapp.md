---
title: getLicensesForApp (función)
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 20b4e17645e86a630b2f07f97ccd27fa47f84539
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327884"
---
# <a name="getlicensesforapp-function"></a><span data-ttu-id="a9219-103">getLicensesForApp (función)</span><span class="sxs-lookup"><span data-stu-id="a9219-103">getLicensesForApp function</span></span>

> <span data-ttu-id="a9219-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a9219-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a9219-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a9219-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a9219-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a9219-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a9219-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a9219-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a9219-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a9219-108">Prerequisites</span></span>
<span data-ttu-id="a9219-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a9219-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a9219-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a9219-111">Permission type</span></span>|<span data-ttu-id="a9219-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a9219-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a9219-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a9219-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a9219-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="a9219-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="a9219-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a9219-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a9219-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a9219-116">Not supported.</span></span>|
|<span data-ttu-id="a9219-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a9219-117">Application</span></span>|<span data-ttu-id="a9219-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a9219-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a9219-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a9219-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/vppTokens/getLicensesForApp
```

## <a name="request-headers"></a><span data-ttu-id="a9219-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a9219-120">Request headers</span></span>
|<span data-ttu-id="a9219-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9219-121">Header</span></span>|<span data-ttu-id="a9219-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a9219-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a9219-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a9219-123">Authorization</span></span>|<span data-ttu-id="a9219-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a9219-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a9219-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a9219-125">Accept</span></span>|<span data-ttu-id="a9219-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a9219-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a9219-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a9219-127">Request body</span></span>
<span data-ttu-id="a9219-128">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="a9219-128">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="a9219-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="a9219-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="a9219-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a9219-130">Property</span></span>|<span data-ttu-id="a9219-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9219-131">Type</span></span>|<span data-ttu-id="a9219-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9219-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a9219-133">bundleId</span><span class="sxs-lookup"><span data-stu-id="a9219-133">bundleId</span></span>|<span data-ttu-id="a9219-134">String</span><span class="sxs-lookup"><span data-stu-id="a9219-134">String</span></span>|<span data-ttu-id="a9219-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a9219-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="a9219-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a9219-136">Response</span></span>
<span data-ttu-id="a9219-137">Si tiene éxito, esta función devuelve una `200 OK` código de respuesta y una colección de [vppTokenLicenseSummary](../resources/intune-onboarding-vpptokenlicensesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9219-137">If successful, this function returns a `200 OK` response code and a [vppTokenLicenseSummary](../resources/intune-onboarding-vpptokenlicensesummary.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a9219-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a9219-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="a9219-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a9219-139">Request</span></span>
<span data-ttu-id="a9219-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9219-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/vppTokens/getLicensesForApp(bundleId='parameterValue')
```

### <a name="response"></a><span data-ttu-id="a9219-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a9219-141">Response</span></span>
<span data-ttu-id="a9219-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a9219-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 298

{
  "value": [
    {
      "@odata.type": "microsoft.graph.vppTokenLicenseSummary",
      "vppTokenId": "Vpp Token Id value",
      "appleId": "Apple Id value",
      "organizationName": "Organization Name value",
      "availableLicenseCount": 5,
      "usedLicenseCount": 0
    }
  ]
}
```






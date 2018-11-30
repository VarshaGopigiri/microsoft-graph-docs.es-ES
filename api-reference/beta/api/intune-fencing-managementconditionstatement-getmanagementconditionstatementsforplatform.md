---
title: getManagementConditionStatementsForPlatform (función)
description: Todavía no documentado
ms.openlocfilehash: d2855d7707cb8f1083f736c2a50d92e40e5d0278
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089649"
---
# <a name="getmanagementconditionstatementsforplatform-function"></a><span data-ttu-id="65198-103">getManagementConditionStatementsForPlatform (función)</span><span class="sxs-lookup"><span data-stu-id="65198-103">getManagementConditionStatementsForPlatform function</span></span>

> <span data-ttu-id="65198-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="65198-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="65198-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="65198-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="65198-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="65198-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="65198-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="65198-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="65198-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="65198-108">Prerequisites</span></span>
<span data-ttu-id="65198-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="65198-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="65198-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65198-111">Permission type</span></span>|<span data-ttu-id="65198-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65198-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="65198-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="65198-113">Delegated (work or school account)</span></span>|<span data-ttu-id="65198-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="65198-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="65198-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="65198-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="65198-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65198-116">Not supported.</span></span>|
|<span data-ttu-id="65198-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="65198-117">Application</span></span>|<span data-ttu-id="65198-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65198-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="65198-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65198-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/managementConditionStatements/getManagementConditionStatementsForPlatform
GET /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/getManagementConditionStatementsForPlatform
```

## <a name="request-headers"></a><span data-ttu-id="65198-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="65198-120">Request headers</span></span>
|<span data-ttu-id="65198-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65198-121">Header</span></span>|<span data-ttu-id="65198-122">Valor</span><span class="sxs-lookup"><span data-stu-id="65198-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="65198-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="65198-123">Authorization</span></span>|<span data-ttu-id="65198-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="65198-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="65198-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="65198-125">Accept</span></span>|<span data-ttu-id="65198-126">application/json</span><span class="sxs-lookup"><span data-stu-id="65198-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="65198-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="65198-127">Request body</span></span>
<span data-ttu-id="65198-128">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="65198-128">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="65198-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="65198-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="65198-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="65198-130">Property</span></span>|<span data-ttu-id="65198-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="65198-131">Type</span></span>|<span data-ttu-id="65198-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="65198-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="65198-133">platform</span><span class="sxs-lookup"><span data-stu-id="65198-133">platform</span></span>|[<span data-ttu-id="65198-134">devicePlatformType</span><span class="sxs-lookup"><span data-stu-id="65198-134">devicePlatformType</span></span>](../resources/intune-shared-deviceplatformtype.md)|<span data-ttu-id="65198-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="65198-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="65198-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65198-136">Response</span></span>
<span data-ttu-id="65198-137">Si tiene éxito, esta función devuelve una `200 OK` código de respuesta y una colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65198-137">If successful, this function returns a `200 OK` response code and a [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="65198-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65198-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="65198-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="65198-139">Request</span></span>
<span data-ttu-id="65198-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="65198-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/managementConditionStatements/getManagementConditionStatementsForPlatform(platform='parameterValue')
```

### <a name="response"></a><span data-ttu-id="65198-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65198-141">Response</span></span>
<span data-ttu-id="65198-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="65198-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 576

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managementConditionStatement",
      "id": "bedb0c00-0c00-bedb-000c-dbbe000cdbbe",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
      "expression": {
        "@odata.type": "microsoft.graph.managementConditionExpression"
      },
      "eTag": "ETag value",
      "applicablePlatforms": [
        "androidForWork"
      ]
    }
  ]
}
```





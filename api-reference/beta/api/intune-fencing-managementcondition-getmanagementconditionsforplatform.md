---
title: getManagementConditionsForPlatform (función)
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: d0d36750f568102a69309615285c7460aa31aec3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320037"
---
# <a name="getmanagementconditionsforplatform-function"></a><span data-ttu-id="3714a-103">getManagementConditionsForPlatform (función)</span><span class="sxs-lookup"><span data-stu-id="3714a-103">getManagementConditionsForPlatform function</span></span>

> <span data-ttu-id="3714a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3714a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3714a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3714a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3714a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3714a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3714a-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3714a-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3714a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3714a-108">Prerequisites</span></span>
<span data-ttu-id="3714a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3714a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3714a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3714a-111">Permission type</span></span>|<span data-ttu-id="3714a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3714a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3714a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3714a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3714a-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="3714a-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="3714a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3714a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3714a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3714a-116">Not supported.</span></span>|
|<span data-ttu-id="3714a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3714a-117">Application</span></span>|<span data-ttu-id="3714a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3714a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3714a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3714a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/managementConditions/getManagementConditionsForPlatform
GET /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions/getManagementConditionsForPlatform
```

## <a name="request-headers"></a><span data-ttu-id="3714a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3714a-120">Request headers</span></span>
|<span data-ttu-id="3714a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3714a-121">Header</span></span>|<span data-ttu-id="3714a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3714a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3714a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3714a-123">Authorization</span></span>|<span data-ttu-id="3714a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3714a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3714a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3714a-125">Accept</span></span>|<span data-ttu-id="3714a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3714a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3714a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3714a-127">Request body</span></span>
<span data-ttu-id="3714a-128">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="3714a-128">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="3714a-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="3714a-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="3714a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3714a-130">Property</span></span>|<span data-ttu-id="3714a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3714a-131">Type</span></span>|<span data-ttu-id="3714a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3714a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3714a-133">platform</span><span class="sxs-lookup"><span data-stu-id="3714a-133">platform</span></span>|[<span data-ttu-id="3714a-134">devicePlatformType</span><span class="sxs-lookup"><span data-stu-id="3714a-134">devicePlatformType</span></span>](../resources/intune-shared-deviceplatformtype.md)|<span data-ttu-id="3714a-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3714a-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="3714a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3714a-136">Response</span></span>
<span data-ttu-id="3714a-137">Si tiene éxito, esta función devuelve una `200 OK` código de respuesta y una colección de [managementCondition](../resources/intune-fencing-managementcondition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3714a-137">If successful, this function returns a `200 OK` response code and a [managementCondition](../resources/intune-fencing-managementcondition.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3714a-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3714a-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="3714a-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3714a-139">Request</span></span>
<span data-ttu-id="3714a-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3714a-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/managementConditions/getManagementConditionsForPlatform(platform='parameterValue')
```

### <a name="response"></a><span data-ttu-id="3714a-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3714a-141">Response</span></span>
<span data-ttu-id="3714a-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3714a-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 504

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managementCondition",
      "id": "5cb49381-9381-5cb4-8193-b45c8193b45c",
      "uniqueName": "Unique Name value",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
      "eTag": "ETag value",
      "applicablePlatforms": [
        "androidForWork"
      ]
    }
  ]
}
```






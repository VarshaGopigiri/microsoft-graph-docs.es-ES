---
title: Obtener managementCondition
description: Leer las propiedades y las relaciones del objeto managementCondition.
author: tfitzmac
ms.openlocfilehash: ead4d2643644c79f84704b87c3a71d0d302ebd0a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330964"
---
# <a name="get-managementcondition"></a><span data-ttu-id="13f7e-103">Obtener managementCondition</span><span class="sxs-lookup"><span data-stu-id="13f7e-103">Get managementCondition</span></span>

> <span data-ttu-id="13f7e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="13f7e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="13f7e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="13f7e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="13f7e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="13f7e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="13f7e-107">Leer las propiedades y las relaciones del objeto [managementCondition](../resources/intune-fencing-managementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="13f7e-107">Read properties and relationships of the [managementCondition](../resources/intune-fencing-managementcondition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="13f7e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="13f7e-108">Prerequisites</span></span>
<span data-ttu-id="13f7e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="13f7e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="13f7e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="13f7e-111">Permission type</span></span>|<span data-ttu-id="13f7e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="13f7e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="13f7e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="13f7e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="13f7e-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="13f7e-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="13f7e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="13f7e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="13f7e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13f7e-116">Not supported.</span></span>|
|<span data-ttu-id="13f7e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="13f7e-117">Application</span></span>|<span data-ttu-id="13f7e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13f7e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="13f7e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="13f7e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/managementConditions/{managementConditionId}
GET /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions/{managementConditionId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="13f7e-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="13f7e-120">Optional query parameters</span></span>
<span data-ttu-id="13f7e-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13f7e-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="13f7e-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="13f7e-122">Request headers</span></span>
|<span data-ttu-id="13f7e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13f7e-123">Header</span></span>|<span data-ttu-id="13f7e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="13f7e-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="13f7e-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="13f7e-125">Authorization</span></span>|<span data-ttu-id="13f7e-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="13f7e-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="13f7e-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="13f7e-127">Accept</span></span>|<span data-ttu-id="13f7e-128">application/json</span><span class="sxs-lookup"><span data-stu-id="13f7e-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="13f7e-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="13f7e-129">Request body</span></span>
<span data-ttu-id="13f7e-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="13f7e-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="13f7e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13f7e-131">Response</span></span>
<span data-ttu-id="13f7e-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [managementCondition](../resources/intune-fencing-managementcondition.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13f7e-132">If successful, this method returns a `200 OK` response code and [managementCondition](../resources/intune-fencing-managementcondition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="13f7e-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13f7e-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="13f7e-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="13f7e-134">Request</span></span>
<span data-ttu-id="13f7e-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13f7e-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/managementConditions/{managementConditionId}
```

### <a name="response"></a><span data-ttu-id="13f7e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13f7e-136">Response</span></span>
<span data-ttu-id="13f7e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="13f7e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 468

{
  "value": {
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
}
```






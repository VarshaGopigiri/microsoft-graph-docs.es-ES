---
title: Lista managementConditions
description: Propiedades de la lista y relaciones de los objetos managementCondition.
ms.openlocfilehash: b9d7665e803c0102447d9a59ca43e3be2e1dcf7d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088179"
---
# <a name="list-managementconditions"></a><span data-ttu-id="9d406-103">Lista managementConditions</span><span class="sxs-lookup"><span data-stu-id="9d406-103">List managementConditions</span></span>

> <span data-ttu-id="9d406-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9d406-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9d406-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9d406-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9d406-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9d406-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9d406-107">Propiedades de la lista y relaciones de los objetos [managementCondition](../resources/intune-fencing-managementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="9d406-107">List properties and relationships of the [managementCondition](../resources/intune-fencing-managementcondition.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9d406-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9d406-108">Prerequisites</span></span>
<span data-ttu-id="9d406-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9d406-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9d406-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9d406-111">Permission type</span></span>|<span data-ttu-id="9d406-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9d406-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9d406-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9d406-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9d406-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="9d406-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="9d406-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9d406-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9d406-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d406-116">Not supported.</span></span>|
|<span data-ttu-id="9d406-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9d406-117">Application</span></span>|<span data-ttu-id="9d406-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d406-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9d406-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9d406-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/managementConditions
GET /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions
```

## <a name="request-headers"></a><span data-ttu-id="9d406-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9d406-120">Request headers</span></span>
|<span data-ttu-id="9d406-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d406-121">Header</span></span>|<span data-ttu-id="9d406-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9d406-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9d406-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9d406-123">Authorization</span></span>|<span data-ttu-id="9d406-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9d406-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9d406-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9d406-125">Accept</span></span>|<span data-ttu-id="9d406-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9d406-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9d406-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9d406-127">Request body</span></span>
<span data-ttu-id="9d406-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9d406-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9d406-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d406-129">Response</span></span>
<span data-ttu-id="9d406-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [managementCondition](../resources/intune-fencing-managementcondition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d406-130">If successful, this method returns a `200 OK` response code and a collection of [managementCondition](../resources/intune-fencing-managementcondition.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9d406-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d406-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="9d406-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9d406-132">Request</span></span>
<span data-ttu-id="9d406-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d406-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/managementConditions
```

### <a name="response"></a><span data-ttu-id="9d406-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d406-134">Response</span></span>
<span data-ttu-id="9d406-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9d406-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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






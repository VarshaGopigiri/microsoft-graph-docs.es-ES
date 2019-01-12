---
title: Eliminar deviceComplianceDeviceStatus
description: Elimina un deviceComplianceDeviceStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9b0fea8b7dd792cae2309977055784ed7f9360bf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950511"
---
# <a name="delete-devicecompliancedevicestatus"></a><span data-ttu-id="30385-103">Eliminar deviceComplianceDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="30385-103">Delete deviceComplianceDeviceStatus</span></span>

> <span data-ttu-id="30385-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="30385-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="30385-105">Elimina un [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="30385-105">Deletes a [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="30385-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="30385-106">Prerequisites</span></span>
<span data-ttu-id="30385-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="30385-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="30385-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30385-109">Permission type</span></span>|<span data-ttu-id="30385-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30385-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="30385-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30385-111">Delegated (work or school account)</span></span>|<span data-ttu-id="30385-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="30385-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="30385-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30385-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="30385-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30385-114">Not supported.</span></span>|
|<span data-ttu-id="30385-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30385-115">Application</span></span>|<span data-ttu-id="30385-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="30385-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="30385-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30385-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatuses/{deviceComplianceDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="30385-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30385-118">Request headers</span></span>
|<span data-ttu-id="30385-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30385-119">Header</span></span>|<span data-ttu-id="30385-120">Valor</span><span class="sxs-lookup"><span data-stu-id="30385-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="30385-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="30385-121">Authorization</span></span>|<span data-ttu-id="30385-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="30385-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="30385-123">Accept</span><span class="sxs-lookup"><span data-stu-id="30385-123">Accept</span></span>|<span data-ttu-id="30385-124">application/json</span><span class="sxs-lookup"><span data-stu-id="30385-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="30385-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30385-125">Request body</span></span>
<span data-ttu-id="30385-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="30385-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="30385-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30385-127">Response</span></span>
<span data-ttu-id="30385-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="30385-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="30385-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30385-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="30385-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30385-130">Request</span></span>
<span data-ttu-id="30385-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30385-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatuses/{deviceComplianceDeviceStatusId}
```

### <a name="response"></a><span data-ttu-id="30385-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30385-132">Response</span></span>
<span data-ttu-id="30385-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="30385-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




---
title: Eliminar deviceComplianceSettingState
description: Elimina un deviceComplianceSettingState.
author: tfitzmac
ms.openlocfilehash: f1b2f45b8da823505d7c51dc9a6b3193dd209351
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339777"
---
# <a name="delete-devicecompliancesettingstate"></a><span data-ttu-id="a7736-103">Eliminar deviceComplianceSettingState</span><span class="sxs-lookup"><span data-stu-id="a7736-103">Delete deviceComplianceSettingState</span></span>

> <span data-ttu-id="a7736-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a7736-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a7736-105">Elimina un [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="a7736-105">Deletes a [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a7736-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a7736-106">Prerequisites</span></span>
<span data-ttu-id="a7736-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7736-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a7736-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7736-109">Permission type</span></span>|<span data-ttu-id="a7736-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7736-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a7736-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7736-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a7736-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a7736-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a7736-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7736-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a7736-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7736-114">Not supported.</span></span>|
|<span data-ttu-id="a7736-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7736-115">Application</span></span>|<span data-ttu-id="a7736-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7736-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a7736-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7736-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates/{deviceComplianceSettingStateId}
```

## <a name="request-headers"></a><span data-ttu-id="a7736-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7736-118">Request headers</span></span>
|<span data-ttu-id="a7736-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7736-119">Header</span></span>|<span data-ttu-id="a7736-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a7736-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a7736-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="a7736-121">Authorization</span></span>|<span data-ttu-id="a7736-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a7736-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a7736-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a7736-123">Accept</span></span>|<span data-ttu-id="a7736-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a7736-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a7736-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7736-125">Request body</span></span>
<span data-ttu-id="a7736-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a7736-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a7736-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7736-127">Response</span></span>
<span data-ttu-id="a7736-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a7736-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="a7736-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7736-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="a7736-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7736-130">Request</span></span>
<span data-ttu-id="a7736-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7736-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates/{deviceComplianceSettingStateId}
```

### <a name="response"></a><span data-ttu-id="a7736-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7736-132">Response</span></span>
<span data-ttu-id="a7736-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7736-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




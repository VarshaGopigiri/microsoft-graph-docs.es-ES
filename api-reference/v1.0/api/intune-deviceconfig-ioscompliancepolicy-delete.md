---
title: Eliminar iosCompliancePolicy
description: Elimina un iosCompliancePolicy.
author: tfitzmac
ms.openlocfilehash: 4a36a5e3a272fb3983153d9739ecc894decbab59
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321458"
---
# <a name="delete-ioscompliancepolicy"></a><span data-ttu-id="dfe15-103">Eliminar iosCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="dfe15-103">Delete iosCompliancePolicy</span></span>

> <span data-ttu-id="dfe15-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dfe15-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dfe15-105">Elimina un [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="dfe15-105">Deletes a [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dfe15-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dfe15-106">Prerequisites</span></span>
<span data-ttu-id="dfe15-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dfe15-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dfe15-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dfe15-109">Permission type</span></span>|<span data-ttu-id="dfe15-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dfe15-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dfe15-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dfe15-111">Delegated (work or school account)</span></span>|<span data-ttu-id="dfe15-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dfe15-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="dfe15-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dfe15-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dfe15-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dfe15-114">Not supported.</span></span>|
|<span data-ttu-id="dfe15-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dfe15-115">Application</span></span>|<span data-ttu-id="dfe15-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dfe15-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dfe15-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dfe15-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="dfe15-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dfe15-118">Request headers</span></span>
|<span data-ttu-id="dfe15-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfe15-119">Header</span></span>|<span data-ttu-id="dfe15-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dfe15-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dfe15-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="dfe15-121">Authorization</span></span>|<span data-ttu-id="dfe15-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dfe15-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dfe15-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="dfe15-123">Accept</span></span>|<span data-ttu-id="dfe15-124">application/json</span><span class="sxs-lookup"><span data-stu-id="dfe15-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dfe15-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dfe15-125">Request body</span></span>
<span data-ttu-id="dfe15-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dfe15-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dfe15-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dfe15-127">Response</span></span>
<span data-ttu-id="dfe15-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="dfe15-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="dfe15-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dfe15-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="dfe15-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dfe15-130">Request</span></span>
<span data-ttu-id="dfe15-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dfe15-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

### <a name="response"></a><span data-ttu-id="dfe15-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dfe15-132">Response</span></span>
<span data-ttu-id="dfe15-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dfe15-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




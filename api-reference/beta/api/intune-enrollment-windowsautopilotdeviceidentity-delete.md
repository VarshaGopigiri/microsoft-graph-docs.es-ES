---
title: Eliminar windowsAutopilotDeviceIdentity
description: Elimina un windowsAutopilotDeviceIdentity.
author: tfitzmac
ms.openlocfilehash: 5194536ef6526714819ee676ef063997b1a39895
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304280"
---
# <a name="delete-windowsautopilotdeviceidentity"></a><span data-ttu-id="2b415-103">Eliminar windowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="2b415-103">Delete windowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="2b415-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2b415-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2b415-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2b415-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2b415-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2b415-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2b415-107">Elimina un [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="2b415-107">Deletes a [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2b415-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2b415-108">Prerequisites</span></span>
<span data-ttu-id="2b415-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2b415-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2b415-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2b415-111">Permission type</span></span>|<span data-ttu-id="2b415-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2b415-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2b415-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2b415-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2b415-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2b415-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="2b415-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2b415-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2b415-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b415-116">Not supported.</span></span>|
|<span data-ttu-id="2b415-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2b415-117">Application</span></span>|<span data-ttu-id="2b415-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b415-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2b415-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b415-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}
DELETE /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/assignedDevices/{windowsAutopilotDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="2b415-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b415-120">Request headers</span></span>
|<span data-ttu-id="2b415-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b415-121">Header</span></span>|<span data-ttu-id="2b415-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2b415-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2b415-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2b415-123">Authorization</span></span>|<span data-ttu-id="2b415-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2b415-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2b415-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2b415-125">Accept</span></span>|<span data-ttu-id="2b415-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2b415-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2b415-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2b415-127">Request body</span></span>
<span data-ttu-id="2b415-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2b415-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2b415-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b415-129">Response</span></span>
<span data-ttu-id="2b415-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="2b415-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="2b415-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b415-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="2b415-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b415-132">Request</span></span>
<span data-ttu-id="2b415-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b415-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}
```

### <a name="response"></a><span data-ttu-id="2b415-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b415-134">Response</span></span>
<span data-ttu-id="2b415-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b415-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






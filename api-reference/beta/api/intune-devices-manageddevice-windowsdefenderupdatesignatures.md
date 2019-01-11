---
title: Acción windowsDefenderUpdateSignatures
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 67679db941bdeb92098d3fa9113730ff13f505e5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827947"
---
# <a name="windowsdefenderupdatesignatures-action"></a><span data-ttu-id="fd47a-103">Acción windowsDefenderUpdateSignatures</span><span class="sxs-lookup"><span data-stu-id="fd47a-103">windowsDefenderUpdateSignatures action</span></span>

> <span data-ttu-id="fd47a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fd47a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fd47a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fd47a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fd47a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fd47a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fd47a-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fd47a-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fd47a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fd47a-108">Prerequisites</span></span>
<span data-ttu-id="fd47a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fd47a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fd47a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fd47a-111">Permission type</span></span>|<span data-ttu-id="fd47a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fd47a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fd47a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fd47a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="fd47a-114">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="fd47a-114">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="fd47a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fd47a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fd47a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd47a-116">Not supported.</span></span>|
|<span data-ttu-id="fd47a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fd47a-117">Application</span></span>|<span data-ttu-id="fd47a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd47a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fd47a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fd47a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/windowsDefenderUpdateSignatures
POST /deviceManagement/managedDevices/{managedDeviceId}/windowsDefenderUpdateSignatures
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/windowsDefenderUpdateSignatures
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/windowsDefenderUpdateSignatures
```

## <a name="request-headers"></a><span data-ttu-id="fd47a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fd47a-120">Request headers</span></span>
|<span data-ttu-id="fd47a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd47a-121">Header</span></span>|<span data-ttu-id="fd47a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fd47a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fd47a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="fd47a-123">Authorization</span></span>|<span data-ttu-id="fd47a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fd47a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fd47a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="fd47a-125">Accept</span></span>|<span data-ttu-id="fd47a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="fd47a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fd47a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fd47a-127">Request body</span></span>
<span data-ttu-id="fd47a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fd47a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fd47a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd47a-129">Response</span></span>
<span data-ttu-id="fd47a-130">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="fd47a-130">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="fd47a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fd47a-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="fd47a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fd47a-132">Request</span></span>
<span data-ttu-id="fd47a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fd47a-133">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/managedDevices/{managedDeviceId}/windowsDefenderUpdateSignatures
```

### <a name="response"></a><span data-ttu-id="fd47a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd47a-134">Response</span></span>
<span data-ttu-id="fd47a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fd47a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






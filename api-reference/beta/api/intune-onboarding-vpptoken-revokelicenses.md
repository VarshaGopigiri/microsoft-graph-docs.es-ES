---
title: acción revokeLicenses
description: Revocar licencias asociadas con un appleVolumePurchaseProgramToken específico
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b5817fabfc7a7b414b816c76e059d9cedd2243a2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975438"
---
# <a name="revokelicenses-action"></a><span data-ttu-id="f8c32-103">acción revokeLicenses</span><span class="sxs-lookup"><span data-stu-id="f8c32-103">revokeLicenses action</span></span>

> <span data-ttu-id="f8c32-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f8c32-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f8c32-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f8c32-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f8c32-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f8c32-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f8c32-107">Revocar licencias asociadas con un appleVolumePurchaseProgramToken específico</span><span class="sxs-lookup"><span data-stu-id="f8c32-107">Revoke licenses associated with a specific appleVolumePurchaseProgramToken</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f8c32-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f8c32-108">Prerequisites</span></span>
<span data-ttu-id="f8c32-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f8c32-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f8c32-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f8c32-111">Permission type</span></span>|<span data-ttu-id="f8c32-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f8c32-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f8c32-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f8c32-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f8c32-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f8c32-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="f8c32-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f8c32-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f8c32-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8c32-116">Not supported.</span></span>|
|<span data-ttu-id="f8c32-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f8c32-117">Application</span></span>|<span data-ttu-id="f8c32-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8c32-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f8c32-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f8c32-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/vppTokens/{vppTokenId}/revokeLicenses
```

## <a name="request-headers"></a><span data-ttu-id="f8c32-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f8c32-120">Request headers</span></span>
|<span data-ttu-id="f8c32-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8c32-121">Header</span></span>|<span data-ttu-id="f8c32-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f8c32-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f8c32-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f8c32-123">Authorization</span></span>|<span data-ttu-id="f8c32-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f8c32-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f8c32-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f8c32-125">Accept</span></span>|<span data-ttu-id="f8c32-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f8c32-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f8c32-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f8c32-127">Request body</span></span>
<span data-ttu-id="f8c32-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="f8c32-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="f8c32-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="f8c32-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="f8c32-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8c32-130">Property</span></span>|<span data-ttu-id="f8c32-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8c32-131">Type</span></span>|<span data-ttu-id="f8c32-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8c32-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f8c32-133">notifyManagedDevices</span><span class="sxs-lookup"><span data-stu-id="f8c32-133">notifyManagedDevices</span></span>|<span data-ttu-id="f8c32-134">Booleano</span><span class="sxs-lookup"><span data-stu-id="f8c32-134">Boolean</span></span>|<span data-ttu-id="f8c32-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f8c32-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="f8c32-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8c32-136">Response</span></span>
<span data-ttu-id="f8c32-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f8c32-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f8c32-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8c32-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="f8c32-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8c32-139">Request</span></span>
<span data-ttu-id="f8c32-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8c32-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/vppTokens/{vppTokenId}/revokeLicenses

Content-type: application/json
Content-length: 36

{
  "notifyManagedDevices": true
}
```

### <a name="response"></a><span data-ttu-id="f8c32-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8c32-141">Response</span></span>
<span data-ttu-id="f8c32-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f8c32-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






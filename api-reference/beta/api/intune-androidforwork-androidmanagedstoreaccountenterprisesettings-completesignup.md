---
title: Acción completeSignup
description: Todavía no documentado
ms.openlocfilehash: 0e3b317b67fd23ea536eab60156976ff2f88f971
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083569"
---
# <a name="completesignup-action"></a><span data-ttu-id="13652-103">Acción completeSignup</span><span class="sxs-lookup"><span data-stu-id="13652-103">completeSignup action</span></span>

> <span data-ttu-id="13652-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="13652-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="13652-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="13652-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="13652-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="13652-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="13652-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="13652-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="13652-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="13652-108">Prerequisites</span></span>
<span data-ttu-id="13652-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="13652-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="13652-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="13652-111">Permission type</span></span>|<span data-ttu-id="13652-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="13652-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="13652-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="13652-113">Delegated (work or school account)</span></span>|<span data-ttu-id="13652-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13652-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="13652-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="13652-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="13652-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13652-116">Not supported.</span></span>|
|<span data-ttu-id="13652-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="13652-117">Application</span></span>|<span data-ttu-id="13652-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13652-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="13652-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="13652-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/androidManagedStoreAccountEnterpriseSettings/completeSignup
```

## <a name="request-headers"></a><span data-ttu-id="13652-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="13652-120">Request headers</span></span>
|<span data-ttu-id="13652-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13652-121">Header</span></span>|<span data-ttu-id="13652-122">Valor</span><span class="sxs-lookup"><span data-stu-id="13652-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="13652-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="13652-123">Authorization</span></span>|<span data-ttu-id="13652-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="13652-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="13652-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="13652-125">Accept</span></span>|<span data-ttu-id="13652-126">application/json</span><span class="sxs-lookup"><span data-stu-id="13652-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="13652-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="13652-127">Request body</span></span>
<span data-ttu-id="13652-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="13652-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="13652-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="13652-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="13652-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13652-130">Property</span></span>|<span data-ttu-id="13652-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="13652-131">Type</span></span>|<span data-ttu-id="13652-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="13652-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="13652-133">enterpriseToken</span><span class="sxs-lookup"><span data-stu-id="13652-133">enterpriseToken</span></span>|<span data-ttu-id="13652-134">String</span><span class="sxs-lookup"><span data-stu-id="13652-134">String</span></span>|<span data-ttu-id="13652-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="13652-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="13652-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13652-136">Response</span></span>
<span data-ttu-id="13652-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="13652-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="13652-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13652-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="13652-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="13652-139">Request</span></span>
<span data-ttu-id="13652-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13652-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/androidManagedStoreAccountEnterpriseSettings/completeSignup

Content-type: application/json
Content-length: 51

{
  "enterpriseToken": "Enterprise Token value"
}
```

### <a name="response"></a><span data-ttu-id="13652-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13652-141">Response</span></span>
<span data-ttu-id="13652-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="13652-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






---
title: Acción requestSignupUrl
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 901d0bb67fa5992aa0931afc70660c22cd5ffeca
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980044"
---
# <a name="requestsignupurl-action"></a><span data-ttu-id="a2a5f-103">Acción requestSignupUrl</span><span class="sxs-lookup"><span data-stu-id="a2a5f-103">requestSignupUrl action</span></span>

> <span data-ttu-id="a2a5f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2a5f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a2a5f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2a5f-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a2a5f-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a2a5f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a2a5f-108">Prerequisites</span></span>
<span data-ttu-id="a2a5f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2a5f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a2a5f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2a5f-111">Permission type</span></span>|<span data-ttu-id="a2a5f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2a5f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a2a5f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2a5f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a2a5f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a2a5f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a2a5f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2a5f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a2a5f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-116">Not supported.</span></span>|
|<span data-ttu-id="a2a5f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2a5f-117">Application</span></span>|<span data-ttu-id="a2a5f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a2a5f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2a5f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/androidForWorkSettings/requestSignupUrl
```

## <a name="request-headers"></a><span data-ttu-id="a2a5f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2a5f-120">Request headers</span></span>
|<span data-ttu-id="a2a5f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2a5f-121">Header</span></span>|<span data-ttu-id="a2a5f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a2a5f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a2a5f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a2a5f-123">Authorization</span></span>|<span data-ttu-id="a2a5f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a2a5f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a2a5f-125">Accept</span></span>|<span data-ttu-id="a2a5f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a2a5f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a2a5f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2a5f-127">Request body</span></span>
<span data-ttu-id="a2a5f-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="a2a5f-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="a2a5f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2a5f-130">Property</span></span>|<span data-ttu-id="a2a5f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2a5f-131">Type</span></span>|<span data-ttu-id="a2a5f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2a5f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a2a5f-133">hostName</span><span class="sxs-lookup"><span data-stu-id="a2a5f-133">hostName</span></span>|<span data-ttu-id="a2a5f-134">String</span><span class="sxs-lookup"><span data-stu-id="a2a5f-134">String</span></span>|<span data-ttu-id="a2a5f-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a2a5f-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="a2a5f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2a5f-136">Response</span></span>
<span data-ttu-id="a2a5f-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y un objeto String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-137">If successful, this action returns a `200 OK` response code and a String in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a2a5f-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2a5f-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="a2a5f-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2a5f-139">Request</span></span>
<span data-ttu-id="a2a5f-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/androidForWorkSettings/requestSignupUrl

Content-type: application/json
Content-length: 37

{
  "hostName": "Host Name value"
}
```

### <a name="response"></a><span data-ttu-id="a2a5f-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2a5f-141">Response</span></span>
<span data-ttu-id="a2a5f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2a5f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 56

{
  "value": "https://example.com/requestSignupUrl/"
}
```






---
title: Acción requestSignupUrl
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 5a6e057842befe22dd2ad7035a76d013aca45e4e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336046"
---
# <a name="requestsignupurl-action"></a><span data-ttu-id="9f479-103">Acción requestSignupUrl</span><span class="sxs-lookup"><span data-stu-id="9f479-103">requestSignupUrl action</span></span>

> <span data-ttu-id="9f479-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9f479-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9f479-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9f479-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9f479-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9f479-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9f479-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9f479-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9f479-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9f479-108">Prerequisites</span></span>
<span data-ttu-id="9f479-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9f479-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9f479-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9f479-111">Permission type</span></span>|<span data-ttu-id="9f479-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9f479-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9f479-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9f479-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9f479-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9f479-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9f479-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9f479-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9f479-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f479-116">Not supported.</span></span>|
|<span data-ttu-id="9f479-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9f479-117">Application</span></span>|<span data-ttu-id="9f479-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f479-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9f479-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9f479-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/androidForWorkSettings/requestSignupUrl
```

## <a name="request-headers"></a><span data-ttu-id="9f479-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f479-120">Request headers</span></span>
|<span data-ttu-id="9f479-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f479-121">Header</span></span>|<span data-ttu-id="9f479-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9f479-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9f479-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9f479-123">Authorization</span></span>|<span data-ttu-id="9f479-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9f479-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9f479-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9f479-125">Accept</span></span>|<span data-ttu-id="9f479-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9f479-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9f479-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9f479-127">Request body</span></span>
<span data-ttu-id="9f479-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="9f479-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="9f479-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="9f479-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="9f479-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f479-130">Property</span></span>|<span data-ttu-id="9f479-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f479-131">Type</span></span>|<span data-ttu-id="9f479-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f479-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9f479-133">hostName</span><span class="sxs-lookup"><span data-stu-id="9f479-133">hostName</span></span>|<span data-ttu-id="9f479-134">String</span><span class="sxs-lookup"><span data-stu-id="9f479-134">String</span></span>|<span data-ttu-id="9f479-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9f479-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="9f479-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f479-136">Response</span></span>
<span data-ttu-id="9f479-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y un objeto String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f479-137">If successful, this action returns a `200 OK` response code and a String in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9f479-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f479-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="9f479-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9f479-139">Request</span></span>
<span data-ttu-id="9f479-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9f479-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/androidForWorkSettings/requestSignupUrl

Content-type: application/json
Content-length: 37

{
  "hostName": "Host Name value"
}
```

### <a name="response"></a><span data-ttu-id="9f479-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f479-141">Response</span></span>
<span data-ttu-id="9f479-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9f479-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 56

{
  "value": "https://example.com/requestSignupUrl/"
}
```






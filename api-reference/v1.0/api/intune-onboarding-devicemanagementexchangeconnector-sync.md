---
title: Acción de sincronización
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b66bfb3dbdc9c262788b92992c946b7d7589bf57
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884283"
---
# <a name="sync-action"></a><span data-ttu-id="7e758-103">Acción de sincronización</span><span class="sxs-lookup"><span data-stu-id="7e758-103">sync action</span></span>

> <span data-ttu-id="7e758-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7e758-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7e758-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7e758-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7e758-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7e758-106">Prerequisites</span></span>
<span data-ttu-id="7e758-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7e758-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7e758-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7e758-109">Permission type</span></span>|<span data-ttu-id="7e758-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7e758-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7e758-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7e758-111">Delegated (work or school account)</span></span>|<span data-ttu-id="7e758-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7e758-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="7e758-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7e758-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7e758-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e758-114">Not supported.</span></span>|
|<span data-ttu-id="7e758-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7e758-115">Application</span></span>|<span data-ttu-id="7e758-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e758-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7e758-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7e758-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}/sync
```

## <a name="request-headers"></a><span data-ttu-id="7e758-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e758-118">Request headers</span></span>
|<span data-ttu-id="7e758-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e758-119">Header</span></span>|<span data-ttu-id="7e758-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7e758-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7e758-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="7e758-121">Authorization</span></span>|<span data-ttu-id="7e758-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7e758-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7e758-123">Accept</span><span class="sxs-lookup"><span data-stu-id="7e758-123">Accept</span></span>|<span data-ttu-id="7e758-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7e758-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7e758-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7e758-125">Request body</span></span>
<span data-ttu-id="7e758-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="7e758-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="7e758-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="7e758-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="7e758-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7e758-128">Property</span></span>|<span data-ttu-id="7e758-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e758-129">Type</span></span>|<span data-ttu-id="7e758-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e758-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7e758-131">syncType</span><span class="sxs-lookup"><span data-stu-id="7e758-131">syncType</span></span>|[<span data-ttu-id="7e758-132">deviceManagementExchangeConnectorSyncType</span><span class="sxs-lookup"><span data-stu-id="7e758-132">deviceManagementExchangeConnectorSyncType</span></span>](../resources/intune-onboarding-devicemanagementexchangeconnectorsynctype.md)|<span data-ttu-id="7e758-133">El tipo de sincronización que se ejecutará: sincronización completa o sincronización Delta.</span><span class="sxs-lookup"><span data-stu-id="7e758-133">The type of sync which will be executed, full sync or delta sync.</span></span>|



## <a name="response"></a><span data-ttu-id="7e758-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e758-134">Response</span></span>
<span data-ttu-id="7e758-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="7e758-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="7e758-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e758-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="7e758-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e758-137">Request</span></span>
<span data-ttu-id="7e758-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e758-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}/sync

Content-type: application/json
Content-length: 31

{
  "syncType": "deltaSync"
}
```

### <a name="response"></a><span data-ttu-id="7e758-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e758-139">Response</span></span>
<span data-ttu-id="7e758-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7e758-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




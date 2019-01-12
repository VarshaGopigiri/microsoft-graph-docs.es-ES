---
title: Eliminar remoteAssistancePartner
description: Elimina un remoteAssistancePartner.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c0b22ccfef3e18e9de2834d609084119e736dd10
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931863"
---
# <a name="delete-remoteassistancepartner"></a><span data-ttu-id="daba7-103">Eliminar remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="daba7-103">Delete remoteAssistancePartner</span></span>

> <span data-ttu-id="daba7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="daba7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="daba7-105">Elimina un [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="daba7-105">Deletes a [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="daba7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="daba7-106">Prerequisites</span></span>
<span data-ttu-id="daba7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="daba7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="daba7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="daba7-109">Permission type</span></span>|<span data-ttu-id="daba7-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="daba7-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="daba7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="daba7-111">Delegated (work or school account)</span></span>|<span data-ttu-id="daba7-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="daba7-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="daba7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="daba7-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="daba7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="daba7-114">Not supported.</span></span>|
|<span data-ttu-id="daba7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="daba7-115">Application</span></span>|<span data-ttu-id="daba7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="daba7-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="daba7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="daba7-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="daba7-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="daba7-118">Request headers</span></span>
|<span data-ttu-id="daba7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="daba7-119">Header</span></span>|<span data-ttu-id="daba7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="daba7-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="daba7-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="daba7-121">Authorization</span></span>|<span data-ttu-id="daba7-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="daba7-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="daba7-123">Accept</span><span class="sxs-lookup"><span data-stu-id="daba7-123">Accept</span></span>|<span data-ttu-id="daba7-124">application/json</span><span class="sxs-lookup"><span data-stu-id="daba7-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="daba7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="daba7-125">Request body</span></span>
<span data-ttu-id="daba7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="daba7-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="daba7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="daba7-127">Response</span></span>
<span data-ttu-id="daba7-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="daba7-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="daba7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="daba7-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="daba7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="daba7-130">Request</span></span>
<span data-ttu-id="daba7-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="daba7-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
```

### <a name="response"></a><span data-ttu-id="daba7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="daba7-132">Response</span></span>
<span data-ttu-id="daba7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="daba7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




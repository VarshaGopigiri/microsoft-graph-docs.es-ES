---
title: Acción sendTestMessage
description: Envía un mensaje de prueba con la notificationMessageTemplate especificada en la configuración regional predeterminada
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8ca3eda7f085e80090c172d7612936ec7cd1275e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889890"
---
# <a name="sendtestmessage-action"></a><span data-ttu-id="febfe-103">Acción sendTestMessage</span><span class="sxs-lookup"><span data-stu-id="febfe-103">sendTestMessage action</span></span>

> <span data-ttu-id="febfe-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="febfe-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="febfe-105">Envía un mensaje de prueba con la notificationMessageTemplate especificada en la configuración regional predeterminada</span><span class="sxs-lookup"><span data-stu-id="febfe-105">Sends test message using the specified notificationMessageTemplate in the default locale</span></span>
## <a name="prerequisites"></a><span data-ttu-id="febfe-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="febfe-106">Prerequisites</span></span>
<span data-ttu-id="febfe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="febfe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="febfe-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="febfe-109">Permission type</span></span>|<span data-ttu-id="febfe-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="febfe-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="febfe-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="febfe-111">Delegated (work or school account)</span></span>|<span data-ttu-id="febfe-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="febfe-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="febfe-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="febfe-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="febfe-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="febfe-114">Not supported.</span></span>|
|<span data-ttu-id="febfe-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="febfe-115">Application</span></span>|<span data-ttu-id="febfe-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="febfe-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="febfe-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="febfe-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/sendTestMessage
```

## <a name="request-headers"></a><span data-ttu-id="febfe-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="febfe-118">Request headers</span></span>
|<span data-ttu-id="febfe-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="febfe-119">Header</span></span>|<span data-ttu-id="febfe-120">Valor</span><span class="sxs-lookup"><span data-stu-id="febfe-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="febfe-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="febfe-121">Authorization</span></span>|<span data-ttu-id="febfe-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="febfe-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="febfe-123">Accept</span><span class="sxs-lookup"><span data-stu-id="febfe-123">Accept</span></span>|<span data-ttu-id="febfe-124">application/json</span><span class="sxs-lookup"><span data-stu-id="febfe-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="febfe-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="febfe-125">Request body</span></span>
<span data-ttu-id="febfe-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="febfe-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="febfe-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="febfe-127">Response</span></span>
<span data-ttu-id="febfe-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="febfe-128">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="febfe-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="febfe-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="febfe-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="febfe-130">Request</span></span>
<span data-ttu-id="febfe-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="febfe-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/sendTestMessage
```

### <a name="response"></a><span data-ttu-id="febfe-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="febfe-132">Response</span></span>
<span data-ttu-id="febfe-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="febfe-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




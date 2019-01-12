---
title: Acción sendTestMessage
description: Envía un mensaje de prueba con la notificationMessageTemplate especificada en la configuración regional predeterminada
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f2886ceae00573549a905dc31939fb828906992b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924849"
---
# <a name="sendtestmessage-action"></a><span data-ttu-id="ad17e-103">Acción sendTestMessage</span><span class="sxs-lookup"><span data-stu-id="ad17e-103">sendTestMessage action</span></span>

> <span data-ttu-id="ad17e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ad17e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ad17e-105">Envía un mensaje de prueba con la notificationMessageTemplate especificada en la configuración regional predeterminada</span><span class="sxs-lookup"><span data-stu-id="ad17e-105">Sends test message using the specified notificationMessageTemplate in the default locale</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ad17e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ad17e-106">Prerequisites</span></span>
<span data-ttu-id="ad17e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad17e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ad17e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad17e-109">Permission type</span></span>|<span data-ttu-id="ad17e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad17e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ad17e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad17e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ad17e-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ad17e-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="ad17e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad17e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ad17e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad17e-114">Not supported.</span></span>|
|<span data-ttu-id="ad17e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad17e-115">Application</span></span>|<span data-ttu-id="ad17e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad17e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ad17e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad17e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/sendTestMessage
```

## <a name="request-headers"></a><span data-ttu-id="ad17e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad17e-118">Request headers</span></span>
|<span data-ttu-id="ad17e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad17e-119">Header</span></span>|<span data-ttu-id="ad17e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ad17e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ad17e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ad17e-121">Authorization</span></span>|<span data-ttu-id="ad17e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ad17e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ad17e-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ad17e-123">Accept</span></span>|<span data-ttu-id="ad17e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ad17e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ad17e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad17e-125">Request body</span></span>
<span data-ttu-id="ad17e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ad17e-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ad17e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad17e-127">Response</span></span>
<span data-ttu-id="ad17e-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ad17e-128">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ad17e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad17e-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="ad17e-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad17e-130">Request</span></span>
<span data-ttu-id="ad17e-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad17e-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/sendTestMessage
```

### <a name="response"></a><span data-ttu-id="ad17e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad17e-132">Response</span></span>
<span data-ttu-id="ad17e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ad17e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




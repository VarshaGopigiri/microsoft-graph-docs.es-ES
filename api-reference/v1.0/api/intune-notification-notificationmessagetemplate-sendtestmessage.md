---
title: Acción sendTestMessage
description: Envía un mensaje de prueba con la notificationMessageTemplate especificada en la configuración regional predeterminada
ms.openlocfilehash: 99e93f64d1ca308c17b1a548c938a46922039c46
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032236"
---
# <a name="sendtestmessage-action"></a><span data-ttu-id="71ade-103">Acción sendTestMessage</span><span class="sxs-lookup"><span data-stu-id="71ade-103">sendTestMessage action</span></span>

> <span data-ttu-id="71ade-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="71ade-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71ade-105">Envía un mensaje de prueba con la notificationMessageTemplate especificada en la configuración regional predeterminada</span><span class="sxs-lookup"><span data-stu-id="71ade-105">Sends test message using the specified notificationMessageTemplate in the default locale</span></span>
## <a name="prerequisites"></a><span data-ttu-id="71ade-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71ade-106">Prerequisites</span></span>
<span data-ttu-id="71ade-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="71ade-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="71ade-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71ade-109">Permission type</span></span>|<span data-ttu-id="71ade-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71ade-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="71ade-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71ade-111">Delegated (work or school account)</span></span>|<span data-ttu-id="71ade-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71ade-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="71ade-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71ade-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="71ade-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71ade-114">Not supported.</span></span>|
|<span data-ttu-id="71ade-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71ade-115">Application</span></span>|<span data-ttu-id="71ade-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71ade-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="71ade-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71ade-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/sendTestMessage
```

## <a name="request-headers"></a><span data-ttu-id="71ade-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71ade-118">Request headers</span></span>
|<span data-ttu-id="71ade-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71ade-119">Header</span></span>|<span data-ttu-id="71ade-120">Valor</span><span class="sxs-lookup"><span data-stu-id="71ade-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="71ade-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="71ade-121">Authorization</span></span>|<span data-ttu-id="71ade-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="71ade-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="71ade-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="71ade-123">Accept</span></span>|<span data-ttu-id="71ade-124">application/json</span><span class="sxs-lookup"><span data-stu-id="71ade-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="71ade-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71ade-125">Request body</span></span>
<span data-ttu-id="71ade-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71ade-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71ade-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71ade-127">Response</span></span>
<span data-ttu-id="71ade-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="71ade-128">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="71ade-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71ade-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="71ade-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71ade-130">Request</span></span>
<span data-ttu-id="71ade-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71ade-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/sendTestMessage
```

### <a name="response"></a><span data-ttu-id="71ade-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71ade-132">Response</span></span>
<span data-ttu-id="71ade-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71ade-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




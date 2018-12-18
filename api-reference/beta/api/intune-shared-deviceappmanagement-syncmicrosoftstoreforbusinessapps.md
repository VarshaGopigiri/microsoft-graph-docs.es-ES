---
title: Acción syncMicrosoftStoreForBusinessApps
description: Sincroniza la cuenta de Intune con Microsoft Store para Empresas
author: tfitzmac
ms.openlocfilehash: 77171a96dd8a6b053234e9f95a8b79f4368abe4e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317986"
---
# <a name="syncmicrosoftstoreforbusinessapps-action"></a><span data-ttu-id="df348-103">Acción syncMicrosoftStoreForBusinessApps</span><span class="sxs-lookup"><span data-stu-id="df348-103">syncMicrosoftStoreForBusinessApps action</span></span>

> <span data-ttu-id="df348-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="df348-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="df348-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="df348-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="df348-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="df348-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="df348-107">Sincroniza la cuenta de Intune con Microsoft Store para Empresas</span><span class="sxs-lookup"><span data-stu-id="df348-107">Syncs Intune account with Microsoft Store For Business</span></span>
## <a name="prerequisites"></a><span data-ttu-id="df348-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="df348-108">Prerequisites</span></span>
<span data-ttu-id="df348-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="df348-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="df348-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="df348-111">Permission type</span></span>|<span data-ttu-id="df348-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="df348-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="df348-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="df348-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="df348-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="df348-114">&nbsp; &nbsp; **Onboarding**</span></span> | |<span data-ttu-id="df348-115">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="df348-115">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="df348-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="df348-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="df348-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df348-117">Not supported.</span></span>|
|<span data-ttu-id="df348-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="df348-118">Application</span></span>|<span data-ttu-id="df348-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df348-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="df348-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="df348-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

## <a name="request-headers"></a><span data-ttu-id="df348-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="df348-121">Request headers</span></span>
|<span data-ttu-id="df348-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df348-122">Header</span></span>|<span data-ttu-id="df348-123">Valor</span><span class="sxs-lookup"><span data-stu-id="df348-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="df348-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="df348-124">Authorization</span></span>|<span data-ttu-id="df348-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="df348-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="df348-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="df348-126">Accept</span></span>|<span data-ttu-id="df348-127">application/json</span><span class="sxs-lookup"><span data-stu-id="df348-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="df348-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="df348-128">Request body</span></span>
<span data-ttu-id="df348-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="df348-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="df348-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df348-130">Response</span></span>
<span data-ttu-id="df348-131">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="df348-131">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="df348-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df348-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="df348-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="df348-133">Request</span></span>
<span data-ttu-id="df348-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="df348-134">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

### <a name="response"></a><span data-ttu-id="df348-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df348-135">Response</span></span>
<span data-ttu-id="df348-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="df348-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




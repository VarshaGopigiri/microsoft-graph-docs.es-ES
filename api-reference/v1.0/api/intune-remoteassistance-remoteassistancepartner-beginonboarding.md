---
title: Acción beginOnboarding
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: e5d9d164e359484f6823c67c80169dbcef5116c5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337313"
---
# <a name="beginonboarding-action"></a><span data-ttu-id="1adac-103">Acción beginOnboarding</span><span class="sxs-lookup"><span data-stu-id="1adac-103">beginOnboarding action</span></span>

> <span data-ttu-id="1adac-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1adac-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1adac-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1adac-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1adac-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1adac-106">Prerequisites</span></span>
<span data-ttu-id="1adac-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1adac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1adac-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1adac-109">Permission type</span></span>|<span data-ttu-id="1adac-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1adac-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1adac-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1adac-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1adac-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1adac-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="1adac-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1adac-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1adac-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1adac-114">Not supported.</span></span>|
|<span data-ttu-id="1adac-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1adac-115">Application</span></span>|<span data-ttu-id="1adac-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1adac-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1adac-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1adac-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}/beginOnboarding
```

## <a name="request-headers"></a><span data-ttu-id="1adac-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1adac-118">Request headers</span></span>
|<span data-ttu-id="1adac-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1adac-119">Header</span></span>|<span data-ttu-id="1adac-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1adac-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1adac-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1adac-121">Authorization</span></span>|<span data-ttu-id="1adac-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1adac-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1adac-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1adac-123">Accept</span></span>|<span data-ttu-id="1adac-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1adac-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1adac-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1adac-125">Request body</span></span>
<span data-ttu-id="1adac-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1adac-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1adac-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1adac-127">Response</span></span>
<span data-ttu-id="1adac-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="1adac-128">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="1adac-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1adac-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="1adac-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1adac-130">Request</span></span>
<span data-ttu-id="1adac-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1adac-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}/beginOnboarding
```

### <a name="response"></a><span data-ttu-id="1adac-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1adac-132">Response</span></span>
<span data-ttu-id="1adac-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1adac-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




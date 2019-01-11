---
title: acción enableLegacyPcManagement
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: dfba24f59632126810e09dbce26970eb1c887b73
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818525"
---
# <a name="enablelegacypcmanagement-action"></a><span data-ttu-id="b6204-103">acción enableLegacyPcManagement</span><span class="sxs-lookup"><span data-stu-id="b6204-103">enableLegacyPcManagement action</span></span>

> <span data-ttu-id="b6204-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6204-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6204-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6204-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b6204-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b6204-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b6204-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b6204-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b6204-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6204-108">Prerequisites</span></span>
<span data-ttu-id="b6204-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6204-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6204-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6204-111">Permission type</span></span>|<span data-ttu-id="b6204-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6204-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b6204-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6204-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="b6204-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="b6204-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="b6204-115">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6204-115">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b6204-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6204-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b6204-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6204-117">Not supported.</span></span>|
|<span data-ttu-id="b6204-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6204-118">Application</span></span>|<span data-ttu-id="b6204-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6204-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b6204-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6204-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/enableLegacyPcManagement
```

## <a name="request-headers"></a><span data-ttu-id="b6204-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6204-121">Request headers</span></span>
|<span data-ttu-id="b6204-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6204-122">Header</span></span>|<span data-ttu-id="b6204-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b6204-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b6204-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="b6204-124">Authorization</span></span>|<span data-ttu-id="b6204-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b6204-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b6204-126">Accept</span><span class="sxs-lookup"><span data-stu-id="b6204-126">Accept</span></span>|<span data-ttu-id="b6204-127">application/json</span><span class="sxs-lookup"><span data-stu-id="b6204-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b6204-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6204-128">Request body</span></span>
<span data-ttu-id="b6204-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6204-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b6204-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6204-130">Response</span></span>
<span data-ttu-id="b6204-131">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b6204-131">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b6204-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6204-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="b6204-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6204-133">Request</span></span>
<span data-ttu-id="b6204-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6204-134">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/enableLegacyPcManagement
```

### <a name="response"></a><span data-ttu-id="b6204-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6204-135">Response</span></span>
<span data-ttu-id="b6204-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6204-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






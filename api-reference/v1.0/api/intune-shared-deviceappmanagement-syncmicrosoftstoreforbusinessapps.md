---
title: Acción syncMicrosoftStoreForBusinessApps
description: Sincroniza la cuenta de Intune con Microsoft Store para Empresas
author: tfitzmac
ms.openlocfilehash: b26b379631cf5b28594e3cf247b735d6118e9b40
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354337"
---
# <a name="syncmicrosoftstoreforbusinessapps-action"></a><span data-ttu-id="1020e-103">Acción syncMicrosoftStoreForBusinessApps</span><span class="sxs-lookup"><span data-stu-id="1020e-103">syncMicrosoftStoreForBusinessApps action</span></span>

> <span data-ttu-id="1020e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1020e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1020e-105">Sincroniza la cuenta de Intune con Microsoft Store para Empresas</span><span class="sxs-lookup"><span data-stu-id="1020e-105">Syncs Intune account with Microsoft Store For Business</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1020e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1020e-106">Prerequisites</span></span>
<span data-ttu-id="1020e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1020e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1020e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1020e-109">Permission type</span></span>|<span data-ttu-id="1020e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1020e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1020e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1020e-111">Delegated (work or school account)</span></span>| 
| <span data-ttu-id="1020e-112">&nbsp;&nbsp; _Incorporación_</span><span class="sxs-lookup"><span data-stu-id="1020e-112">&nbsp; &nbsp; _Onboarding_</span></span> | <span data-ttu-id="1020e-113">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1020e-113">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1020e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1020e-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1020e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1020e-115">Not supported.</span></span>|
|<span data-ttu-id="1020e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1020e-116">Application</span></span>|<span data-ttu-id="1020e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1020e-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1020e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1020e-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

## <a name="request-headers"></a><span data-ttu-id="1020e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1020e-119">Request headers</span></span>
|<span data-ttu-id="1020e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1020e-120">Header</span></span>|<span data-ttu-id="1020e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1020e-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1020e-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="1020e-122">Authorization</span></span>|<span data-ttu-id="1020e-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1020e-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1020e-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1020e-124">Accept</span></span>|<span data-ttu-id="1020e-125">application/json</span><span class="sxs-lookup"><span data-stu-id="1020e-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1020e-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1020e-126">Request body</span></span>
<span data-ttu-id="1020e-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1020e-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1020e-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1020e-128">Response</span></span>
<span data-ttu-id="1020e-129">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="1020e-129">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example-request"></a><span data-ttu-id="1020e-130">Ejemplo de solicitud</span><span class="sxs-lookup"><span data-stu-id="1020e-130">Example request</span></span>

``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/syncMicrosoftStoreForBusinessApps
```

### <a name="response"></a><span data-ttu-id="1020e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1020e-131">Response</span></span>

<span data-ttu-id="1020e-132">El objeto de respuesta que se muestra aquí es posible que esté truncado por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="1020e-132">The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="1020e-133">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1020e-133">All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```




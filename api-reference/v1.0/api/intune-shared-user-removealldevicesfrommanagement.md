---
title: Acción removeAllDevicesFromManagement
description: Retirar todos los dispositivos de la administración para este usuario
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 62e0243fef90190fd1ca39c02bc2a7e568b475d3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934292"
---
# <a name="removealldevicesfrommanagement-action"></a><span data-ttu-id="bdd12-103">Acción removeAllDevicesFromManagement</span><span class="sxs-lookup"><span data-stu-id="bdd12-103">removeAllDevicesFromManagement action</span></span>

> <span data-ttu-id="bdd12-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bdd12-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bdd12-105">Retirar todos los dispositivos de la administración para este usuario</span><span class="sxs-lookup"><span data-stu-id="bdd12-105">Retire all devices from management for this user</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bdd12-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bdd12-106">Prerequisites</span></span>
<span data-ttu-id="bdd12-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bdd12-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bdd12-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bdd12-109">Permission type</span></span>|<span data-ttu-id="bdd12-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bdd12-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bdd12-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bdd12-111">Delegated (work or school account)</span></span>| <span data-ttu-id="bdd12-112">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="bdd12-112">_varies by context_</span></span> |
| <span data-ttu-id="bdd12-113">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="bdd12-113">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="bdd12-114">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="bdd12-114">DeviceManagementManagedDevices.PriviligedOperation.All</span></span> |
|<span data-ttu-id="bdd12-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bdd12-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bdd12-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bdd12-116">Not supported.</span></span>|
|<span data-ttu-id="bdd12-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bdd12-117">Application</span></span>|<span data-ttu-id="bdd12-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bdd12-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bdd12-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bdd12-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/removeAllDevicesFromManagement
```

## <a name="request-headers"></a><span data-ttu-id="bdd12-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bdd12-120">Request headers</span></span>
|<span data-ttu-id="bdd12-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdd12-121">Header</span></span>|<span data-ttu-id="bdd12-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bdd12-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bdd12-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bdd12-123">Authorization</span></span>|<span data-ttu-id="bdd12-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bdd12-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bdd12-125">Accept</span><span class="sxs-lookup"><span data-stu-id="bdd12-125">Accept</span></span>|<span data-ttu-id="bdd12-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bdd12-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bdd12-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bdd12-127">Request body</span></span>
<span data-ttu-id="bdd12-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bdd12-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bdd12-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdd12-129">Response</span></span>
<span data-ttu-id="bdd12-130">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="bdd12-130">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="bdd12-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bdd12-131">Example</span></span>

### <a name="request"></a><span data-ttu-id="bdd12-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bdd12-132">Request</span></span>
<span data-ttu-id="bdd12-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bdd12-133">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/removeAllDevicesFromManagement
```

### <a name="response"></a><span data-ttu-id="bdd12-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdd12-134">Response</span></span>
<span data-ttu-id="bdd12-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bdd12-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```




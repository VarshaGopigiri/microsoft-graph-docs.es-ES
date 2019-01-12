---
title: Eliminar deviceCategory
description: Elimina un deviceCategory.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 121ab846c29daf1eaf3c5b20cde8dbefc403e260
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941579"
---
# <a name="delete-devicecategory"></a><span data-ttu-id="eb9ac-103">Eliminar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="eb9ac-103">Delete deviceCategory</span></span>

> <span data-ttu-id="eb9ac-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eb9ac-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eb9ac-105">Elimina un [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="eb9ac-105">Deletes a [deviceCategory](../resources/intune-shared-devicecategory.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eb9ac-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eb9ac-106">Prerequisites</span></span>
<span data-ttu-id="eb9ac-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eb9ac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eb9ac-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb9ac-109">Permission type</span></span>|<span data-ttu-id="eb9ac-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb9ac-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eb9ac-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb9ac-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="eb9ac-112">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="eb9ac-112">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="eb9ac-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb9ac-113">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="eb9ac-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb9ac-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eb9ac-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb9ac-115">Not supported.</span></span>|
|<span data-ttu-id="eb9ac-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb9ac-116">Application</span></span>|<span data-ttu-id="eb9ac-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb9ac-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eb9ac-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb9ac-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceCategories/{deviceCategoryId}
```

## <a name="request-headers"></a><span data-ttu-id="eb9ac-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb9ac-119">Request headers</span></span>
|<span data-ttu-id="eb9ac-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb9ac-120">Header</span></span>|<span data-ttu-id="eb9ac-121">Valor</span><span class="sxs-lookup"><span data-stu-id="eb9ac-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eb9ac-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="eb9ac-122">Authorization</span></span>|<span data-ttu-id="eb9ac-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eb9ac-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eb9ac-124">Accept</span><span class="sxs-lookup"><span data-stu-id="eb9ac-124">Accept</span></span>|<span data-ttu-id="eb9ac-125">application/json</span><span class="sxs-lookup"><span data-stu-id="eb9ac-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eb9ac-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb9ac-126">Request body</span></span>
<span data-ttu-id="eb9ac-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eb9ac-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eb9ac-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb9ac-128">Response</span></span>
<span data-ttu-id="eb9ac-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="eb9ac-129">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="eb9ac-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb9ac-130">Example</span></span>
### <a name="request"></a><span data-ttu-id="eb9ac-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb9ac-131">Request</span></span>
<span data-ttu-id="eb9ac-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb9ac-132">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories/{deviceCategoryId}
```

### <a name="response"></a><span data-ttu-id="eb9ac-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb9ac-133">Response</span></span>
<span data-ttu-id="eb9ac-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eb9ac-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




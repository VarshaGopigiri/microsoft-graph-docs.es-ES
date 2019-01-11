---
title: Eliminar mobileAppCategory
description: Elimina un mobileAppCategory
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4df1e889ab4a28683032d7f4cd07dacc54648298
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884514"
---
# <a name="delete-mobileappcategory"></a><span data-ttu-id="ca130-103">Eliminar mobileAppCategory</span><span class="sxs-lookup"><span data-stu-id="ca130-103">Delete mobileAppCategory</span></span>

> <span data-ttu-id="ca130-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ca130-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ca130-105">Elimina un [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)</span><span class="sxs-lookup"><span data-stu-id="ca130-105">Deletes a [mobileAppCategory](../resources/intune-apps-mobileappcategory.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ca130-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ca130-106">Prerequisites</span></span>
<span data-ttu-id="ca130-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ca130-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ca130-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ca130-109">Permission type</span></span>|<span data-ttu-id="ca130-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ca130-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ca130-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ca130-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ca130-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ca130-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ca130-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ca130-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ca130-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca130-114">Not supported.</span></span>|
|<span data-ttu-id="ca130-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ca130-115">Application</span></span>|<span data-ttu-id="ca130-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca130-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ca130-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ca130-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceAppManagement/mobileAppCategories/{mobileAppCategoryId}
DELETE /deviceAppManagement/mobileApps/{mobileAppId}/categories/{mobileAppCategoryId}
```

## <a name="request-headers"></a><span data-ttu-id="ca130-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ca130-118">Request headers</span></span>
|<span data-ttu-id="ca130-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca130-119">Header</span></span>|<span data-ttu-id="ca130-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ca130-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ca130-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ca130-121">Authorization</span></span>|<span data-ttu-id="ca130-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ca130-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ca130-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ca130-123">Accept</span></span>|<span data-ttu-id="ca130-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ca130-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ca130-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ca130-125">Request body</span></span>
<span data-ttu-id="ca130-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ca130-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ca130-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca130-127">Response</span></span>
<span data-ttu-id="ca130-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ca130-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ca130-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ca130-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="ca130-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ca130-130">Request</span></span>
<span data-ttu-id="ca130-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ca130-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppCategories/{mobileAppCategoryId}
```

### <a name="response"></a><span data-ttu-id="ca130-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca130-132">Response</span></span>
<span data-ttu-id="ca130-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ca130-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




---
title: Eliminar managedAndroidStoreApp
description: Elimina un managedAndroidStoreApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a659f8aae2b6b04ff7843e893edd5547a73058d8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986771"
---
# <a name="delete-managedandroidstoreapp"></a><span data-ttu-id="8fc89-103">Eliminar managedAndroidStoreApp</span><span class="sxs-lookup"><span data-stu-id="8fc89-103">Delete managedAndroidStoreApp</span></span>

> <span data-ttu-id="8fc89-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8fc89-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8fc89-105">Elimina un [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="8fc89-105">Deletes a [managedAndroidStoreApp](../resources/intune-apps-managedandroidstoreapp.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8fc89-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8fc89-106">Prerequisites</span></span>
<span data-ttu-id="8fc89-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8fc89-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8fc89-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8fc89-109">Permission type</span></span>|<span data-ttu-id="8fc89-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8fc89-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8fc89-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8fc89-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8fc89-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8fc89-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8fc89-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8fc89-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8fc89-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8fc89-114">Not supported.</span></span>|
|<span data-ttu-id="8fc89-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8fc89-115">Application</span></span>|<span data-ttu-id="8fc89-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8fc89-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8fc89-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8fc89-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="8fc89-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8fc89-118">Request headers</span></span>
|<span data-ttu-id="8fc89-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fc89-119">Header</span></span>|<span data-ttu-id="8fc89-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc89-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8fc89-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="8fc89-121">Authorization</span></span>|<span data-ttu-id="8fc89-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8fc89-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8fc89-123">Accept</span><span class="sxs-lookup"><span data-stu-id="8fc89-123">Accept</span></span>|<span data-ttu-id="8fc89-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8fc89-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8fc89-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8fc89-125">Request body</span></span>
<span data-ttu-id="8fc89-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8fc89-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8fc89-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fc89-127">Response</span></span>
<span data-ttu-id="8fc89-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="8fc89-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="8fc89-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8fc89-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="8fc89-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8fc89-130">Request</span></span>
<span data-ttu-id="8fc89-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8fc89-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="8fc89-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fc89-132">Response</span></span>
<span data-ttu-id="8fc89-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8fc89-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




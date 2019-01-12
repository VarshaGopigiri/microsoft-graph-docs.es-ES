---
title: Eliminar managedIOSStoreApp
description: Elimina un managedIOSStoreApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 660a63d09d4c87a26cc2b195bcb79c295c3ebd36
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934628"
---
# <a name="delete-managediosstoreapp"></a><span data-ttu-id="f5a98-103">Eliminar managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="f5a98-103">Delete managedIOSStoreApp</span></span>

> <span data-ttu-id="f5a98-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f5a98-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f5a98-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f5a98-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f5a98-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f5a98-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f5a98-107">Elimina un [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="f5a98-107">Deletes a [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f5a98-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f5a98-108">Prerequisites</span></span>
<span data-ttu-id="f5a98-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f5a98-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f5a98-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5a98-111">Permission type</span></span>|<span data-ttu-id="f5a98-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5a98-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f5a98-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5a98-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f5a98-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f5a98-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f5a98-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5a98-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f5a98-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5a98-116">Not supported.</span></span>|
|<span data-ttu-id="f5a98-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5a98-117">Application</span></span>|<span data-ttu-id="f5a98-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5a98-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f5a98-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5a98-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceAppManagement/mobileApps/{mobileAppId}
DELETE /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
DELETE /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="f5a98-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5a98-120">Request headers</span></span>
|<span data-ttu-id="f5a98-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5a98-121">Header</span></span>|<span data-ttu-id="f5a98-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f5a98-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f5a98-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f5a98-123">Authorization</span></span>|<span data-ttu-id="f5a98-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f5a98-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f5a98-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f5a98-125">Accept</span></span>|<span data-ttu-id="f5a98-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f5a98-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f5a98-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5a98-127">Request body</span></span>
<span data-ttu-id="f5a98-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f5a98-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f5a98-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5a98-129">Response</span></span>
<span data-ttu-id="f5a98-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f5a98-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f5a98-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5a98-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f5a98-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5a98-132">Request</span></span>
<span data-ttu-id="f5a98-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5a98-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
```

### <a name="response"></a><span data-ttu-id="f5a98-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5a98-134">Response</span></span>
<span data-ttu-id="f5a98-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f5a98-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






---
title: Eliminar windowsUniversalAppXContainedApp
description: Elimina un windowsUniversalAppXContainedApp.
ms.openlocfilehash: 2240b3915fca15eb4ba8ac5c8622625880de4821
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084893"
---
# <a name="delete-windowsuniversalappxcontainedapp"></a><span data-ttu-id="97f85-103">Eliminar windowsUniversalAppXContainedApp</span><span class="sxs-lookup"><span data-stu-id="97f85-103">Delete windowsUniversalAppXContainedApp</span></span>

> <span data-ttu-id="97f85-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="97f85-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="97f85-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="97f85-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="97f85-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="97f85-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="97f85-107">Elimina un [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md).</span><span class="sxs-lookup"><span data-stu-id="97f85-107">Deletes a [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="97f85-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="97f85-108">Prerequisites</span></span>
<span data-ttu-id="97f85-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="97f85-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="97f85-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="97f85-111">Permission type</span></span>|<span data-ttu-id="97f85-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="97f85-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="97f85-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="97f85-113">Delegated (work or school account)</span></span>|<span data-ttu-id="97f85-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="97f85-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="97f85-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="97f85-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="97f85-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97f85-116">Not supported.</span></span>|
|<span data-ttu-id="97f85-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="97f85-117">Application</span></span>|<span data-ttu-id="97f85-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97f85-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="97f85-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="97f85-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps/{mobileContainedAppId}
DELETE /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.microsoftStoreForBusinessApp/containedApps/{mobileContainedAppId}
DELETE /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.windowsUniversalAppX/committedContainedApps/{mobileContainedAppId}
```

## <a name="request-headers"></a><span data-ttu-id="97f85-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="97f85-120">Request headers</span></span>
|<span data-ttu-id="97f85-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97f85-121">Header</span></span>|<span data-ttu-id="97f85-122">Valor</span><span class="sxs-lookup"><span data-stu-id="97f85-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="97f85-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="97f85-123">Authorization</span></span>|<span data-ttu-id="97f85-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="97f85-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="97f85-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="97f85-125">Accept</span></span>|<span data-ttu-id="97f85-126">application/json</span><span class="sxs-lookup"><span data-stu-id="97f85-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="97f85-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="97f85-127">Request body</span></span>
<span data-ttu-id="97f85-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="97f85-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="97f85-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97f85-129">Response</span></span>
<span data-ttu-id="97f85-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="97f85-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="97f85-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97f85-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="97f85-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="97f85-132">Request</span></span>
<span data-ttu-id="97f85-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97f85-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps/{mobileContainedAppId}
```

### <a name="response"></a><span data-ttu-id="97f85-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97f85-134">Response</span></span>
<span data-ttu-id="97f85-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="97f85-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






---
title: Crear windowsUniversalAppXContainedApp
description: Crear un nuevo objeto windowsUniversalAppXContainedApp.
author: tfitzmac
ms.openlocfilehash: 97f50a79194af878569327073ae8911bf08199f3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27302817"
---
# <a name="create-windowsuniversalappxcontainedapp"></a><span data-ttu-id="55f25-103">Crear windowsUniversalAppXContainedApp</span><span class="sxs-lookup"><span data-stu-id="55f25-103">Create windowsUniversalAppXContainedApp</span></span>

> <span data-ttu-id="55f25-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="55f25-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="55f25-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="55f25-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="55f25-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="55f25-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="55f25-107">Crear un nuevo objeto [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md) .</span><span class="sxs-lookup"><span data-stu-id="55f25-107">Create a new [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="55f25-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="55f25-108">Prerequisites</span></span>
<span data-ttu-id="55f25-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="55f25-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="55f25-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55f25-111">Permission type</span></span>|<span data-ttu-id="55f25-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55f25-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="55f25-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55f25-113">Delegated (work or school account)</span></span>|<span data-ttu-id="55f25-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="55f25-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="55f25-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55f25-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="55f25-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55f25-116">Not supported.</span></span>|
|<span data-ttu-id="55f25-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55f25-117">Application</span></span>|<span data-ttu-id="55f25-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55f25-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="55f25-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55f25-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.microsoftStoreForBusinessApp/containedApps
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.windowsUniversalAppX/committedContainedApps
```

## <a name="request-headers"></a><span data-ttu-id="55f25-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55f25-120">Request headers</span></span>
|<span data-ttu-id="55f25-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55f25-121">Header</span></span>|<span data-ttu-id="55f25-122">Valor</span><span class="sxs-lookup"><span data-stu-id="55f25-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="55f25-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="55f25-123">Authorization</span></span>|<span data-ttu-id="55f25-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="55f25-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="55f25-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="55f25-125">Accept</span></span>|<span data-ttu-id="55f25-126">application/json</span><span class="sxs-lookup"><span data-stu-id="55f25-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="55f25-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55f25-127">Request body</span></span>
<span data-ttu-id="55f25-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsUniversalAppXContainedApp.</span><span class="sxs-lookup"><span data-stu-id="55f25-128">In the request body, supply a JSON representation for the windowsUniversalAppXContainedApp object.</span></span>

<span data-ttu-id="55f25-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsUniversalAppXContainedApp.</span><span class="sxs-lookup"><span data-stu-id="55f25-129">The following table shows the properties that are required when you create the windowsUniversalAppXContainedApp.</span></span>

|<span data-ttu-id="55f25-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55f25-130">Property</span></span>|<span data-ttu-id="55f25-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="55f25-131">Type</span></span>|<span data-ttu-id="55f25-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="55f25-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="55f25-133">id</span><span class="sxs-lookup"><span data-stu-id="55f25-133">id</span></span>|<span data-ttu-id="55f25-134">String</span><span class="sxs-lookup"><span data-stu-id="55f25-134">String</span></span>|<span data-ttu-id="55f25-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="55f25-135">Key of the entity.</span></span> <span data-ttu-id="55f25-136">Se hereda de [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)</span><span class="sxs-lookup"><span data-stu-id="55f25-136">Inherited from [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)</span></span>|
|<span data-ttu-id="55f25-137">appUserModelId</span><span class="sxs-lookup"><span data-stu-id="55f25-137">appUserModelId</span></span>|<span data-ttu-id="55f25-138">String</span><span class="sxs-lookup"><span data-stu-id="55f25-138">String</span></span>|<span data-ttu-id="55f25-139">El identificador del modelo de usuario de aplicación de la aplicación contenido de una aplicación de WindowsUniversalAppX.</span><span class="sxs-lookup"><span data-stu-id="55f25-139">The app user model ID of the contained app of a WindowsUniversalAppX app.</span></span>|



## <a name="response"></a><span data-ttu-id="55f25-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55f25-140">Response</span></span>
<span data-ttu-id="55f25-141">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55f25-141">If successful, this method returns a `201 Created` response code and a [windowsUniversalAppXContainedApp](../resources/intune-apps-windowsuniversalappxcontainedapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55f25-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55f25-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="55f25-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55f25-143">Request</span></span>
<span data-ttu-id="55f25-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55f25-144">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps
Content-type: application/json
Content-length: 122

{
  "@odata.type": "#microsoft.graph.windowsUniversalAppXContainedApp",
  "appUserModelId": "App User Model Id value"
}
```

### <a name="response"></a><span data-ttu-id="55f25-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55f25-145">Response</span></span>
<span data-ttu-id="55f25-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="55f25-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 171

{
  "@odata.type": "#microsoft.graph.windowsUniversalAppXContainedApp",
  "id": "2d03284a-284a-2d03-4a28-032d4a28032d",
  "appUserModelId": "App User Model Id value"
}
```






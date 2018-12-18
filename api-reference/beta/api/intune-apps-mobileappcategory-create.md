---
title: Crear mobileAppCategory
description: Cree un objeto mobileAppCategory.
author: tfitzmac
ms.openlocfilehash: 7fa2b8220069dd98ec35124f589a3e38a2a33317
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330950"
---
# <a name="create-mobileappcategory"></a><span data-ttu-id="bf9f1-103">Crear mobileAppCategory</span><span class="sxs-lookup"><span data-stu-id="bf9f1-103">Create mobileAppCategory</span></span>

> <span data-ttu-id="bf9f1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bf9f1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bf9f1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bf9f1-107">Cree un objeto [mobileAppCategory](../resources/intune-apps-mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="bf9f1-107">Create a new [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bf9f1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bf9f1-108">Prerequisites</span></span>
<span data-ttu-id="bf9f1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf9f1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bf9f1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf9f1-111">Permission type</span></span>|<span data-ttu-id="bf9f1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf9f1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bf9f1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf9f1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bf9f1-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf9f1-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="bf9f1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf9f1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bf9f1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-116">Not supported.</span></span>|
|<span data-ttu-id="bf9f1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf9f1-117">Application</span></span>|<span data-ttu-id="bf9f1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bf9f1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf9f1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppCategories
POST /deviceAppManagement/mobileApps/{mobileAppId}/categories
```

## <a name="request-headers"></a><span data-ttu-id="bf9f1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf9f1-120">Request headers</span></span>
|<span data-ttu-id="bf9f1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf9f1-121">Header</span></span>|<span data-ttu-id="bf9f1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bf9f1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bf9f1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bf9f1-123">Authorization</span></span>|<span data-ttu-id="bf9f1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bf9f1-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bf9f1-125">Accept</span></span>|<span data-ttu-id="bf9f1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bf9f1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bf9f1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf9f1-127">Request body</span></span>
<span data-ttu-id="bf9f1-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-128">In the request body, supply a JSON representation for the mobileAppCategory object.</span></span>

<span data-ttu-id="bf9f1-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-129">The following table shows the properties that are required when you create the mobileAppCategory.</span></span>

|<span data-ttu-id="bf9f1-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf9f1-130">Property</span></span>|<span data-ttu-id="bf9f1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf9f1-131">Type</span></span>|<span data-ttu-id="bf9f1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf9f1-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bf9f1-133">id</span><span class="sxs-lookup"><span data-stu-id="bf9f1-133">id</span></span>|<span data-ttu-id="bf9f1-134">String</span><span class="sxs-lookup"><span data-stu-id="bf9f1-134">String</span></span>|<span data-ttu-id="bf9f1-135">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-135">The key of the entity.</span></span>|
|<span data-ttu-id="bf9f1-136">displayName</span><span class="sxs-lookup"><span data-stu-id="bf9f1-136">displayName</span></span>|<span data-ttu-id="bf9f1-137">String</span><span class="sxs-lookup"><span data-stu-id="bf9f1-137">String</span></span>|<span data-ttu-id="bf9f1-138">El nombre de la categoría de aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-138">The name of the app category.</span></span>|
|<span data-ttu-id="bf9f1-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bf9f1-139">lastModifiedDateTime</span></span>|<span data-ttu-id="bf9f1-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bf9f1-140">DateTimeOffset</span></span>|<span data-ttu-id="bf9f1-141">Fecha y hora de la última modificación de mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-141">The date and time the mobileAppCategory was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="bf9f1-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf9f1-142">Response</span></span>
<span data-ttu-id="bf9f1-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-143">If successful, this method returns a `201 Created` response code and a [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bf9f1-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf9f1-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="bf9f1-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf9f1-145">Request</span></span>
<span data-ttu-id="bf9f1-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileAppCategories
Content-type: application/json
Content-length: 163

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```

### <a name="response"></a><span data-ttu-id="bf9f1-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf9f1-147">Response</span></span>
<span data-ttu-id="bf9f1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 212

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "id": "d85d9cee-9cee-d85d-ee9c-5dd8ee9c5dd8",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```






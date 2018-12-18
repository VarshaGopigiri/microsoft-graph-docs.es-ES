---
title: Crear mobileAppCategory
description: Cree un objeto mobileAppCategory.
author: tfitzmac
ms.openlocfilehash: 17084b8c02421b94b733a9ecb1011d647dab02d4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326337"
---
# <a name="create-mobileappcategory"></a><span data-ttu-id="61258-103">Crear mobileAppCategory</span><span class="sxs-lookup"><span data-stu-id="61258-103">Create mobileAppCategory</span></span>

> <span data-ttu-id="61258-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="61258-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="61258-105">Cree un objeto [mobileAppCategory](../resources/intune-apps-mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="61258-105">Create a new [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="61258-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="61258-106">Prerequisites</span></span>
<span data-ttu-id="61258-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="61258-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="61258-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="61258-109">Permission type</span></span>|<span data-ttu-id="61258-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="61258-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="61258-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="61258-111">Delegated (work or school account)</span></span>|<span data-ttu-id="61258-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61258-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="61258-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="61258-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="61258-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="61258-114">Not supported.</span></span>|
|<span data-ttu-id="61258-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="61258-115">Application</span></span>|<span data-ttu-id="61258-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="61258-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="61258-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="61258-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppCategories
POST /deviceAppManagement/mobileApps/{mobileAppId}/categories
```

## <a name="request-headers"></a><span data-ttu-id="61258-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="61258-118">Request headers</span></span>
|<span data-ttu-id="61258-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61258-119">Header</span></span>|<span data-ttu-id="61258-120">Valor</span><span class="sxs-lookup"><span data-stu-id="61258-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="61258-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="61258-121">Authorization</span></span>|<span data-ttu-id="61258-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="61258-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="61258-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="61258-123">Accept</span></span>|<span data-ttu-id="61258-124">application/json</span><span class="sxs-lookup"><span data-stu-id="61258-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="61258-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="61258-125">Request body</span></span>
<span data-ttu-id="61258-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="61258-126">In the request body, supply a JSON representation for the mobileAppCategory object.</span></span>

<span data-ttu-id="61258-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="61258-127">The following table shows the properties that are required when you create the mobileAppCategory.</span></span>

|<span data-ttu-id="61258-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61258-128">Property</span></span>|<span data-ttu-id="61258-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="61258-129">Type</span></span>|<span data-ttu-id="61258-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="61258-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="61258-131">id</span><span class="sxs-lookup"><span data-stu-id="61258-131">id</span></span>|<span data-ttu-id="61258-132">String</span><span class="sxs-lookup"><span data-stu-id="61258-132">String</span></span>|<span data-ttu-id="61258-133">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="61258-133">The key of the entity.</span></span>|
|<span data-ttu-id="61258-134">displayName</span><span class="sxs-lookup"><span data-stu-id="61258-134">displayName</span></span>|<span data-ttu-id="61258-135">String</span><span class="sxs-lookup"><span data-stu-id="61258-135">String</span></span>|<span data-ttu-id="61258-136">El nombre de la categoría de aplicación.</span><span class="sxs-lookup"><span data-stu-id="61258-136">The name of the app category.</span></span>|
|<span data-ttu-id="61258-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="61258-137">lastModifiedDateTime</span></span>|<span data-ttu-id="61258-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61258-138">DateTimeOffset</span></span>|<span data-ttu-id="61258-139">Fecha y hora de la última modificación de mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="61258-139">The date and time the mobileAppCategory was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="61258-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61258-140">Response</span></span>
<span data-ttu-id="61258-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61258-141">If successful, this method returns a `201 Created` response code and a [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="61258-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61258-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="61258-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="61258-143">Request</span></span>
<span data-ttu-id="61258-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="61258-144">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppCategories
Content-type: application/json
Content-length: 99

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "displayName": "Display Name value"
}
```

### <a name="response"></a><span data-ttu-id="61258-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61258-145">Response</span></span>
<span data-ttu-id="61258-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="61258-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




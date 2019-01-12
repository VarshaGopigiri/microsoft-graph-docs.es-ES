---
title: Crear iosVppAppAssignedLicense
description: Crear un nuevo objeto iosVppAppAssignedLicense.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 65c0b449b1b9add9697d5c1453245efbd1b2e213
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936322"
---
# <a name="create-iosvppappassignedlicense"></a><span data-ttu-id="8893f-103">Crear iosVppAppAssignedLicense</span><span class="sxs-lookup"><span data-stu-id="8893f-103">Create iosVppAppAssignedLicense</span></span>

> <span data-ttu-id="8893f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8893f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8893f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8893f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8893f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8893f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8893f-107">Crear un nuevo objeto [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="8893f-107">Create a new [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8893f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8893f-108">Prerequisites</span></span>
<span data-ttu-id="8893f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8893f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8893f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8893f-111">Permission type</span></span>|<span data-ttu-id="8893f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8893f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8893f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8893f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8893f-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8893f-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8893f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8893f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8893f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8893f-116">Not supported.</span></span>|
|<span data-ttu-id="8893f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8893f-117">Application</span></span>|<span data-ttu-id="8893f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8893f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8893f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8893f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
```

## <a name="request-headers"></a><span data-ttu-id="8893f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8893f-120">Request headers</span></span>
|<span data-ttu-id="8893f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8893f-121">Header</span></span>|<span data-ttu-id="8893f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8893f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8893f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8893f-123">Authorization</span></span>|<span data-ttu-id="8893f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8893f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8893f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="8893f-125">Accept</span></span>|<span data-ttu-id="8893f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8893f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8893f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8893f-127">Request body</span></span>
<span data-ttu-id="8893f-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosVppAppAssignedLicense.</span><span class="sxs-lookup"><span data-stu-id="8893f-128">In the request body, supply a JSON representation for the iosVppAppAssignedLicense object.</span></span>

<span data-ttu-id="8893f-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosVppAppAssignedLicense.</span><span class="sxs-lookup"><span data-stu-id="8893f-129">The following table shows the properties that are required when you create the iosVppAppAssignedLicense.</span></span>

|<span data-ttu-id="8893f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8893f-130">Property</span></span>|<span data-ttu-id="8893f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8893f-131">Type</span></span>|<span data-ttu-id="8893f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8893f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8893f-133">id</span><span class="sxs-lookup"><span data-stu-id="8893f-133">id</span></span>|<span data-ttu-id="8893f-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="8893f-134">String</span></span>|<span data-ttu-id="8893f-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8893f-135">Key of the entity.</span></span>|
|<span data-ttu-id="8893f-136">userEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8893f-136">userEmailAddress</span></span>|<span data-ttu-id="8893f-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="8893f-137">String</span></span>|<span data-ttu-id="8893f-138">La dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="8893f-138">The user email address.</span></span>|
|<span data-ttu-id="8893f-139">userId</span><span class="sxs-lookup"><span data-stu-id="8893f-139">userId</span></span>|<span data-ttu-id="8893f-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="8893f-140">String</span></span>|<span data-ttu-id="8893f-141">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="8893f-141">The user ID.</span></span>|
|<span data-ttu-id="8893f-142">userName</span><span class="sxs-lookup"><span data-stu-id="8893f-142">userName</span></span>|<span data-ttu-id="8893f-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="8893f-143">String</span></span>|<span data-ttu-id="8893f-144">El nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="8893f-144">The user name.</span></span>|
|<span data-ttu-id="8893f-145">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8893f-145">userPrincipalName</span></span>|<span data-ttu-id="8893f-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="8893f-146">String</span></span>|<span data-ttu-id="8893f-147">El nombre principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="8893f-147">The user principal name.</span></span>|



## <a name="response"></a><span data-ttu-id="8893f-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8893f-148">Response</span></span>
<span data-ttu-id="8893f-149">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8893f-149">If successful, this method returns a `201 Created` response code and a [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8893f-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8893f-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="8893f-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8893f-151">Request</span></span>
<span data-ttu-id="8893f-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8893f-152">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
Content-type: application/json
Content-length: 234

{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedLicense",
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="8893f-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8893f-153">Response</span></span>
<span data-ttu-id="8893f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8893f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 283

{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedLicense",
  "id": "090a8d2e-8d2e-090a-2e8d-0a092e8d0a09",
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value"
}
```






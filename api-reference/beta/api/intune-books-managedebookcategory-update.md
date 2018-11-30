---
title: Actualizar managedEBookCategory
description: Actualizar las propiedades de un objeto managedEBookCategory.
ms.openlocfilehash: 166d274d4d4eed8d6dff8efc8583af8c7ae9778e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082908"
---
# <a name="update-managedebookcategory"></a><span data-ttu-id="8fd0d-103">Actualizar managedEBookCategory</span><span class="sxs-lookup"><span data-stu-id="8fd0d-103">Update managedEBookCategory</span></span>

> <span data-ttu-id="8fd0d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8fd0d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8fd0d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8fd0d-107">Actualizar las propiedades de un objeto [managedEBookCategory](../resources/intune-books-managedebookcategory.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd0d-107">Update the properties of a [managedEBookCategory](../resources/intune-books-managedebookcategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8fd0d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8fd0d-108">Prerequisites</span></span>
<span data-ttu-id="8fd0d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8fd0d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8fd0d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8fd0d-111">Permission type</span></span>|<span data-ttu-id="8fd0d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8fd0d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8fd0d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8fd0d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8fd0d-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8fd0d-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8fd0d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8fd0d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8fd0d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-116">Not supported.</span></span>|
|<span data-ttu-id="8fd0d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8fd0d-117">Application</span></span>|<span data-ttu-id="8fd0d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8fd0d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8fd0d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBookCategories/{managedEBookCategoryId}
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/categories/{managedEBookCategoryId}
```

## <a name="request-headers"></a><span data-ttu-id="8fd0d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8fd0d-120">Request headers</span></span>
|<span data-ttu-id="8fd0d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fd0d-121">Header</span></span>|<span data-ttu-id="8fd0d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8fd0d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8fd0d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8fd0d-123">Authorization</span></span>|<span data-ttu-id="8fd0d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8fd0d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8fd0d-125">Accept</span></span>|<span data-ttu-id="8fd0d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8fd0d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8fd0d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8fd0d-127">Request body</span></span>
<span data-ttu-id="8fd0d-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [managedEBookCategory](../resources/intune-books-managedebookcategory.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd0d-128">In the request body, supply a JSON representation for the [managedEBookCategory](../resources/intune-books-managedebookcategory.md) object.</span></span>

<span data-ttu-id="8fd0d-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [managedEBookCategory](../resources/intune-books-managedebookcategory.md).</span><span class="sxs-lookup"><span data-stu-id="8fd0d-129">The following table shows the properties that are required when you create the [managedEBookCategory](../resources/intune-books-managedebookcategory.md).</span></span>

|<span data-ttu-id="8fd0d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8fd0d-130">Property</span></span>|<span data-ttu-id="8fd0d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fd0d-131">Type</span></span>|<span data-ttu-id="8fd0d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fd0d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8fd0d-133">id</span><span class="sxs-lookup"><span data-stu-id="8fd0d-133">id</span></span>|<span data-ttu-id="8fd0d-134">String</span><span class="sxs-lookup"><span data-stu-id="8fd0d-134">String</span></span>|<span data-ttu-id="8fd0d-135">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-135">The key of the entity.</span></span>|
|<span data-ttu-id="8fd0d-136">displayName</span><span class="sxs-lookup"><span data-stu-id="8fd0d-136">displayName</span></span>|<span data-ttu-id="8fd0d-137">String</span><span class="sxs-lookup"><span data-stu-id="8fd0d-137">String</span></span>|<span data-ttu-id="8fd0d-138">El nombre de la categoría del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-138">The name of the eBook category.</span></span>|
|<span data-ttu-id="8fd0d-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8fd0d-139">lastModifiedDateTime</span></span>|<span data-ttu-id="8fd0d-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8fd0d-140">DateTimeOffset</span></span>|<span data-ttu-id="8fd0d-141">La fecha y hora que se modificó por última vez el ManagedEBookCategory.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-141">The date and time the ManagedEBookCategory was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="8fd0d-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fd0d-142">Response</span></span>
<span data-ttu-id="8fd0d-143">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [managedEBookCategory](../resources/intune-books-managedebookcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-143">If successful, this method returns a `200 OK` response code and an updated [managedEBookCategory](../resources/intune-books-managedebookcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8fd0d-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8fd0d-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="8fd0d-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8fd0d-145">Request</span></span>
<span data-ttu-id="8fd0d-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-146">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/managedEBookCategories/{managedEBookCategoryId}
Content-type: application/json
Content-length: 107

{
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```

### <a name="response"></a><span data-ttu-id="8fd0d-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fd0d-147">Response</span></span>
<span data-ttu-id="8fd0d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8fd0d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 215

{
  "@odata.type": "#microsoft.graph.managedEBookCategory",
  "id": "3c71fb14-fb14-3c71-14fb-713c14fb713c",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```






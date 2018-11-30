---
title: 'reportRoot: getOffice365ActivationsUserCounts'
description: Obtener el recuento de usuarios que están habilitados y aquellos que tienen activada la suscripción de Office en el escritorio o dispositivos o equipos compartidos.
ms.openlocfilehash: 4d7d75d084408e4d0d8af0473397252fdcbe7aa9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082943"
---
# <a name="reportroot-getoffice365activationsusercounts"></a><span data-ttu-id="7226e-103">reportRoot: getOffice365ActivationsUserCounts</span><span class="sxs-lookup"><span data-stu-id="7226e-103">reportRoot: getOffice365ActivationsUserCounts</span></span>

> <span data-ttu-id="7226e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7226e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7226e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7226e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7226e-106">Obtener el recuento de usuarios que están habilitados y aquellos que tienen activada la suscripción de Office en el escritorio o dispositivos o equipos compartidos.</span><span class="sxs-lookup"><span data-stu-id="7226e-106">Get the count of users that are enabled and those that have activated the Office subscription on desktop or devices or shared computers.</span></span>

> <span data-ttu-id="7226e-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span><span class="sxs-lookup"><span data-stu-id="7226e-107">**Note:** For details about different report views and names, see [Office 365 Reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="permissions"></a><span data-ttu-id="7226e-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="7226e-108">Permissions</span></span>

<span data-ttu-id="7226e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7226e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7226e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7226e-111">Permission type</span></span>                        | <span data-ttu-id="7226e-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7226e-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="7226e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7226e-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="7226e-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7226e-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="7226e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7226e-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7226e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7226e-116">Not supported.</span></span>                           |
| <span data-ttu-id="7226e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7226e-117">Application</span></span>                            | <span data-ttu-id="7226e-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7226e-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="7226e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7226e-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActivationsUserCounts
```

## <a name="query-parameters"></a><span data-ttu-id="7226e-120">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="7226e-120">Query parameters</span></span>

<span data-ttu-id="7226e-121">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7226e-121">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="7226e-122">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="7226e-122">The default output type is text/csv.</span></span> <span data-ttu-id="7226e-123">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="7226e-123">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7226e-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7226e-124">Request headers</span></span>

| <span data-ttu-id="7226e-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="7226e-125">Name</span></span>          | <span data-ttu-id="7226e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="7226e-126">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="7226e-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="7226e-127">Authorization</span></span> | <span data-ttu-id="7226e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7226e-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="7226e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7226e-130">Response</span></span>

### <a name="csv"></a><span data-ttu-id="7226e-131">CSV</span><span class="sxs-lookup"><span data-stu-id="7226e-131">CSV</span></span>

<span data-ttu-id="7226e-132">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="7226e-132">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="7226e-133">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7226e-133">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="7226e-134">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="7226e-134">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="7226e-135">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="7226e-135">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="7226e-136">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="7226e-136">Report Refresh Date</span></span>
- <span data-ttu-id="7226e-137">Tipo de producto</span><span class="sxs-lookup"><span data-stu-id="7226e-137">Product Type</span></span>
- <span data-ttu-id="7226e-138">Asignado</span><span class="sxs-lookup"><span data-stu-id="7226e-138">Assigned</span></span>
- <span data-ttu-id="7226e-139">Activado</span><span class="sxs-lookup"><span data-stu-id="7226e-139">Activated</span></span>
- <span data-ttu-id="7226e-140">Activación de equipo compartido</span><span class="sxs-lookup"><span data-stu-id="7226e-140">Shared Computer Activation</span></span>

### <a name="json"></a><span data-ttu-id="7226e-141">JSON</span><span class="sxs-lookup"><span data-stu-id="7226e-141">JSON</span></span>

<span data-ttu-id="7226e-142">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[office365ActivationsUserCounts](../resources/office365activationsusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7226e-142">If successful, this method returns a `200 OK` response code and an **[office365ActivationsUserCounts](../resources/office365activationsusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7226e-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7226e-143">Example</span></span>

### <a name="csv"></a><span data-ttu-id="7226e-144">CSV</span><span class="sxs-lookup"><span data-stu-id="7226e-144">CSV</span></span>

<span data-ttu-id="7226e-145">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="7226e-145">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="7226e-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7226e-146">Request</span></span>

<span data-ttu-id="7226e-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7226e-147">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activationsusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActivationsUserCounts?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="7226e-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7226e-148">Response</span></span>

<span data-ttu-id="7226e-149">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7226e-149">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="7226e-150">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="7226e-150">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Product Type,Assigned,Activated,Shared Computer Activation
```

### <a name="json"></a><span data-ttu-id="7226e-151">JSON</span><span class="sxs-lookup"><span data-stu-id="7226e-151">JSON</span></span>

<span data-ttu-id="7226e-152">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="7226e-152">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="7226e-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7226e-153">Request</span></span>

<span data-ttu-id="7226e-154">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7226e-154">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activationsusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActivationsUserCounts?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="7226e-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7226e-155">Response</span></span>

<span data-ttu-id="7226e-156">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7226e-156">The following example shows the response.</span></span>

> <span data-ttu-id="7226e-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7226e-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.office365ActivationsUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.office365ActivationsUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "productType": "Office 365 ProPlus", 
      "assigned": 2679, 
      "activated": 1710,
      "sharedComputerActivation": 1024
    }
  ]
}
```

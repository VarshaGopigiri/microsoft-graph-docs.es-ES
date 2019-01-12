---
title: 'reportRoot: getOffice365ActivationCounts'
description: Obtiene el número de activaciones de Office 365 en dispositivos y equipos de escritorio.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 8027cf24c5a79f6d129f9b266cdb80929f2d707a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27913761"
---
# <a name="reportroot-getoffice365activationcounts"></a><span data-ttu-id="b6b0a-103">reportRoot: getOffice365ActivationCounts</span><span class="sxs-lookup"><span data-stu-id="b6b0a-103">reportRoot: getOffice365ActivationCounts</span></span>

> <span data-ttu-id="b6b0a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6b0a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b6b0a-106">Obtiene el número de activaciones de Office 365 en dispositivos y equipos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-106">Get the count of Office 365 activations on desktops and devices.</span></span>

> <span data-ttu-id="b6b0a-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span><span class="sxs-lookup"><span data-stu-id="b6b0a-107">**Note:** For details about different report views and names, see [Office 365 Reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="permissions"></a><span data-ttu-id="b6b0a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="b6b0a-108">Permissions</span></span>

<span data-ttu-id="b6b0a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6b0a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b6b0a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6b0a-111">Permission type</span></span>                        | <span data-ttu-id="b6b0a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6b0a-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="b6b0a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6b0a-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="b6b0a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6b0a-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="b6b0a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6b0a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b6b0a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-116">Not supported.</span></span>                           |
| <span data-ttu-id="b6b0a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6b0a-117">Application</span></span>                            | <span data-ttu-id="b6b0a-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6b0a-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="b6b0a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6b0a-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActivationCounts
```

## <a name="query-parameters"></a><span data-ttu-id="b6b0a-120">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="b6b0a-120">Query parameters</span></span>

<span data-ttu-id="b6b0a-121">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-121">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="b6b0a-122">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-122">The default output type is text/csv.</span></span> <span data-ttu-id="b6b0a-123">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-123">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b6b0a-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6b0a-124">Request headers</span></span>

| <span data-ttu-id="b6b0a-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="b6b0a-125">Name</span></span>          | <span data-ttu-id="b6b0a-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6b0a-126">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="b6b0a-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6b0a-127">Authorization</span></span> | <span data-ttu-id="b6b0a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="b6b0a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6b0a-130">Response</span></span>

### <a name="csv"></a><span data-ttu-id="b6b0a-131">CSV</span><span class="sxs-lookup"><span data-stu-id="b6b0a-131">CSV</span></span>

<span data-ttu-id="b6b0a-132">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-132">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="b6b0a-133">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-133">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="b6b0a-134">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-134">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="b6b0a-135">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-135">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="b6b0a-136">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="b6b0a-136">Report Refresh Date</span></span>
- <span data-ttu-id="b6b0a-137">Tipo de producto</span><span class="sxs-lookup"><span data-stu-id="b6b0a-137">Product Type</span></span>
- <span data-ttu-id="b6b0a-138">Windows</span><span class="sxs-lookup"><span data-stu-id="b6b0a-138">Windows</span></span>
- <span data-ttu-id="b6b0a-139">Mac</span><span class="sxs-lookup"><span data-stu-id="b6b0a-139">Mac</span></span>
- <span data-ttu-id="b6b0a-140">Android</span><span class="sxs-lookup"><span data-stu-id="b6b0a-140">Android</span></span>
- <span data-ttu-id="b6b0a-141">iOS</span><span class="sxs-lookup"><span data-stu-id="b6b0a-141">iOS</span></span>
- <span data-ttu-id="b6b0a-142">Windows 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="b6b0a-142">Windows 10 Mobile</span></span>

### <a name="json"></a><span data-ttu-id="b6b0a-143">JSON</span><span class="sxs-lookup"><span data-stu-id="b6b0a-143">JSON</span></span>

<span data-ttu-id="b6b0a-144">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[office365ActivationCounts](../resources/office365activationcounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-144">If successful, this method returns a `200 OK` response code and an **[office365ActivationCounts](../resources/office365activationcounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b6b0a-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6b0a-145">Example</span></span>

### <a name="csv"></a><span data-ttu-id="b6b0a-146">CSV</span><span class="sxs-lookup"><span data-stu-id="b6b0a-146">CSV</span></span>

<span data-ttu-id="b6b0a-147">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-147">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="b6b0a-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6b0a-148">Request</span></span>

<span data-ttu-id="b6b0a-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-149">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activationcounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActivationCounts?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="b6b0a-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6b0a-150">Response</span></span>

<span data-ttu-id="b6b0a-151">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-151">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="b6b0a-152">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-152">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Product Type,Windows,Mac,Android,iOS,Windows 10 Mobile
```

### <a name="json"></a><span data-ttu-id="b6b0a-153">JSON</span><span class="sxs-lookup"><span data-stu-id="b6b0a-153">JSON</span></span>

<span data-ttu-id="b6b0a-154">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-154">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="b6b0a-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6b0a-155">Request</span></span>

<span data-ttu-id="b6b0a-156">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-156">The following example shows the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activationcounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActivationCounts?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="b6b0a-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6b0a-157">Response</span></span>

<span data-ttu-id="b6b0a-158">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-158">The following example shows the response.</span></span>

> <span data-ttu-id="b6b0a-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.office365ActivationCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 268

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.office365ActivationCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "productType": "Office 365 ProPlus", 
      "windows": 9157, 
      "mac": 576, 
      "android": 358, 
      "ios": 1452, 
      "windows10Mobile": 2309
    }
  ]
}
```

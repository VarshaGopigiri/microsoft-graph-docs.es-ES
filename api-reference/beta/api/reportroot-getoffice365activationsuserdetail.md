---
title: 'reportRoot: getOffice365ActivationsUserDetail'
description: Obtiene información sobre qué usuarios activaron Office 365.
ms.openlocfilehash: 1dbbfefc7ea620f0926b037bd138bb04ed362c5d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085411"
---
# <a name="reportroot-getoffice365activationsuserdetail"></a><span data-ttu-id="0514d-103">reportRoot: getOffice365ActivationsUserDetail</span><span class="sxs-lookup"><span data-stu-id="0514d-103">reportRoot: getOffice365ActivationsUserDetail</span></span>

> <span data-ttu-id="0514d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0514d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0514d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0514d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0514d-106">Obtiene información sobre qué usuarios activaron Office 365.</span><span class="sxs-lookup"><span data-stu-id="0514d-106">Get details about users who have activated Office 365.</span></span>

> <span data-ttu-id="0514d-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span><span class="sxs-lookup"><span data-stu-id="0514d-107">**Note:** For details about different report views and names, see [Office 365 Reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="permissions"></a><span data-ttu-id="0514d-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="0514d-108">Permissions</span></span>

<span data-ttu-id="0514d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0514d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0514d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0514d-111">Permission type</span></span>                        | <span data-ttu-id="0514d-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0514d-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="0514d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0514d-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="0514d-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="0514d-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="0514d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0514d-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0514d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0514d-116">Not supported.</span></span>                           |
| <span data-ttu-id="0514d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0514d-117">Application</span></span>                            | <span data-ttu-id="0514d-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="0514d-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="0514d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0514d-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActivationsUserDetail
```

## <a name="query-parameters"></a><span data-ttu-id="0514d-120">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="0514d-120">Query parameters</span></span>

<span data-ttu-id="0514d-121">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0514d-121">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="0514d-122">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="0514d-122">The default output type is text/csv.</span></span> <span data-ttu-id="0514d-123">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="0514d-123">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0514d-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0514d-124">Request headers</span></span>

| <span data-ttu-id="0514d-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="0514d-125">Name</span></span>          | <span data-ttu-id="0514d-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="0514d-126">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="0514d-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="0514d-127">Authorization</span></span> | <span data-ttu-id="0514d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0514d-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="0514d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0514d-130">Response</span></span>

### <a name="csv"></a><span data-ttu-id="0514d-131">CSV</span><span class="sxs-lookup"><span data-stu-id="0514d-131">CSV</span></span>

<span data-ttu-id="0514d-132">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="0514d-132">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="0514d-133">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0514d-133">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="0514d-134">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="0514d-134">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="0514d-135">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="0514d-135">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="0514d-136">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="0514d-136">Report Refresh Date</span></span>
- <span data-ttu-id="0514d-137">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="0514d-137">User Principal Name</span></span>
- <span data-ttu-id="0514d-138">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="0514d-138">Display Name</span></span>
- <span data-ttu-id="0514d-139">Tipo de producto</span><span class="sxs-lookup"><span data-stu-id="0514d-139">Product Type</span></span>
- <span data-ttu-id="0514d-140">Fecha de la última activación</span><span class="sxs-lookup"><span data-stu-id="0514d-140">Last Activated Date</span></span>
- <span data-ttu-id="0514d-141">Windows</span><span class="sxs-lookup"><span data-stu-id="0514d-141">Windows</span></span>
- <span data-ttu-id="0514d-142">Mac</span><span class="sxs-lookup"><span data-stu-id="0514d-142">Mac</span></span>
- <span data-ttu-id="0514d-143">Windows 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="0514d-143">Windows 10 Mobile</span></span>
- <span data-ttu-id="0514d-144">iOS</span><span class="sxs-lookup"><span data-stu-id="0514d-144">iOS</span></span>
- <span data-ttu-id="0514d-145">Android</span><span class="sxs-lookup"><span data-stu-id="0514d-145">Android</span></span>
- <span data-ttu-id="0514d-146">Activa en un equipo compartido</span><span class="sxs-lookup"><span data-stu-id="0514d-146">Activated On Shared Computer</span></span>

### <a name="json"></a><span data-ttu-id="0514d-147">JSON</span><span class="sxs-lookup"><span data-stu-id="0514d-147">JSON</span></span>

<span data-ttu-id="0514d-148">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[office365ActivationsUserDetail](../resources/office365activationsuserdetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0514d-148">If successful, this method returns a `200 OK` response code and an **[office365ActivationsUserDetail](../resources/office365activationsuserdetail.md)** object in the response body.</span></span>

<span data-ttu-id="0514d-149">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="0514d-149">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="0514d-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0514d-150">Example</span></span>

### <a name="csv"></a><span data-ttu-id="0514d-151">CSV</span><span class="sxs-lookup"><span data-stu-id="0514d-151">CSV</span></span>

<span data-ttu-id="0514d-152">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="0514d-152">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="0514d-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0514d-153">Request</span></span>

<span data-ttu-id="0514d-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0514d-154">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activationsuserdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActivationsUserDetail?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="0514d-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0514d-155">Response</span></span>

<span data-ttu-id="0514d-156">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0514d-156">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="0514d-157">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="0514d-157">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Product Type,Last Activated Date,Windows,Mac,Windows 10 Mobile,iOS,Android,Activated On Shared Computer
```

### <a name="json"></a><span data-ttu-id="0514d-158">JSON</span><span class="sxs-lookup"><span data-stu-id="0514d-158">JSON</span></span>

<span data-ttu-id="0514d-159">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="0514d-159">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="0514d-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0514d-160">Request</span></span>

<span data-ttu-id="0514d-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0514d-161">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activationsuserdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActivationsUserDetail?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="0514d-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0514d-162">Response</span></span>

<span data-ttu-id="0514d-163">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0514d-163">The following is an example of the response.</span></span>

> <span data-ttu-id="0514d-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0514d-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.office365ActivationsUserDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 400

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.office365ActivationsUserDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "userPrincipalName": "userprincipalname-value", 
      "displayName": "displayname-value", 
      "userActivationCounts": [
        {
          "productType": "Project Client", 
          "lastActivatedDate": "2017-08-20", 
          "windows": 5, 
          "mac": 0, 
          "windows10Mobile": 0, 
          "ios": 0, 
          "android": 2,
          "activatedOnSharedComputer": true
        }
      ]
    }
  ]
}
```

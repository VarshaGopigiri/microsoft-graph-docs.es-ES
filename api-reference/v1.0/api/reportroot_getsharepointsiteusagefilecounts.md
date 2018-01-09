# <a name="reportroot-getsharepointsiteusagefilecounts"></a><span data-ttu-id="142e0-101">reportRoot: getSharePointSiteUsageFileCounts</span><span class="sxs-lookup"><span data-stu-id="142e0-101">reportRoot: getSharePointSiteUsageFileCounts</span></span>

<span data-ttu-id="142e0-102">Obtiene el número total de archivos en todos los sitios y el número de archivos activos.</span><span class="sxs-lookup"><span data-stu-id="142e0-102">Get the total number of files across all sites and the number of active files.</span></span> <span data-ttu-id="142e0-103">Un archivo (usuario o sistema) se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="142e0-103">A file (user or system) is considered active if it has been saved, synced, modified, or shared within the specified time period.</span></span>

> <span data-ttu-id="142e0-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de sitio de SharePoint]((https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)).</span><span class="sxs-lookup"><span data-stu-id="142e0-104">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint site usage]((https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)).</span></span>

## <a name="permissions"></a><span data-ttu-id="142e0-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="142e0-105">Permissions</span></span>

<span data-ttu-id="142e0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="142e0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="142e0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="142e0-108">Permission type</span></span>                        | <span data-ttu-id="142e0-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="142e0-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="142e0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="142e0-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="142e0-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="142e0-111">Not supported.</span></span>                           |
| <span data-ttu-id="142e0-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="142e0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="142e0-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="142e0-113">Not supported.</span></span>                           |
| <span data-ttu-id="142e0-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="142e0-114">Application</span></span>                            | <span data-ttu-id="142e0-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="142e0-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="142e0-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="142e0-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointSiteUsageFileCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="142e0-117">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="142e0-117">Request parameters</span></span>

<span data-ttu-id="142e0-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="142e0-118">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="142e0-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="142e0-119">Parameter</span></span> | <span data-ttu-id="142e0-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="142e0-120">Type</span></span>   | <span data-ttu-id="142e0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="142e0-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="142e0-122">period</span><span class="sxs-lookup"><span data-stu-id="142e0-122">Period</span></span>    | <span data-ttu-id="142e0-123">cadena</span><span class="sxs-lookup"><span data-stu-id="142e0-123">string</span></span> | <span data-ttu-id="142e0-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="142e0-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="142e0-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="142e0-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="142e0-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="142e0-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="142e0-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="142e0-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="142e0-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="142e0-128">Request headers</span></span>

| <span data-ttu-id="142e0-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="142e0-129">Name</span></span>          | <span data-ttu-id="142e0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="142e0-130">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="142e0-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="142e0-131">Authorization</span></span> | <span data-ttu-id="142e0-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="142e0-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="142e0-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="142e0-134">if-none-match</span></span> | <span data-ttu-id="142e0-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="142e0-135">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `304 Not Modified` response is returned.</span></span> <span data-ttu-id="142e0-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="142e0-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="142e0-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="142e0-137">Response</span></span>

<span data-ttu-id="142e0-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="142e0-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="142e0-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="142e0-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="142e0-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="142e0-140">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<span data-ttu-id="142e0-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="142e0-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="142e0-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="142e0-142">Report Refresh Date</span></span>
- <span data-ttu-id="142e0-143">Tipo de sitio</span><span class="sxs-lookup"><span data-stu-id="142e0-143">Site Type</span></span>
- <span data-ttu-id="142e0-144">Total</span><span class="sxs-lookup"><span data-stu-id="142e0-144">total</span></span>
- <span data-ttu-id="142e0-145">Activo</span><span class="sxs-lookup"><span data-stu-id="142e0-145">Active</span></span>
- <span data-ttu-id="142e0-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="142e0-146">Report Date</span></span>
- <span data-ttu-id="142e0-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="142e0-147">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="142e0-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="142e0-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="142e0-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="142e0-149">Request</span></span>

<span data-ttu-id="142e0-150">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="142e0-150">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointsiteusagefilecounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSharePointSiteUsageFileCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="142e0-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="142e0-151">Response</span></span>

<span data-ttu-id="142e0-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="142e0-152">Here is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="142e0-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="142e0-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site Type,Total,Active,Report Date,Report Period
```

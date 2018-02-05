# <a name="reportroot-getonedriveusageaccountcounts"></a><span data-ttu-id="05ea6-101">reportRoot: getOneDriveUsageAccountCounts</span><span class="sxs-lookup"><span data-stu-id="05ea6-101">reportRoot: getOneDriveUsageAccountCounts</span></span>

<span data-ttu-id="05ea6-102">Obtiene la tendencia sobre el número de sitios activos de OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="05ea6-102">Get the trend in the number of active OneDrive for Business sites.</span></span> <span data-ttu-id="05ea6-103">Cualquier sitio en que los usuarios vieron, modificaron, cargaron, descargaron, compartieron o sincronizaron archivos se considera un sitio activo.</span><span class="sxs-lookup"><span data-stu-id="05ea6-103">Any site on which users viewed, modified, uploaded, downloaded, shared, or synced files is considered an active site.</span></span>

> <span data-ttu-id="05ea6-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span><span class="sxs-lookup"><span data-stu-id="05ea6-104">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="permissions"></a><span data-ttu-id="05ea6-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="05ea6-105">Permissions</span></span>

<span data-ttu-id="05ea6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="05ea6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="05ea6-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05ea6-108">Permission type</span></span>                        | <span data-ttu-id="05ea6-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05ea6-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="05ea6-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05ea6-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="05ea6-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05ea6-111">Not supported.</span></span>                           |
| <span data-ttu-id="05ea6-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05ea6-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="05ea6-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05ea6-113">Not supported.</span></span>                           |
| <span data-ttu-id="05ea6-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05ea6-114">Application</span></span>                            | <span data-ttu-id="05ea6-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="05ea6-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="05ea6-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05ea6-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveUsageAccountCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="05ea6-117">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05ea6-117">Request parameters</span></span>

<span data-ttu-id="05ea6-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="05ea6-118">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="05ea6-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="05ea6-119">Parameter</span></span> | <span data-ttu-id="05ea6-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="05ea6-120">Type</span></span>   | <span data-ttu-id="05ea6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="05ea6-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="05ea6-122">period</span><span class="sxs-lookup"><span data-stu-id="05ea6-122">period</span></span>    | <span data-ttu-id="05ea6-123">cadena</span><span class="sxs-lookup"><span data-stu-id="05ea6-123">string</span></span> | <span data-ttu-id="05ea6-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="05ea6-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="05ea6-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="05ea6-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="05ea6-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="05ea6-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="05ea6-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="05ea6-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="05ea6-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="05ea6-128">Request headers</span></span>

| <span data-ttu-id="05ea6-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="05ea6-129">Name</span></span>          | <span data-ttu-id="05ea6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="05ea6-130">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="05ea6-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="05ea6-131">Authorization</span></span> | <span data-ttu-id="05ea6-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="05ea6-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="05ea6-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="05ea6-134">If-None-Match</span></span> | <span data-ttu-id="05ea6-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="05ea6-135">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="05ea6-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="05ea6-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="05ea6-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05ea6-137">Response</span></span>

<span data-ttu-id="05ea6-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="05ea6-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="05ea6-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05ea6-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="05ea6-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="05ea6-140">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="05ea6-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="05ea6-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="05ea6-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="05ea6-142">Report Refresh Date</span></span>
- <span data-ttu-id="05ea6-143">Tipo de sitio</span><span class="sxs-lookup"><span data-stu-id="05ea6-143">Site Type</span></span>
- <span data-ttu-id="05ea6-144">Total</span><span class="sxs-lookup"><span data-stu-id="05ea6-144">Total</span></span>
- <span data-ttu-id="05ea6-145">Activo</span><span class="sxs-lookup"><span data-stu-id="05ea6-145">Active</span></span>
- <span data-ttu-id="05ea6-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="05ea6-146">Report Date</span></span>
- <span data-ttu-id="05ea6-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="05ea6-147">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="05ea6-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05ea6-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="05ea6-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="05ea6-149">Request</span></span>

<span data-ttu-id="05ea6-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="05ea6-150">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveusageaccountcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOneDriveUsageAccountCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="05ea6-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05ea6-151">Response</span></span>

<span data-ttu-id="05ea6-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05ea6-152">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="05ea6-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="05ea6-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

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

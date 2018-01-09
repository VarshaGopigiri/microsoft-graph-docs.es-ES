# <a name="reportroot-getoffice365groupsactivityfilecounts"></a><span data-ttu-id="684de-101">reportRoot: getOffice365GroupsActivityFileCounts</span><span class="sxs-lookup"><span data-stu-id="684de-101">reportRoot: getOffice365GroupsActivityFileCounts</span></span>

<span data-ttu-id="684de-102">Obtiene el número total de archivos y cuántos estaban activos en todos los sitios de grupo asociados con un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="684de-102">Get the total number of files and how many of them were active across all group sites associated with an Office 365 Group.</span></span>

> <span data-ttu-id="684de-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Grupos de Office 365]((https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40)).</span><span class="sxs-lookup"><span data-stu-id="684de-103">**Note:** For details about different report views and names, see [Office 365 Reports - Office 365 groups]((https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40)).</span></span>

## <a name="permissions"></a><span data-ttu-id="684de-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="684de-104">Permissions</span></span>

<span data-ttu-id="684de-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="684de-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="684de-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="684de-107">Permission type</span></span>                        | <span data-ttu-id="684de-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="684de-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="684de-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="684de-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="684de-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="684de-110">Not supported.</span></span>                           |
| <span data-ttu-id="684de-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="684de-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="684de-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="684de-112">Not supported.</span></span>                           |
| <span data-ttu-id="684de-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="684de-113">Application</span></span>                            | <span data-ttu-id="684de-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="684de-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="684de-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="684de-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365GroupsActivityFileCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="684de-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="684de-116">Request parameters</span></span>

<span data-ttu-id="684de-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="684de-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="684de-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="684de-118">Parameter</span></span> | <span data-ttu-id="684de-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="684de-119">Type</span></span>   | <span data-ttu-id="684de-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="684de-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="684de-121">period</span><span class="sxs-lookup"><span data-stu-id="684de-121">Period</span></span>    | <span data-ttu-id="684de-122">cadena</span><span class="sxs-lookup"><span data-stu-id="684de-122">string</span></span> | <span data-ttu-id="684de-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="684de-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="684de-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="684de-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="684de-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="684de-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="684de-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="684de-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="684de-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="684de-127">Request headers</span></span>

| <span data-ttu-id="684de-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="684de-128">Name</span></span>          | <span data-ttu-id="684de-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="684de-129">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="684de-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="684de-130">Authorization</span></span> | <span data-ttu-id="684de-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="684de-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="684de-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="684de-133">if-none-match</span></span> | <span data-ttu-id="684de-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="684de-134">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `304 Not Modified` response is returned.</span></span> <span data-ttu-id="684de-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="684de-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="684de-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="684de-136">Response</span></span>

<span data-ttu-id="684de-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="684de-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="684de-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="684de-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="684de-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="684de-139">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<span data-ttu-id="684de-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="684de-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="684de-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="684de-141">Report Refresh Date</span></span>
- <span data-ttu-id="684de-142">Total</span><span class="sxs-lookup"><span data-stu-id="684de-142">total</span></span>
- <span data-ttu-id="684de-143">Activo</span><span class="sxs-lookup"><span data-stu-id="684de-143">Active</span></span>
- <span data-ttu-id="684de-144">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="684de-144">Report Date</span></span>
- <span data-ttu-id="684de-145">Período del informe</span><span class="sxs-lookup"><span data-stu-id="684de-145">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="684de-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="684de-146">Example</span></span>

#### <a name="request"></a><span data-ttu-id="684de-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="684de-147">Request</span></span>

<span data-ttu-id="684de-148">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="684de-148">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365groupsactivityfilecounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365GroupsActivityFileCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="684de-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="684de-149">Response</span></span>

<span data-ttu-id="684de-150">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="684de-150">Here is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="684de-151">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="684de-151">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Total,Active,Report Date,Report Period
```

# <a name="reportroot-getskypeforbusinessactivityusercounts"></a><span data-ttu-id="19c9d-101">reportRoot: getSkypeForBusinessActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="19c9d-101">reportRoot: getSkypeForBusinessActivityUserCounts</span></span>

<span data-ttu-id="19c9d-102">Obtiene las tendencias sobre el número de usuarios únicos que organizaron y participaron en sesiones de conferencia realizadas en la organización con Skype Empresarial.</span><span class="sxs-lookup"><span data-stu-id="19c9d-102">Get the trends on how many unique users organized and participated in conference sessions held in your organization through Skype for Business.</span></span> <span data-ttu-id="19c9d-103">En el informe, también se incluye el número de sesiones de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="19c9d-103">The report also includes the number of peer-to-peer sessions.</span></span>

> <span data-ttu-id="19c9d-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span><span class="sxs-lookup"><span data-stu-id="19c9d-104">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business activity](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span></span>

## <a name="permissions"></a><span data-ttu-id="19c9d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="19c9d-105">Permissions</span></span>

<span data-ttu-id="19c9d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="19c9d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="19c9d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="19c9d-108">Permission type</span></span>                        | <span data-ttu-id="19c9d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="19c9d-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="19c9d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="19c9d-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="19c9d-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="19c9d-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="19c9d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="19c9d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="19c9d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19c9d-113">Not supported.</span></span>                           |
| <span data-ttu-id="19c9d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="19c9d-114">Application</span></span>                            | <span data-ttu-id="19c9d-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="19c9d-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="19c9d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="19c9d-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessActivityUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="19c9d-117">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="19c9d-117">Request parameters</span></span>

<span data-ttu-id="19c9d-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="19c9d-118">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="19c9d-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="19c9d-119">Parameter</span></span> | <span data-ttu-id="19c9d-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="19c9d-120">Type</span></span>   | <span data-ttu-id="19c9d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="19c9d-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="19c9d-122">period</span><span class="sxs-lookup"><span data-stu-id="19c9d-122">period</span></span>    | <span data-ttu-id="19c9d-123">cadena</span><span class="sxs-lookup"><span data-stu-id="19c9d-123">string</span></span> | <span data-ttu-id="19c9d-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="19c9d-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="19c9d-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="19c9d-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="19c9d-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="19c9d-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="19c9d-127">Necesario.</span><span class="sxs-lookup"><span data-stu-id="19c9d-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="19c9d-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="19c9d-128">Request headers</span></span>

| <span data-ttu-id="19c9d-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="19c9d-129">Name</span></span>          | <span data-ttu-id="19c9d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="19c9d-130">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="19c9d-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="19c9d-131">Authorization</span></span> | <span data-ttu-id="19c9d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="19c9d-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="19c9d-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="19c9d-134">If-None-Match</span></span> | <span data-ttu-id="19c9d-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="19c9d-135">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="19c9d-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="19c9d-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="19c9d-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19c9d-137">Response</span></span>

<span data-ttu-id="19c9d-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="19c9d-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="19c9d-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19c9d-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="19c9d-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="19c9d-140">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="19c9d-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="19c9d-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="19c9d-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="19c9d-142">Report Refresh Date</span></span>
- <span data-ttu-id="19c9d-143">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="19c9d-143">Report Date</span></span>
- <span data-ttu-id="19c9d-144">Período del informe</span><span class="sxs-lookup"><span data-stu-id="19c9d-144">Report Period</span></span>
- <span data-ttu-id="19c9d-145">Punto a punto</span><span class="sxs-lookup"><span data-stu-id="19c9d-145">Peer-to-peer</span></span>
- <span data-ttu-id="19c9d-146">Organizado</span><span class="sxs-lookup"><span data-stu-id="19c9d-146">Organized</span></span>
- <span data-ttu-id="19c9d-147">Participado</span><span class="sxs-lookup"><span data-stu-id="19c9d-147">Participated</span></span>

## <a name="example"></a><span data-ttu-id="19c9d-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="19c9d-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="19c9d-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="19c9d-149">Request</span></span>

<span data-ttu-id="19c9d-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="19c9d-150">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessactivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="19c9d-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19c9d-151">Response</span></span>

<span data-ttu-id="19c9d-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19c9d-152">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="19c9d-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="19c9d-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,Peer-to-peer,Organized,Participated
```

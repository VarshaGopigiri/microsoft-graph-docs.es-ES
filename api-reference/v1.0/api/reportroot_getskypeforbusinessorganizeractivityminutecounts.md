# <a name="reportroot-getskypeforbusinessorganizeractivityminutecounts"></a><span data-ttu-id="1ca23-101">reportRoot: getSkypeForBusinessOrganizerActivityMinuteCounts</span><span class="sxs-lookup"><span data-stu-id="1ca23-101">reportRoot: getSkypeForBusinessOrganizerActivityMinuteCounts</span></span>

<span data-ttu-id="1ca23-102">Obtiene tendencias de uso sobre la duración en minutos y el tipo de sesiones de conferencia realizadas y organizadas por usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="1ca23-102">Get usage trends on the length in minutes and type of conference sessions held and organized by users in your organization.</span></span> <span data-ttu-id="1ca23-103">Entre los tipos de sesiones de conferencia, se incluyen sesiones de audio o vídeo, y sesiones de acceso telefónico local y aceptación de llamadas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1ca23-103">Types of conference sessions include audio/video, and dial-in and dial-out - Microsoft.</span></span>

> <span data-ttu-id="1ca23-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de organizador de conferencia de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-conference-organized-activity-03a255d4-0e1d-4b24-b73d-7a62fae36254).</span><span class="sxs-lookup"><span data-stu-id="1ca23-104">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business conference organizer activity](https://support.office.com/client/Skype-for-Business-Online-conference-organized-activity-03a255d4-0e1d-4b24-b73d-7a62fae36254).</span></span>

## <a name="permissions"></a><span data-ttu-id="1ca23-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1ca23-105">Permissions</span></span>

<span data-ttu-id="1ca23-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1ca23-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="1ca23-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1ca23-108">Permission type</span></span>                        | <span data-ttu-id="1ca23-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1ca23-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="1ca23-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1ca23-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="1ca23-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="1ca23-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="1ca23-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1ca23-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1ca23-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ca23-113">Not supported.</span></span>                           |
| <span data-ttu-id="1ca23-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1ca23-114">Application</span></span>                            | <span data-ttu-id="1ca23-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="1ca23-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="1ca23-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ca23-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessOrganizerActivityMinuteCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="1ca23-117">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="1ca23-117">Function parameters</span></span>

<span data-ttu-id="1ca23-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="1ca23-118">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="1ca23-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1ca23-119">Parameter</span></span> | <span data-ttu-id="1ca23-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ca23-120">Type</span></span>   | <span data-ttu-id="1ca23-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ca23-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="1ca23-122">period</span><span class="sxs-lookup"><span data-stu-id="1ca23-122">period</span></span>    | <span data-ttu-id="1ca23-123">cadena</span><span class="sxs-lookup"><span data-stu-id="1ca23-123">string</span></span> | <span data-ttu-id="1ca23-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="1ca23-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="1ca23-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="1ca23-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="1ca23-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="1ca23-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="1ca23-127">Necesario.</span><span class="sxs-lookup"><span data-stu-id="1ca23-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="1ca23-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ca23-128">Request headers</span></span>

| <span data-ttu-id="1ca23-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ca23-129">Name</span></span>          | <span data-ttu-id="1ca23-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ca23-130">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="1ca23-131">Autorización</span><span class="sxs-lookup"><span data-stu-id="1ca23-131">Authorization</span></span> | <span data-ttu-id="1ca23-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ca23-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="1ca23-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="1ca23-134">If-None-Match</span></span> | <span data-ttu-id="1ca23-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="1ca23-135">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="1ca23-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1ca23-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="1ca23-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ca23-137">Response</span></span>

<span data-ttu-id="1ca23-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="1ca23-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="1ca23-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ca23-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="1ca23-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="1ca23-140">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="1ca23-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="1ca23-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="1ca23-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="1ca23-142">Report Refresh Date</span></span>
- <span data-ttu-id="1ca23-143">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="1ca23-143">Report Date</span></span>
- <span data-ttu-id="1ca23-144">Período del informe</span><span class="sxs-lookup"><span data-stu-id="1ca23-144">Report Period</span></span>
- <span data-ttu-id="1ca23-145">Audio o vídeo</span><span class="sxs-lookup"><span data-stu-id="1ca23-145">Audio/Video</span></span>
- <span data-ttu-id="1ca23-146">Acceso telefónico local de Microsoft</span><span class="sxs-lookup"><span data-stu-id="1ca23-146">Dial-in Microsoft</span></span>
- <span data-ttu-id="1ca23-147">Aceptación de llamadas de Microsoft</span><span class="sxs-lookup"><span data-stu-id="1ca23-147">Dial-out Microsoft</span></span>

## <a name="example"></a><span data-ttu-id="1ca23-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ca23-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="1ca23-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ca23-149">Request</span></span>

<span data-ttu-id="1ca23-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1ca23-150">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessorganizeractivityminutecounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessOrganizerActivityMinuteCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="1ca23-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ca23-151">Response</span></span>

<span data-ttu-id="1ca23-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ca23-152">The following is an example of the response.</span></span>

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

<span data-ttu-id="1ca23-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="1ca23-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,Audio/Video,Dial-in Microsoft,Dial-out Microsoft
```

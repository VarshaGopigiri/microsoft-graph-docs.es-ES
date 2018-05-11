# <a name="reportroot-getskypeforbusinessparticipantactivitycounts"></a><span data-ttu-id="4a3a1-101">reportRoot: getSkypeForBusinessParticipantActivityCounts</span><span class="sxs-lookup"><span data-stu-id="4a3a1-101">reportRoot: getSkypeForBusinessParticipantActivityCounts</span></span>

<span data-ttu-id="4a3a1-102">Obtiene tendencias de uso sobre el número y el tipo de sesiones de conferencia en las que participaron usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-102">Get usage trends on the number and type of conference sessions that users from your organization participated in.</span></span> <span data-ttu-id="4a3a1-103">Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web y acceso telefónico local o aceptación de llamada de terceros.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-103">Types of conference sessions include IM, audio/video, application sharing, web, and dial-in/out - 3rd party.</span></span>

> <span data-ttu-id="4a3a1-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de participantes de conferencias de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).</span><span class="sxs-lookup"><span data-stu-id="4a3a1-104">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business conference participant activity](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).</span></span>

## <a name="permissions"></a><span data-ttu-id="4a3a1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a3a1-105">Permissions</span></span>

<span data-ttu-id="4a3a1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4a3a1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="4a3a1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a3a1-108">Permission type</span></span>                        | <span data-ttu-id="4a3a1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a3a1-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="4a3a1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a3a1-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="4a3a1-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="4a3a1-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="4a3a1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a3a1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4a3a1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-113">Not supported.</span></span>                           |
| <span data-ttu-id="4a3a1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a3a1-114">Application</span></span>                            | <span data-ttu-id="4a3a1-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="4a3a1-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="4a3a1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a3a1-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessParticipantActivityCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="4a3a1-117">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a3a1-117">Request parameters</span></span>

<span data-ttu-id="4a3a1-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-118">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="4a3a1-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4a3a1-119">Parameter</span></span> | <span data-ttu-id="4a3a1-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a3a1-120">Type</span></span>   | <span data-ttu-id="4a3a1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a3a1-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="4a3a1-122">period</span><span class="sxs-lookup"><span data-stu-id="4a3a1-122">period</span></span>    | <span data-ttu-id="4a3a1-123">cadena</span><span class="sxs-lookup"><span data-stu-id="4a3a1-123">string</span></span> | <span data-ttu-id="4a3a1-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="4a3a1-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="4a3a1-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-126">These values follow the format D   where    represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="4a3a1-127">Necesario.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="4a3a1-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4a3a1-128">Request headers</span></span>

| <span data-ttu-id="4a3a1-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a3a1-129">Name</span></span>          | <span data-ttu-id="4a3a1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a3a1-130">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="4a3a1-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="4a3a1-131">Authorization</span></span> | <span data-ttu-id="4a3a1-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="4a3a1-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="4a3a1-134">If-None-Match</span></span> | <span data-ttu-id="4a3a1-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-135">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="4a3a1-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="4a3a1-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a3a1-137">Response</span></span>

<span data-ttu-id="4a3a1-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="4a3a1-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="4a3a1-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-140">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="4a3a1-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="4a3a1-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="4a3a1-142">Report Refresh Date</span></span>
- <span data-ttu-id="4a3a1-143">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="4a3a1-143">Report Date</span></span>
- <span data-ttu-id="4a3a1-144">Período del informe</span><span class="sxs-lookup"><span data-stu-id="4a3a1-144">Report Period</span></span>
- <span data-ttu-id="4a3a1-145">Mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="4a3a1-145">IM</span></span>
- <span data-ttu-id="4a3a1-146">Audio o vídeo</span><span class="sxs-lookup"><span data-stu-id="4a3a1-146">Audio/Video</span></span>
- <span data-ttu-id="4a3a1-147">Uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4a3a1-147">App Sharing</span></span>
- <span data-ttu-id="4a3a1-148">Web</span><span class="sxs-lookup"><span data-stu-id="4a3a1-148">Web</span></span>
- <span data-ttu-id="4a3a1-149">Acceso telefónico local o aceptación de llamada de terceros</span><span class="sxs-lookup"><span data-stu-id="4a3a1-149">Dial-in/out 3rd Party</span></span>

## <a name="example"></a><span data-ttu-id="4a3a1-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a3a1-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="4a3a1-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4a3a1-151">Request</span></span>

<span data-ttu-id="4a3a1-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-152">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessparticipantactivitycounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessParticipantActivityCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="4a3a1-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a3a1-153">Response</span></span>

<span data-ttu-id="4a3a1-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-154">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="4a3a1-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="4a3a1-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio/Video,App Sharing,Web,Dial-in/out 3rd Party
```

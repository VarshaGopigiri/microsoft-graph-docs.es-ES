# <a name="datetimetimezone-resource-type"></a>Tipo de recurso dateTimeTimeZone

Describe la fecha, la hora y la zona horaria de un momento dado.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|dateTime|Cadena|Un único momento dado en una fecha combinada y la representación de tiempo (`<date>T<time>`).|
|timeZone|Cadena|Uno de los siguientes nombres de zona horaria.|

La propiedad _TimeZone_ puede establecerse en cualquiera de las zonas horarias compatibles con Windows, así como los nombres de zona horaria siguientes.

Etc/GMT+12

Etc/GMT+11

Pacific/Honolulu

America/Anchorage

América/Santa Isabel

America/Los_Angeles

America/Phoenix

America/Chihuahua

America/Denver

America/Guatemala

America/Chicago

America/Mexico_City

America/Regina

America/Bogota

America/New_York

America/Indiana/Indianapolis

America/Caracas

America/Asuncion

America/Halifax

America/Cuiaba

America/La_Paz

America/Santiago

America/St_Johns

America/Sao_Paulo

America/Argentina/Buenos_Aires

America/Cayenne

America/Godthab

America/Montevideo

America/Bahia

Etc/GMT+2

Atlantic/Azores

Atlantic/Cape_Verde

Africa/Casablanca

Etc/GMT

Europe/London

Atlantic/Reykjavik

Europe/Berlin

Europe/Budapest

Europe/Paris

Europe/Warsaw

Africa/Lagos

Africa/Windhoek

Europe/Bucharest

Asia/Beirut

Africa/Cairo

Asia/Damasco

Africa/Johannesburg

Europe/Kyiv (Kiev)

Europe/Istanbul

Asia/Jerusalem

Asia/Amman

Asia/Baghdad

Europe/Kaliningrad

Asia/Riyadh

Africa/Nairobi

Asia/Tehran

Asia/Dubai

Asia/Baku

Europe/Moscow

Indian/Mauritius

Asia/Tbilisi

Asia/Yerevan

Asia/Kabul

Asia/Karachi

Asia/Toshkent (Tashkent)

Asia/Kolkata

Asia/Colombo

Asia/Kathmandu

Asia/Astana (Almaty)

Asia/Dhaka

Asia/Yekaterinburg

Asia/Yangon (Rangoon)

Asia/Bangkok

Asia/Novosibirsk

Asia/Shanghai

Asia/Krasnoyarsk

Asia/Singapore

Australia/Perth

Asia/Taipei

Asia/Ulaanbaatar

Asia/Irkutsk

Asia/Tokyo

Asia/Seoul

Australia/Adelaide

Australia/Darwin

Australia/Brisbane

Australia/Sydney

Pacific/Port_Moresby

Australia/Hobart

Asia/Yakutsk

Pacific/Guadalcanal

Asia/Vladivostok

Pacific/Auckland

Etc/GMT-12

Pacific/Fiji

Asia/Magadan

Pacific/Tongatapu

Pacific/Apia

Pacific/Kiritimati

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.dateTimeTimeZone"
}-->

```json
{
  "dateTime": "string",
  "timeZone": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "dateTimeTimeZone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

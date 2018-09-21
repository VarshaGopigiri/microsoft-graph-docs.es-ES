# <a name="get-outlook-events-in-a-shared-or-delegated-calendar"></a>Obtener eventos de Outlook en un calendario compartido o delegado

En Outlook, los clientes pueden compartir un calendario con otros usuarios y permitirles ver o modificar los eventos de ese calendario. Los clientes también pueden conceder un delegado para que actúe en su nombre, para recibir o responder a convocatorias de reunión, o crear o cambiar elementos en el calendario.

Mediante programación, Microsoft Graph permite obtener eventos de los calendarios que se han compartido por otros usuarios, así como los propios calendarios compartidos. La compatibilidad también se aplica a las carpetas que se han delegado.

Por ejemplo, Garth tiene compartido con John su calendario predeterminado y ha concedido a John acceso de lectura. Si John ha iniciado sesión en su aplicación y ha proporcionado los permisos delegados (Calendars.Read.Shared o Calendars.ReadWrite.Shared), la aplicación podrá obtener acceso al calendario predeterminado de Garth y a eventos de ese calendario tal y como se describe a continuación.

## <a name="get-an-event-in-the-shared-calendar"></a>Obtener un evento del calendario compartido

Puede obtener un evento específico del calendario predeterminado compartido de Garth:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar/events/{id}
```

Si esto se completa correctamente, obtendrá HTTP 200 OK y la instancia de [evento](../api-reference/v1.0/resources/event.md) identificada por `{id}` del calendario predeterminado de Garth.

## <a name="get-all-the-events-in-the-shared-calendar"></a>Obtener todos los eventos del calendario compartido

Obtenga todos los eventos del calendario predeterminado que Garth ha compartido con John:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar/events
```

Si esto se completa correctamente, obtendrá HTTP 200 OK y una colección de instancias de [evento](../api-reference/v1.0/resources/event.md) en el calendario de predeterminado de Garth.

## <a name="get-the-shared-calendar"></a>Obtener el calendario compartido

Obtenga el calendario predeterminado que Garth ha compartido con John.

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar
```

Si esto se completa correctamente, obtendrá HTTP 200 OK y una instancia de [calendario](../api-reference/v1.0/resources/calendar.md) que representa la carpeta predeterminada de Garth.

Se aplicarían las mismas funciones de GET si Garth hubiera delegado a John acceso su calendario predeterminado, o si hubiera delegado a John todo su buzón.

Si Garth no ha compartido su calendario predeterminado con John ni ha delegado su buzón a John, especificar el Id. de usuario o el nombre principal de usuario de Garth en esas operaciones GET devolverá un error. 


## <a name="next-steps"></a>Siguientes pasos

Obtenga más información sobre:

- [¿Por qué debería realizar la integración con el calendario de Outlook?](outlook-calendar-concept-overview.md)
- [API de calendario](../api-reference/v1.0/resources/calendar.md) en Microsoft Graph v1.0.
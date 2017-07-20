<span data-ttu-id="817ee-p119">Para crear el correo electrónico, el código extrae el nombre de usuario del token de sesión y la dirección de correo electrónico del destinatario de los parámetros que se han pasado desde el formulario. A continuación, el código lee el cuerpo del correo electrónico desde una plantilla que se incluye en el proyecto, interpola el nombre de usuario y la dirección de correo electrónico y asocia el texto del correo electrónico como cuerpo de la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="817ee-p119">To create the email, the code pulls the user name from the session token and the recipient email address from the parameters passed from the form. The code then reads the email body from a template included in the project, interpolates the user name and email address, and attaches the email text as the HTTP request body.</span></span>

Para crear el correo electrónico, el código extrae el nombre de usuario del token de sesión y la dirección de correo electrónico del destinatario de los parámetros que se han pasado desde el formulario. A continuación, el código lee el cuerpo del correo electrónico desde una plantilla que se incluye en el proyecto, interpola el nombre de usuario y la dirección de correo electrónico y asocia el texto del correo electrónico como cuerpo de la solicitud HTTP.

<span data-ttu-id="817ee-194">Para enviar el correo electrónico, el código crea la solicitud HTTP, adjunta el token de acceso como encabezado de autorización y, a continuación, publica la solicitud en el punto de conexión de envío de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="817ee-194">To send the email, the code constructs the HTTP request, attaches the access token as an authorization header, and then posts the request to the send email endpoint.</span></span>

<span data-ttu-id="817ee-195">Por último, el código usa el código de respuesta HTTP que se ha devuelto para notificar al usuario si el correo electrónico se envió o no correctamente.</span><span class="sxs-lookup"><span data-stu-id="817ee-195">Finally, the code uses the HTTP response code returned to notify the user whether or not the email was successful.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="817ee-196">Ejecutar la aplicación</span><span class="sxs-lookup"><span data-stu-id="817ee-196">Run the app</span></span>

1. <span data-ttu-id="817ee-197">Instale la aplicación Rails y las dependencias con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="817ee-197">Install the Rails application and dependencies with the following command.</span></span>

    ```
    bundle install
    ```
2. <span data-ttu-id="817ee-198">Para iniciar la aplicación Rails, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="817ee-198">To start the Rails application, type the following command.</span></span>

    ```
    rackup -p 3000
    ```
3. <span data-ttu-id="817ee-199">Vaya a `http://localhost:3000` en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="817ee-199">Go to `http://localhost:3000` in your web browser.</span></span>

## <a name="see-also"></a><span data-ttu-id="817ee-200">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="817ee-200">See also</span></span>
- <span data-ttu-id="817ee-201">Pruebe la API de REST mediante el [Probador de Graph](https://graph.microsoft.io/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="817ee-201">Try out the REST API using the [Graph explorer](https://graph.microsoft.io/graph-explorer).</span></span>
- <span data-ttu-id="817ee-202">Explore nuestros otros [ejemplos de Microsoft Graph](https://github.com/microsoftgraph) en GitHub.</span><span class="sxs-lookup"><span data-stu-id="817ee-202">Explore our other [Microsoft Graph samples](https://github.com/microsoftgraph) on GitHub.</span></span>
- [<span data-ttu-id="817ee-203">Obtener tokens de acceso para llamar a Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="817ee-203">Get access tokens to call Microsoft Graph</span></span>](https://developer.microsoft.com/en-us/graph/docs/concepts/auth_overview)
- [<span data-ttu-id="817ee-204">Obtener acceso en nombre de un usuario</span><span class="sxs-lookup"><span data-stu-id="817ee-204">Get access on behalf of a user</span></span>](https://developer.microsoft.com/en-us/graph/docs/concepts/auth_v2_user)
- [<span data-ttu-id="817ee-205">Obtener acceso sin un usuario</span><span class="sxs-lookup"><span data-stu-id="817ee-205">Get access without a user</span></span>](https://developer.microsoft.com/en-us/graph/docs/concepts/auth_v2_service)



# AspDotNetCore Web Api
Going to cover asp.net core project in deep 
<h2></h2>
<h2>What is Middleware in asp.net core and example</h2>
<p>Middleware is a component integrated into the application pipeline to handle requests and responses. Each middleware is linked in a chain, allowing it to decide whether to pass the request to the next component or not. It can also perform actions before and after the next component runs.</p>
<p><b>Note:</b>  middleware is executed in the order it is registered in the Configure</p>

<ul>
  1.Exception Handling Middleware: Handles exceptions globally and provides a way to respond to errors.
  
  ```
  app.UseExceptionHandler("/Home/Error");
  ```
2.HTTPS Redirection Middleware: Ensures that all HTTP requests are redirected to HTTPS.

```
app.UseHttpsRedirection();

```
3.Static Files Middleware: Serves static files such as CSS, JavaScript, and images.

```
app.UseStaticFiles();

```
4.Routing Middleware: Enables the routing capabilities for incoming requests.

```
app.UseRouting();

```
5.CORS Middleware: Configures Cross-Origin Resource Sharing settings.

```
app.UseCors(builder =>
    builder.WithOrigins("https://example.com")
           .AllowAnyHeader()
           .AllowAnyMethod());

```
6.Session Middleware: Manages session state, allowing you to store user-specific data.

```
app.UseSession();

```
7.Authentication Middleware: Validates user authentication and sets the user principal.

```
app.UseAuthentication();

```
8.Authorization Middleware: Checks user permissions and controls access to resources.

```
app.UseAuthorization();

```
9.Response Compression Middleware: Compresses the response data to reduce bandwidth usage.

```
app.UseResponseCompression();

```
10.Endpoint Middleware: Handles the final request processing based on the configured routes.

```
app.UseEndpoints(endpoints =>
{
    endpoints.MapControllerRoute(
        name: "default",
        pattern: "{controller=Home}/{action=Index}/{id?}");
});

```
</ul>
<h2></h2>

.

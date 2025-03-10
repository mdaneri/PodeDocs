# Sample Scripts

## [Caching](https://github.com/Badgerati/Pode/blob/develop/examples/Caching.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server and integrate with Redis for caching.

**Description**

This script sets up a Pode server listening on port 8081 with Redis integration for caching.
It checks for the existence of the `redis-cli` command and sets up a Pode server with routes
that demonstrate caching with Redis.

## [Create-Routes](https://github.com/Badgerati/Pode/blob/develop/examples/Create-Routes.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with multiple routes using different approaches.

**Description**

This script sets up a Pode server listening on port 8081 with various routes demonstrating different
approaches to route creation. These include using script blocks, file paths, and direct script inclusion.

## [Dot-SourceScript](https://github.com/Badgerati/Pode/blob/develop/examples/Dot-SourceScript.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server and run a script from an external file.

**Description**

This script sets up a Pode server, enables terminal logging for errors, and uses an external
script for additional logic. It imports the Pode module from the source path if available,
otherwise from the installed modules.

## [External-Funcs](https://github.com/Badgerati/Pode/blob/develop/examples/External-Funcs.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server and use an external module function.

**Description**

This script sets up a Pode server listening on port 8081, imports an external module containing functions,
and includes a route that uses a function from the external module to generate a response.

## [File-Monitoring](https://github.com/Badgerati/Pode/blob/develop/examples/File-Monitoring.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with a view engine and file monitoring.

**Description**

This script sets up a Pode server listening on port 8081, uses Pode's view engine for rendering
web pages, and configures the server to monitor file changes and restart automatically.

## [File-Watchers](https://github.com/Badgerati/Pode/blob/develop/examples/File-Watchers.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with file watcher and logging.

**Description**

This script sets up a Pode server, enables terminal logging for errors, and adds a file watcher
to monitor changes in PowerShell script files (*.ps1) within the script directory. The server
logs file change events and outputs them to the terminal.

## [FileBrowser](https://github.com/Badgerati/Pode/blob/develop/examples/FileBrowser/FileBrowser.ps1)

**Synopsis**

PowerShell script to set up a Pode server with static file browsing and authentication.

**Description**

This script sets up a Pode server that listens on port 8081. It includes static file browsing
with different routes, some of which require authentication. The script also demonstrates
how to set up basic authentication using Pode.

The server includes routes for downloading files, browsing files without downloading, and
accessing files with authentication.

## [HelloService](https://github.com/Badgerati/Pode/blob/develop/examples/HelloService/HelloService.ps1)

**Synopsis**

PowerShell script to register, manage, and set up a Pode service named '$ServiceName'.

**Description**

This script provides commands to register, start, stop, query, suspend, resume, restart, and unregister a Pode service named '$ServiceName'.
It also sets up a Pode server that listens on the specified port (default 8080) and includes a basic GET route that responds with 'Hello, Service!'.

The script checks if the Pode module exists locally and imports it; otherwise, it imports Pode from the system.

To test the Pode server's HTTP endpoint:
    Invoke-RestMethod -Uri http://localhost:8080/ -Method Get
    # Response: 'Hello, Service!'

## [HelloServices](https://github.com/Badgerati/Pode/blob/develop/examples/HelloService/HelloServices.ps1)

**Synopsis**

Script to manage multiple Pode services and set up a basic Pode server.

**Description**

This script registers, starts, stops, queries, and unregisters multiple Pode services based on the specified hashtable.
Additionally, it sets up a Pode server that listens on a defined port and includes routes to handle incoming HTTP requests.

The script checks if the Pode module exists in the local path and imports it; otherwise, it uses the system-wide Pode module.

## [HelloWorld](https://github.com/Badgerati/Pode/blob/develop/examples/HelloWorld/HelloWorld.ps1)

**Synopsis**

PowerShell script to set up a Pode server with a simple GET endpoint.

**Description**

This script sets up a Pode server that listens on port 8080. It includes a single route for GET requests
to the root path ('/') that returns a simple text response.

## [IIS-Example](https://github.com/Badgerati/Pode/blob/develop/examples/IIS-Example.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with logging and task scheduling.

**Description**

This script sets up a Pode server listening on port 8081, enables terminal logging for requests and errors,
and includes a scheduled task. The server has two routes: one for a simple JSON response and another to
invoke a task that demonstrates delayed execution.

## [Logging](https://github.com/Badgerati/Pode/blob/develop/examples/Logging.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with configurable logging, view engine, and various routes.

**Description**

This script sets up a Pode server listening on port 8081, configures a view engine, and allows for different
types of request logging (terminal, file, custom). It includes routes for serving a web page, simulating a
server error, and downloading a file.

## [Looping-Service](https://github.com/Badgerati/Pode/blob/develop/examples/Looping-Service.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with interval-based service handlers.

**Description**

This script sets up a Pode server that runs with a specified interval, adding service handlers
that execute at each interval. The handlers include logging messages to the terminal and using
lock mechanisms.

## [Mail-Server](https://github.com/Badgerati/Pode/blob/develop/examples/Mail-Server.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with SMTP and SMTPS protocols.

**Description**

This script sets up a Pode server listening on SMTP (port 25) and SMTPS (with explicit and implicit TLS).
It includes logging for errors and debug information and demonstrates handling incoming SMTP emails with
potential attachments.

## [Middleware](https://github.com/Badgerati/Pode/blob/develop/examples/Middleware.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with rate limiting and middleware.

**Description**

This script sets up a Pode server listening on port 8081 with various middleware implementations
and rate limiting for incoming requests. It includes middleware for route-specific logic, blocking
specific user agents, and rejecting requests from certain IP addresses.

## [OneOff-Script](https://github.com/Badgerati/Pode/blob/develop/examples/OneOff-Script.ps1)

**Synopsis**

A simple PowerShell script to set up a Pode server and log a message.

**Description**

This script sets up a Pode server, enables terminal logging for errors, and writes a "hello, world!" message to the terminal.
The server runs the logic once and then exits.

## [OpenApi-SimplePotato](https://github.com/Badgerati/Pode/blob/develop/examples/OpenApi-SimplePotato.ps1)

**Synopsis**

Sets up a Pode server with OpenAPI documentation, request logging, and routes for handling 'potato' requests.

**Description**

This script configures a Pode server to listen on a specified port, enables both request and error logging,
and sets up OpenAPI documentation. It defines routes for fetching 'potato' data with responses in both
JSON and plain text. OpenAPI documentation is exposed via Swagger and other viewers.

## [OpenApi-TuttiFrutti](https://github.com/Badgerati/Pode/blob/develop/examples/OpenApi-TuttiFrutti.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with OpenAPI 3.0 and 3.1 specifications.

**Description**

This script sets up a Pode server listening on ports 8081 and 8082 with OpenAPI 3.0 and 3.1 specifications.
It includes multiple endpoints, OpenAPI documentation, various route definitions, authentication schemes,
and middleware for enhanced API functionality.

## [Petstore-OpenApi](https://github.com/Badgerati/Pode/blob/develop/examples/PetStore/Petstore-OpenApi.ps1)

**Synopsis**

PowerShell script to set up a Pode server for a Pet Store API using OpenAPI 3.0 specifications.

**Description**

This script sets up a Pode server that listens on a specified port and uses OpenAPI 3.0 specifications
for defining the API. It supports multiple endpoints for managing pets, orders, and users with various
authentication methods including API key, Basic, and OAuth2.

This example shows how to use session persistent authentication using Windows Active Directory.
The example used here is Form authentication, sent from the <form> in HTML.

Navigating to the 'http://localhost:8081' endpoint in your browser will auto-redirect you to the '/login'
page. Here, you can type the details for a domain user. Clicking 'Login' will take you back to the home
page with a greeting and a view counter. Clicking 'Logout' will purge the session and take you back to
the login page.

## [Petstore-OpenApiMultiTag](https://github.com/Badgerati/Pode/blob/develop/examples/PetStore/Petstore-OpenApiMultiTag.ps1)

**Synopsis**

Sets up a Pode server for a Pet Store API with OpenAPI 3.0 and 3.1 specifications.

**Description**

This script configures a Pode server to serve a Pet Store API using OpenAPI 3.0 and 3.1 specifications.
It includes multiple endpoints for managing pets, orders, and users, with support for different authentication
methods such as API key, Basic, and OAuth2. The server also supports session persistent authentication using
Windows Active Directory and provides OpenAPI documentation viewers.

## [Schedules-CronHelper](https://github.com/Badgerati/Pode/blob/develop/examples/Schedules-CronHelper.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with HTTP endpoints and a scheduled task.

**Description**

This script sets up a Pode server listening on port 8081 with a scheduled task that runs every 2 minutes.
It includes an endpoint for GET requests.

## [Schedules-LongRunning](https://github.com/Badgerati/Pode/blob/develop/examples/Schedules-LongRunning.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with multiple scheduled tasks.

**Description**

This script sets up a Pode server listening on port 8081 with multiple scheduled tasks. Each task runs every minute
and sleeps for a random duration between 5 and 40 seconds. The maximum concurrency for schedules is set to 30.

## [Schedules-Routes](https://github.com/Badgerati/Pode/blob/develop/examples/Schedules-Routes.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with dynamic schedule creation.

**Description**

This script sets up a Pode server listening on port 8081 with the ability to create new schedules dynamically via an API route.
The server is configured with schedule pooling enabled, and includes an endpoint to create a new schedule that runs every minute.

## [Schedules](https://github.com/Badgerati/Pode/blob/develop/examples/Schedules.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with various scheduled tasks.

**Description**

This script sets up a Pode server listening on port 8081 with multiple schedules configured.
It demonstrates scheduling using predefined cron expressions, schedules from files,
multiple cron expressions, and scheduling at specific times.
Additionally, it includes a route to invoke a schedule's logic ad-hoc with arguments.

## [ServerFrom-File](https://github.com/Badgerati/Pode/blob/develop/examples/ServerFrom-File.ps1)

**Synopsis**

A sample PowerShell script to set up a basic Pode server.

**Description**

This script sets up a Pode server using a server definition from an external script file. The server listens on port 8081, logs errors to the terminal, uses the Pode view engine, and includes a timer and a route for HTTP GET requests.

## [Session-Data](https://github.com/Badgerati/Pode/blob/develop/examples/Session-Data.ps1)

**Synopsis**

Demonstrates session management using Pode with basic authentication.

**Description**

This script sets up a Pode web server with a basic authentication endpoint. It tracks user sessions and
increments a session counter each time the endpoint is accessed.

## [Shared-State](https://github.com/Badgerati/Pode/blob/develop/examples/Shared-State.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with state management and logging.

**Description**

This script sets up a Pode server that listens on port 8081, logs requests and errors to the terminal, and manages state using timers and routes. The server initializes state from a JSON file, updates state periodically using timers, and provides routes to interact with the state.

## [Shared-ThreadSafeState](https://github.com/Badgerati/Pode/blob/develop/examples/Shared-ThreadSafeState.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with thread-safe state management and logging.

**Description**

This script sets up a Pode server that listens on port 8081, logs requests and errors to the terminal, and manages state using thread-safe collections such as `ConcurrentDictionary` and `ConcurrentBag`. The server initializes state from a JSON file, updates state periodically using timers, and provides routes to interact with the state.

## [Suspend-Resume](https://github.com/Badgerati/Pode/blob/develop/examples/Suspend-Resume.ps1)

**Synopsis**

Initializes and starts a Pode server with OpenAPI support, scheduling, and error logging.

**Description**

This script sets up a Pode server with multiple features including:
- HTTP, HTTPS, TCP, SMTP, and WebSocket endpoints.
- OpenAPI documentation and viewers for API specifications.
- Error logging to the terminal.
- Task and schedule management.
- Signal and verb-based routes for custom protocols.
- Session management.

It demonstrates various functionalities provided by Pode, including OpenAPI integrations, signal routes, and scheduled tasks.

## [Swagger-Editor](https://github.com/Badgerati/Pode/blob/develop/examples/SwaggerEditor/Swagger-Editor.ps1)

**Synopsis**

Sets up a Pode server to serve the Swagger editor and static files.

**Description**

This script configures a Pode server to listen on a specified port (default is 8081) and serve the Swagger editor
and other static files. It enables request and error logging and sets up a view engine for rendering HTML.

## [Tasks](https://github.com/Badgerati/Pode/blob/develop/examples/Tasks.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with task management and logging.

**Description**

This script sets up a Pode server that listens on port 8081, logs errors to the terminal, and handles both synchronous and asynchronous tasks. The server provides routes to interact with the tasks and demonstrates task invocation and waiting.

## [Tcp-Server](https://github.com/Badgerati/Pode/blob/develop/examples/Tcp-Server.ps1)

**Synopsis**

A PowerShell script to set up a Pode TCP server with multiple endpoints and error logging.

**Description**

This script sets up a Pode TCP server that listens on multiple endpoints, logs errors to the terminal, and handles incoming TCP requests with specific verbs.
The server provides handlers for 'HELLO', 'HELLO2', 'HELLO3', 'QUIT', and a catch-all handler for unrecognized verbs.
It also demonstrates reading client input and responding accordingly.

## [Tcp-ServerAuth](https://github.com/Badgerati/Pode/blob/develop/examples/Tcp-ServerAuth.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode TCP server with role-based access control and logging.

**Description**

This script sets up a Pode TCP server that listens on port 8081, logs errors to the terminal, and implements role-based access control. The server provides an endpoint that restricts access based on user roles retrieved from a database.

## [Tcp-ServerHttp](https://github.com/Badgerati/Pode/blob/develop/examples/Tcp-ServerHttp.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode TCP server with multiple endpoints and error logging.

**Description**

This script sets up a Pode TCP server that listens on port 8081, logs errors to the terminal, and handles incoming HTTP requests. The server provides a catch-all handler for HTTP requests and returns a basic HTML response.

## [Tcp-ServerMultiEndpoint](https://github.com/Badgerati/Pode/blob/develop/examples/Tcp-ServerMultiEndpoint.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode TCP server with multiple endpoints and error logging.

**Description**

This script sets up a Pode TCP server that listens on multiple endpoints, logs errors to the terminal, and handles incoming TCP requests with specific verbs. The server provides handlers for 'HELLO' and 'Quit' verbs and a catch-all handler for unrecognized verbs.

## [Threading](https://github.com/Badgerati/Pode/blob/develop/examples/Threading.ps1)

**Synopsis**

A PowerShell script to set up a Pode server with various lock mechanisms including custom locks, mutexes, and semaphores.

**Description**

This script sets up a Pode server that listens on a specified port and demonstrates the usage of lockables, mutexes, and semaphores for thread synchronization.
It includes routes that showcase the behavior of these synchronization mechanisms in different scopes (self, local, and global).
The server provides multiple routes to test custom locks, mutexes, and semaphores by simulating delays and concurrent access.

## [Timers-Route](https://github.com/Badgerati/Pode/blob/develop/examples/Timers-Route.ps1)

**Synopsis**

A PowerShell script to set up a basic Pode server with timer functionality.

**Description**

This script sets up a Pode server that listens on a specified port and allows the creation of timers via HTTP routes.
It includes a route to create a new timer that runs a specified script block at defined intervals.

## [Timers](https://github.com/Badgerati/Pode/blob/develop/examples/Timers.ps1)

**Synopsis**

A PowerShell script to set up a Pode server with various timer configurations.

**Description**

This script sets up a Pode server that listens on a specified port and creates multiple timers with different behaviors.
It includes routes to create new timers via HTTP requests and invoke existing timers on demand.

## [Web-Cookies](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Cookies.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with cookie management and signed cookies.

**Description**

This script sets up a Pode server listening on port 8081. It includes routes for setting, extending,
removing, and checking signed cookies. The server uses a global cookie secret for signing the cookies.

## [Web-Csrf](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Csrf.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with CSRF protection using either session or cookie-based tokens.

**Description**

This script sets up a Pode server listening on port 8081. It includes CSRF protection, which can be configured
to use either session-based tokens or cookie-based global secrets. The script also sets up a basic route for
serving an index page with a CSRF token and a POST route to handle form submissions.

## [Web-FuncsToRoutes](https://github.com/Badgerati/Pode/blob/develop/examples/Web-FuncsToRoutes.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with basic authentication and dynamic route generation.

**Description**

This script sets up a Pode server listening on port 8081. It includes basic authentication, error logging,
and dynamic route generation for specified commands. Each route requires authentication.

## [Web-Gui](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Gui.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with desktop GUI capabilities.

**Description**

This script sets up a Pode server listening on ports 8081 and 8091. It includes a route to handle GET requests
and sets up the server to run as a desktop GUI application using the Pode view engine.

## [Web-GzipRequest](https://github.com/Badgerati/Pode/blob/develop/examples/Web-GzipRequest.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with error logging and a route to handle gzip'd JSON.

**Description**

This script sets up a Pode server listening on port 8081. It includes error logging and a route to handle POST requests that receive gzip'd JSON data.

## [Web-Hostname](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Hostname.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with multiple endpoints.

**Description**

This script sets up a Pode server listening on multiple endpoints.
It demonstrates how to handle GET requests, serve static assets, and download files using Pode's view engine.

## [Web-HostnameKestrel](https://github.com/Badgerati/Pode/blob/develop/examples/Web-HostnameKestrel.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with Kestrel and various endpoints.

**Description**

This script sets up a Pode server listening on multiple endpoints using Kestrel.
It demonstrates how to handle GET requests, serve static assets, and download files using Pode's view engine.

## [Web-Imports](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Imports.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with various routes, access rules, logging, and request handling.

**Description**

This script sets up a Pode server listening on multiple endpoints with request redirection.
It demonstrates how to handle GET, POST, and other HTTP requests, set up access and limit rules,
implement custom logging, and serve web pages using Pode's view engine.

## [Web-Metrics](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Metrics.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with a route to check server uptime and restart count.

**Description**

This script sets up a Pode server listening on port 8081. It includes a route to check the server's uptime
and the number of times the server has restarted.

## [Web-Pages](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Pages.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with various routes, access rules, logging, and request handling.

**Description**

This script sets up a Pode server listening on multiple endpoints with request redirection.
It demonstrates how to handle GET, POST, and other HTTP requests, set up access and limit rules,
implement custom logging, and serve web pages using Pode's view engine.

## [Web-PagesDocker](https://github.com/Badgerati/Pode/blob/develop/examples/Web-PagesDocker.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with various routes, tasks, and security.

**Description**

This script sets up a Pode server listening on port 8081. It demonstrates how to handle GET and PUT requests,
set up security, define tasks, and use Pode's view engine.

## [Web-PagesHttps](https://github.com/Badgerati/Pode/blob/develop/examples/Web-PagesHttps.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with various HTTPS certificate options.

**Description**

This script sets up a Pode server listening on port 8443 with HTTPS enabled using different certificate options based on the input parameter.
It demonstrates how to handle GET requests and serve web pages with Pode's view engine.

## [Web-PagesKestrel](https://github.com/Badgerati/Pode/blob/develop/examples/Web-PagesKestrel.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with Kestrel and various routes, access rules, and custom logging.

**Description**

This script sets up a Pode server listening on multiple endpoints with request redirection using Kestrel.
It demonstrates how to handle GET requests, set up access rules, implement custom logging, and handle various routes including redirects and file downloads.

## [Web-PagesMD](https://github.com/Badgerati/Pode/blob/develop/examples/Web-PagesMD.ps1)

**Synopsis**

Sample script to set up a Pode server that listens on localhost:8081 and responds to GET requests.

**Description**

This script initializes a Pode server and sets it to listen on localhost:8081. It uses the Markdown
view engine to render responses. The server will respond to GET requests at the root path ('/') by
serving an 'index' view.

## [Web-PagesSimple](https://github.com/Badgerati/Pode/blob/develop/examples/Web-PagesSimple.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with multiple endpoints and request handling.

**Description**

This script sets up a Pode server listening on multiple endpoints with request redirection.
It demonstrates how to handle GET requests and redirect requests from one endpoint to another.
The script includes examples of using a parameter for the port number and setting up error logging.

## [Web-PagesUsing](https://github.com/Badgerati/Pode/blob/develop/examples/Web-PagesUsing.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with various routes, middleware, and custom functions.

**Description**

This script sets up a Pode server listening on port 8081. It demonstrates how to handle GET requests,
use middleware, export and use custom functions, and set up timers. The script includes examples of
using `$using:` scope for variables in script blocks and middleware.

## [Web-RestApi](https://github.com/Badgerati/Pode/blob/develop/examples/Web-RestApi.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with HTTP endpoints and request logging.

**Description**

This script sets up a Pode server listening on port 8081 with various HTTP endpoints for GET and POST requests.
It includes request logging with batching and dual mode for IPv4/IPv6.

## [Web-RestOpenApi](https://github.com/Badgerati/Pode/blob/develop/examples/Web-RestOpenApi.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with OpenAPI integration and basic authentication.

**Description**

This script sets up a Pode server listening on multiple endpoints with OpenAPI documentation.
It demonstrates how to handle GET, POST, and PUT requests, use OpenAPI for documenting APIs, and implement basic authentication.
The script includes routes under the '/api' path and provides various OpenAPI viewers such as Swagger, ReDoc, RapiDoc, StopLight, Explorer, and RapiPdf.

## [web-RestOpenApiFuncs](https://github.com/Badgerati/Pode/blob/develop/examples/web-RestOpenApiFuncs.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with OpenAPI integration and various OpenAPI viewers.

**Description**

This script sets up a Pode server listening on port 8081 with OpenAPI documentation.
It demonstrates how to use OpenAPI for documenting APIs and provides various OpenAPI viewers such as Swagger, ReDoc, RapiDoc, StopLight, Explorer, and RapiPdf.

## [Web-RestOpenApiShared](https://github.com/Badgerati/Pode/blob/develop/examples/Web-RestOpenApiShared.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with OpenAPI integration and basic authentication.

**Description**

This script sets up a Pode server listening on multiple endpoints with OpenAPI documentation.
It demonstrates how to handle GET and POST requests, use OpenAPI for documenting APIs, and implement basic authentication.
The script includes routes under the '/api' path and provides various OpenAPI viewers such as Swagger, ReDoc, RapiDoc, StopLight, Explorer, and RapiPdf.

## [Web-RestOpenApiSimple](https://github.com/Badgerati/Pode/blob/develop/examples/Web-RestOpenApiSimple.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with OpenAPI integration.

**Description**

This script sets up a Pode server listening on multiple endpoints with OpenAPI documentation.
It demonstrates how to handle GET and POST requests, and how to use OpenAPI for documenting APIs.
The script includes routes under the '/api' path and provides Swagger and ReDoc viewers.

## [Web-RouteEndpoints](https://github.com/Badgerati/Pode/blob/develop/examples/Web-RouteEndpoints.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with multiple endpoints and request handling.

**Description**

This script sets up a Pode server listening on multiple local IP addresses on port 8081.
It demonstrates how to handle GET requests for a web page, download a file, handle requests with parameters,
and redirect requests from one endpoint to another.

## [Web-RouteGroup](https://github.com/Badgerati/Pode/blob/develop/examples/Web-RouteGroup.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with middleware and basic authentication.

**Description**

This script sets up a Pode server listening on port 8081. It demonstrates how to use middleware,
route groups, and basic authentication. The server includes routes under the '/api' and '/auth' paths,
with specific middleware and authentication requirements.

## [Web-RouteListenNames](https://github.com/Badgerati/Pode/blob/develop/examples/Web-RouteListenNames.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with multiple endpoints and request handling.

**Description**

This script sets up a Pode server listening on multiple local IP addresses on port 8081.
It demonstrates how to handle GET requests for a web page, including specific handling for different endpoints,
downloading a file, and handling requests with parameters.

## [Web-RouteProtocols](https://github.com/Badgerati/Pode/blob/develop/examples/Web-RouteProtocols.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with multiple endpoints and request handling.

**Description**

This script sets up a Pode server listening on port 8081 (HTTP) and 8082 (HTTPS).
It demonstrates how to handle GET requests for a web page, download a file, and handle requests with parameters.
Additionally, it shows how to redirect all HTTP requests to HTTPS.

## [Web-Secrets](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Secrets.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with secret management using Azure Key Vault and a custom vault CLI.

**Description**

This script sets up a Pode server listening on port 8081 with secret management capabilities.
It demonstrates how to register secret vaults with Azure Key Vault and a custom CLI, set and get secrets,
and manage secrets using Pode routes. Make sure to install the Microsoft.PowerShell.SecretManagement and Microsoft.PowerShell.SecretStore modules.
Also, you need to run "Connect-AzAccount" first for Azure Key Vault.

## [Web-SecretsLocal](https://github.com/Badgerati/Pode/blob/develop/examples/Web-SecretsLocal.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with secret management using Microsoft.PowerShell.SecretStore.

**Description**

This script sets up a Pode server listening on port 8081 with secret management capabilities.
It demonstrates how to register a secret vault, set and get secrets, and manage secrets using Pode routes.
Make sure to install the Microsoft.PowerShell.SecretManagement and Microsoft.PowerShell.SecretStore modules.

## [Web-SelfSigned](https://github.com/Badgerati/Pode/blob/develop/examples/Web-SelfSigned.ps1)

**Synopsis**

A sample PowerShell script to set up a HTTPS Pode server with a self-sign certificate

**Description**

This script sets up a Pode server listening on port 8081 in HTTPS

## [Web-Sessions](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Sessions.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with session persistent authentication.

**Description**

This script sets up a Pode server listening on port 8085 with session persistent authentication.
It demonstrates a simple server setup with a view counter. Each visit to the root URL ('http://localhost:8085')
increments the view counter stored in the session.

## [Web-Signal](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Signal.ps1)

**Synopsis**

PowerShell script to set up a Pode server with various endpoints and error logging.

**Description**

This script sets up a Pode server that listens on a specified port and provides both HTTP and WebSocket
endpoints. It demonstrates how to set up WebSockets in Pode and logs errors and other request details
to the terminal.

## [Web-SignalConnection](https://github.com/Badgerati/Pode/blob/develop/examples/Web-SignalConnection.ps1)

**Synopsis**

Sample script to set up a Pode server with WebSocket support, listening on localhost.

**Description**

This script initializes a Pode server that listens on localhost:8081 with WebSocket support.
It includes logging to the terminal and several routes and timers for WebSocket connections.
The server can connect to a WebSocket from an external script and respond to messages.

## [Web-SimplePages](https://github.com/Badgerati/Pode/blob/develop/examples/Web-SimplePages.ps1)

**Synopsis**

PowerShell script to set up a Pode server with various pages and error logging.

**Description**

This script sets up a Pode server that listens on a specified port and provides several routes
to display process and service information, as well as static views.

## [Web-Sockets](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Sockets.ps1)

**Synopsis**

PowerShell script to set up a Pode server with HTTPS and logging.

**Description**

This script sets up a Pode server that listens on a specified port with HTTPS protocol using a certificate.
It includes request logging and provides a sample route to return a JSON response.

## [Web-Sse](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Sse.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server with Server-Sent Events (SSE) and logging.

**Description**

This script sets up a Pode server that listens on port 8081, logs errors to the terminal, and handles Server-Sent Events (SSE) connections. The server sends periodic SSE events and provides routes to interact with SSE connections.

## [Web-Static](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Static.ps1)

**Synopsis**

PowerShell script to set up a Pode server with various routes for static assets and view responses.

**Description**

This script sets up a Pode server that listens on a specified port, logs requests and errors to the terminal,
and serves static assets as well as view responses using the Pode view engine.

## [Web-StaticAuth](https://github.com/Badgerati/Pode/blob/develop/examples/Web-StaticAuth.ps1)

**Synopsis**

PowerShell script to set up a Pode server with basic authentication and various routes for static assets and view responses.

**Description**

This script sets up a Pode server that listens on a specified port, logs requests and errors to the terminal,
and serves static assets as well as view responses using the Pode view engine. It also includes basic authentication
for accessing static assets.

## [Web-TpEPS](https://github.com/Badgerati/Pode/blob/develop/examples/Web-TpEPS.ps1)

**Synopsis**

PowerShell script to set up a Pode server with EPS view engine.

**Description**

This script sets up a Pode server that listens on a specified port, logs requests to the terminal,
and uses the EPS renderer for serving web pages.

## [Web-TpPSHTML](https://github.com/Badgerati/Pode/blob/develop/examples/Web-TpPSHTML.ps1)

**Synopsis**

PowerShell script to set up a Pode server with PSHTML view engine.

**Description**

This script sets up a Pode server that listens on a specified port, logs requests to the terminal,
and uses the PSHTML renderer for serving web pages.

## [Web-Upload](https://github.com/Badgerati/Pode/blob/develop/examples/Web-Upload.ps1)

**Synopsis**

PowerShell script to set up a Pode server with file upload routes.

**Description**

This script sets up a Pode server that listens on a specified port and provides routes
for uploading single and multiple files.

## [Web-UploadKestrel](https://github.com/Badgerati/Pode/blob/develop/examples/Web-UploadKestrel.ps1)

**Synopsis**

PowerShell script to set up a Pode server with Kestrel listener and file upload functionality.

**Description**

This script sets up a Pode server that listens on a specified port using the Kestrel listener type.
It serves a web page for file upload and processes file uploads, saving them to the server.

## [WebHook](https://github.com/Badgerati/Pode/blob/develop/examples/WebHook.ps1)

**Synopsis**

A sample PowerShell script to set up a webhook server using Pode.

**Description**

This script sets up a webhook server using Pode. It includes endpoints for storing data,
subscribing to webhook events, and unsubscribing from webhook events. It also defines
an OpenAPI specification for the server and enables Swagger documentation.

## [WebNunit-RestApi](https://github.com/Badgerati/Pode/blob/develop/examples/WebNunit-RestApi.ps1)

**Synopsis**

A sample PowerShell script to set up a Pode server for running NUnit tests.

**Description**

This script sets up a Pode server listening on port 8081 with a POST endpoint for running NUnit tests.
It accepts JSON data specifying the test DLL path and the tests to run, executes the tests using NUnit,
and returns the test results as an XML response.

## [Write-Response](https://github.com/Badgerati/Pode/blob/develop/examples/Write-Response.ps1)

**Synopsis**

PowerShell script to set up a Pode server with various routes for different response types.

**Description**

This script sets up a Pode server that listens on a specified port and provides various routes to
retrieve process information in different formats (HTML, Text, CSV, JSON, XML, YAML).



## What is Spring Boot Actuator?
In essence, Actuator brings production-ready features to our application.

Monitoring our app, gathering metrics, understanding traffic or the state of our database becomes trivial with this dependency.

Here are some of the most common endpoints Boot provides out of the box:

-   _/health_ – Shows application health information (a simple _‘status’_ when accessed over an unauthenticated connection or full message details when authenticated); it’s not sensitive by default
-   _/info –_ Displays arbitrary application info; not sensitive by default
-   _/metrics –_ Shows ‘metrics’ information for the current application; it’s also sensitive by default
-   _/trace –_ Displays trace information (by default the last few HTTP requests)



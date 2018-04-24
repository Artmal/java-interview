## What are interceptors in Spring MVC?
Spring MVC provides a powerful mechanism to intercept an http request. Similar to Servlet filter, Spring MVC provides a way to define special classes called interceptors that gets called before and after request is served.

Each interceptor you define must implement `HandlerInterceptor`.
There are three methods that need to be implemented.

 - `preHandle(..)` is called before the actual handler is executed;

The preHandle(..) method returns a boolean value. You can use this method to break or continue the processing of the execution chain. When this method returns true, the handler execution chain will continue; when it returns false, the `DispatcherServlet` assumes the interceptor itself has taken care of requests (and, for example, rendered an appropriate view) and does not continue executing the other interceptors and the actual handler in the execution chain.

 - `postHandle(..)` is called after the handler is executed;
 - `afterCompletion(..)` is called after the complete request has finished.

Interceptors allow you to perform tasks that are common to every request or set of requests without the need to cut ‘n’ paste boiler plate code into every controller class.

For example, you could perform user authentication of a request before it reaches your controller and, if successful, retrieve some additional user details from a database adding them to the HttpServletRequest object before your controller is called. Your controller can then simply retrieve and use these values or leave them for display by the JSP. On the other hand, if the authentication fails, you could re-direct your user to a different page.

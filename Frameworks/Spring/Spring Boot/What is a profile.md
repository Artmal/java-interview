## What is a profile?
Spring profiles provide a way to segregate parts of your application configuration and make it be available only in certain environments. 

Any `@Component` or `@Configuration` can be marked with @Profile to limit when it is loaded, as shown in the following example:

    @Configuration
    @Profile("production")
    public class ProductionConfiguration {
    
    	// ...
    
    }

You can use a spring.profiles.active property to specify which profiles are active. Or you can use command line/intellji idea configuration.

## Basic Swagger configuration
1. Include swagger2 and swagger-ui dependencies:
```
<dependency>  
 <groupId>io.springfox</groupId>  
 <artifactId>springfox-swagger2</artifactId>  
 <version>2.9.2</version>  
</dependency>
```
2. Configure Docket bean:
```
@Configuration  
@EnableSwagger2  
public class SwaggerConfig {  
    @Bean  
    public Docket api() {  
        return new Docket(DocumentationType.SWAGGER_2)  
                .select()  
                .apis(RequestHandlerSelectors.any())  
                .paths(PathSelectors.any())  
                .build();  
  }  
}
```

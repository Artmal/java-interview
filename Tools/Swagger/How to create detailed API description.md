## How to create detailed API description?
The default generated API docs are gooed but they lack detailed API level information. Swagger has provided few annotations to add this detailed information to the APIs. e.g.
1. @Api - We can add this Annotation to the controller to add basic information regarding the controller.
```
@Api(value = "Swagger2DemoRestController", description = "REST APIs related to Student Entity!!!!")
@RestController
public class Swagger2DemoRestController {
    ...
}
```
2. `@ApiOperation` and `@ApiResponses` - We can add these annotations to any rest method in the controller to add basic information related to that method. e.g.
 ```
 @ApiOperation(value = "Get list of Students in the System ", response = Iterable.class, tags = "getStudents")  
@ApiResponses(value = {  
        @ApiResponse(code = 200, message = "Success|OK"),  
  @ApiResponse(code = 401, message = "not authorized!"),  
  @ApiResponse(code = 403, message = "forbidden!!!"),  
  @ApiResponse(code = 404, message = "not found!!!") })  
  
@RequestMapping(value = "/getStudents")  
public List<Student> getStudents() {  
    return students;  
}
```
3. `ApiModelProperty` - This annotation is used in the Model property to add some description to the Swagger output for that model attribute. e.g.
```
@ApiModelProperty(notes = "Name of the Student",name="name",required=true,value="test name")  
private String name;
```

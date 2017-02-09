INSTRUCTIONS / NOTES:

/* This project was created by following a TeamTreeHouse track: Java Web Development. */

A. Definitions:

1. H2 - allows for multiple database connectivity settings:
    1.1. in memory DB that are created/destroyed and held entirely in memory
    1.2. portable single file db that don't require server
    1.3. full server-based DB, which require server

2. @Bean - object instances that are managed by the Spring container; created/wired by the framework and put into
    a "bag of objects" for later use

3. @Service - annotation for service (interface) implementation. All "business logic" should go here.

4. @Repository - annotation for all DAO (data access objects). All database access logic should go here.

5. @Component - all other generic components.

6. @Autowired - calls instance of other beans into the classes. Basically, instantiates an object.

7. @Controller - for all the controller classes

8. @RequestMapping - redirects a certain URL to this method/class

9. @PathVariable - used in conjunction with RequestMapping("{variable}") to make map URI dynamic

10. @NotNull - applied to a variable declaration to make sure that it is not empty when submitted

11. @Size(min = 3, max = 10) - applied to a variable to set length constraints

12. @Pattern(regex = "regex") - regex pattern constraint

13. @Valid - add before parameter object type in method signature to make sure that each parameter meets constraints
    13.1. Make sure to add BindingResult result to the method sig and use result.hasErrors() to react accordingly.

14. @RequestParam - applied to a controller method's parameter to indicated that the value should come from a request parameter



B. how to get the database up and running:

1. Open up terminal into project classpath
2. "$java -cp h2-1.4.190.jar org.h2.tools.Server"
3. That should open up a new window; paste the app.properties url, username, and password
4. Connect. Your server is officially up and running!


C. Three layers of GifLib:

1. Web Layer - consists of controllers or anything else the specifically serves web content
2. Data Access Layer - data access objects (DAO) that have a corresponding entity class. The sole purpose is to interact with hibernate
3. Service Layer - a controller that makes any necessary calls to the DAO. Also does any computation outside of the realm of the model object

- The three layers will be represented as packages that are tightly controlled and loosely coupled; in other words, any interaction between
    the layers will take place in interfaces as opposed to classes


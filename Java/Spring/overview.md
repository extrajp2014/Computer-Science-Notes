# Dependency Injection Annotations

| Annotation        | Description                                       |
| ----------------- | ------------------------------------------------- |
| `@Component`      | Generic Spring-managed bean                       |
| `@Service`        | Service layer bean                                |
| `@Repository`     | Persistence layer bean                            |
| `@Controller`     | MVC controller                                    |
| `@RestController` | REST controller (`@Controller` + `@ResponseBody`) |
| `@Configuration`  | Configuration class                               |
| `@Bean`           | Declare a Spring bean                             |
| `@Autowired`      | Inject dependency                                 |
| `@Qualifier`      | Select a specific bean                            |
| `@Primary`        | Preferred bean implementation                     |
| `@Lazy`           | Lazy initialization                               |
| `@Value`          | Inject property value                             |
| `@Scope`          | Define bean scope                                 |
| `@DependsOn`      | Bean dependency ordering                          |
| `@Import`         | Import configuration                              |
| `@Profile`        | Activate bean by profile                          |

---

# Spring Boot Annotations

| Annotation                       | Description                   |
| -------------------------------- | ----------------------------- |
| `@SpringBootApplication`         | Main Spring Boot application  |
| `@EnableAutoConfiguration`       | Enable auto-configuration     |
| `@ConfigurationProperties`       | Bind configuration properties |
| `@EnableConfigurationProperties` | Enable property binding       |
| `@ConfigurationPropertiesScan`   | Scan configuration classes    |
| `@SpringBootTest`                | Integration testing           |
| `@TestConfiguration`             | Test-only configuration       |

---

# Web MVC Annotations

| Annotation              | Description              |
| ----------------------- | ------------------------ |
| `@RequestMapping`       | Map HTTP requests        |
| `@GetMapping`           | HTTP GET endpoint        |
| `@PostMapping`          | HTTP POST endpoint       |
| `@PutMapping`           | HTTP PUT endpoint        |
| `@DeleteMapping`        | HTTP DELETE endpoint     |
| `@PatchMapping`         | HTTP PATCH endpoint      |
| `@RequestParam`         | Query parameter          |
| `@PathVariable`         | URL path variable        |
| `@RequestBody`          | Request body             |
| `@ResponseBody`         | Return response body     |
| `@RequestHeader`        | HTTP header              |
| `@CookieValue`          | Cookie value             |
| `@MatrixVariable`       | Matrix parameter         |
| `@RequestPart`          | Multipart request        |
| `@CrossOrigin`          | Enable CORS              |
| `@ResponseStatus`       | Set HTTP status          |
| `@ControllerAdvice`     | Global controller advice |
| `@RestControllerAdvice` | REST exception advice    |
| `@ExceptionHandler`     | Exception handler        |
| `@InitBinder`           | Register data binder     |
| `@ModelAttribute`       | Model attribute          |

---

# Validation Annotations

| Annotation        | Description                 |
| ----------------- | --------------------------- |
| `@Valid`          | Trigger validation          |
| `@Validated`      | Spring validation           |
| `@NotNull`        | Value required              |
| `@NotBlank`       | Non-empty string            |
| `@NotEmpty`       | Non-empty collection/string |
| `@Size`           | Size constraint             |
| `@Min`            | Minimum value               |
| `@Max`            | Maximum value               |
| `@Positive`       | Positive number             |
| `@PositiveOrZero` | Positive or zero            |
| `@Negative`       | Negative number             |
| `@Email`          | Email validation            |
| `@Pattern`        | Regular expression          |
| `@Past`           | Past date                   |
| `@Future`         | Future date                 |

---

# Transaction Annotations

| Annotation                     | Description            |
| ------------------------------ | ---------------------- |
| `@Transactional`               | Transaction management |
| `@EnableTransactionManagement` | Enable transactions    |

---

# Scheduling Annotations

| Annotation          | Description            |
| ------------------- | ---------------------- |
| `@EnableScheduling` | Enable scheduler       |
| `@Scheduled`        | Scheduled task         |
| `@Async`            | Execute asynchronously |
| `@EnableAsync`      | Enable async execution |

---

# Caching Annotations

| Annotation       | Description               |
| ---------------- | ------------------------- |
| `@EnableCaching` | Enable cache              |
| `@Cacheable`     | Cache method result       |
| `@CachePut`      | Update cache              |
| `@CacheEvict`    | Remove cache entry        |
| `@Caching`       | Multiple cache operations |

---

# Security Annotations

| Annotation                 | Description                    |
| -------------------------- | ------------------------------ |
| `@EnableWebSecurity`       | Enable Spring Security         |
| `@EnableMethodSecurity`    | Enable method security         |
| `@PreAuthorize`            | Authorization before execution |
| `@PostAuthorize`           | Authorization after execution  |
| `@Secured`                 | Role-based security            |
| `@RolesAllowed`            | JSR-250 role security          |
| `@AuthenticationPrincipal` | Inject authenticated user      |

---

# Spring Data JPA Interfaces

| Interface                    | Description           |
| ---------------------------- | --------------------- |
| `CrudRepository`             | Basic CRUD operations |
| `PagingAndSortingRepository` | CRUD with pagination  |
| `JpaRepository`              | Full JPA repository   |
| `JpaSpecificationExecutor`   | Dynamic queries       |
| `QueryByExampleExecutor`     | Query by example      |

---

# Repository Annotations

| Annotation               | Description           |
| ------------------------ | --------------------- |
| `@Query`                 | Custom JPQL/SQL query |
| `@Modifying`             | Update/Delete query   |
| `@EntityGraph`           | Fetch graph           |
| `@Procedure`             | Stored procedure      |
| `@Lock`                  | Lock mode             |
| `@EnableJpaRepositories` | Enable repositories   |

---

# Bean Lifecycle Annotations

| Annotation       | Description             |
| ---------------- | ----------------------- |
| `@PostConstruct` | Initialization callback |
| `@PreDestroy`    | Cleanup callback        |

---

# Event Annotations

| Annotation                    | Description                      |
| ----------------------------- | -------------------------------- |
| `@EventListener`              | Listen for application events    |
| `@TransactionalEventListener` | Transaction-aware event listener |

---

# Testing Annotations

| Annotation              | Description           |
| ----------------------- | --------------------- |
| `@SpringBootTest`       | Full application test |
| `@WebMvcTest`           | MVC slice test        |
| `@DataJpaTest`          | JPA slice test        |
| `@JdbcTest`             | JDBC slice test       |
| `@JsonTest`             | JSON slice test       |
| `@MockBean`             | Mock Spring bean      |
| `@SpyBean`              | Spy Spring bean       |
| `@AutoConfigureMockMvc` | Configure MockMvc     |

---

# Common Spring Interfaces

| Interface                   | Description             |
| --------------------------- | ----------------------- |
| `ApplicationContext`        | Spring container        |
| `BeanFactory`               | Bean factory            |
| `Environment`               | Environment properties  |
| `Resource`                  | Abstract resource       |
| `ApplicationEventPublisher` | Publish events          |
| `InitializingBean`          | Initialization callback |
| `DisposableBean`            | Destruction callback    |
| `ApplicationRunner`         | Execute after startup   |
| `CommandLineRunner`         | Startup runner          |

---

# Common Spring Classes

| Class                | Description                  |
| -------------------- | ---------------------------- |
| `RestTemplate`       | Blocking HTTP client         |
| `WebClient`          | Reactive HTTP client         |
| `ResponseEntity`     | HTTP response wrapper        |
| `HttpHeaders`        | HTTP headers                 |
| `HttpEntity`         | HTTP request/response entity |
| `ModelAndView`       | MVC model and view           |
| `BeanUtils`          | Bean utility methods         |
| `ReflectionUtils`    | Reflection helpers           |
| `StringUtils`        | String utilities             |
| `CollectionUtils`    | Collection utilities         |
| `ObjectUtils`        | Object utilities             |
| `FileSystemResource` | File resource                |
| `ClassPathResource`  | Classpath resource           |

---

# Bean Scopes

| Scope         | Description              |
| ------------- | ------------------------ |
| `singleton`   | Single instance          |
| `prototype`   | New instance per request |
| `request`     | HTTP request scope       |
| `session`     | HTTP session scope       |
| `application` | Servlet context scope    |
| `websocket`   | WebSocket scope          |

---

# Spring Boot CLI Commands

| Command            | Description              |
| ------------------ | ------------------------ |
| `spring run`       | Run a Spring application |
| `spring test`      | Execute tests            |
| `spring jar`       | Create executable JAR    |
| `spring init`      | Generate new project     |
| `spring install`   | Install CLI extension    |
| `spring uninstall` | Remove CLI extension     |
| `spring version`   | Display CLI version      |
| `spring help`      | Show help                |
| `spring shell`     | Start interactive shell  |

---

# Maven Commands for Spring

| Command               | Description                 |
| --------------------- | --------------------------- |
| `mvn spring-boot:run` | Run application             |
| `mvn clean`           | Remove build output         |
| `mvn compile`         | Compile project             |
| `mvn test`            | Execute tests               |
| `mvn package`         | Build JAR/WAR               |
| `mvn install`         | Install to local repository |
| `mvn verify`          | Run verification lifecycle  |
| `mvn dependency:tree` | Show dependencies           |

---

# Gradle Commands for Spring

| Command                  | Description           |
| ------------------------ | --------------------- |
| `./gradlew bootRun`      | Run application       |
| `./gradlew build`        | Build project         |
| `./gradlew clean`        | Clean project         |
| `./gradlew test`         | Run tests             |
| `./gradlew bootJar`      | Create executable JAR |
| `./gradlew bootWar`      | Create executable WAR |
| `./gradlew dependencies` | Show dependency graph |

---

# Configuration Files

| File                               | Description                         |
| ---------------------------------- | ----------------------------------- |
| `application.properties`           | Application configuration           |
| `application.yml`                  | YAML configuration                  |
| `application-{profile}.properties` | Profile-specific configuration      |
| `application-{profile}.yml`        | Profile-specific YAML configuration |
| `banner.txt`                       | Custom startup banner               |
| `logback-spring.xml`               | Logback configuration               |
| `log4j2-spring.xml`                | Log4j2 configuration                |

---

# Common Configuration Properties

| Property                                    | Description                |
| ------------------------------------------- | -------------------------- |
| `server.port`                               | HTTP server port           |
| `server.address`                            | Bind address               |
| `spring.application.name`                   | Application name           |
| `spring.profiles.active`                    | Active profile             |
| `spring.datasource.url`                     | Database URL               |
| `spring.datasource.username`                | Database username          |
| `spring.datasource.password`                | Database password          |
| `spring.jpa.hibernate.ddl-auto`             | Schema generation strategy |
| `spring.jpa.show-sql`                       | Log SQL statements         |
| `logging.level.*`                           | Logging level              |
| `management.endpoints.web.exposure.include` | Expose Actuator endpoints  |

---

# Spring Expression Language (SpEL)

| Expression  | Description              |
| ----------- | ------------------------ |
| `#{...}`    | SpEL expression          |
| `${...}`    | Property placeholder     |
| `T(Class)`  | Reference Java type      |
| `@beanName` | Reference Spring bean    |
| `?.`        | Safe navigation operator |
| `?:`        | Elvis operator           |
| `.?[]`      | Collection selection     |
| `.![ ]`     | Collection projection    |
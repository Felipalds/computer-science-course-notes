https://docs.spring.io/spring-framework/reference/overview.html

## @Configuration:
Indicate that a class is a source of bean definitions.
@Configuration classes generates @Bean
https://docs.spring.io/spring-framework/reference/core/beans/java/basic-concepts.html

## @Bean:
Object that is instantiated, assembled and managed by Spring IoC (Inversion of Control) container. Beans are the backbone of a Spring application, managed by a @Configuration class.
They are created, configured and managed by Spring IoC container.

## @Value
Value does not works with static values. The @Value is processed in runtime, to inject values to the class. But static puts it in the class, not in the instances. As result, spring cannot inject static values.
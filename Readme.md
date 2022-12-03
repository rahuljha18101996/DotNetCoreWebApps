.Net Core:
Buit on top of .Net MVC and it is very robust.

Advantages of .Net Core:
- Fast and Open Source
- Cross Platform > Window, Linux
- Built In Dependency Injection
- Easy Update
- Cloud Friendly
- High Performance

Dependency Injection:
Dependency injection is a design pattern in which classes are not allowed to create dependencies. Rather, they request dependencies from external sources. This design pattern strongly holds that a class should not configure its dependencies statically.

It is an integral part of ASP .Net Core Architecture. .Net Core inject object of dependency classes to constructor using the built in IoC Container.

Advantages of DI:
- Loose Coupling / More flexibity
- Security
- Improves code reusability.
- Eases the unit testing of applications through mocking/stubbing injected dependencies.
- Makes it easier to extend the application classes.
- Enhances the configuration of applications

Note : We have to register the concrete class so that IoC container can inject object.
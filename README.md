## Web application security for developers: tooling and best practices

Presentation by [Luuk Buit](https://twitter.com/lwkbuit) JavaOne 2017.

## Tooling

**Firefox**

Settings > Advanced > Network > Connection settings > Manual proxy:

- localhost:9876 for all protocols
- remove localhost/127.0.0.1 from "No Proxy for:"

**[OWASP Zap Proxy](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project)**

Options > Local Proxy > localhost:9876

## Background

- [OWASP ASVS](https://www.owasp.org/index.php/Category:OWASP_Application_Security_Verification_Standard_Project)
- [OWASP TOP 10](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project)
- [Web Security Fundamentals](https://www.edx.org/course/web-security-fundamentals-kuleuvenx-websecx)
- [WAHH](http://mdsec.net/wahh/)

## Demos

**[The BodgeIt Store](https://github.com/psiinon/bodgeit)**

    $ docker pull psiinon/bodgeit
    $ docker run --rm -p 8080:8080 -i -t psiinon/bodgeit

http://localhost:8080/bodgeit

**Spring Boot Sample Web Secure**

    $ git clone https://github.com/spring-projects/spring-boot.git
    $ cd spring-boot/spring-boot-samples/spring-boot-sample-web-secure
    $ mvn spring-boot:run

http://localhost:8080/

**[OWASP Dependency Check](https://www.owasp.org/index.php/OWASP_Dependency_Check)**

    $ brew install dependency-check
    $ cd struts2
    $ mvn package
    $ dependency-check --scan . --project struts
    $ open dependency-check-report.html




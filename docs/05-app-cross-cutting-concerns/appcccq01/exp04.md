# Some automated unit and regression testing, basic CI/CD pipeline testing; modern test practices are not followed

**Risk Level**: Medium

The development and build stages are heavily making use of Unit Testing, since
the application development could follow a TDD (Test Driven Development)
approach. However, in other stages testing is mainly manual with basic
automation, if any.

To fully leverage the features Kubernetes offers to streamline the
deployment process and to reach a stage where Continuous Delivery or
even Continuous Deployment[1] can be implemented, a high degree of automation
is required, including automated testing.

While it is not a strict technical dependency, it is strongly suggested to
look at test automation frameworks such as JUnit (at build time), Cucumber,
Selenium, etc[2] to incorporate automated testing in
your delivery / deployment pipelines.

References:
[1. Elements of an OpenShift CI/CD Pipeline](http://v1.uncontained.io/playbooks/continuous_delivery/ci-cd-elements.html)
[2. Introduction to BDD and TDD](https://cucumber.io/blog/bdd/intro-to-bdd-and-tdd/)

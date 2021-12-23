# No testing or minimal manual testing only

<div class="risk-rounded-box high">High</div>

topic for the question **How is the application tested?**.

Testing is a very important topic to make sure that our application is
functioning properly, secure, and can be used without any unexpected errors
or behaviors. Having a high degree of test automation is not specific to
Kubernetes as a container platform but a general good practice in software
engineering.

To fully leverage the features Kubernetes offers to streamline the deployment
process and to reach a stage where Continuous Delivery or even
Continuous Deployment[1] can be implemented, a high degree of automation
is required, including automated testing.

While it is not a strict technical dependency, it is strongly suggested to
look at test automation frameworks such as JUnit (at build time), Cucumber,
Selenium, etc[2] to incorporate automated testing in your
delivery / deployment pipelines.

References:
1. [Elements of an OpenShift CI/CD Pipeline](http://v1.uncontained.io/playbooks/continuous_delivery/ci-cd-elements.html)
2. [Introduction to BDD and TDD](https://cucumber.io/blog/bdd/intro-to-bdd-and-tdd/)

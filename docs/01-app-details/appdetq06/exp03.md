# Licensing requirements

<div class="risk-rounded-box medium">Medium</div>

topic for the question **Does the application have legal and/or licensing requirements?**.

Examples: per server, per CPU

Using 3rd party solutions required licenses. In a container deployment it should be
considered how those licenses are counted and if they are unique to a specific
container (e.g. bound to an IP address). In other words, it must be verified with
the 3rd party vendor if these components are supported in a container and how it
affects license handling (and incurred cost).

At the same time it is possible to evaluate if some of these 3rd party solutions
have alternatives in the container space based on open-sourced projects. These
alternatives could fit better and improve the migration process to Kubernetes.

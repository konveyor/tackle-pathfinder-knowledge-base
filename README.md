# Tackle Pathfinder Knowledge Base

Tackle Pathfinder is one of the open-source tools of the [Konveyor Community](https://www.konveyor.io)
to assess your app portfolio to getting containerization recommendations, to automated
testing for your modernized app into Kubernetes platforms.

[Tackle Pathfinder](https://github.com/konveyor/tackle-pathfinder) is a questionnaire
based tool that assesses the suitability of applications for modernization in order
to be deployed in Containers on an enterprise Kubernetes platform. Through
interaction with the questionnaire, and review process, the system is enriched
with application knowledge which is exposed via a collection of reports.
The reports provide information about applications’ suitability for Kubernetes
highlight associated risks, and generate an adoption plan informed by the
applications’ prioritization, business criticality and dependencies.

This repo includes a set of recommendations to be used as standard knowledge base
for each of the questions in a Pathfinder report when some of the topics are
identified as `High` or `Medium`.

## Running the docs site locally

To launch the site, ensure you have NodeJS installed or run it in a NodeJS container if you prefer.

```shell
npm i docsify-cli -g
docsify serve ./docs
```

* Open the browser to http://localhost:3000 to view the tech exercise.

## How to Contribute

This is a live knowledge base and open to get contributions, revisions, and updates for anyone.
Please, review the [Contribution Guide](./CONTRIBUTING.md) to get more details.

Changes approved and pushed to main will automatically be published to the docs site.

**Easy starting point**: Find an entry with the `TBD` block, that is a great place to start. :tada:

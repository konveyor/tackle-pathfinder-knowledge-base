# Legal requirements

<div class="risk-rounded-box medium">Medium</div>

topic for the question **Does the application have legal and/or licensing requirements?**.

Examples: cluster isolation, hardware, PCI or HIPAA compliance

Since the application stores and processes customer data, there are some
legal compliance requirements. OpenShift can be configured to meet high
data protection requirements e.g. PCI DSS or HIPAA[1], however, it should
be discussed between OpenShift administration and the requirements owner
if and how much OpenShift should be configured to become certifiable
(if a formal compliance certification is necessary). 

The same is applicable to the application - if it has to be certified in
its current state, then it probably will need to be re-certified.

References:
1. [Red Hat OpenShift Container Platform Product Applicability Guide for HIPAA Security Rule](https://www.redhat.com/cms/managed-files/ve-openshift-hipaa-coalfire-analyst-materal-f23549-202005-en.pdf)

# infrastructure-as-code resources
tools, frameworks, accelerators, and _learnings_ in platforms and infrastructure-as-code.  

### Bills you will pay  

Scope always includes:
* Tests: with each commit and nightly (everything not tested should be considered broken)
* Security: Encryption at rest and in transit, secure secrets management including rotation, automated Auth N and Z, server-OS hardening
* Identity: Security Groups, IAM permissions, SSO
* Networking: VPC, subnets, eip, natgw, transitgw, firewalls, DNS, ssh access, PVN/direct connect
* Provisioning: managed services, instances, load balancers, storage
* Software Installation and Configuration: deployments (zero-downtime, B/G, Canary), dependencies, environment config management
* Resiliency and Availability: Zones, regions, master/slave, scalability (both vertical and horizontal), disaster recovery
* Observability: Comprehensive aggregated logging, metrics covering - health, performance, events, tracing, all in terms of the business purposes prompting investment, and with comprehensive monitoring/alerting.
* Documentation: Architecture, conventions, practices, incident runbooks, and knowledge transfer
* Preservation of Investment: Culture of refactoring, maintaining current version of software/tools/best practices, technical Debt is tracked(socialized)/estimated/prioritized (irresponsible not to, frankly)
* Backups: Databases, caches, stores, replication
* Cost Optimization: Justifying level of observability, instance sizing, reserved vs spot, utilization levels, cleanup of underused resources
*  - arguably among the top priorities

-every client will say, "we can don't have to have to that at the start." But by the first milestone will simultaneously  
expect that it be done and deny that it was every agreed to defer...no matter what is written down.

For each story, [Definition of Done](definition_of_done.md)  

And, you may think that you won't have to [shave](https://seths.blog/2005/03/dont_shave_that) that, but you will...


:cloud:  :wrench:  :whale:  :octocat:  

#### Working with IaaS or Cloud providers

[aws-cli](https://docs.aws.amazon.com/cli/latest/userguide/installing.html)  
[boto3](https://boto3.readthedocs.io/en/latest/)  
[gcloud](https://cloud.google.com/sdk/install)  
[terraform](https://www.terraform.io)  

#### build and deploy

[circleci](https://circleci.com)  
[consul](https://www.consul.io/)  
[quay](https://quay.io)  

#### containers and service orchestration

[docker](https://docs.docker.com)  
[kops](https://github.com/kubernetes/kops)  
[kubernetes](https://kubernetes.io)  
[istio](https://github.com/istio/istio)  
[spiffe](https://spiffe.io)  
[coreDNS](https://coredns.io)  
[linkerd](https://linkerd.io)  

[kubectx](https://github.com/ahmetb/kubectx) easy switch context and namespace  

#### monitoring, metrics, logs

[datadog](https://datadoghq.com)  
[logzio](https://logz.io)  
[prometheus](https://prometheus.io)  
[fluentd](https://www.fluentd.org)  
[cachet](https://github.com/CachetHQ/Cachet) status page  

#### security and governance

[vault](https://vaultproject.io)  
[twistlock](https://twistlock.com)  
[snyk](https://snyk.io/)  
[hawkeye](https://github.com/hawkeyesec/scanner-cli)  
[auth0](https://auth0.com)  
[kubernetes-policy-controller](https://github.com/Azure/kubernetes-policy-controller)  
[kube-hunter](https://github.com/aquasecurity/kube-hunter)  

#### validation

[sonabouy](https://github.com/heptio/sonobuoy)  
[kube-bench](https://github.com/aquasecurity/kube-bench) CIS inspection  
[docker-bench](https://github.com/docker/docker-bench-security) CIS inspection  

#### server virtualization

[vagrant](https://www.vagrantup.com)   
[packer](https://www.packer.io)   
[virtualbox](https://www.virtualbox.org)  

#### languages, testing, and develop frameworks

[stern](https://github.com/wercker/stern)
[ShellCheck](https://github.com/koalaman/shellcheck) shell script inspection  
[inspec](https://www.inspec.io)  
[awspec](https://github.com/k1LoW/awspec)  
[hadolint](https://github.com/hadolint/hadolint) Dockerfile lint/inspection  
[kubeval](https://github.com/garethr/kubeval) k8 yaml lint/inspection  
[kube-score](https://github.com/zegl/kube-score) k8 yaml resiliency evaluation  
[yamllint](https://pypi.org/project/yamllint/)  

#### misc

[nevergreen](https://nevergreen.io)  
[smashing](https://smashing.github.io)  
[ark](https://github.com/heptio/ark)  
[container-structure-test](https://github.com/GoogleContainerTools/container-structure-test)  
[moby](https://github.com/moby)  
[terratest](https://github.com/gruntwork-io/terratest)  
[dice](https://github.com/dmathieu/dice) roll all nodes, zero-dt  
[crane](https://github.com/google/go-containerregistry/blob/master/cmd/crane/doc/crane.md) registry management  
[aws-service-operator](https://github.com/awslabs/aws-service-operator) service broker  
[kubespy](https://github.com/pulumi/kubespy)  
[envconsul](https://github.com/hashicorp/envconsul)


[kube-ps1](https://github.com/jonmosco/kube-ps1) prompt tool  


#### evaluating

Using in various situations to evaluate effectiveness/efficiency/quality, etc.  

[popeye](https://github.com/derailed/popeye)
[kube-score](https://github.com/zegl/kube-score)

[grit](https://github.com/grailbio/grit)
[kubefwd](https://github.com/txn2/kubefwd)

an evolving list...

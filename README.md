# infrastructure-as-code resources [![currated](https://img.shields.io/badge/Tested-Pharrell-green)]
tools, frameworks, accelerators, and _learnings_ in platforms and infrastructure-as-code.  

### you can learn these the hard way, but i don't recommend it  

Saying, 'the tools don't matter' means - no tool can overcome regressive culture and process. It does NOT mean all tools  
can deliver equal result. Used in a supporting culture and with effective team organization and empowerment, certain  
tools delivery dramatically better results (velocity, sustainability, reliability, cost).  

Everything is an Architectural concern.  

"Automation" does not necessarily mean Infrastructure as Code. IaC is using test-driven development in the continuous  
integration and delivery of infrastructure. Use IaC if you want to delivery infrastructure that is resilient, secure  
and capable of safe continuous change (change at scale).  

Architect your infrastructure code in modular, multi-repo, multi-pipeline _Domain_ bounded patterns, striving to maintain  
loose coupling both between these pipelines and amongst the technologies and capabilities delivered. Rationales for not  
doing so are nearly always anti-patterns (and expensive).  

because the following characteristics must be sustained...  
* constrains complexity
* comprehension
* blast radius
* testability
* rbac
* velocity

...and even though you can feel the impact of loosing these traits in any architecture, within distributed compute there  
is an amplifier effect. Imagine the tech debt analogies, but with a 28% interest rate instead of %12.5 :smirk:

Scope always includes (_whether you want it to or not_):
* Tests: with each commit and nightly (everything not tested should be considered broken)
* Security: Encryption at rest and in transit, Auth N and Z, secure secrets management including rotation, configuration hardening, audit logging
* Identity: Security Groups, IAM permissions, SSO, DNS
* Networking: VPC, subnets, eip, natgw, transitgw, firewalls, DNS, ssh access, VPN/direct connect
* Provisioning: managed services, instances, storage, load balancers, firewalls
* Software Installation and Configuration: deployments (zero-downtime, B/G, Canary), dependencies, environment config management
* Resiliency and Availability: Zones, regions, master/slave, scalability (both vertical and horizontal), disaster recovery
* Observability: Comprehensive aggregated logging, metrics covering - health, performance, events, tracing, including in terms of the business purposes guiding investment, and with comprehensive monitoring/alerting.
* Documentation: Architecture, conventions, practices, incident runbooks, and knowledge transfer
* for each story: [Definition of Done](definition_of_done.md)
* Preservation of Investment: Culture of refactoring, maintaining current version of software/tools/best practices, technical Debt is tracked(socialized)/estimated/prioritized (irresponsible not to)
* Backups: Databases, caches, stores, replication
* Cost Optimization: Justifying level of observability, instance sizing, reserved vs spot, utilization levels, cleanup of underused resources - arguably among the top priorities

> A complex system that works is invariably found to have evolved from a simple system that worked. A complex system designed from scratch never works and cannot be made to work. You have to start over, beginning with a working simple system. - John Gall

> “You don’t have to be an engineer (infrastructure engineer) to be be a racing driver (software developer), but you do have to have Mechanical Sympathy.” - Jackie Stewart (inserted to show application in platform setting)

> infrastructure code without automated tests is broken

> every client may say, "we don't have to have to that at the start." But be cautious - by the first milestone can simultaneously  
expect that it be done and not remember every agreeing to defer...no matter what is written down.


_and, you may think that you won't have to [shave](https://seths.blog/2005/03/dont_shave_that) that, but you will..._


:cloud:  :wrench:  :whale:  :octocat:  

#### Working with IaaS or Cloud providers

[aws-cli](https://docs.aws.amazon.com/cli/latest/userguide/installing.html)  
[boto3](https://boto3.readthedocs.io/en/latest/)  
[gcloud](https://cloud.google.com/sdk/install)  
[terraform](https://www.terraform.io)  

#### build and deploy

[circleci](https://circleci.com)  
[buildkite](https://buildkite.com)
[consul](https://www.consul.io/)  
[quay](https://quay.io)  

#### containers and service orchestration

[docker](https://docs.docker.com)  
[kops](https://github.com/kubernetes/kops)  
[kubernetes](https://kubernetes.io)  
[kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
[istio](https://github.com/istio/istio)  
[spiffe](https://spiffe.io)  
[coreDNS](https://coredns.io)  
[linkerd](https://linkerd.io)  

[kubectx](https://github.com/ahmetb/kubectx) easy switch context and namespace  

#### monitoring, metrics, logs

[datadog](https://datadoghq.com)  
[honeycomb](https://www.honeycomb.io)  
[logzio](https://logz.io)  
[prometheus](https://prometheus.io)  
[fluentd](https://www.fluentd.org)  
[cachet](https://github.com/CachetHQ/Cachet) status page  

#### security and governance

[vault](https://vaultproject.io)  
[styra](https://www.styra.com)
[twistlock](https://twistlock.com)  
[snyk](https://snyk.io/)  
[hawkeye](https://github.com/hawkeyesec/scanner-cli)  
[auth0](https://auth0.com)  
[open policy agent](https://www.openpolicyagent.org)
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

[GPL, DSL, and related](./languages.md)

#### misc

[homebrew](https://brew.sh)
[nevergreen](https://nevergreen.io)  
[smashing](https://smashing.github.io)  
[velero](https://github.com/heptio/velero) _formerly_ ark
[container-structure-test](https://github.com/GoogleContainerTools/container-structure-test)  
[moby](https://github.com/moby)  
[aws-service-operator](https://github.com/awslabs/aws-service-operator) service broker  
[kubespy](https://github.com/pulumi/kubespy)  
[envconsul](https://github.com/hashicorp/envconsul)

[kube-ps1](https://github.com/jonmosco/kube-ps1) prompt tool  
[krew](https://github.com/kubernetes-sigs/krew/) kubectl plugin manager    
(_some useful plugins_)  
- access-matrix                  Show an access matrix for server resources  
- config-cleanup                 Automatically clean up your kubeconfig  
- exec-as                        Like kubectl exec, but offers a `user` flag to ...  
- get-all                        Like 'kubectl get all', but _really_ everything      
- iexec                          Interactive selection tool for `kubectl exec`      
- kubesec-scan                   Scan Kubernetes resources with kubesec.io.         
- match-name                     Match names of pods and other API objects          
- mtail                          Tail logs from multiple pods matching label sel...  
- oidc-login                     Login for OpenID Connect authentication            
- pod-logs                       Display a list of pods to get logs from            
- pod-shell                      Display a list of pods to execute a shell in       
- rbac-lookup                    Reverse lookup for RBAC                            
- rbac-view                      A tool to visualize your RBAC permissions.         
- resource-capacity              Provides an overview of resource requests, limi...  
- restart                        Restarts a pod with the given name                 
- view-secret                    Decode secrets                                     
- view-serviceaccount-kubeconfig Show a kubeconfig setting to access the apiserv...  
- view-utilization               Shows cluster cpu and memory utilization           
- warp                           Sync and execute local files in Pod  
- who-can                        like can-i but evaluates who at a permission level                           

#### evaluating

Using in various situations to evaluate effectiveness/efficiency/quality, etc.  

[prow](https://github.com/kubernetes/test-infra/tree/master/prow)
[popeye](https://github.com/derailed/popeye)  
[kube-score](https://github.com/zegl/kube-score)  
[squash](https://github.com/solo-io/squash)  
[grit](https://github.com/grailbio/grit)  
[terratest](https://github.com/gruntwork-io/terratest)  
[kubefwd](https://github.com/txn2/kubefwd)  
[dice](https://github.com/dmathieu/dice) roll all nodes, zero-dt  

[harbor](https://goharbor.io) self-managed container registry with quay.io-like features  

an evolving list...

_[brief comments about selected items above](./comments.md)_

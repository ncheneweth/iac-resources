<div align="center">
  <h2>Resources for software defined infrastructure</h2>
  tools, frameworks, accelerators, and _learnings_ in infrastructure-as-code and building platforms
</div>
<br />


### you can learn these the hard way, but i don't recommend it  

Saying, "the tools don't matter" means - no tool can overcome a regressive culture or process. It does **NOT** mean all tools can deliver equal result. Used in a supporting culture and with effective team organization and empowerment, certain tools delivery dramatically better results (velocity, sustainability, reliability, cost).  

_Everything_ is an Architectural concern.  

"Automation" does not mean Infrastructure as Code ("IaC"). IaC is using test-driven development in the continuous integration and delivery of infrastructure. Use IaC if you want to delivery infrastructure that is resilient, secure and capable of safe continuous change (change at scale).  

Architect your infrastructure code in modular, multi-repo, multi-pipeline _Domain_ bounded patterns, striving to maintain loose coupling both between these pipelines and amongst the technologies and capabilities delivered. Most rationales for not doing so are nearly always anti-patterns (and expensive).  

In building Platforms the following [characteristics](in-building-platforms.md) must be sustained...  
* complexity constrained
* comprehension
* observability
* idp integrated rbac
* agility

Even though you can feel the impact of failing to maintain those traits in any architecture, within distributed compute there is an amplifier effect. Imagine the tech debt analogies, but with a 50% interest rate instead of %12.5 :smirk:

Scope always includes (_whether you want it to or not_):
* Tests: with each commit and nightly (everything not tested should be considered broken)
* Security: Encryption at rest and in transit, Auth N and Z (Identity), secure secrets management including rotation, configuration hardening, audit logging
* Networking: VPC, subnets, eip, natgw, transitgw, firewalls, DNS, ssh access, VPN/direct connect
* Provisioning: managed services, instances, storage, load balancers, firewalls
* Software Installation and Configuration: deployments (zero-downtime, B/G, Canary), dependencies, environment config management
* Resiliency and Availability: Zones, regions, master/slave, scalability (both vertical and horizontal), disaster recovery
* Observability: Comprehensive aggregated logging, metrics covering - health, performance, events, tracing, including imeasures of the business purposes guiding investment, and with comprehensive monitoring/alerting.
* Documentation: Architecture, conventions, practices, incident runbooks, and knowledge transfer
* for each story: [Definition of Done](definition_of_done.md)
* Preservation of Investment: Culture of refactoring, maintaining current version of software/tools/best practices, technical Debt is tracked(socialized)/estimated/prioritized (irresponsible not to)
* Backups: e.g., loose data, loose  your job
* Cost Optimization: Justifying level of observability, instance sizing, reserved vs spot, utilization levels, cleanup of underused resources - arguably among the top priorities

_to the un-experienced, refactoring looks like [shaving](https://seths.blog/2005/03/dont_shave_that), but it isn't._


#### notable quotes (some attributed)

> "A complex system that works is invariably found to have evolved from a simple system that worked. A complex system designed from scratch never works and cannot be made to work. You have to start over, beginning with a working simple system." - John Gall

> “You don’t have to be an engineer to be be a racing driver, but you do have to have Mechanical Sympathy.” - Jackie Stewart

> "infrastructure code without automated tests is broken"

> every client, "we don't have to have to that at the start." (But by the first milestone will simultaneously expect that it be done and not remember every agreeing to defer...even if it is written down.

<div align="center">
  <h2>"But, I </h2>
  tools, frameworks, accelerators, and _learnings_ in infrastructure-as-code and building platforms
</div>
<br />

## Resources  

#### Working with IaaS or Cloud providers :cloud:

[terraform](https://www.terraform.io)  
[aws-cli](https://docs.aws.amazon.com/cli/latest/userguide/installing.html)  
[boto3](https://boto3.readthedocs.io/en/latest/)  
[gcloud](https://cloud.google.com/sdk/install)  
[auth0](https://auth0.com)  

#### build and deploy :octocat:

<div align="center">
  <h5>Developer being told IT is buying OpenShift</h5>
  <img alt="SecOps" src="https://raw.githubusercontent.com/ncheneweth/iac-resources/master/img/devs.gif" />
</div>
<br />

[github](https://github.com)
[circleci](https://circleci.com)  
[buildkite](https://buildkite.com)  
[consul](https://www.consul.io/)  
[vault](https://www.vaultproject.io)  
[packer](https://www.packer.io)  

#### containers and service orchestration :whale:

[docker](https://docs.docker.com)  
[kops](https://github.com/kubernetes/kops)  
[kubespray](https://github.com/kubernetes-sigs/kubespray)
[kubernetes](https://kubernetes.io)  
[kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
[istio](https://github.com/istio/istio)  
[spiffe](https://spiffe.io)  
[coreDNS](https://coredns.io) 

[kubectx](https://github.com/ahmetb/kubectx)   

#### monitoring, metrics, logs :stopwatch:

[datadog](https://datadoghq.com)  
[honeycomb](https://www.honeycomb.io)  
[prometheus](https://prometheus.io)  
[grafana](https://grafana.com)  
[fluentd](https://www.fluentd.org)  
[cachet](https://github.com/CachetHQ/Cachet)  

#### validation and governance :classical_building:

<div align="center">
  <h5>SecOps arriving at the meeting</h5>
  <img alt="SecOps" src="https://raw.githubusercontent.com/ncheneweth/iac-resources/master/img/secops.gif" />
</div>
<br />

[styra](https://www.styra.com)  
[open policy agent](https://www.openpolicyagent.org)  
[twistlock](https://twistlock.com)  
[snyk](https://snyk.io/)  
[sonabouy](https://github.com/heptio/sonobuoy)  
[kube-bench](https://github.com/aquasecurity/kube-bench)  
[docker-bench](https://github.com/docker/docker-bench-security)  
[hawkeye](https://github.com/hawkeyesec/scanner-cli)  
[kubernetes-policy-controller](https://github.com/Azure/kubernetes-policy-controller)  
[kube-hunter](https://github.com/aquasecurity/kube-hunter)  

#### languages, testing, and develop frameworks :desktop_computer:

[awspec](https://github.com/k1LoW/awspec)  
[inspec](https://www.inspec.io)  
[bats](https://github.com/bats-core/bats-core/blob/v1.2.0/README.md)  
[tflint](https://github.com/terraform-linters/tflint)  
[hadolint](https://github.com/hadolint/hadolint)  
[ShellCheck](https://github.com/koalaman/shellcheck)  
... too long, continue to [local and pipeline tools](./languages.md) for extensive language, GPL, DSL, and related tools  

#### misc :wrench:  

[stern](https://github.com/wercker/stern)  
[homebrew](https://brew.sh)  
[nevergreen](https://nevergreen.io)  
[smashing](https://smashing.github.io)  
[velero](https://github.com/heptio/velero) _formerly_ ark  
[container-structure-test](https://github.com/GoogleContainerTools/container-structure-test)  
[moby](https://github.com/moby)  
[kubespy](https://github.com/pulumi/kubespy)  
[envconsul](https://github.com/hashicorp/envconsul)  

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

currently evaluating the effectiveness/efficiency/quality, etc.  

[prow](https://github.com/kubernetes/test-infra/tree/master/prow)  
[squash](https://github.com/solo-io/squash)  
[grit](https://github.com/grailbio/grit)  
[kubefwd](https://github.com/txn2/kubefwd)  
[dice](https://github.com/dmathieu/dice)   
[harbor](https://goharbor.io) self-managed container registry with quay.io-like features  

an evolving list...

_[brief comments about selected items above](./comments.md)_

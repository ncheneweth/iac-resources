# tl;dr for certain capabilities  

_alphabetical_  

*[auth0](https://auth0.com)*. Poster child for good developer experience using an idp  

*[buildkite](https://buildkite.com)*. If you have to run compute on-prem but can otherwise use cloud, p-l-e-a-s-e consider  

*[cachet](https://github.com/CachetHQ/Cachet)*. Well, how were you planning on managing your status page? And wire it  
into Slack so you can CRUD via chatops, simultaneously updating the internal channels as well.  

*[circleci](https://circleci.com)*. Cannot understate the ongoing value of the inherit constraints and accelerators in Circle  

*[datadog](https://datadoghq.com)*. Hard to find better proof that self-managing observability tools is very wasteful  

*[honeycomb](https://www.honeycomb.io)*. Make this the benchmark for the 'platform user' experience. e.g., for teams that  
own their own api (microservices) all the way to production, use this - or at least make the experience the benchmark  


*[istio](https://github.com/istio/istio)*. You'll only regret not using it sooner rather than later  

*[kops](https://github.com/kubernetes/kops)*. Of course I actually mean use EKS, but if you must self manage, honestly kops  
makes IaC of k8s very easy  

*[styra](https://www.styra.com)*. If you are interested in governance and compliance without velocity-crushing command  
and control, and you're on k8s, then seriously consider this :smile:  

*[secrethub]https://secrethub.io)*. Excellent implementation, hugely accelerating, highly recommended.  

*[inspec](https://www.inspec.io)*. You will save duplication later if your tdd framework supports 'policy' based  
assertions. Review the CIS examples if nothing else. When even the non-config remediations are in the test outputs,  
with links to the policies...well the endgame is that PCI and SOX (etc) audits should be zero interrupt for the platform  
developers. That is achievable.  

*[nevergreen](https://nevergreen.io)*. Not saying it has to be nevergreen, but radiating a bunch of 'healthy' to the  
folks who actually build and support the platform is an anti-pattern (actually has a negative impact)



And there are things that are just a necessary part of maturing at being a dev in this space. The ones listed below  
are hardly exhaustive from a local tooling perspective, but if they are not on your computer (or equally accelerating  
similes thereof) then install them now and start becoming proficient. Yes, of course these are all very linux/darwin  
oriented, it's overwhelming what the underlying cloud-native/platform building technologies are developed on. Not a  
statement about the relative value of alternative development OS environments. If throughout your journey as an  
infra-dev (from newbie to intermediate to expert), you can consistently demonstrate the same relative velocity and  
effectiveness on your local OS of choice, more power to you :punch:

[iterm](https://iterm2.com) [tmux](https://github.com/tmux/tmux) zsh  
vi [atom](https://atom.io)  
[homebrew](https://brew.sh) [krew](https://github.com/kubernetes-sigs/krew/)  
[kube-ps1](https://github.com/jonmosco/kube-ps1) [kubectx](https://github.com/ahmetb/kubectx)  
[stern](https://github.com/wercker/stern)  

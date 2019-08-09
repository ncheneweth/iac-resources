# Definition of Done

## infrastructure story acceptance criteria

For each Story:  
1. Same code used to build all environments (desired state is known qty, all production state exists in all non-prod state)
1. Change begins and ends with _git push_ (complete lifecycle via pipelines from diff-able source version control)
1. Tests with commit, and recurring (only authoritative source for state is Actual state)
1. Secrets managed (securely stored, automated access and rotation)
1. Observable: events logged, state metered (metrics collected) and monitored (alerted), and accessible (to all relevant parties, and they know it/how)
1. Resilient (effectively usable in _failed_ state, actual state will self-correct to desired state)
1. Technical Debt decisions turned into stories, estimated, prioritized
1. Persistent data backed-up with appropriate frequency, restores part of game-day
1. Domain included in game-day (on rotation)

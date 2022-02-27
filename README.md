**rlacalc** crunches the numbers for risk-limiting post-election audits.
It can calculate sample sizes, as well as calculate risk levels based on observed ballots.
It can handle many of the commonly used RLA tests, including ballot-level comparison via Kaplan-Markov and
ballot polling via BRAVO.

# Goals
It is important to emphasize that the output of an audit should be
a report providing evidence related to election outcome, details about and explanations of any discrepancies found,
and conclusions based on that evidence.  See the paper
[Evidence-Based Elections Stark and Wagner](http://www.stat.berkeley.edu/~stark/Preprints/evidenceVote12.pdf)
and the report [Risk-Limiting Post-Election Audits: Why and How](http://www.stat.berkeley.edu/~stark/Preprints/RLAwhitepaper12.pdf).

rlacalc helps observers to explore the best way to do an audit beforehand, and to check the numbers in reports published after an audit, e.g. as described for a [Public RLA Oversight Protocol](http://bcn.boulder.co.us/~neal/elections/PublicRLAOversightProtocol.pdf).

rlacalc can be used to perform calculations from the command line or used as a library in Python. In addition, if the hug package
is available, it can be accessed over the web.

# Installation

rlacalc works with Python 2.7 and Python 3.x.
There are no other mandatory dependencies beyond the standard library.

If hug is installed, rlacalc can be deployed via a web server.

# Usage

```
$ rlacalc --help
...

$ rlacalc --test
...

$ rlacalc -m 1 -n
Sample size = 479 for margin 1%, risk 10%, gamma 1.03905, o1 0, o2 0, u1 0, u2 0

$ rlacalc -m 1 -n --o1 1
Sample size = 615 for margin 1%, risk 10%, gamma 1.03905, o1 1, o2 0, u1 0, u2 0

$ rlacalc -m 3 -r 5
KM_exp_rnd  = 226 for margin 3%, risk 5%, gamma 1.03905, or1 0.001, or2 0.0001, ur1 0.001, ur2 0.0001, roundUp1 1, roundUp2 0
```

# Background
For tools implemented in javascript, with plots, see

* [Tools for Comparison Risk\-Limiting Election Audits](https://www.stat.berkeley.edu/~stark/Vote/auditTools.htm)
* [Tools for Ballot\-Polling Risk\-Limiting Election Audits](https://www.stat.berkeley.edu/~stark/Vote/ballotPollTools.htm)

# History
rlacalc was included as part of [audit_cvrs](https://github.com/nealmcb/audit_cvrs) in 2015 to help run some early pilot audits in Colorado as part of the [The Colorado Risk-Limiting Audit Project (CORLA)](http://bcn.boulder.co.us/~neal/elections/corla/).

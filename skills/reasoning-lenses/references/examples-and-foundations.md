# Examples and foundations

These are synthetic illustrations of applying the lenses. They are not evidence
that a particular architecture or policy is generally superior.

## Constructive design review

**Request:** "Help improve a dashboard that stores everything locally. It has to
work offline, and I want to keep the interface simple."

A faithful reading keeps offline operation and local storage as constraints.
The strongest case is immediate access and control of the stored data; neither
guarantees reliability or security by itself. A material uncertainty is what the
user expects after losing a device. A constructive improvement might be an
explicit local export and restore flow. Cloud synchronization is a separate
alternative requiring a changed constraint, not an assumption smuggled into the
steelman. A useful next test is an offline export/restore exercise on a second
test profile, with success defined by recovery of the saved records.

## Adversarial engineering review

**Request:** "Stress-test our proposal to retry a failed job up to five times."

The strongest case is recovery from transient failures without user intervention.
The strongest objection depends on the job: if it can charge an account and then
lose the acknowledgement, retrying could duplicate the charge. That is a
conditional failure mechanism, not a claim that duplication has happened.
Preserve the original five-retry proposal in the assessment. An idempotency key
or a narrower list of retryable failures is a proposed repair. A sandbox test
could interrupt acknowledgement after the side effect and check whether only
one effect remains. Recommend or describe that test; the review request alone
does not authorize touching a live payment system.

## Unequal evidence

**Request:** "Make the best case for both algorithms. In the supplied randomized
benchmark with identical workloads, A passed 98 of 100 runs and B passed 61."

For that benchmark, the observed reliability favors A. Do not invent a speed,
cost or privacy benefit for B to make the comparison balanced. B could remain
worth investigating if such a benefit were independently established, but that
is a conditional research direction. The benchmark does not establish behavior
on every workload. State what it supports, what is unmeasured, and whether a
further workload test would actually change the choice.

## Correcting a caricature

**Request:** "Critics of automation just hate progress. Help me rebut them."

That description does not establish what any particular critic believes. Ask for
the actual objection if needed, or tentatively distinguish plausible concerns
such as error recovery, accountability and maintenance. Evaluate a stated concern
against evidence. Do not attribute those reconstructed concerns to absent people
or turn the insult into a premise for the rebuttal.

## Finding a crux without erasing values

**Request:** "One person wants to launch this week; another wants another month
of testing. Help us make progress together."

Identify whether the disagreement concerns expected failure rates, consequences
of failure, cost of delay, or tolerance for risk. If both say their choice depends
on recovery time, a recovery drill may answer a shared decision-changing
question. If they agree on the facts but value speed and reliability differently,
expose that tradeoff and seek a decision rule or owner preference. A drill cannot
prove which priority they ought to hold. A shared crux requires actual stated
dependencies; the agent's guess is only a candidate.

## Conceptual sources

- Daniel Dennett's account of Rapoport's rules emphasizes fair restatement,
  agreement and learning before criticism. This skill borrows that discipline
  without claiming that fair restatement and strengthening an argument are
  identical. [Dennett interview, Point of Inquiry (2013)](https://pointofinquiry.org/2013/06/daniel_dennett_tools_for_thinking/).
- Duncan Sabien's account of Double Crux describes finding a shared underlying
  question that would change both positions. This skill uses it as a practical
  technique when appropriate, not as a guarantee of agreement or a validated
  improvement in agent performance. [Double Crux: A Strategy for Mutual Understanding (2017)](https://www.lesswrong.com/posts/exa5kmvopeRyfJgCy/double-crux-a-strategy-for-resolving-disagreement).

The lens selection, output guidance and examples here are an adaptation for
agent-assisted work. These sources motivate parts of the approach; they do not
establish that this package improves reasoning accuracy.

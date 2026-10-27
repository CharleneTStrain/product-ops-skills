# Feature flag tracking

**The problem:** Nobody outside engineering can answer "can this customer see that feature?", and old flags pile up long after full rollout.

**What it does:** Keeps a register of every flag in plain words: what it controls, its type, who it's on for, the owner, the target rollout date, and when it should be removed. Flags stale, ownerless, past-due, and conflicting flags, and lists partial rollouts support and sales should know about.

**Use it with:** a flag export, rollout plan, or engineering notes.

**You get:** a current flag register and a cleanup list. It never changes a flag.

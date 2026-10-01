# Risk Register

> Initial planning register. Owners will be assigned by the team.

| ID | Risk and trigger | Impact | Mitigation | Owner |
| --- | --- | --- | --- | --- |
| R-01 | Scope expands into AI, social or complex farming before P0 works | Incomplete Alpha | Route additions through scope review; defer outside core journey | |
| R-02 | Shared models change independently across teams | Integration failures | One contract owner; affected-module review | |
| R-03 | Repeated completion or partial writes corrupt rewards | Untrustworthy progression | Atomic workflow, unique grant identity and failure tests | |
| R-04 | SQLite driver or assets fail on chosen demo target | Demo cannot run | Select target early and test clean setup | |
| R-05 | Local data is lost on restart or migration | User data loss | Persistence/restart tests; migration fixtures; preserve corrupt files | |
| R-06 | Collision projection differs from scene rendering | Clipping and stuck movement | Separate logical coordinates; check boundaries and wall sliding | |
| R-07 | Documents describe planned behavior as completed | Misleading assessment | Separate designed, implemented and verified status | |
| R-08 | Asset origin or reuse rights are unclear | Release cannot include assets | Record source, attribution and permitted use before release | |
| R-09 | Team members cannot reproduce the environment | Slow collaboration | Verified shell-specific setup and pinned SDK/lockfile | |
| R-10 | Late backend work introduces sync/conflict defects | Deadline slippage | Keep cloud outside Alpha runtime; require separate decision | |

Review risks at milestone gates and when a trigger occurs. Record assigned owner, mitigation progress and the evidence used to close a risk. Do not mark a risk resolved because a mitigation is merely planned.

[Management index](README.md)

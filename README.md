# Claude Code: `/ground` skill and verifier subagent

> **Part of a larger collection.** This repo is the focused, single-purpose home for the
> `/ground` skill + verifier subagent. It's also bundled - alongside a theory-formation
> reasoning discipline and a send-time verification-claim Stop hook - in
> [barzins-cc-improvements](https://github.com/BarzinL/barzins-cc-improvements), my full
> set of Claude Code honesty/grounding tools. Grab just this, or the whole collection there.


Battle-tested `/ground` skill and verifier subagent for Claude Code: consistently produce 95% bug-free code with Opus 4.8 by grounding the agent in your codebase's actual wiring, eliminating Opus 4.8's tendency to often make assumptions, inferences, and assertions about how things work without actually checking them and knowing whether that is the case for sure.

Completely serviceable for production codebase development.

## How to Use:

1. Place the files in your project or Claude's global skills and subagent definition directories.
2. For whatever feature sprint or phase of development you're working on, simply prompt with something like:
   
   `Proceed by using /ground + verifier sub-agent, set to Ceiling 2`

### Autonomy Ceilings:

You can specify in your prompt what level of autonomy you want to invoke the grounding skill with: Ceiling 1 is fully autonomous and will automatically commit, Ceiling 2 stages everything for HITL review before committing, while Ceiling 3 escalates more decisions to you as the operator instead of seeking to have the answers fall out naturally from diving deeper into the code and wiring.

Ceiling 2 is typically a reasonable balance.

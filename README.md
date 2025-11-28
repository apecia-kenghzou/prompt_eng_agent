# Prompt Engineering Agent System

An iterative prompt improvement approach using critique and enhancement cycles.

## Philosophy

This is NOT a Python automation system. Instead, this is a **manual iterative process** where Claude acts as different agent roles to systematically improve prompts.

## The Roles

### Master Orchestrator (You/Claude)
- Coordinates the improvement process
- Decides when to stop iterating
- Manages file organization
- Tracks versions and changes

### Improvement Agent (Claude)
- Analyzes configuration requirements
- Identifies gaps in current prompts
- Builds enhanced versions
- Documents all changes

### Critique Agent (Claude)
- Rigorously analyzes prompts
- Identifies weaknesses (CRITICAL, MAJOR, MINOR)
- Finds contradictions and edge cases
- Suggests alternatives

## The Process

```
1. Load agent_config.yaml
2. Create/load current prompt
3. [IMPROVEMENT AGENT] Enhance the prompt
4. [CRITIQUE AGENT] Analyze for weaknesses
5. Evaluate severity:
   - CRITICAL or MAJOR issues? → Go to step 3
   - Only MINOR issues? → Done!
6. Save version, critique, and changelog
```

## Directory Structure

```
prompts/domains/{domain}/{agent}/
├── versions/
│   ├── v1.0.0.md (initial)
│   ├── v2.0.0.md (major improvements)
│   └── v2.1.0.md (final)
├── critiques/
│   ├── critique_v1.0.0.md
│   ├── critique_v2.0.0.md
│   └── critique_v2.1.0.md
├── improvements/
│   ├── changelog.md (what changed and why)
│   └── iteration_log.md (iteration history)
└── current.md (latest production-ready version)
```

## Example: Frontend Developer Agent

### Iteration 1
- **Input**: Basic technology list from agent_config.yaml
- **Output**: v1.0.0.md
- **Critique**: 4 CRITICAL, 5 MAJOR, 5+ MINOR issues
- **Decision**: Continue (critical issues exist)

### Iteration 2
- **Input**: v1.0.0.md + critique feedback
- **Improvement**: Added decision frameworks, error handling, performance techniques
- **Output**: v2.0.0.md
- **Critique**: 0 CRITICAL, 2 MAJOR (routing, i18n), 7 MINOR
- **Decision**: Continue (major issues remain)

### Iteration 3
- **Input**: v2.0.0.md + critique feedback
- **Improvement**: Added routing and internationalization sections
- **Output**: v2.1.0.md
- **Critique**: 0 CRITICAL, 0 MAJOR, 7 MINOR (optional enhancements)
- **Decision**: COMPLETE ✓

**Result**: Production-ready prompt improved from 40/100 → 97/100

## How to Use

1. **Choose an agent** from `agent_config.yaml`
2. **Create initial prompt** based on configuration
3. **Switch to Critique Agent role** and analyze rigorously
4. **Switch to Improvement Agent role** and enhance based on critique
5. **Repeat steps 3-4** until only MINOR issues remain
6. **Mark as current.md** when production-ready
7. **Commit all versions, critiques, and changelogs**

## Key Files

- `agent_config.yaml` - Agent configurations (domains, focus areas, success metrics)
- `master_orchestrator_prompt.md` - Orchestrator responsibilities and workflow
- `prompt_improvement_agent.md` - Improvement agent methodology
- `prompt_critique_agent.md` - Critique agent analysis framework
- `agent_interaction_example.md` - Complete walkthrough example

## Completed Agents

- ✅ **Frontend Developer** (v2.1.0) - Production-ready
  - 3 iterations
  - 11 critical/major issues resolved
  - Comprehensive guide with decision frameworks

## Next Steps

Apply the same process to other agents:
- Backend Developer
- DevOps Engineer
- QA Engineer
- Risk Management (Financial)
- Technical Analysis (Financial)
- Fundamental Analysis (Financial)
- ML Engineer (Data Science)

## Why This Approach?

1. **Systematic**: Follows consistent methodology
2. **Traceable**: Every change documented with rationale
3. **Iterative**: Addresses highest-priority issues first
4. **Quality-Focused**: Continues until threshold met
5. **Evidence-Based**: Critiques provide specific examples
6. **Production-Ready**: Final prompts are comprehensive guides, not checklists

## No Scripts Needed

The power is in the **process**, not automation. Claude can act as different agents in sequence to systematically improve any prompt through structured critique and enhancement cycles.

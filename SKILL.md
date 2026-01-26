---
name: council
description: Send an idea to the Council of the Wise for multi-perspective feedback. Spawns sub-agents (Devil's Advocate, Architect, Engineer, Artist) to challenge, design, implement, and refine ideas.
version: 1.0.0
author: jeffaf
credits: Inspired by Daniel Miessler's PAI (Personal AI Infrastructure) and agent architecture concepts.
---

# Council of the Wise

When the user says "send it to the council" or "council of the wise" or similar, spawn a sub-agent to analyze the idea from multiple expert perspectives.

## Usage

```
"Send this to the council: [idea/plan/document]"
"Council of the wise: [topic]"
"Get the council's feedback on [thing]"
```

## Council Members

The skill includes bundled agent personas in `agents/`:

1. **DevilsAdvocate.md** — Challenges assumptions, finds weaknesses, stress-tests
2. **Architect.md** — Designs systems, structure, high-level approach  
3. **Engineer.md** — Implementation details, technical feasibility
4. **Artist.md** — Voice, style, presentation, user experience

### Custom Agents (Optional)

If the user has custom PAI agents at `~/.claude/Agents/`, those can be used instead:
- Check if `~/.claude/Agents/DevilsAdvocate.md` exists
- If yes, use custom agents from that directory
- If no, use the bundled agents in this skill's `agents/` folder

## Process

1. Receive the idea/topic from the user
2. Determine agent source (custom or bundled)
3. Spawn a sub-agent with this task template:

```
Analyze this idea/plan from multiple expert perspectives.

**The Idea:**
[user's idea here]

**Your Task:**
Read and apply these agent perspectives from [AGENT_PATH]:
- DevilsAdvocate.md — Challenge it. What could go wrong? What assumptions are shaky?
- Architect.md — How should it be structured? What's the high-level design?
- Engineer.md — How would you implement it? What's technically feasible?
- Artist.md — How should it feel? What's the voice/style/UX?

For each perspective, provide:
1. Key insights (2-3 bullets)
2. Concerns or questions
3. Recommendations

End with a **Synthesis** section that combines the best ideas and flags critical decisions.
```

4. Return the consolidated feedback to the user

## Output Format

```markdown
## 🏛️ Council of the Wise — [Topic]

### 👹 Devil's Advocate
[challenges and risks]

### 🏗️ Architect  
[structure and design]

### 🛠️ Engineer
[implementation notes]

### 🎨 Artist
[voice and presentation]

### ⚖️ Synthesis
[combined recommendation + key decisions needed]
```

## Optional Members

For security-related topics, consider adding:
- **Pentester** — Security implications, attack surface
- **QATester** — Quality, edge cases, testing scenarios

## Notes

- Council review takes 2-5 minutes depending on complexity
- Use for: business ideas, content plans, project designs, major decisions
- Don't use for: quick questions, simple tasks, time-sensitive requests
- Sub-agent spawns use the default model unless overridden

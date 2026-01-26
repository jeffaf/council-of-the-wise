# Council of the Wise

A Clawdbot skill that spawns sub-agents to analyze ideas from multiple expert perspectives.

## What It Does

When you say "send this to the council" or "council of the wise," Clawdbot spawns a sub-agent that analyzes your idea through four lenses:

- **👹 Devil's Advocate** — Challenges assumptions, finds weaknesses
- **🏗️ Architect** — High-level structure and design
- **🛠️ Engineer** — Implementation feasibility and details
- **🎨 Artist** — Voice, style, and user experience

The sub-agent returns a synthesized report with insights, concerns, and recommendations from each perspective.

## Installation

### Via ClawdHub (Coming Soon)
```bash
clawdhub install council
```

### Manual
Copy the `council/` folder to your Clawdbot skills directory:
```bash
cp -r council/ ~/clawd/skills/council/
```

## Usage

```
"Send this to the council: [your idea]"
"Council of the wise: [topic to analyze]"
"Get the council's feedback on [thing]"
```

## Example

**Input:**
> Send this to the council: I want to start a newsletter about offensive security and AI-assisted coding

**Output:**
```
## 🏛️ Council of the Wise — Security Newsletter

### 👹 Devil's Advocate
- Niche may be too narrow...
- What's the content pipeline after initial ideas?

### 🏗️ Architect
- Four content pillars recommended...
- Monthly cadence with deep content...

### 🛠️ Engineer
- beehiiv is the right platform choice...
- Set up content pipeline: drafts → review → publish

### 🎨 Artist
- First-person authentic voice is right for this audience...
- Nail the welcome email...

### ⚖️ Synthesis
- Core idea is strong
- Biggest risk: content sustainability
- Recommended: Build 3-issue buffer before launch
```

## Custom Agents

The skill includes bundled agent personas, but if you have custom PAI agents at `~/.claude/Agents/`, those will be used instead.

## Best Used For

✅ Business ideas and plans
✅ Content strategies
✅ Project designs
✅ Major decisions

## Not Ideal For

❌ Quick questions
❌ Simple tasks
❌ Time-sensitive requests (takes 2-5 min)

## Credits

Inspired by [Daniel Miessler](https://danielmiessler.com/)'s PAI (Personal AI Infrastructure) concepts. The Architect, Engineer, and Artist agent personas are adapted from PAI patterns. The Devil's Advocate is an original creation.

## License

MIT

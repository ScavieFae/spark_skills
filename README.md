# Spark Skills

Books distilled into Claude Code skills. Load a book's wisdom as actionable guidance.

## What This Is

Spark Skills are [Claude Code skills](https://docs.anthropic.com/en/docs/claude-code/skills) based on influential books. Each skill distills a book's core principles into instructions Claude can apply while working with you.

Think of it as having a writing coach, strategy advisor, or management mentor on call—except instead of asking "what would Grove say?", Claude already knows.

## Available Skills

### Writing
- **[Elements of Style](writing/elements-of-style/)** — Strunk & White's blade for cutting prose
- **[On Writing Well](writing/on-writing-well/)** — Zinsser's warm, exacting eye for nonfiction
- **[Bird by Bird](writing/bird-by-bird/)** — Lamott's survival guide for writers facing the blank page

### Strategy
- **[The Lean Startup](strategy/lean-startup/)** — Ries's methodology for building under uncertainty
- **[Good Strategy Bad Strategy](strategy/good-strategy-bad-strategy/)** — Rumelt's bullshit detector for strategy
- **[7 Powers](strategy/7-powers/)** — Helmer's diagnostic for durable competitive advantage

### Leadership
- **[High Output Management](leadership/high-output-management/)** — Grove's operating system for managers who build things
- **[The Manager's Path](leadership/managers-path/)** — Fournier's guide to each level of the engineering ladder
- **[Radical Candor](leadership/radical-candor/)** — Scott's discipline for feedback that's both kind and clear

### Product
- **[Inspired](product/inspired/)** — Cagan's diagnosis of product org dysfunction
- **[The Mom Test](product/mom-test/)** — Fitzpatrick's discipline for customer conversations that reveal truth

### Thinking & Decisions
- **[Thinking, Fast and Slow](thinking/thinking-fast-slow/)** — Kahneman's toolkit for when intuition lies

### Operations
- **[The Goal](operations/the-goal/)** — Goldratt's Theory of Constraints as diagnostic tool

### Communication
- **[Made to Stick](communication/made-to-stick/)** — Heath brothers' craft of ideas that survive

## Usage

### Install a single skill

```bash
claude skill install /path/to/spark_skills/writing/elements-of-style
```

Or add the skill folder path to your Claude Code settings.

### Using skills

Once installed, skills activate based on their description triggers. For Elements of Style, ask Claude to edit prose, tighten writing, or review for clarity—the skill loads automatically.

You can also invoke directly:

```
/elements-of-style Review this paragraph for wordiness
```

## Philosophy

A spark skill isn't a book summary. It's a translation: taking what made the book useful and reformulating it as guidance Claude can execute.

**What makes a good spark skill:**
- **Actionable** — Not "good writing is clear" but "cut every word that serves no function"
- **Opinionated** — Captures the book's point of view, not generic advice
- **Expert frame** — Written as if by someone who's internalized the book, not summarized it
- **Contextual** — Knows when to apply (and when not to)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the skill template and guidelines.

## License

MIT. The skills are original distillations, not reproductions of copyrighted text.

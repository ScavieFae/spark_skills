---
name: design-of-everyday-things
description: Norman's systematic lens for usability and user-centered design. Activate when evaluating why something feels confusing, when designing interactions, or when someone blames user error. If users fail, the design failed.
allowed-tools: Read, Edit, AskUserQuestion
---

# The Design of Everyday Things

## When to Use This

- Someone says "I couldn't figure out how to..." and you're tempted to blame them
- You're designing interactions and need to think through affordances, mapping, feedback
- Error rates are high and people blame training instead of the design

**The rule:** When users struggle, the design is on trial. Not the users.

---

## The Core Insight

Good design is invisible. You don't notice doors that open correctly, faucets that work intuitively, tools that fit your hand. You only notice design when it fails.

When users make errors, when they're confused, when they do the "wrong" thing—that's design failure. Every human error is a design opportunity. Blame the system, not the person.

The goal: create designs where the right action is the obvious action, where the system guides rather than puzzles, where errors are either impossible or trivially recoverable.

---

## The Principles

These are Norman's fundamental concepts. Learn to see designs through this vocabulary.

### Affordances

What actions are physically possible? A button affords pressing. A handle affords pulling. A flat plate affords pushing.

Affordances exist whether you perceive them or not. A chair affords sitting even if you don't notice it. The question is: does the design make the affordance obvious?

### Signifiers

How do users discover what's possible? Signifiers communicate where the action should take place.

A "push" sign on a door is a signifier. Underlined blue text signifying a link. A raised edge signifying where to grip. Signifiers answer "where?" and "how?"

The problem: affordances exist in the world; signifiers exist in perception. When signifiers are missing or misleading, users get stuck. They have capabilities they can't discover.

### Mapping

What's the relationship between controls and results? Natural mapping uses spatial correspondence—turn a wheel left, the car goes left. Stove controls that match burner layout.

Bad mapping: a row of identical switches controlling lights in a different spatial arrangement. You have to memorize or guess. Every bad mapping is a usability tax.

### Feedback

The system must communicate what happened. Immediately. Clearly.

Did my click register? Is the system working? What state am I in? Feedback answers these without forcing users to guess.

Poor feedback: a button that gives no visual response. A process running with no progress indicator. A state change with no confirmation. Users lose trust; they click again, they wonder, they give up.

### Constraints

Limit what's possible to prevent errors. Physical constraints (the plug only fits one way). Semantic constraints (meaningful actions in context). Cultural constraints (conventions everyone knows). Logical constraints (one remaining option).

Good constraints make errors impossible rather than just unlikely. If the only remaining action is the right one, the user can't fail.

### Conceptual Models

Users build mental models of how things work. Designers have their own model. The system has its actual model.

When these align: intuitive use. When they diverge: confusion, errors, frustration. Users aren't stupid—they're working from a reasonable model that happens to be wrong. Fix the design so the model becomes obvious.

---

## When Activated

Determine the mode from context or by asking:

- **Evaluate mode** — "I have a design, interface, or experience. Help me see what's wrong."
- **Design mode** — "I'm creating something. Help me apply these principles."

---

## Evaluate Mode: The Diagnostic

You have something to analyze—an interface, a product, a flow, a physical design. Let's see it with Norman's eyes.

### The Seven-Stage Walkthrough

For any task a user attempts, walk through the stages:

**The gulf of execution** (what do I do?):
1. Goal — What are they trying to achieve?
2. Plan — What sequence of actions will achieve it?
3. Specify — What specific actions, on what controls?
4. Perform — Execute the physical actions

**The gulf of evaluation** (what happened?):
5. Perceive — What does the system now show?
6. Interpret — What does that state mean?
7. Compare — Did I achieve my goal?

At each stage, ask: where does the design help? Where does it fail? The wider the gulf, the worse the design.

### The Principle Scan

Work through each principle systematically:

**Affordances:** What actions are possible? Are the wrong actions too possible?

**Signifiers:** Can users discover what to do? Are the signals clear, visible, unambiguous?

**Mapping:** Do controls correspond naturally to results? Or must users memorize arbitrary relationships?

**Feedback:** Does the system communicate what's happening? Immediately? Clearly? In the right modality?

**Constraints:** What errors are still possible? Could constraints make them impossible?

**Conceptual model:** What model will users build? Does the design communicate how it actually works?

### Error Analysis

When users make errors, diagnose them:

**Slips:** Right intention, wrong action. Typically motor/attention failures.
- Mode errors (acting as if in a different mode)
- Capture errors (frequent action captures similar rare action)
- Description errors (right action, wrong object)

**Mistakes:** Wrong intention altogether. Model or plan failures.
- Rule-based: applied the wrong rule
- Knowledge-based: incomplete or incorrect mental model

**The question:** What in the design made this error possible? What would prevent it?

### Output Format for Evaluate Mode

1. **Overall read** (2-3 sentences): What's the design trying to do? What's the main usability issue?

2. **The seven-stage walkthrough**: For the core task, where does the design fail users?

3. **Principle violations** (most impactful first): Specific issues with affordances, signifiers, mapping, feedback, constraints, or conceptual models

4. **Error patterns**: What errors are users making? What type? What enables them?

5. **Redesign suggestions**: Concrete changes, prioritized by impact

---

## Design Mode: Building for Humans

You're creating something new. Let's design it right from the start.

### The Scaffolding Questions

Before designing, answer:

**1. What's the user's actual goal?**
Not the feature goal. The human goal. What are they trying to accomplish in their life?

**2. What will they already know?**
What conceptual models will they bring from similar experiences? Design with those models, not against them.

**3. What errors are most likely?**
Given the task, what will people mess up? Plan for those errors now.

**4. What's the simplest path?**
The obvious action should be the correct action. If it isn't, redesign.

### The Design Checklist

For each control/interaction:

**Signifiers:**
- Is it obvious that this can be acted on?
- Is it obvious *how* to act on it?
- Is the signifier visible at the moment of need?

**Mapping:**
- Does the control's position correspond to its effect?
- Would a new user guess correctly which control does what?

**Feedback:**
- Will users know their action registered?
- Will they know what state the system is in?
- Is the feedback immediate? Appropriate in magnitude?

**Constraints:**
- What errors are still possible?
- Could physical/semantic/logical constraints eliminate them?
- Can we make error states impossible rather than just warning about them?

### The Conceptual Model Test

Ask: If a user had to explain how this works to someone else, what would they say?

If their explanation would be wrong—if the true model is hidden—redesign. The system's behavior should teach its own model through use.

### Designing for Error

Errors will happen. Design for recovery:

- **Make errors reversible.** Undo is mercy.
- **Make errors visible.** Users need to notice before damage spreads.
- **Make recovery obvious.** Don't require documentation to escape.
- **Blame the system.** If your error message implies user stupidity, rewrite it.

### Output Format for Design Mode

1. **Goal restatement**: What is the user actually trying to do?

2. **Conceptual model**: How should users think about this? What mental model serves them?

3. **Core interactions**: For each major interaction:
   - Signifiers: how users discover it
   - Mapping: how controls relate to effects
   - Feedback: how the system responds
   - Constraints: what errors are prevented

4. **Error scenarios**: Most likely errors and how the design handles them

5. **Model test**: Can a new user explain how it works after one use?

---

## The Voice

Norman is professorial but accessible. He gets genuinely frustrated at bad design—not at users, never at users—but at the designers who failed them. There's warmth in his frustration; he believes design can be better, and the stakes are human dignity.

When you use this skill, you're looking at designs the way Norman does: systematically, principled, slightly indignant at unnecessary confusion, always advocating for the human caught in a badly designed world.

Bad design isn't a minor inconvenience. It wastes lives, one confused moment at a time.

---

## Quick Reference

### The Principles

- **Affordances** — What's possible?
- **Signifiers** — How do users know?
- **Mapping** — Controls match results?
- **Feedback** — System communicates?
- **Constraints** — Errors prevented?
- **Conceptual models** — Mental model matches reality?

### The Two Gulfs

- **Gulf of execution:** The gap between user's goal and knowing what to do
- **Gulf of evaluation:** The gap between system state and understanding it

### The Human Error Principle

Every human error is a design opportunity. If users are making mistakes, the design is making them possible. Fix the design, not the training.

### Norman's Frustration Test

If a design makes you want to ask "why would anyone think *that* was intuitive?"—and the answer is "because that's what users expected"—the design failed. Not the users.

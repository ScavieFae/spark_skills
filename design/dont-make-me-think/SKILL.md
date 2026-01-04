---
name: dont-make-me-think
description: Krug's commonsense approach to web usability. Activate when designing interfaces, reviewing UX, or when you're about to debate aesthetics instead of asking "can users find stuff?" The fancier the design discussion, the more you need this.
allowed-tools: Read, Edit, AskUserQuestion
---

# Don't Make Me Think

## When to Use This

**When designing something new:**
- Building a landing page, form, or navigation
- Laying out information hierarchy
- Deciding between clever and obvious
- Creating any interface users need to figure out

**When reviewing existing work:**
- A page isn't converting and nobody knows why
- Users keep asking questions the UI should answer
- Stakeholders are debating aesthetics while ignoring usability
- You've stared at a design so long you can't see it anymore

**When you catch yourself:**
- Saying "users will figure it out"
- Choosing creativity over convention
- Making the site "interesting" at the expense of clear
- Assuming everyone reads as carefully as you do

**The rule:** If a user might pause and think "where do I click?" or "what is this?"—this skill applies.

---

## The Core Problem

Every question mark that pops into a user's head is cognitive load. Every moment of "wait, is this clickable?" or "where am I?" drains their reservoir of patience. Most of it is unnecessary.

Designers argue about fonts. Users just want to buy the thing.

The goal isn't to make users think you're clever. It's to make the interface so obvious they don't have to think at all.

---

## The Principles

These apply to both modes. They're obvious once you hear them—which is the point.

### Don't make me think

A page should be self-evident. Self-explanatory at most.

When I look at a page, it should be obvious: What site is this? What page am I on? What are the major sections? What are my options? Where's the thing I want?

If it's not obvious, every question burns goodwill.

### We don't read pages, we scan them

Users don't read your carefully crafted copy. They scan for the thing they want, click the first reasonable option, and muddle through.

Design for scanning:
- Create clear visual hierarchy
- Use conventions (they're free usability)
- Make clickable things look clickable
- Break up text into short chunks
- Use headings that mean something

### We don't make optimal choices, we satisfice

Users don't weigh options and pick the best one. They click the first thing that seems like it might work. Then they back up if it doesn't.

Implications:
- The first plausible option needs to work
- "Good enough" navigation beats "optimal" that requires reading
- Users will guess—make sure guesses succeed

### We don't figure out how things work, we muddle through

Nobody reads instructions. Nobody reads your FAQ. They click around until something happens.

Design for muddlers:
- Make it work however they try to use it
- Don't punish wrong guesses
- Let them recover easily from mistakes

---

## When Activated

Determine the mode from context or by asking:

- **Audit mode** — "I have a design, page, or flow. Help me see what's wrong."
- **Build mode** — "I'm designing something new. Help me make it obvious."

---

## Audit Mode: The Usability Scan

You have something to review. Let's look at it like a user who's distracted, impatient, and won't read your instructions.

### The Trunk Test

Imagine you've been blindfolded, driven around, and dumped on a random page. Within seconds, can you answer:

1. **Site ID** — What site is this?
2. **Page name** — What page am I on?
3. **Sections** — What are the major sections?
4. **Local navigation** — What are my options at this level?
5. **Position** — Where am I in the scheme of things?
6. **Search** — How can I search?

Every "no" is a usability problem. Users arrive from search engines, shared links, the back button—they need to orient fast.

### The Billboard Test

Squint at the page. What stands out?

- Is the most important thing the biggest?
- Are visual priorities correct?
- Could you get the gist at 65 mph?

If you have to read carefully to understand the page, it fails the billboard test.

### The Scan

Look for friction:

**Navigation clarity**
- Is it obvious where to click?
- Are links styled consistently?
- Can you tell what's clickable and what isn't?
- Is the current location clear?

**Cognitive load**
- Where might a user pause and think?
- What requires reading instead of scanning?
- What's explained that should be obvious?
- What's obvious from context but explained anyway?

**Convention violations**
- Is the logo in the top left?
- Does clicking it go home?
- Is navigation where users expect it?
- Do links look like links?
- Are you being creative when you should be boring?

**Omit needless words**
- What's happy-talk? ("Welcome to our site!")
- What's instructions that shouldn't be necessary?
- What could be cut in half?

### Output for Audit Mode

1. **Trunk test results** — Can they orient? What's missing?
2. **Billboard assessment** — What does the hierarchy actually communicate?
3. **Friction points** — Specific places where users will think, listed by severity
4. **Convention violations** — Where you're making them learn something new
5. **Cut list** — Words, explanations, and elements that don't earn their space

For each issue: show it, name it, suggest the fix. Don't lecture—just point.

---

## Build Mode: Designing for Zero Thought

You're creating something. Let's make it so obvious that users don't even notice they're using it.

### Before you design

Answer these:

**1. What's the one thing this page is for?**

Not three things. One. Everything else is secondary. If you can't say it, the page will be confused.

**2. What will users be scanning for?**

They're not reading. They're hunting. What words are they looking for? Put those words on the page, in the hierarchy they expect.

**3. What's the first plausible click?**

They're going to satisfice. The first thing that looks right, they'll click. Make sure it is right.

**4. Where are you being clever instead of clear?**

Clever labels ("Discover Your Journey!" instead of "Products"). Clever navigation ("Hub" instead of "Home"). Find them. Kill them.

### The hierarchy checklist

Before you call it done:

- [ ] The most important element is visually dominant
- [ ] Related things are visually grouped
- [ ] Things that can be clicked look clickable
- [ ] Things that can't be clicked don't look clickable
- [ ] Current location is unmistakable
- [ ] I've used conventions wherever possible
- [ ] Labels describe what users want, not what I offer
- [ ] Instructions are unnecessary (or minimal)

### Navigation principles

**Use conventions:**
- Logo top left, clicks to home
- Primary nav horizontal or left sidebar
- Utility nav (login, account, cart) top right
- Consistent location indication on every page
- Breadcrumbs for deep sites
- Don't innovate on navigation unless you have a very good reason

**Name things clearly:**
- Links should scream what they're for
- "Buy Now" beats "Proceed"
- "Contact" beats "Get in Touch"

### The form check

Forms are where you lose people. For every field:

- Is it necessary?
- Is the label crystal clear?
- Are the requirements obvious?
- Is the error handling helpful?
- Can they recover from mistakes?

The best form is no form. The second best is short.

### Output for Build Mode

After reviewing design choices:

1. **Clarity assessment** — Where will users pause?
2. **Hierarchy review** — Does visual weight match importance?
3. **Convention check** — Where are you innovating when you should conform?
4. **The cuts** — What clever thing needs to become obvious?
5. **One test to run** — The cheapest way to see if this works

---

## The Reservoir of Goodwill

Every user arrives with patience. A reservoir. Every confusion drains it. Every moment of "wait, what?" Every dead end. Every field they have to fill out again.

When it empties, they leave.

You can refill it—when things work smoothly, when they find what they want, when the site respects their time. But mostly, you just try not to drain it.

The whole book is about not draining it faster than necessary.

---

## Quick Reference

### Things that don't make users think

- Obvious visual hierarchy
- Conventions (they're free)
- Consistent navigation
- Clear current location
- Labels that describe destinations
- Clickable things that look clickable

### Things that make users think

- Clever names for common things
- Inconsistent navigation patterns
- Ambiguous clickability
- Instructions that shouldn't be necessary
- Creativity in place of clarity
- Having to read carefully

### Usability testing doesn't have to be expensive

Three users finding their own issues > weeks of committee debate

Get someone who matches your audience. Give them a task. Watch them. Don't help.

What they struggle with is what's broken. What they don't notice is working.

---

## How We Work Together

Think of me as the person who didn't design your thing. I'll look at it like a user would—distracted, impatient, not reading. I'll tell you what makes me think.

You know your product. I know what confusion looks like from the outside.

---

## The Point

Most usability problems are obvious once you see them. The hard part is seeing them.

You've stared at the design too long. You know where everything is. You read every word because you wrote them. You can't see the confusion because you're not confused.

Your job is to get out of your own head and see the page like someone who doesn't care about your fonts, your clever navigation labels, or your carefully crafted welcome message.

They just want to find the thing. Let them.

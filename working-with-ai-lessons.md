# Working with AI Like a Good Professional

> AI-generated summary extracted from Akita On Rails' blog posts:
>
> - [How to Talk to Claude Code Effectively](https://akitaonrails.com/en/2026/04/15/how-to-talk-to-claude-code-effectively/)
> - [VS Code é o novo Cartão Perfurado](https://akitaonrails.com/2026/04/11/vs-code-e-o-novo-cartao-perfurado/)

---

## Mindset Lessons

### AI amplifies who you already are

If you're good, AI accelerates good code. If you're bad, it accelerates technical debt at industrial speed. AI won't turn a bad programmer into a good one. It never did, it doesn't, and it won't.

### Fundamentals matter more now, not less

With AI handling syntax and boilerplate, what remains is the hard part: domain modeling, architecture, trade-offs, performance, scalability, security, observability, maintainability, and cost. These still require human judgment. The agent can write code — knowing whether the code is any good is still on you.

### The real skill was never typing code

Each era changes the input interface (punch cards → assembler → compilers → IDEs → AI agents), but the core discipline remains: instructing a machine to compute something useful within real constraints. Whoever understands this survives any tool change. Whoever doesn't becomes an operator of the current trend.

### Developers are terrible communicators — that's the root problem

Most frustrations with LLMs come from asking too little and expecting too much. People fire off requests assuming everything in their head is also in the AI's context. When the result falls short, they blame the tool instead of the question. Vague requests + undefined scope = guaranteed failure — with humans or AI.

### Think Stark + Jarvis, not magic

Jarvis alone doesn't build Iron Man. Stark's vision, judgment, and stubbornness are what make it real. And even Stark iterated through 85 suits — engineering was never about one perfect shot. AI speeds up each lap of the cycle, it doesn't erase the laps.

### Stop being a code typist — become a tech lead

The shift is from "operator of an editor" to orchestrator: define intent, explain context, demand criteria, request plans, ask for tests, request refactoring, compare alternatives, review changes. Leave the manual labor to the agent; use your brain for direction, priority, risk, and quality.

### Use AI aggressively while the window is open

Don't freeze waiting for the "perfect" moment or worrying about sustainability of AI pricing. Reevaluate when things change, but extract maximum value now. The rational move is to learn and leverage everything you can while others are busy explaining why they haven't started yet.

### AI won't replace good professionals

It will replace people who can't frame their own questions, don't know what they want, and can't validate results. Those people were always replaceable — now the replacement is just cheaper. The good professional got a 2 a.m. pair programmer with no ego.

---

## Practical Tips

### Structure every request in 4 blocks

1. **What you want** — the end goal in plain language
2. **How you want it** — broad strokes, leaving room for suggestions
3. **What you DON'T want** — the most critical and most skipped part; this is where unspoken assumptions live
4. **How to validate** — expected result, test criteria, the "done" signal

### Front-load context, then switch to asking

In the opening turns, pour in everything: goal, constraints, method, validation. Once the ground is solid, stop prescribing and start asking: *"Given everything we've covered, what's the best approach here?"* The LLM has more breadth than you — let it propose options you hadn't considered.

### Treat it as pair programming, not fire-and-forget

Stay in the conversation. Watch execution, suggest adjustments, catch errors mid-flight, add context you just remembered. The initial prompt is a starting point, not a final contract. Short cycles, fast feedback, continuous correction.

### State domain knowledge explicitly

The AI can't discover what's only in your head. Environment context (hardware, network, infra), domain rules, past decisions, edge cases — if it's not in the code, docs, or your prompt, it doesn't exist for the model.

### Design for resilience in long tasks

- Break work into numbered, idempotent steps
- Persist state (e.g., SQLite) instead of relying on in-memory variables
- Add human gates between planning and execution phases
- Set explicit safety constraints (e.g., "zero deletions on source directories")

### Balance oversight — avoid both extremes

Don't blindly `git push` everything the agent produces (outsourcing responsibility). Don't nitpick every semicolon either (killing productivity). The sweet spot: use XP practices — continuous refactoring, tests, CI, code review, fast feedback, small incremental changes.

### Output quality is proportional to input effort

If you don't care about the result (quick experiment, throwaway prototype), cut back on detail. If the result matters, invest the time to explain properly. This has always been true with contractors, teams, and now with AI.

### Use the right harness, not just the right model

The model matters less than the tooling around it. Evaluate planning capabilities, parallel execution, task tracking, and workflow integration. A weaker model with a better harness can outperform a stronger model with a worse one.

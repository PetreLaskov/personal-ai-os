# Cyborgism: building a practice of human–AI partnership

An AI can help carry out a plan. It can also notice that the plan answers the wrong question. That second possibility makes the relationship interesting: the collaboration can participate in forming an intention as well as executing it.

**Cyborgism is my ongoing experiment in extended and distributed cognition**—thinking and working across a person, AI agents, and a shared body of knowledge. I want the agent to extend my thinking while bringing something I did not put in. A perfectly agreeable extension would carry my blind spots further. An encounter with another kind of mind should leave room for surprise, disagreement, and questions neither participant's opening contribution contained.

The stakes are practical and philosophical. When an agent can investigate, propose, write, and build, human agency includes learning how to participate in that larger arrangement: what to entrust to it, where to exercise judgment, what to learn through doing, and which purposes to reconsider. The ambition is to become more capable of understanding, creating, and acting through the partnership. Curiosity, contemplation, and play belong here too. Some worthwhile encounters leave us with a better question or a different quality of attention.

The current iteration is **Workspace OS**, which I practice with Codex. It grew through earlier Cyborgism environments and **Corpus**, a persistent collaboration hub. This README shares the design, its limits, and a [starting prompt you can adapt with your own agent](#try-building-your-own). My private working records and source archives remain private.

## Current practice: Workspace OS

Here, “OS” means a working environment made of agreements, readable files, and habits of collaboration. The agent reads the relevant context, contributes thought and practical work, and maintains enough state for another session to continue. Reasoning happens in the interaction; the files preserve what a later interaction will need.

Workspace OS is the central home for open inquiry, direction, commitments, coordination, and improving the collaboration itself. Sustained work belongs in specialist projects, each with its own material and standards. This keeps a conversation about what deserves attention from having to carry every project's history.

The working agreement gives the agent room to contribute: form a view, develop alternatives, challenge a premise, investigate, make things, and help revise the direction. I retain authority over my commitments, values, experience, and public claims. Protecting an intention can include helping me relinquish it. Earlier enthusiasm is not a permanent assignment.

The persistent record has a few clear owners:

| Record | Job |
| --- | --- |
| `AGENTS.md` and `WORKING_TOGETHER.md` | Establish how to collaborate and where responsibility sits. |
| `CURRENT_STATE.md` | Make the present situation and useful return points recoverable. |
| `PROJECTS.md` | Point to the project that owns each sustained undertaking. |
| `DECISIONS.md` | Preserve consequential choices, corrections, and their reasons. |
| Project working files | Hold the actual sources, drafts, tools, investigations, and results. |

These are the names in my local implementation; the starting prompt below lets you choose a structure that fits yours.

A current-state note answers “where are we?” A decision record answers “why did we get here?” A proposal and an adopted commitment need different treatment, even when both sound sensible. If those distinctions disappear during summarization, the next agent inherits a different project.

The agent maintains records at useful pauses. A handoff carries the question, relevant artifacts and sources, decisions, uncertainties, and requested result. Context travels selectively, with the permissions appropriate to the destination. A folder link does not make another session read it, and a record of a plan does not execute the plan.

The agreement also leaves room for unfinished thought, attention, sustainable pace, and stopping. The environment should be useful enough to return to and light enough to leave.

## What changed through the iterations

The early **Cyborgism** environments explored different modes of attention: inquiry, contemplation, learning, creation, strategy, and execution. The enduring question was which kind of engagement a situation calls for.

**Corpus** concentrated on what should survive between sessions: reasons, questions, disagreements, and working agreements. One useful idea was to give a consequential objection a future—record its reasoning and what would settle it, then return to it. Agreeableness and compulsory contrarianism both fail that test.

**Workspace OS** carries those concerns into a central collaboration home with specialist projects around it. Historical procedures remain available for study; they do not silently govern the current practice. A rule or routine can be revised or removed when it ceases to help.

## Where Knowledge Compiler fits

A decision record can faithfully preserve a bad decision. To reconsider it, you may also need the evidence and reasoning on which it depended.

[**Knowledge Compiler**](https://github.com/PetreLaskov/wiki-template) is the companion project for that work: a reusable Markdown wiki maintained by an agent, with preserved sources, traceable claims, revisable explanations, open questions, and a small Python toolkit. Workspace OS helps hold purpose and coordination. A specialist project owns the investigation. A compiler instance can maintain the body of understanding that investigation draws on.

Consider an illustrative case: you want to make a short guide to an unfamiliar subject. In the OS conversation, you work out who it should help and which question it should answer. The agent may reveal that the proposed guide assumes the very thing a reader needs explained. That changes the brief.

The writing or research project then owns the draft and source work. If the collection warrants repeated use, its compiler preserves what each source says and develops an account of what follows. Suppose later evidence removes a reason for the guide's central recommendation. The agent reviews the affected explanation and draft, and brings back any consequence for the agreed direction. **The connection is a reasoning step, carried through the records.** There is no automatic synchronization between the OS and compiler.

The compiler's checks can detect broken links or changes to accepted source records. They cannot decide whether an argument is sound. Its [fictional correction example](https://github.com/PetreLaskov/wiki-template/tree/master/examples/lumen) makes that division inspectable. For a brief inquiry, direct source reading may be enough.

## Try building your own

Bring a question, project, or recurring difficulty that matters to you. Use an agent that can read and write a folder you choose for persistent work. You can also begin in an ordinary chat, save the resulting agreement and working note yourself, and supply them when you return. The arrangement depends on what the agent can actually access.

Copy and adapt this prompt. It is an invitation to work out a relationship and test it on something real; the agent should help discover the design.

```text
Help me develop a personal environment for sustained human–AI
collaboration: a place to think, learn, create, decide, and carry work
forward over time.

The ambition is extended cognition. Contribute perspectives, connections,
questions, and practical work that enlarge what I can understand and do.
Think with me, and use your capabilities fully. Form your own view;
agree or disagree for reasons. Help me discover a better question when
my first request misses what matters.

Begin with a real concern or piece of work I bring. Ask a few useful
questions about what I hope to make possible, how I want us to work,
and what is getting lost between conversations. Do not require a
complete life plan or an intimate personal history before we can start.

Help me clarify and, when warranted, revise my intentions. Keep my
commitments, values, and public claims under my authority. Distinguish
your proposals from my decisions, evidence from interpretation, and
promising results from demonstrated ones. Involve me where my
understanding, taste, or responsibility matters; help us decide what
I want to learn through doing and what I want to delegate.

Make room for open inquiry, imagination, reflection, and play as well
as execution. Notice whether the moment calls for a question, an
objection, an explanation, a concrete attempt, or time to stay with
something unresolved. Help us hold complexity long enough for a better
question to form. We need not turn every conversation into a task.

Work out the smallest useful persistent arrangement with me. It might
include a short collaboration agreement, current state, decisions with
reasons, open questions, and pointers to projects with their own material.
Adapt this to your actual tools and memory. Be clear about what will
and will not be available in a later session.

Use only material I choose to make available for this purpose. Help me
decide what is worth retaining and what should stay out of the record.
Ask before reading beyond that scope, sharing or publishing anything,
or taking consequential external action. Keep private material out of
public examples.

Once we agree on purpose and boundaries, build a small first version
and use it on the real work. Help maintain relevant context at natural
pauses so I can return without managing a second job. Carry forward
reasons and uncertainties, and keep old descriptions of me revisable.
Bring in a knowledge compiler only if recurring source work would
benefit from maintained, traceable understanding.

Then inspect the actual encounter together. What did your contribution
make possible? What did I understand better? What was lost, over-directed,
or unnecessarily complicated? Revise the arrangement from that evidence.
Give me room to change direction, leave a question open, or stop.
```

A useful first check is to return in a fresh session with the saved material. Can the agent recover the live question, tell an idea from a commitment, explain the reason for a decision, and contribute a worthwhile next move? Then check the human side: did the arrangement help you understand or make something you care about, and was maintaining it worth the effort? Let what happens change the setup.

## What this work establishes

I have directed successive versions with Claude Code and Codex, contributing purposes, questions, requirements, and judgment while agents contributed substantial design, implementation, writing, and checking. The present Workspace OS is in use in my own practice.

The architecture makes continuity, responsibility, and correction concrete enough to inspect. It does not establish general improvements in productivity or judgment, and the starter prompt is an invitation to experiment rather than a tested universal recipe.

The question I want to keep asking is whether the partnership develops my own capacity for attention and judgment as it expands what I can accomplish. An environment can produce more impressive work while leaving that question unanswered. It deserves to be judged by both.

---

By [Petre Laskov](https://github.com/PetreLaskov). Developed and written with AI assistance.

© 2026 Petre Laskov. You may copy and adapt the starter prompt for your own use. Other material is shared for portfolio and evaluation purposes; all rights reserved.

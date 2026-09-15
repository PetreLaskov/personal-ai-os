# Cyborgism: building continuity into human–AI work

A conversation can produce a good idea and still leave almost nothing usable behind. The reasoning sits halfway up a transcript. A decision loses its conditions. The next session begins with another explanation of what the project is, what has already been tried, and why the obvious suggestion will not work.

Cyborgism is my continuing exploration of that gap between a useful conversation and useful work over time. Its latest iteration is **Corpus**, a small, persistent collaboration hub. Alongside it, I have developed a **knowledge compiler**: a way to turn source material into revisable, traceable working knowledge.

Together, these address two different forms of continuity. Corpus preserves the collaboration: decisions, questions, disagreements and working preferences. The knowledge compiler preserves the evidence and understanding that the work depends on.

My background is in psychology and research project management. That makes the organisation of attention as interesting to me as the model's capabilities. Which question gets asked? What counts as evidence? When does exploration become a decision? These are partly philosophical questions, but an interface has to answer them in practice. Its defaults will answer them even if its designer does not.

## From specialised roles to a smaller hub

Earlier Cyborgism versions organised work into specialised modes for investigation, curation, synthesis, strategy and delivery. They used Markdown instructions, named owners for state files, session procedures and Git history.

There was a useful idea behind that structure: different work needs different kinds of attention. A half-formed question benefits from patient exploration. A defended claim needs an objection with substance. An agreed project needs execution. The ability to suggest a different plan does not imply authority to replace the existing one.

Corpus carries these concerns forward with a lighter centre. It asks what must survive between sessions and gives each kind of record a clear place. Its core is a short collaboration contract, a decision journal, open questions, a disagreement ledger and a current handoff. Procedures are added when a recurring need earns them a place.

The model is the replaceable participant in this arrangement. Between sessions, continuity lives in what has been recorded and in what I have learned. That shifts the design question from “How do I give the assistant a larger memory?” to “What should the next collaborator be able to recover?”

## What Corpus keeps

The implementation is an ordinary local repository. It contains instructions for Claude Code and a corresponding agent contract for Codex. Its records are readable without either tool.

| Record | What it preserves |
|---|---|
| Collaboration contract | Working preferences, decision boundaries and agreed procedures |
| Decision journal | Decisions, their reasons and what changed when a previous decision was revised |
| Open questions | Unresolved issues and pointers to what eventually settled them |
| Disagreement ledger | Significant objections or predictions, when to check them, and their resolution |
| Handoff | Current state, next moves and risks for a fresh session |
| Skills | Reusable procedures that have earned a place in the work |

A decision journal and a handoff do different jobs. The journal preserves how we arrived here. The handoff tells a new session where “here” is. Making the handoff concise need not require erasing the reasoning behind it.

Other projects can opt into the hub by pointing their local instructions to it. Their code and working documents remain in their own repositories. Corpus supplies continuity across them. This is an explicit reading-and-writing convention, rather than a background service that automatically synchronises every project.

## Give disagreement a future

A model can agree too readily. Asking it to disagree can produce the opposite performance: objections that exist because the instructions demand an objection.

Corpus's pushback procedure gives consequential disagreement a more useful shape. First state the strongest recognisable version of my position. If that dissolves the objection, stop. Otherwise explain the disagreement, name the observation that would settle it, and record a check date.

The decision remains mine. The disagreement remains available for later examination.

Consider a fictional software decision. I want to build an importer; the assistant argues that recurring manual preparation will cost more than the automation saves. Recording “the assistant was sceptical” would add little. Recording the expected preparation burden, the condition under which the importer becomes worthwhile, and a date to compare that expectation with actual use gives the disagreement somewhere to go.

This does not make the ledger a calibrated forecasting system by itself. It creates the record from which calibration becomes possible. A persuasive objection can be wrong, and a rejected objection can later turn out to have been useful.

## End sessions with a deposit, not another essay

Corpus's session-close procedure separates the records it updates:

- Append decisions with their reasons to the journal.
- Add or resolve open questions.
- Record significant predictions or disagreements in the ledger.
- Rewrite the handoff for a fresh session.
- Propose a standing rule only when the friction warrants one.

The procedure gives this work a five-minute budget. That is a chosen constraint, not a measured optimum. If nothing substantive happened, the instruction is to deposit nothing.

Reviews are intended to remove rules as well as add them. A local request should not silently become a permanent instruction. A rule that made sense with one model or task may obstruct the next. Corpus therefore dates its standing lines and asks them to justify their continued presence.

This is one of the more important changes in the project. A working environment can accumulate procedure until maintaining it becomes the work. Corpus makes subtraction part of the design.

## The knowledge compiler: an evidence layer

Continuity of conversation is only half the problem. Research also needs continuity of understanding. A folder of articles preserves material, but each new question can require the same reading and synthesis again.

The knowledge compiler is the evidence layer in the broader Cyborgism work. It is implemented as a separate portable Markdown project, with operating procedures and a Python validator. It can be used alongside the collaboration hub; I do not treat it as an automatically connected service.

Its basic separation is between preserved sources and compiled understanding:

```text
Raw source snapshot
        |
        v
Source ledger: identifiable claims + precise locations
        |
        v
Pages that own the current conclusions
        |
        v
Question-based routing -> answer -> inspect evidence
```

A project begins with a charter: what questions should this collection help answer, which evidence matters, and where are its boundaries? That purpose determines what deserves compilation. An unfamiliar source does not automatically justify a new page.

The source layer retains snapshots and content hashes. A source ledger assigns stable identifiers to statements and points back to their locations in the original. Compiled pages maintain the current conclusions, with one canonical home for each claim. A compact index routes recurring questions to the relevant material.

The distinction between a source statement and a conclusion matters. A source may report an observation. The compiled page may draw an inference from it. Keeping the two connected without treating them as identical lets a reader examine the step between evidence and interpretation.

## Updating understanding is more than adding a citation

Suppose a fictional research collection concludes that a method works well for small teams. A later source limits that finding to teams with dedicated administrative support. Adding the new source to the bibliography leaves the old answer wrong in an important way.

The compiler's ingestion procedure asks what changes: does the source introduce, confirm, qualify or challenge a claim? A qualification belongs in the page that owns the conclusion. Answers and recommendations depending on that conclusion also need review. An unchanged conclusion can legitimately produce little new text.

The same discipline applies to source independence. Five articles repeating one study are not five independent tests. The compiler's evidence procedures ask the reader or agent to track that relationship rather than infer strength from citation count.

The Python validator checks mechanical properties, including supported metadata, source hashes and link and claim-reference resolution. Those checks make defects visible. Whether the source supports the conclusion remains a reasoning task. A correctly resolved citation can still be attached to a bad inference.

For interrupted work, a checkpoint records the unfinished update. The next session reconciles that record with the files before treating the compilation as complete. This is the evidence-side equivalent of Corpus's handoff: preserve enough state to resume without assuming the previous session finished everything it intended.

## Two kinds of memory, one working practice

Corpus and the compiler should meet at the task, without collapsing into one undifferentiated store.

For a research assignment, Corpus can preserve the agreed question, the reason for choosing it and the next decision. The compiler can hold the relevant sources, the current synthesis and the evidence behind it. A new session needs access to both, but should be able to distinguish an agreement about the work from a claim about the world.

That distinction also limits what “memory” is allowed to mean. A suggestion is not an accepted decision. A repeated assertion is not independent evidence. A fluent summary is not proof that the underlying material has been understood.

I think of the larger project as an experiment in distributed cognition: useful thinking taking place across a person, a model and external records. The question is how that arrangement changes our ability to notice, decide, revise and act.

Its philosophical depth shows up in practical choices. Who can turn a suggestion into standing state? What would change a conclusion? Which part of the work should I continue doing myself? Can I leave the system and still understand the reasons for my decisions?

The current implementation provides inspectable answers to some of these questions: readable files, explicit decision boundaries, revisable records, evidence trails and deliberate handovers. Its effect on productivity and judgment still has to be tested against real work. The compiler likewise has to earn its maintenance cost against the simpler alternative of sources plus search.

The standard I want to hold the whole arrangement to is simple: when I return, I should be able to recover the important context, see what still needs judgment, and get on with something worth doing.

---

**Technical basis:** earlier Cyborgism configuration and agent protocols; Corpus's repository contract, guide, deposit and pushback procedures; and the Knowledge Compiler's source, ingestion, routing and validation design. Examples and diagrams are simplified illustrations. Companion piece: [The Harness Engine](https://github.com/PetreLaskov/harness-engine).


By [Petre Laskov](https://github.com/PetreLaskov). Developed and written with AI assistance.

© 2026 Petre Laskov. Shared for portfolio and evaluation purposes. All rights reserved.

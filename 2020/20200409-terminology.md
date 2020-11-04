# About

## Purpose

This meeting serves as a discussion and decision-making moment for several proposed terminology changes. The results may lead to changes in the Hypergraph glossary and p2pcommons specs.

## Meeting format

We run by the topics 1-by-1 and make decisions on each. If we don’t have time for each topic, we decide whether to meet again (possibly in smaller groups) for the remaining topics.

# Topics

## Publish

### Reasons to change

- Publish feels very “definitive” - perhaps even scary for new users?
- Unpublish action is not self-evident
- Publish to profile vs publish to vault may be confusing

### Suggestions

- JL: It makes sense to me to not define vault terminology yet, as the appropriate verbiage depends on the implementation, which is not decided yet. For example, we could use publish, sync, backup, archive, register, secure…
- CH (added by JL): If we use “publish”, does that make us a publisher? Might be wiser not to use “publish” at all.
- JL: Use “Add to profile” (or “Post to profile”) and “Remove from profile”. This feels less definitive and very literally matches the action performed.
- JG: I like “add / remove to profile”, or register / unregister as we had before, but now I really understood it.

### Decision

- Add to / remove from profile <- JL creates issues
- Update specs "register" terminology when approaching v1

## Dat archives + protocol://

### Reasons to change

Hyperdrive is more “correct” as Dat is the user-facing technology and Hyperdrive is the dev-facing technology

### Suggestions

- JL: Replace Dat archive with Hyperdrive and use Hyperdrive key, Hyperdrive version and Module URL with a custom protocol, for example p2pcommons://
- CHJH: Leave out the protocol name in the p2pcommons specs for futureproofing (e.g., Beaker is maybe switching to hyper:// → begs the question whether dat.json manifest stays with that name too?)
- JG: +1 for moving from Dat to Hyper. Not sure about the protocol yet, but ideally it matches the json file name.

### Decision

- Adjust terminology from Dat archive to Hyperdrive, (versioned/unversioned) Hyperdrive key, Hyperdrive version (remove mentions of URL)
- Remove protocol from specs
- Maintain interoperability with other Hyperdrive-based applications
- Talk to Paul regarding dat.json filename CHJH
- Settle nearer v1 of the module specs - mid June
- JL and/or CH

## Parents

### Reasons to change

The Hypergraph Desktop app uses "follows from" instead of parents and it helps to keep terminology in sync across products

### Suggestions

- JG (from Glossary doc): “.follows = []”
- JL: “.follows-from = []”
- JL: Should we then also change “.subtype” to “.content-type”?
- JL: Leave as-is. User-facing terminology might change frequently. Is it worth it to make breaking changes to the SDK each time? And what about when we’re past SDK 1.0?
- CHJH: I don’t see this as a spec discussion? It’s a user-facing question right? Parents is apt and specific for the spec.
- JG: “follows-from” is inconvenient in JavaScript and uncommon for JSON, as it needs to be escaped: `module[‘follows-from’]` vs `module.follows`. If we want to keep the “from”, it would more conveniently be “followsFrom”
- JG: It’s confusing to call it “parent” here and “follows from” there, extra points if we can unify. In the end we’re building an ecosystem, and not dev-tooling vs user-tooling.

### Decision
Leave as-is for now

# Deferred Time-Event Scope

`daysPassed` is used by map/scenario systems rather than by ordinary reusable adventure objects. It appears in at least two families:

- scenario victory/defeat conditions, where `DAYS_PASSED` means "the scenario reaches a fixed day threshold";
- reward or quest limiters, where `daysPassed` prevents a reward or mission from being available before a given global day.

Timed map events and town events are handled separately through `firstOccurrence` and `nextOccurrence`. These are editor-authored events that can give or remove resources, display messages, and remove objects at a chosen date or repeating interval.

For the first implementation pass of monthly/weekly simultaneous turns, these systems are intentionally out of scope. They are mostly used by custom scenario and campaign maps, and mapmakers for this mod should avoid relying on them during the desynchronized first-month phase until a dedicated local-clock design is implemented.

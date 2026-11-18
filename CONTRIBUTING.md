# Contributing

Thank you for helping other APIC users.

## Tips

One tip per file in `tips/`, named `<short-name>.md`:

```markdown
# <What the tip does, as a short sentence>

<When it helps, in one or two sentences.>

<The streams.json / config.json lines or the steps.>

Manual: <name of the Help page and section>
```

A tip must work with a released APIC version. Say which version you tried it with.

## Samples

Each sample is its own folder `samples/<name>/` (lower case, words joined with `-`):

- `README.md`: what it shows, what hardware it needs, how to run it (copy one of the existing READMEs);
- `project/`: the project folder (`config.json`, `Setups/streams.json`, `Models/`, `ICD/`, `CMakeLists.txt`);
- no build output (`out/`, `.vs/`), no recordings larger than a few MB, nothing you may not share.

When the pull request is merged, the workflow zips the folder and publishes it as the release `sample-<name>`
(see [samples/README.md](samples/README.md)).

## Problem reports

Use the Bug report form. The more of the CoreEngine's printed text you include, the faster it is answered.

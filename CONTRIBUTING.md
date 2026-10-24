# Contributing to llm-es

## Specs model the normative text

A spec describes the standard's own rule, not a simplification of it. If a rule is
not modelled yet, file a **Spec gap** issue that quotes the section and its
MUST/SHOULD/MAY text. Don't ship a shortcut.

## Changes to a spec

- Every rule you add or change needs an assertion that would fail under the old behaviour.
- Run `npm run validate -- <spec dir>` from a compiler checkout on each top-level package your change touches.
- A spec used by only one other spec lives in that spec's `deps/`. When it gains a
  second consumer, move it to the top level and update the `dependencies:` paths.

## Commits

Keep commits focused. A change that touches several specs belongs in one PR.

## License

By contributing, you agree that your contributions are licensed under the MIT License.

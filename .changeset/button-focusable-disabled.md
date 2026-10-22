---
'@astryxdesign/core': patch
---

[fix] Button: disabled buttons no longer render the native `disabled` attribute. They stay focusable in keyboard tab order, retain focus when becoming disabled while focused, and expose `aria-disabled="true"`. All activation paths (mouse clicks, Enter, Space) and clickAction/onClick callbacks remain blocked without losing focus to the document body. This satisfies AST-085 (FR1–FR4, FR6). Tests that assert `toBeDisabled()` or `:disabled` should query `[aria-disabled="true"]` instead.

@Geervan

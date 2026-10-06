---
'@astryxdesign/core': patch
---

[fix] Re-promote ToastViewport to the top layer when adding a toast so it paints above modal dialog backdrops

Top layer elements stack in insertion order. When a modal dialog opens after `ToastViewport` mounted, the dialog previously rendered above the toast viewport and obscured toasts behind its backdrop. `ToastViewport` now re-promotes its popover whenever a toast is dispatched, keeping toasts dispatched while a modal dialog is open visible above the dialog backdrop.

@Geervan

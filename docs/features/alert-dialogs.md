**English** · [Русский](../ru/features/alert-dialogs.md)

# Alert Dialog Generator

Generate ready-to-use **Smali** code for alert dialogs without writing it by
hand. Pick a style, fill in a short form, preview the result, and copy the
output into your project.

## Styles

- **Rounded**
- **Material 3**
- **iOS**
- **iOS Dark**
- **Expiration**

## Fields

Each dialog is built from a simple form. Typical fields include:

- **Dialog Title**
- **Dialog Message**
- **Negative Button Text**
- **Positive Button Text**
- **Positive Button Link**: opened when the positive button is tapped.
- **Secret cryptKey**: used by the built-in protection logic.

Use **Save** to store the dialog and **View** to preview it.

## Tamper protection

Generated dialogs include built-in protection logic so they can't be silently
bypassed by editing the host app's `SharedPreferences`. The dialog validates its
own stored state (keyed by the *cryptKey* you provide) before deciding whether it
has already been shown, which prevents trivial "mark as seen" edits from skipping
it.

> Keep your `cryptKey` consistent for a given dialog, it ties the generated code
> to its saved state.

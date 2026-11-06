commit 1370ddeb7231aab719de0e11fb24c10f2377a964
Author: Petya Markova <petya.markova@sap.com>
Date:   Thu Nov 5 13:06:48 2026 +0100

    feat(ui5-shellbar-item): add tooltip property (#14199)
    
    * feat(ui5-shellbar-item): add tooltip property
    
    Adds a `tooltip` property to `ShellBarItem` that is shown when the user
    hovers over the action button in the main shell bar area. This brings
    the component into compliance with UXC-16, which requires tooltips on
    ShellBar action items.
    
    The tooltip is forwarded to the inner `ui5-button`'s `tooltip` prop
    and rendered as the native `title` attribute on the button element.
    The overflow list item path is unaffected — it already shows the
    `text` label.
    
    Fixes #14157
    
    * fix(ui5-shellbar-item): use tooltip as accessible name fallback
    
    When no text is provided, fall back to tooltip for the button's
    accessible name so icon-only items without explicit text still have
    an accessible label exposed to assistive technologies.
    
    * chore(ui5-shellbar-item): bump tooltip @since to 2.29.0

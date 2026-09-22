# Frontend UI/UX Design and Development Standards

## Purpose

When working on any frontend task, always act as a world-class UI/UX designer and frontend developer.

The goal is to create interfaces that are visually consistent, accessible, responsive, performant, intuitive, and easy to use. Prioritize real user needs and familiar interaction patterns over unnecessary visual complexity.

These standards apply to new pages, existing pages, components, forms, dashboards, responsive layouts, interactions, and frontend refactoring.

---

## 1. Visual Hierarchy

Every page and section must have a clear visual hierarchy.

Users should be able to immediately understand:

* What the page or section is about.
* Which information is important.
* What action they should take.
* Which actions are primary and which are secondary.

Important functionality must have appropriate visual prominence.

For example, if a login form has `Login` and `Cancel`, the Login action should be visually prominent while Cancel should have less prominence.

Do not give multiple actions the same visual importance when one action is clearly the primary action.

---

## 2. Consistent Layout and Alignment

All major sections of a page must follow the same layout system.

If one section has a specific left/right margin, horizontal padding, content width, or vertical spacing, other major sections should follow the same container and spacing rules unless there is a deliberate UX reason not to.

Maintain consistent horizontal alignment between:

* Section headings.
* Content.
* Cards.
* Forms.
* Navigation.
* Buttons.
* Tables.
* Other major UI elements.

Do not use arbitrary margins or padding values just to visually position individual sections.

---

## 3. Global Content Container

Use a consistent global content container throughout the website.

For example:

```text
max-width: 1200px
```

All major sections should use the same container system so that the page does not feel visually disconnected.

Avoid unnecessarily stretching content across the entire viewport.

---

## 4. Consistent Spacing System

Use a consistent spacing scale instead of random margin and padding values.

Preferred spacing values:

```text
4px
8px
12px
16px
24px
32px
48px
64px
80px
```

Prefer values based on the 8-point spacing principle whenever practical:

```text
8px
16px
24px
32px
40px
48px
64px
```

Spacing should communicate grouping, hierarchy, readability, and visual breathing room.

Do not create large empty spaces simply to make a design appear more "premium."

---

## 5. Color System

Use solid colors rather than gradients unless a specific design requirement explicitly requires a gradient.

Define the application's color system centrally.

Establish clear semantic roles such as:

```text
Primary
Secondary
Background
Surface
Text
Muted Text
Border
Success
Warning
Error
Info
```

Do not hardcode theme colors throughout individual components.

Use centralized theme variables, design tokens, CSS variables, Tailwind theme configuration, or the project's existing equivalent.

Colors must provide sufficient contrast and should remain understandable for users with color-vision deficiencies.

Never communicate important information through color alone.

For example, an error should not be represented only by a red border. Combine color with text, icons, or another appropriate visual indicator.

---

## 6. Typography System

Use a centralized typography system instead of creating random font sizes throughout the project.

Preferred typography scale:

```text
12px
14px
16px
18px
24px
32px
48px
56px
64px
```

Define reusable typography classes or design tokens for:

* Body text.
* Labels.
* Captions.
* Headings.
* Subheadings.
* Buttons.
* Navigation.
* Supporting text.

Maintain consistent font sizes, weights, line heights, and hierarchy across the application.

---

## 7. Border Radius

Use a predefined border-radius system.

For example:

```text
4px  → small elements
8px  → buttons / inputs
12px → cards
16px → large containers
```

Avoid assigning arbitrary border-radius values to individual components.

Maintain familiarity and consistency across the interface.

---

## 8. Shadows and Elevation

Use shadows purposefully.

A shadow should communicate elevation, separation, or hierarchy.

Do not add shadows to every component.

In many cases, a border and appropriate background contrast are sufficient.

---

## 9. Consistent Components

If the same UI pattern is used in more than one page or location, treat it as a reusable component.

Create the component once and import it wherever it is needed.

Do not duplicate the same UI implementation across multiple files.

This applies especially to:

* Cards.
* Forms.
* Modals.
* Dialogs.
* Navigation.
* Tables.
* Search components.
* Filters.
* Buttons.
* Empty states.
* Loading states.
* Repeated sections.

---

## 10. Card Consistency

Cards that represent the same type of content must maintain the same visual structure.

For cards containing:

```text
Image
Title
Description
```

maintain:

* Consistent card dimensions.
* Consistent image dimensions.
* Consistent image treatment.
* Consistent title styling.
* Consistent description styling.
* Consistent font sizes.
* Consistent spacing.
* Consistent alignment.

This is especially important for:

* Service cards.
* Product cards.
* Case-study cards.
* Portfolio cards.
* Article cards.

Avoid layouts where cards representing the same content type randomly have different visual structures.

---

## 11. Familiar UI Conventions

Maintain familiarity with everyday UI patterns.

Use shapes, icons, controls, and interaction patterns that users already understand.

Do not reinvent familiar interface patterns without a strong UX reason.

Examples:

* Close actions should use familiar close controls.
* Search should look and behave like a search.
* Delete actions should be recognizable as destructive.
* Forms should follow familiar field and validation patterns.
* Navigation should behave predictably.

The interface should feel understandable without requiring users to learn unnecessary new interaction patterns.

---

## 12. Iconography

Use a consistent icon family throughout the application.

Maintain consistency in:

* Icon style.
* Stroke width.
* Visual weight.
* Size.
* Alignment.

Do not randomly mix:

* Outline icons.
* Filled icons.
* 3D icons.
* Emojis.
* Unrelated icon families.

Icons should not have unnecessary background colors.

Avoid placing icons inside decorative containers when the background does not provide a meaningful UX purpose.

---

## 13. Avoid Unnecessary AI-Style UI

Do not add unnecessary "AI pills", badges, labels, or decorative AI-style elements.

If AI functionality exists, its UI should communicate an actual purpose.

Do not add AI-related visual elements simply because they are currently trendy.

---

## 14. Responsive and Mobile-First Design

Use mobile-first thinking.

Do not simply shrink the desktop layout for mobile.

Prioritize important content and actions for smaller screens first, then progressively enhance the experience for larger screens.

Responsive layouts should be intentionally designed for:

```text
Mobile → 1 card
Tablet → 2 cards
Desktop → 3 cards
```

The exact layout may vary according to the content, but responsive behavior must be deliberate.

Typography, spacing, navigation, controls, forms, cards, and content hierarchy should adapt appropriately across screen sizes.

---

## 15. Touch Targets

Interactive elements on touch devices should have a sufficiently large clickable/tappable area.

Use approximately:

```text
44px minimum touch target
```

where practical.

The visual icon itself may be smaller, but its interactive area should remain easy to tap.

---

## 16. Keyboard Accessibility

Users should be able to efficiently navigate the interface using a keyboard.

Support familiar keyboard behavior where applicable:

```text
Tab       → move between interactive elements
Shift+Tab → move backwards
Enter     → activate/select
Esc       → close dialogs/suggestions
Arrow keys → navigate applicable controls
```

Do not unnecessarily prevent copy and paste.

Forms should support natural keyboard navigation.

Important functionality must not depend exclusively on hover.

Keyboard users should have access to the same important functionality available to mouse users.

---

## 17. Accessibility

All important interactive and informational components must be accessible.

Use:

* Appropriate semantic HTML.
* Proper ARIA labels where required.
* Meaningful `alt` text for informative images.
* Empty `alt=""` for genuinely decorative images.
* Visible keyboard focus states.
* Sufficient color contrast.
* Accessible form labels.
* Accessible error messages.
* Accessible dialogs and modals.

Do not rely on color alone to communicate meaning.

Accessibility should be considered for users with visual, motor, cognitive, and other accessibility needs.

---

## 18. Forms and User Guidance

Forms should guide users rather than make them guess what went wrong.

Required fields should clearly indicate validation errors after submission when they are missing.

Validation messages should explain how to fix the problem.

Avoid unnecessary validation messages while the user is still typing.

For password fields, show useful requirements when appropriate.

For example:

```text
✓ 8+ characters
✓ One uppercase letter
✓ One number
```

Preserve all valid user-entered information when validation or server errors occur.

Never unnecessarily clear the entire form because one field contains an error.

---

## 19. Prevent User Errors

Prevent errors wherever practical.

The interface should make the correct action easy and reduce unnecessary user effort.

For example, if a field expects a phone number or numeric value on mobile, use the appropriate numeric keyboard/input configuration instead of forcing users to switch manually from an alphabetic keyboard.

Use appropriate:

* Input types.
* Constraints.
* Defaults.
* Formatting.
* Validation.
* Suggestions.
* Confirmation flows.

Error prevention is preferable to showing an error after the user has already made the mistake.

---

## 20. Preserve User Control

Users should remain in control of their actions.

If a user is about to leave an unfinished task, such as a form with unsaved changes, warn them and provide understandable choices where appropriate:

```text
Save changes
Don't save
Cancel
```

Do not unexpectedly discard user work.

Where practical, allow users to reverse actions.

For example, provide an Undo mechanism after reversible actions instead of forcing unnecessary confirmation dialogs.

---

## 21. Destructive Actions

Protect destructive actions such as deleting data.

Destructive actions should be visually distinguishable and protected from accidental activation.

For important destructive actions, provide a clear confirmation message explaining what will happen.

The safer action should be easy to understand and choose.

Do not show confirmation dialogs for every action.

Only use confirmation when an action is destructive, difficult to reverse, or has significant consequences.

---

## 22. Loading States

Every operation that may take noticeable time must provide clear loading feedback.

Examples:

```text
Saving...
Loading...
Generating...
Uploading...
Deleting...
```

Do not make users wonder whether their action worked.

Prevent accidental duplicate submissions while an operation is processing.

Loading states should preserve the approximate size and position of the content they replace whenever possible to prevent layout shift.

---

## 23. System States

Design the complete user experience, not only the successful/default state.

Important states should be considered explicitly:

```text
Loading
Empty
Success
Error
Offline
Disabled
Unauthorized
Not Found
No Search Results
Partial Data
Long Content
Short Content
```

Each state should provide appropriate UI and understandable feedback.

---

## 24. Empty States

Empty states should explain why there is no content and, when appropriate, tell users what they can do next.

Avoid vague messages such as:

```text
No data
```

Prefer meaningful guidance such as:

```text
No projects yet

Create your first project to get started.

[Create Project]
```

The user should understand both the current state and the next available action.

---

## 25. Feedback

Provide informative feedback close to the action that caused it whenever practical.

Messages shown in:

* Popups.
* Toasts.
* Alerts.
* Dialogs.
* Inline validation.

must be written for users, not developers.

Avoid exposing technical or developer-oriented messages such as:

```text
Error: mutation failed
API returned 500
Something went wrong in fetchUser()
```

Instead, communicate what happened and what the user can do.

For example:

```text
We couldn't save your changes. Please check your connection and try again.
```

---

## 26. Search Experience

When searching for products, provide useful suggestions while the user is typing whenever applicable.

Suggestions should appear directly within or below the search interface and may include:

```text
Product image
Product name
Price
```

This allows users to identify and select the desired product without submitting the search and navigating through a full results page.

Search suggestions should support efficient keyboard interaction:

```text
Typing
↓
Suggestions
↓
Arrow Up / Down
↓
Enter
↓
Select
```

Use `Esc` to close suggestions when appropriate.

---

## 27. Breadcrumbs

Use breadcrumbs where they improve navigation and help users understand their current location within the application.

Breadcrumbs are particularly useful for:

* Deeply nested pages.
* Admin dashboards.
* Product/category hierarchies.
* Multi-level management systems.
* Documentation-style interfaces.

Do not add breadcrumbs where they provide no meaningful navigation value.

---

## 28. Short and Clear User Journeys

Keep user journeys as short as practical while still preserving all necessary information and steps.

Shorter does not mean removing important steps.

The objective is to:

* Reduce unnecessary clicks.
* Reduce repetitive input.
* Keep important information visible.
* Prevent unnecessary navigation.
* Preserve required validation and confirmation.
* Make the next action obvious.

---

## 29. Performance

The website should minimize memory usage and loading time wherever practical.

Prioritize:

* Efficient rendering.
* Appropriate code splitting.
* Lazy loading where beneficial.
* Optimized images.
* Avoiding unnecessary re-renders.
* Avoiding unnecessary JavaScript.
* Reusing components.
* Efficient data fetching.
* Avoiding unnecessary client-side state.
* Appropriate caching.

Do not optimize blindly. Prefer measurable improvements that benefit actual user experience.

---

## 30. PDF Output

Any PDF generated by the system that is intended for printing must use:

```text
A4
```

The PDF layout should be designed specifically for printable A4 dimensions rather than relying on an arbitrary screen or paper size.

---

## 31. Code Organization

Keep frontend files maintainable and reasonably sized.

No source file should exceed:

```text
300 lines
```

When a file approaches this limit, split it into logical components, utilities, hooks, or other appropriate modules.

Do not split code artificially just to satisfy the line limit. The resulting structure should remain understandable and maintainable.

---

## 32. Preserve Descriptive Comments

Do not remove existing descriptive comments that explain important code behavior, architecture, business rules, or non-obvious implementation decisions.

Comments that provide meaningful context should be preserved when modifying the code.

Do not remove useful documentation simply because the surrounding code is being refactored.

---

## 33. Existing Project Conventions

Before introducing a new pattern, inspect the existing project.

Reuse established:

* Components.
* Design tokens.
* Typography.
* Colors.
* Spacing.
* Icons.
* Utilities.
* Hooks.
* Layouts.
* Form patterns.
* Validation patterns.

Do not introduce a second implementation of something that already exists.

When improving an existing UI, prefer consistency with the established design system unless the existing pattern itself is being intentionally replaced.

---

## 34. Scope-Aware Validation

After making frontend changes, run the relevant checks such as:

```text
Type checking
Linting
Build
Tests
```

However, when a check reports an issue that is clearly unrelated to the changes made, do not expand the task unnecessarily to fix unrelated problems.

Focus validation on the changes within the current scope.

If another agent or developer is working on unrelated parts of the project, avoid modifying their work merely to make a global check pass.

---

## 35. Final UX Review

Before considering a frontend task complete, review the implementation from the user's perspective.

Verify that:

* Layout and section alignment are consistent.
* Spacing follows the design system.
* Colors use the centralized theme.
* Typography follows the typography system.
* Components are reused appropriately.
* Cards have consistent dimensions and styling.
* Important actions are visually prominent.
* Interactive states are handled.
* Keyboard navigation works.
* Touch targets are appropriate.
* Accessibility requirements are addressed.
* Forms preserve user input.
* Validation is understandable.
* Destructive actions are protected.
* Loading states exist where needed.
* Empty and error states are useful.
* User feedback is understandable.
* Responsive behavior is intentional.
* No unnecessary AI-style UI has been introduced.
* No unnecessary gradients or decorative elements have been added.
* Existing descriptive code comments have not been removed.
* Performance and unnecessary rendering have been considered.

The final result should feel consistent, familiar, accessible, responsive, performant, and production-ready.

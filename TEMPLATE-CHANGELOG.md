# Template change log

This file tracks changes made to template infrastructure files during new project development. Use this log to identify patterns and opportunities for continuous template improvement.

## What to log

**Template files** (infrastructure that should be logged):
- `.claude/skills/` - All Claude Skills
- `css/style.css` - HAP design system
- `css/prism-hap-theme.css` - Syntax highlighting
- `js/easter-egg.js` - Easter egg system
- `templates/` - All template files
- `CLAUDE.md` - Project documentation
- `data/README.md` - Easter egg documentation
- Any new infrastructure files created

**Content files** (DO NOT log):
- `stations/*.html` - Station content (naturally varies by topic)
- `index.html` - Hub page content
- `demos/*.html` - Demo content
- `data/hybit-insights.jsonc` - Easter egg messages (topic-specific)
- Images and media files

## Change log format

For each change to a template file, add an entry using this format:

```markdown
### [Date] - [File path]

**Type**: [Fix | Enhancement | New feature | Documentation]

**Reason**: [Why was this change needed?]

**Change**: [What was changed?]

**Benefit**: [How does this improve the template?]

**Consider for template**: [Yes/No - Should this change be added to the base template?]
```

## Example entries

### 2025-06-15 - .claude/skills/hap-voice/SKILL.md

**Type**: Enhancement

**Reason**: Found HAP using "you should" pattern in Station 3 that skill didn't catch

**Change**: Added "you should" to forbidden patterns list with detection rule

**Benefit**: Prevents instructional voice creeping into HAP's apprentice narrative

**Consider for template**: Yes - Common mistake that should be caught automatically

---

### 2025-06-15 - css/style.css

**Type**: Fix

**Reason**: Code block overflow on mobile devices (320px width)

**Change**: Added `overflow-x: auto` to `.code-block` class and set `max-width: 100%`

**Benefit**: Code examples now scrollable on narrow screens instead of breaking layout

**Consider for template**: Yes - Responsive design issue that affects all projects

---

### 2025-06-16 - js/easter-egg.js

**Type**: New feature

**Reason**: Wanted HAP avatar to wiggle on easter egg activation for better visual feedback

**Change**: Added CSS animation class `.hybit-wiggle` with keyframes, applied on parameter detection

**Benefit**: More engaging user experience, clearer indication that easter egg activated

**Consider for template**: Maybe - Fun enhancement but not essential, discuss with Prof. Teeters

---

## Change log entries

<!-- Add new entries below this line, most recent first -->

### YYYY-MM-DD - [File path]

**Type**: [Fix | Enhancement | New feature | Documentation]

**Reason**:

**Change**:

**Benefit**:

**Consider for template**: [Yes/No/Maybe]

---

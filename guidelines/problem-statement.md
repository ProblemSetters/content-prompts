# Problem Statement Guidelines

Standards for creating and evaluating problem statements in coding assessments.

---

## Core Principles

### 1. Product Manager Voice (STRICT)

Write as if it comes from a Product Manager – clear, business-focused, realistic. This checkpoint is **STRICT**: the presence of **ANY** technical implementation detail is an automatic FAIL.

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Describes **what** needs to be achieved from a product/business perspective | Describes **how** to implement technically |
| Clear expectations ("what is expected", "what do we need") | Literal technical implementation guidance |
| Describes desired outcomes and business requirements | Step-by-step "tutorial" instructions |

---

#### ⚠️ AUTOMATIC FAIL TRIGGERS

The presence of **ANY ONE** of the following is an **automatic FAIL** for PM-style voice. Scan the entire problem statement for these violations:

| Category | Examples | Why it's a FAIL |
|----------|----------|-----------------|
| **Variable/State Names** | `isFlipped`, `isLoading`, `setCount`, `userData`, `handleClick` | Prescribes internal naming |
| **Boolean/Conditional Logic** | "When isFlipped is true...", "If X then Y", "When false, show Z" | Prescribes implementation logic |
| **CSS Class Names** | "append `flipped` to className", "add class `active`", "remove `hidden` class" | Prescribes styling implementation |
| **Specific File Paths** | "in FlashCard/index.tsx", "Update src/components/X.ts", "modify file Y" | Prescribes code location |
| **Function/Method Names** | "create a function called X", "implement handleSubmit", "call fetchData()" | Prescribes function design |
| **React/Framework Hooks** | `useState`, `useEffect`, `useMemo`, `useCallback`, `useContext`, `useReducer` | Prescribes state management approach |
| **Type/Interface Definitions** | "Create a type with: id (number), name (string)", "interface should have X, Y, Z" | Prescribes data modeling |
| **DOM Manipulation** | "append X to div", "update innerHTML", "set textContent to Y" | Prescribes DOM approach |
| **Component Architecture** | "The application has two components: X and Y where functionality should be implemented" | Prescribes component structure |
| **Implementation Steps** | "Step 1: Update X, Step 2: Add Y to Z", numbered implementation instructions | Tutorial-style guidance |
| **String/Value Literals** | "'' is appended", "show 'Error' message", "display 'Loading...'" | Prescribes exact values |
| **Data Structure Details** | "store in an array", "use a Map/Set", "create an object with keys X, Y" | Prescribes data structures |

---

#### ✅ What IS Acceptable (PM-Style)

These are acceptable because they describe **outcomes**, not **implementation**:

| Acceptable | Why |
|------------|-----|
| "Users can flip a card to see the answer" | Describes user outcome, not how to implement |
| "The card should show question on front, answer on back" | Describes visual requirement |
| "Clicking a card reveals the other side" | Describes interaction behavior |
| "Cards can be shuffled to appear in random order" | Describes feature outcome |
| "Ensure shuffled order differs from original" | Describes acceptance criteria |

---

#### ❌ What is NOT Acceptable (Technical Hand-Holding)

These are violations because they prescribe **how to implement**:

| Violation | Why it Fails |
|-----------|--------------|
| "Update the isFlipped constant to a state variable" | Prescribes variable name AND implementation approach |
| "When isFlipped is true, flipped is appended to divs with class flashcard-content" | Prescribes boolean logic, CSS class, and DOM manipulation |
| "Create a type for FlashCard with properties: id (number), question (string)" | Prescribes type name and structure |
| "in FlashCard/index.tsx" | Prescribes file location |
| "The application has two components: FlashCardDeck.tsx and FlashCard.tsx" | Prescribes component architecture |

---

### 2. Open-Ended Scope

Allow multiple valid solution paths rather than prescribing a single approach.

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Broad, open-ended problem allowing multiple solution paths | Narrow, prescriptive instructions with single solution path |
| Limited ambiguity only where natural trade-offs exist (e.g., caching vs. querying) | No room for candidate decision-making |

---

### 3. Real-World Alignment

Frame problems that reflect actual product development scenarios.

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Reflects actual product development scenarios | Artificial, academic-style problems |
| Tests real engineering judgment | Tests rote implementation |

The problem should test whether a candidate can:
- Break down the problem into smaller sub-problems
- Prioritize effectively
- Consider edge cases
- Balance quick solutions vs. optimal approaches
- Show awareness of performance and security within scope
- Demonstrate a product mindset beyond "just coding"

---

### 4. Requirements Design

Include both mandatory and optional requirements.

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Contains "good-to-have" requirements alongside core requirements | Only mandatory requirements with no optional enhancements |
| Gives candidates opportunity to demonstrate going above and beyond | Binary pass/fail with no room for excellence |

---

## Structure Requirements

### Mandatory Structure (3 Parts)

1. **Business Context** (2-3 lines MAX)
   - Brief explanation of why this feature matters from a business perspective
   - Sets the stage without technical details
   - Keep it concise – no more than 2-3 sentences

2. **Product Requirements**
   - Bullet-point based requirements (use `<ul>` or `<ol>`)
   - PM-style language – outcomes, not implementation steps
   - Clear, scannable format
   - Include both core and good-to-have requirements

3. **Technical Reference Note**
   - Single line directing candidates to `TECHNICAL_CONSIDERATIONS.md`
   - Example: "For technical specifications including test data and validation rules, refer to TECHNICAL_CONSIDERATIONS.md"

### Formatting Standards

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Small paragraphs and bullet points for easy scanning | Heavily bloated with large paragraphs |
| Well-formatted with clear sections and whitespace | Wall of text without proper formatting |
| Logical flow: Context → Requirements → Notes | Unstructured content that is difficult to parse |

---

## HTML Output Format

### Required Style Tag

**CRITICAL:** Always include this exact style tag at the beginning of the HTML file. Copy it verbatim – do not modify.

```html
<style type="text/css">.ps-content-wrapper-v0 div { margin: 0 auto; overflow: auto; } .ps-content-wrapper-v0 div.preheader { display: none; } .ps-content-wrapper-v0 p { white-space: pre-wrap; padding-left: 4px; padding-right: 4px; padding-top: 0px; padding-bottom: 2px; } .ps-content-wrapper-v0 p.section-title { font-weight: bold; padding-bottom: 0px; } .ps-content-wrapper-v0 ol.plain-list, .ps-content-wrapper-v0 ul.plain-list { list-style-type: none; padding: 4px; } .ps-content-wrapper-v0 li { white-space: normal; margin-top: 4px; margin-bottom: 4px; } .ps-content-wrapper-v0 code { color: black; } .ps-content-wrapper-v0 pre { background-color: #f4faff; border: 0; border-radius: 2px; margin: 8px; padding: 10px; } .ps-content-wrapper-v0 pre.scrollable-full-json { overflow-x: scroll; white-space: pre; } .ps-content-wrapper-v0 pre.scrollable-json { height: 300px; overflow-y: scroll; display: inline-grid; white-space: pre-wrap; padding-left: 8px; padding-right: 8px; padding-top: 4px; padding-bottom: 4px; } .ps-content-wrapper-v0 div.equation-parent { width: 400px; text-align: center; border: 1px solid #000; padding: 8px; } .ps-content-wrapper-v0 div.equation-parent.equation { width: 100%; display: inline-block; } .ps-content-wrapper-v0 figure { background-color: transparent; display: table; margin-top: 8px; margin-bottom: 8px; text-align: center; margin-left: auto; margin-right: auto; } .ps-content-wrapper-v0 figcaption { text-align: center; display: table-caption; caption-side: bottom; margin-top: 4px; margin-bottom: 4px; } .ps-content-wrapper-v0 img { width: auto; max-width: 100%; height: auto; } .ps-content-wrapper-v0 details { background-color: transparent; padding-left: 4px; padding-right: 4px; padding-top: 0px; padding-bottom: 2px; } .ps-content-wrapper-v0 details details { padding-left: 8px; padding-right: 8px; } .ps-content-wrapper-v0 details summary { background-color: #39424e; color: white; font-weight: bold; margin-top: 4px; margin-bottom: 4px; padding: 8px; } .ps-content-wrapper-v0 details details summary code { color: black; font-weight: bold; padding-left: 2px; padding-right: 2px; padding-top: 4px; padding-right: 4px; margin-left: 4px; } .ps-content-wrapper-v0 details div.collapsable-details { margin: 0 auto; padding-left: 4px; padding-right: 4px; padding-top: 0px; padding-bottom: 2px; overflow: auto; } .ps-content-wrapper-v0 details div.collapsable-details pre { margin-left: 4px; margin-right: 4px; margin-top: 4px; margin-bottom: 4px; } .ps-content-wrapper-v0 table.normal { border: 1px solid black; border-collapse: collapse; border-color: darkgray; margin: 0 auto; margin-top: 8px; margin-bottom: 8px; padding: 8px; width: 96%; table-layout: fixed; } .ps-content-wrapper-v0 table.normal tbody { display: block; overflow-x: auto; overflow-y: hidden; } .ps-content-wrapper-v0 table.normal tbody tr:first-child th { font-weight: bold; white-space: normal; } .ps-content-wrapper-v0 table.normal tbody tr th, .ps-content-wrapper-v0 table.normal tbody tr td { font-weight: normal; white-space: nowrap; text-align: center; vertical-align: middle; border: 1px solid black; border-color: darkgray; padding: 8px; } .ps-content-wrapper-v0 table.database-table { border-collapse: collapse; border-color: darkgray; border: 1px solid black; width: auto; margin-left: 4px; margin-top: 8px; margin-bottom: 8px; padding: 8px; } .ps-content-wrapper-v0 table.database-table tbody { overflow-x: auto; overflow-y: hidden; border: none; } .ps-content-wrapper-v0 table.database-table tbody tr th, .ps-content-wrapper-v0 table.database-table tbody tr td { font-weight: normal; white-space: nowrap; text-align: center; vertical-align: middle; border: 1px solid black; border-color: darkgray; padding: 8px; } .ps-content-wrapper-v0 table.database-table tbody tr th { font-weight: bold; border: 1px solid black; } .ps-content-wrapper-v0 table.database-table tbody tr:nth-child(2) td { border: 1px solid black; } .ps-content-wrapper-v0 table.database-table tbody tr:nth-child(n+2) td:first-child { border-left-color: black; } .ps-content-wrapper-v0 table.database-table tbody tr:nth-child(n+2) td:last-child { border-right-color: black; } .ps-content-wrapper-v0 table.database-table tbody tr:last-child td { border-bottom-color: black; } .ps-content-wrapper-v0 table.database-table tbody tr td.description { text-align: left; white-space: pre-wrap; } .ps-content-wrapper-v0 table.normal tbody tr th.description { width: 60%; } .ps-content-wrapper-v0 table.function-params tbody tr:first-child td.headers { border-bottom-width: 2px; } .ps-content-wrapper-v0 table.function-params tbody tr:last-child td { border-top-width: 2px; border-top-color: darkgray; } .ps-content-wrapper-v0 table.function-params tbody tr td.headers { width: 25%; font-weight: bold; text-align: center; border: 1px solid black; border-right-width: 2px; border-color: darkgray; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell { width: 100%; height: 100%; padding: 0px; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table { width: 100%; height: 100%; padding: 0px; margin: 0px; border: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr td.code { white-space: normal; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr th { border-top: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr th:first-child { border-left: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr th:last-child { border-right: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr:last-child td { border-bottom: 0; border-top-width: 1px; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr td:first-child { border-left: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr td:last-child { border-right: 0; } .ps-content-wrapper-v0 table.sudoku { border-collapse: collapse; border-color: darkgray; margin: 0 auto; margin-top: 8px; margin-bottom: 8px; padding: 8px; } .ps-content-wrapper-v0 table.sudoku colgroup, tbody { border: 3px solid black; } .ps-content-wrapper-v0 table.sudoku td { border: 1px solid black; height: 25px; width: 25px; text-align: center; padding: 0; } .ps-content-wrapper-v0 .left { text-align: left; } .ps-content-wrapper-v0 .right { text-align: right; } .ps-content-wrapper-v0 .code { font-family: monospace; white-space: nowrap; } .ps-content-wrapper-v0 .json-object-array ol, .ps-content-wrapper-v0 .json-object-array ol ul { margin-top: 0px; padding-left: 14px; } .json-object-array li { float: left; margin-right: 30px; margin-left: 10px; } .json-object-array pre { padding: 4px; margin-left: 0px; } .dropdown-heading { display: inline; color: #fff !important } details pre { white-space: pre-wrap; word-break: break-word; }
</style>
```

### HTML Structure Template

```html
<style type="text/css">/* ... style tag as above ... */</style>
<div class="ps-content-wrapper-v0">

<!-- SECTION 1: Business Context (2-3 lines max) -->
<p>Brief business context explaining why this feature matters. Keep this to 2-3 sentences maximum.</p>

<p>&nbsp;</p>

<!-- SECTION 2: Product Requirements -->
<p class="section-title"><strong>Product Requirements</strong></p>

<ul>
    <li>Requirement 1 - written as an outcome, not an implementation step</li>
    <li>Requirement 2 - clear and scannable</li>
    <li>Requirement 3 - PM-style language</li>
    <li><em>(Good to have)</em> Optional requirement for candidates to demonstrate excellence</li>
</ul>

<p>&nbsp;</p>

<!-- SECTION 3: Technical Reference Note -->
<p><strong>Note:</strong> For technical specifications including test data, validation rules, and data-testid attributes, refer to <code>TECHNICAL_CONSIDERATIONS.md</code>.</p>

</div>
```

### Semantic Tag Usage

| Element | Usage | Example |
|---------|-------|---------|
| `<p>` | Paragraphs, keep short | `<p>Business context here.</p>` |
| `<p class="section-title">` | Section headers | `<p class="section-title"><strong>Requirements</strong></p>` |
| `<ul>` / `<ol>` | Lists of requirements | `<ul><li>Requirement</li></ul>` |
| `<li>` | List items | `<li>Each requirement as a bullet</li>` |
| `<code>` | Inline code references | `<code>TECHNICAL_CONSIDERATIONS.md</code>` |
| `<pre>` | Code blocks | `<pre>code block content</pre>` |
| `<strong>` | Bold/emphasis for headers | `<strong>Note:</strong>` |
| `<em>` | Italics for optional items | `<em>(Good to have)</em>` |
| `<p>&nbsp;</p>` | Vertical spacing | Used between sections |
| `<table class="normal">` | Data tables | For tabular information |
| `<details>` / `<summary>` | Collapsible sections | Only if needed for optional info |

### HTML Rules

1. **Wrapper Required**: All content must be inside `<div class="ps-content-wrapper-v0">`
2. **No Inline Styles**: Do not add inline `style=""` attributes – use class names only
3. **Spacing**: Use `<p>&nbsp;</p>` for vertical spacing between sections
4. **Special Characters**: Properly escape HTML entities (`&lt;`, `&gt;`, `&amp;`, `&#39;`, `&quot;`)
5. **No Technical Hand-Holding**: Do not include function names, implementation patterns, or code structure guidance

---

## Ambiguity Scale (1-5)

Adjust clarity based on the desired difficulty level:

| Level | Description | Example |
|-------|-------------|---------|
| **1** | Extremely ambiguous – minimal context, candidate infers most details | "Users should be able to find information faster. Do what seems right." |
| **2** | High ambiguity – broad goals with minimal constraints | "We need better search. Consider what users expect." |
| **3** | Moderate ambiguity – clear goals with room for interpretation | "Implement a search feature for articles. Users should find relevant results quickly." |
| **4** | Low ambiguity – detailed requirements with minor decisions left to candidate | "Implement search for articles by title. Display results as a list. Consider pagination." |
| **5** | Extremely hand-held – clear instructions, little room for interpretation | "Implement a search bar on the homepage that queries the `articles` table by title and displays results in a list with pagination of 10 items per page." |

---

## Scope Preservation Rules

When upgrading existing problem statements:

1. **Preserve functional scope exactly** – do not add or remove requirements
2. **Rewrite acceptance criteria in narrative form** – but do NOT omit or alter them
3. **Preserve test data, seeded accounts, and critical details** – candidates need these for validation
4. **Do not split requirements** into functional vs. non-functional – keep blended
5. **Do not prescribe technical steps** – where to code, which functions to use

---

## Quality Indicators

### ✅ High-Quality Problem Statement

- Business context is 2-3 lines max – concise and relevant
- Requirements written as outcomes, not instructions
- Uses bullet points (`<ul>` / `<li>`) for requirements
- Includes both core and good-to-have requirements
- Multiple valid solution approaches possible
- Realistic scenario a candidate might encounter at work
- Properly formatted HTML with correct style tag

### ❌ Low-Quality Problem Statement

- Jumps straight into technical requirements
- Business context is bloated (more than 3 lines)
- Large paragraphs instead of bullet points
- Prescribes specific functions, hooks, or patterns to use
- Only one "correct" way to solve
- Feels like a tutorial or homework assignment
- Missing optional/stretch requirements
- Missing or modified style tag

---

## Scoring Guide (for evaluation)

| Score | Criteria |
|-------|----------|
| **5/5** | Perfect structure (context → requirements → note), 2-3 line context, bullet-point requirements, PM-style, includes optional requirements, correct HTML formatting |
| **4/5** | Good structure and formatting, mostly PM-style, minor technical hand-holding or slightly verbose context |
| **3/5** | Acceptable but has issues (bloated context, some missing bullets, or moderate technical hand-holding) |
| **2/5** | Poor formatting, poor structure, engineering-style, or significant technical hand-holding |
| **1/5** | Unreadable, unstructured, overly prescriptive with technical details, or missing/broken HTML |

---

## Evaluation Checklist

When reviewing a problem statement, assess:

- [ ] **Structure**: Business Context (2-3 lines) → Requirements (bullets) → Technical Note
- [ ] **Context length**: Max 2-3 sentences
- [ ] **Requirements format**: Bullet points, not paragraphs
- [ ] **PM-style voice**: Outcomes, not implementation steps
- [ ] **Scope openness**: Multiple valid approaches possible
- [ ] **Requirements design**: Core + good-to-have requirements present
- [ ] **HTML format**: Correct style tag, wrapper div, semantic tags
- [ ] **No technical hand-holding**: No function names, hooks, or patterns prescribed

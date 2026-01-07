# Interviewer Guidelines Standards

Standards for creating and evaluating interviewer guidelines in coding assessments.

---

## Purpose

Interviewer guidelines serve as the definitive reference for:
- Evaluating candidate submissions fairly and consistently
- Providing a reference implementation (ideal solution)
- Defining what "correct" looks like
- Enabling follow-up discussions that probe deeper understanding

---

## Required Structure (3 Collapsible Sections)

Interviewer guidelines **MUST** contain exactly three sections, each as a **collapsible `<details>` element**. Collapsible sections are mandatory because content can be lengthy and collapsible format improves readability.

### Section 1: Ideal Solution

The ideal solution is the cornerstone of the assessment.

**Requirements:**

| Requirement | Description |
|-------------|-------------|
| **Completeness** | Include ALL files that need modification |
| **Format** | Readable diff format with clear file markers |
| **Correctness** | Syntactically correct and runnable |
| **Alignment** | Must satisfy ALL requirements from the problem statement |
| **Documentation** | Inline comments explaining approach and key decisions |

**Code Format:**

```diff
// File: path/to/file.ext
- removed line
+ added line
```

**Quality Standards:**

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Complete code snippets demonstrating correct solution | Missing critical code snippets |
| Shows best practices and optimal approach for critical parts | Has bugs or shows suboptimal patterns |
| Partial code with key snippets is acceptable (doesn't need complete end-to-end) | Incomplete or unclear snippets |
| Covers both bare minimum and optimal implementations where applicable | Only shows one approach |

---

### Section 2: Evaluation Criteria

Provide clear, tiered criteria for assessment.

**Required Sub-sections:**

| Sub-section | Purpose |
|-------------|---------|
| **Bare Minimum Criteria** | What constitutes a passing solution – the "must haves" |
| **Good-to-Have Criteria** | What separates good from great solutions – excellence indicators |
| **Red Flags** | Common mistakes or anti-patterns to watch for |

**Quality Standards:**

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Criteria are specific and measurable | Vague criteria ("code is clean") |
| Aligned with problem statement requirements | Misaligned or unrelated to requirements |
| Covers both functional and non-functional aspects | Only covers functional correctness |
| Provides clear guidance for fair evaluation | Leaves room for inconsistent evaluation |

---

### Section 3: Recommended Follow-Up Questions

Provide recommended questions to probe candidate's depth.

**Topics to Cover:**

- Trade-offs in their approach
- Edge cases and how they'd handle them
- Scalability considerations
- Alternative approaches they considered
- Performance implications
- Security considerations (where applicable)

**Quality Standards:**

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Tests deeper understanding beyond implementation | Generic questions applicable to any problem |
| Explores extensions and what-if scenarios | Yes/no questions with obvious answers |
| Allows candidates to demonstrate expertise | Leading questions with expected answers |

---

## HTML Output Format

### Required Style Tag

**CRITICAL:** Always include this exact style tag at the beginning of the HTML file. Copy it verbatim – do not modify.

```html
<style type="text/css">.ps-content-wrapper-v0 div { margin: 0 auto; overflow: auto; } .ps-content-wrapper-v0 div.preheader { display: none; } .ps-content-wrapper-v0 p { white-space: pre-wrap; padding-left: 4px; padding-right: 4px; padding-top: 0px; padding-bottom: 2px; } .ps-content-wrapper-v0 p.section-title { font-weight: bold; padding-bottom: 0px; } .ps-content-wrapper-v0 ol.plain-list, .ps-content-wrapper-v0 ul.plain-list { list-style-type: none; padding: 4px; } .ps-content-wrapper-v0 li { white-space: normal; margin-top: 4px; margin-bottom: 4px; } .ps-content-wrapper-v0 code { color: black; } .ps-content-wrapper-v0 pre { background-color: #f4faff; border: 0; border-radius: 2px; margin: 8px; padding: 10px; } .ps-content-wrapper-v0 pre.scrollable-full-json { overflow-x: scroll; white-space: pre; } .ps-content-wrapper-v0 pre.scrollable-json { height: 300px; overflow-y: scroll; display: inline-grid; white-space: pre-wrap; padding-left: 8px; padding-right: 8px; padding-top: 4px; padding-bottom: 4px; } .ps-content-wrapper-v0 div.equation-parent { width: 400px; text-align: center; border: 1px solid #000; padding: 8px; } .ps-content-wrapper-v0 div.equation-parent.equation { width: 100%; display: inline-block; } .ps-content-wrapper-v0 figure { background-color: transparent; display: table; margin-top: 8px; margin-bottom: 8px; text-align: center; margin-left: auto; margin-right: auto; } .ps-content-wrapper-v0 figcaption { text-align: center; display: table-caption; caption-side: bottom; margin-top: 4px; margin-bottom: 4px; } .ps-content-wrapper-v0 img { width: auto; max-width: 100%; height: auto; } .ps-content-wrapper-v0 details { background-color: transparent; padding-left: 4px; padding-right: 4px; padding-top: 0px; padding-bottom: 2px; } .ps-content-wrapper-v0 details details { padding-left: 8px; padding-right: 8px; } .ps-content-wrapper-v0 details summary { background-color: #39424e; color: white; font-weight: bold; margin-top: 4px; margin-bottom: 4px; padding: 8px; } .ps-content-wrapper-v0 details details summary code { color: black; font-weight: bold; padding-left: 2px; padding-right: 2px; padding-top: 4px; padding-right: 4px; margin-left: 4px; } .ps-content-wrapper-v0 details div.collapsable-details { margin: 0 auto; padding-left: 4px; padding-right: 4px; padding-top: 0px; padding-bottom: 2px; overflow: auto; } .ps-content-wrapper-v0 details div.collapsable-details pre { margin-left: 4px; margin-right: 4px; margin-top: 4px; margin-bottom: 4px; } .ps-content-wrapper-v0 table.normal { border: 1px solid black; border-collapse: collapse; border-color: darkgray; margin: 0 auto; margin-top: 8px; margin-bottom: 8px; padding: 8px; width: 96%; table-layout: fixed; } .ps-content-wrapper-v0 table.normal tbody { display: block; overflow-x: auto; overflow-y: hidden; } .ps-content-wrapper-v0 table.normal tbody tr:first-child th { font-weight: bold; white-space: normal; } .ps-content-wrapper-v0 table.normal tbody tr th, .ps-content-wrapper-v0 table.normal tbody tr td { font-weight: normal; white-space: nowrap; text-align: center; vertical-align: middle; border: 1px solid black; border-color: darkgray; padding: 8px; } .ps-content-wrapper-v0 table.database-table { border-collapse: collapse; border-color: darkgray; border: 1px solid black; width: auto; margin-left: 4px; margin-top: 8px; margin-bottom: 8px; padding: 8px; } .ps-content-wrapper-v0 table.database-table tbody { overflow-x: auto; overflow-y: hidden; border: none; } .ps-content-wrapper-v0 table.database-table tbody tr th, .ps-content-wrapper-v0 table.database-table tbody tr td { font-weight: normal; white-space: nowrap; text-align: center; vertical-align: middle; border: 1px solid black; border-color: darkgray; padding: 8px; } .ps-content-wrapper-v0 table.database-table tbody tr th { font-weight: bold; border: 1px solid black; } .ps-content-wrapper-v0 table.database-table tbody tr:nth-child(2) td { border: 1px solid black; } .ps-content-wrapper-v0 table.database-table tbody tr:nth-child(n+2) td:first-child { border-left-color: black; } .ps-content-wrapper-v0 table.database-table tbody tr:nth-child(n+2) td:last-child { border-right-color: black; } .ps-content-wrapper-v0 table.database-table tbody tr:last-child td { border-bottom-color: black; } .ps-content-wrapper-v0 table.database-table tbody tr td.description { text-align: left; white-space: pre-wrap; } .ps-content-wrapper-v0 table.normal tbody tr th.description { width: 60%; } .ps-content-wrapper-v0 table.function-params tbody tr:first-child td.headers { border-bottom-width: 2px; } .ps-content-wrapper-v0 table.function-params tbody tr:last-child td { border-top-width: 2px; border-top-color: darkgray; } .ps-content-wrapper-v0 table.function-params tbody tr td.headers { width: 25%; font-weight: bold; text-align: center; border: 1px solid black; border-right-width: 2px; border-color: darkgray; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell { width: 100%; height: 100%; padding: 0px; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table { width: 100%; height: 100%; padding: 0px; margin: 0px; border: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr td.code { white-space: normal; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr th { border-top: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr th:first-child { border-left: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr th:last-child { border-right: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr:last-child td { border-bottom: 0; border-top-width: 1px; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr td:first-child { border-left: 0; } .ps-content-wrapper-v0 table.function-params tbody tr td.params-table-cell table.params-table tbody tr td:last-child { border-right: 0; } .ps-content-wrapper-v0 table.sudoku { border-collapse: collapse; border-color: darkgray; margin: 0 auto; margin-top: 8px; margin-bottom: 8px; padding: 8px; } .ps-content-wrapper-v0 table.sudoku colgroup, tbody { border: 3px solid black; } .ps-content-wrapper-v0 table.sudoku td { border: 1px solid black; height: 25px; width: 25px; text-align: center; padding: 0; } .ps-content-wrapper-v0 .left { text-align: left; } .ps-content-wrapper-v0 .right { text-align: right; } .ps-content-wrapper-v0 .code { font-family: monospace; white-space: nowrap; } .ps-content-wrapper-v0 .json-object-array ol, .ps-content-wrapper-v0 .json-object-array ol ul { margin-top: 0px; padding-left: 14px; } .json-object-array li { float: left; margin-right: 30px; margin-left: 10px; } .json-object-array pre { padding: 4px; margin-left: 0px; } .dropdown-heading { display: inline; color: #fff !important } details pre { white-space: pre-wrap; word-break: break-word; }
</style>
```

### HTML Structure Template

**CRITICAL:** All three sections MUST be collapsible using `<details>` and `<summary>` elements. This is mandatory because content can be lengthy.

```html
<style type="text/css">/* ... style tag as above ... */</style>
<div class="ps-content-wrapper-v0">

<!-- SECTION 1: Ideal Solution (COLLAPSIBLE) -->
<details open="open">
<summary class="section-title">
<h4 class="dropdown-heading">Ideal Solution</h4>
</summary>
<div class="collapsable-details">

<p>Brief explanation of the solution approach.</p>

<p class="section-title"><strong>File: path/to/file.ext</strong></p>
<pre>
// Complete code diff or implementation
// - removed line
// + added line

function example() {
  // Implementation with inline comments explaining key decisions
}
</pre>

<p>Additional files as needed...</p>

</div>
</details>

<!-- SECTION 2: Evaluation Criteria (COLLAPSIBLE) -->
<details>
<summary class="section-title">
<h4 class="dropdown-heading">Evaluation Criteria</h4>
</summary>
<div class="collapsable-details">

<p class="section-title"><strong>Bare Minimum Criteria</strong></p>
<ul>
    <li>Criterion 1 - what must be present for a passing solution</li>
    <li>Criterion 2 - specific and measurable</li>
</ul>

<p>&nbsp;</p>

<p class="section-title"><strong>Good-to-Have Criteria</strong></p>
<ul>
    <li>Criterion 1 - what separates good from great</li>
    <li>Criterion 2 - excellence indicators</li>
</ul>

<p>&nbsp;</p>

<p class="section-title"><strong>Red Flags</strong></p>
<ul>
    <li>Anti-pattern 1 - common mistake to watch for</li>
    <li>Anti-pattern 2 - indicates poor understanding</li>
</ul>

</div>
</details>

<!-- SECTION 3: Follow-Up Questions (COLLAPSIBLE) -->
<details>
<summary class="section-title">
<h4 class="dropdown-heading">Recommended Follow-Up Questions</h4>
</summary>
<div class="collapsable-details">

<ol>
    <li><strong>Trade-offs:</strong> Why did you choose this approach over alternatives?</li>
    <li><strong>Edge Cases:</strong> How would you handle [specific edge case]?</li>
    <li><strong>Scalability:</strong> How would this solution perform with 10x the data?</li>
    <li><strong>Alternatives:</strong> What other approaches did you consider?</li>
</ol>

</div>
</details>

</div>
```

### Semantic Tag Usage

| Element | Usage | Example |
|---------|-------|---------|
| `<details>` | Collapsible section wrapper | Required for all 3 main sections |
| `<summary class="section-title">` | Collapsible header (clickable) | Contains `<h4 class="dropdown-heading">` |
| `<h4 class="dropdown-heading">` | Section title inside summary | `<h4 class="dropdown-heading">Ideal Solution</h4>` |
| `<div class="collapsable-details">` | Content wrapper inside details | Wrap all content after summary |
| `<p class="section-title">` | Sub-section headers | `<p class="section-title"><strong>Bare Minimum</strong></p>` |
| `<ul>` / `<ol>` | Lists of criteria or questions | `<ul><li>Criterion</li></ul>` |
| `<pre>` | Code blocks | `<pre>code content</pre>` |
| `<code>` | Inline code | `<code>functionName()</code>` |
| `<strong>` | Bold text | `<strong>Important:</strong>` |
| `<p>&nbsp;</p>` | Vertical spacing | Between sub-sections |

### Collapsible Section Rules

1. **All 3 sections MUST be collapsible** using `<details>` and `<summary>`
2. **First section should be open by default**: Add `open="open"` to the first `<details>` tag
3. **Summary structure**: Always use `<summary class="section-title"><h4 class="dropdown-heading">Title</h4></summary>`
4. **Content wrapper**: Always wrap content in `<div class="collapsable-details">`
5. **Nested collapsibles**: Can use nested `<details>` for sub-sections if needed (e.g., multiple files in Ideal Solution)

### HTML Rules

1. **Wrapper Required**: All content must be inside `<div class="ps-content-wrapper-v0">`
2. **No Inline Styles**: Do not add inline `style=""` attributes – use class names only
3. **Spacing**: Use `<p>&nbsp;</p>` for vertical spacing between sub-sections
4. **Special Characters**: Properly escape HTML entities (`&lt;`, `&gt;`, `&amp;`, `&#39;`, `&quot;`)
5. **Code in Pre Tags**: All code snippets must be in `<pre>` tags with proper escaping

---

## Content Quality Standards

### Overall Guidelines Quality

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Provides clear guidance for fair evaluation | Vague or incomplete guidance |
| Helps assess both functional and non-functional aspects | Only focuses on "does it work" |
| Consistent with problem statement | Contradicts or misaligns with problem statement |
| Enables objective evaluation | Leaves too much to evaluator interpretation |
| All 3 collapsible sections present and properly structured | Missing sections or broken HTML |

---

## Scoring Guide (for evaluation)

| Score | Criteria |
|-------|----------|
| **5/5** | Perfect structure (all 3 collapsible sections), correct ideal solution with key code snippets, relevant criteria with all 3 sub-sections, insightful follow-ups, correct HTML formatting |
| **4/5** | Has all parts with minor issues in code snippets, completeness, or relevance |
| **3/5** | Missing one section/sub-section or has significant quality issues |
| **2/5** | Missing multiple sections or poor quality throughout |
| **1/5** | Does not follow structure, non-collapsible sections, or provides inadequate guidance |

---

## Evaluation Checklist

When reviewing interviewer guidelines, assess:

- [ ] **HTML Structure**: Style tag present, wrapper div, all sections collapsible
- [ ] **Section 1 present**: Ideal Solution with complete code snippets in `<pre>` tags
- [ ] **Section 2 present**: Evaluation Criteria with all 3 sub-sections (Bare Minimum, Good-to-Have, Red Flags)
- [ ] **Section 3 present**: Recommended Follow-Up Questions
- [ ] **First section open**: First `<details>` has `open="open"` attribute
- [ ] **Solution correctness**: Code is syntactically correct and runnable
- [ ] **Criteria relevance**: Aligned with problem statement requirements
- [ ] **Follow-up quality**: Questions probe deeper understanding
- [ ] **Consistency**: Guidelines don't contradict problem statement

---

## Constraints

1. **Ideal solution must be complete** – subsequent steps (e.g., test validation) may depend on it
2. **All sections must be collapsible** – using `<details>` and `<summary>` elements
3. **Maintain fairness** – criteria should not punish alternative correct approaches
4. **Ensure clarity** – evaluators should be able to assess consistently
5. **Keep acceptance criteria intact** – reword but don't omit requirements from problem statement

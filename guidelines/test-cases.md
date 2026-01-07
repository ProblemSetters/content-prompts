# Test Cases Guidelines

Standards for creating and evaluating test suites in coding assessments.

---

## Core Principles

### 1. Behavior-Driven Testing (Not Implementation-Driven)

Test what the code **does**, not **how** it does it.

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Test user-facing behavior and outcomes | Test internal implementation details |
| Tests pass for ANY correct solution approach | Tests only pass for one specific implementation |
| Test that user actions produce expected visible outcomes | Test that specific functions exist or are called X times |
| Test rendered output and API responses | Test internal state variables |

**Key Principle:** Tests must pass for any correct solution approach – do not punish alternative implementations.

---

### 2. Problem Statement Alignment

Every test should trace back to a requirement.

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Every requirement has test coverage | Requirements without corresponding tests |
| Tests edge cases and error scenarios | Only tests happy path |
| Map tests to specific acceptance criteria | Tests for features not in problem statement |

---

### 3. Fairness

Tests should evaluate correctness, not predict implementation choices.

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Tests accept multiple valid outputs where applicable | Tests expect exact implementation details |
| Clear error messages on test failures | Cryptic failures that don't help debugging |
| Deterministic tests (no flakiness) | Tests that randomly pass/fail |

---

## Scenario Coverage

### Required Coverage Types

| Coverage Type | Description |
|---------------|-------------|
| **Happy Path** | Normal/expected usage scenarios |
| **Edge Cases** | Boundary conditions, empty inputs, maximum values |
| **Error Scenarios** | Invalid inputs, error responses, failure modes |
| **Input Validation** | Malformed data, type mismatches, missing fields |
| **Business Logic** | Expected outcomes based on requirements |

### Quality Standards

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Covers happy paths, edge cases, boundary conditions, and error scenarios | Only tests happy path scenarios |
| Tests input validation and invalid data handling | Missing critical edge cases or error conditions |
| Tests for expected business logic outcomes | No error handling tests |
| Adequate number of tests for problem complexity | Too few tests for stated requirements |

---

## Test Quality & Best Practices

### Naming & Clarity

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Clear, descriptive test names that explain what is being tested | Generic or unclear test names |
| Names follow pattern: `should [expected behavior] when [condition]` | Names like `test1`, `test_function` |
| Meaningful error messages | No context on failures |

### Test Independence

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Tests are isolated and independent (no shared state) | Tests depend on each other or shared state |
| Proper use of setup/teardown (`beforeEach`, `afterEach`) | Tests must run in specific order |
| Each test can run standalone | Side effects leak between tests |

### Single Responsibility

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Tests one thing at a time | Overly complex tests that test multiple things |
| Clear assertion of one behavior | Multiple unrelated assertions |
| Easy to identify what failed | Unclear which part of test failed |

### Mocking & Isolation

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Mock/stub external dependencies appropriately | Real network calls in unit tests |
| Use `jest.fn()`, `jest.spyOn()`, MSW (Mock Service Worker) | Manual mocks and outdated patterns |
| Isolate unit under test | Tests break due to external service changes |

---

## Modern Testing Patterns

### Frontend (React/Angular/Vue)

**Preferred Libraries:**
- React Testing Library / Angular Testing Library (NOT Enzyme)

**Query Priority:**
1. Query by role, label, text (preferred)
2. Query by test ID (when semantic queries aren't possible)
3. Avoid CSS selectors

**User Interactions:**

```javascript
// ✅ PREFER: userEvent (more realistic - includes focus, blur, keyboard events)
userEvent.click(element)
userEvent.type(input, 'text')
userEvent.selectOptions(select, 'value')
userEvent.clear(input)
userEvent.upload(input, file)

// ✓ USE WHEN NEEDED: fireEvent (less realistic but sometimes necessary)
fireEvent.click(element)
fireEvent.change(input, { target: { value: 'text' } })
fireEvent.submit(form)
```

**Async Handling:**

| ✅ GOOD | ❌ POOR |
|---------|---------|
| `waitFor(() => expect(...))` | `setTimeout` or arbitrary delays |
| `findBy*` queries for async elements | `getBy*` immediately after async action |
| Proper async/await usage | Nested callbacks |

### Backend (Node.js/Python/Java)

| Pattern | Description |
|---------|-------------|
| Test API contracts and responses | Not ORM queries directly |
| Use supertest-style HTTP client testing | Direct function calls bypassing HTTP layer |
| Mock external services appropriately | Real calls to external APIs |
| Validate error responses, status codes, auth flows | Only test happy path responses |

---

## Test Organization

### Structure

| ✅ GOOD | ❌ POOR |
|---------|---------|
| Well-structured test suites with logical grouping (`describe`/`context` blocks) | Flat list of unrelated tests |
| Test files properly organized and named | Random test file locations |
| Related tests grouped together | Related tests scattered across files |

### File Naming Conventions

- `*.test.js` / `*.test.ts`
- `*.spec.js` / `*.spec.ts`
- Located in `__tests__/`, `test/`, `tests/`, or `spec/` directories

---

## Scoring Guide (for evaluation)

| Score | Criteria |
|-------|----------|
| **5/5** | Comprehensive tests covering all scenarios with excellent best practices, behavior-driven, clear names |
| **4/5** | Good test coverage with minor gaps in scenarios or best practices |
| **3/5** | Basic test coverage but missing important scenarios or has quality issues |
| **2/5** | Minimal tests with poor coverage or significant quality problems |
| **1/5** | No relevant tests or completely inadequate test suite |

---

## Evaluation Checklist

When reviewing test cases, assess:

- [ ] **Scenario coverage**: Happy path, edge cases, errors all covered
- [ ] **Problem alignment**: Tests match problem statement requirements
- [ ] **Naming clarity**: Test names explain what is being tested
- [ ] **Independence**: Tests don't depend on each other
- [ ] **Single responsibility**: Each test validates one behavior
- [ ] **Mocking**: External dependencies properly isolated
- [ ] **Async handling**: No arbitrary delays, proper waitFor/findBy usage
- [ ] **Organization**: Logical grouping and file structure
- [ ] **Fairness**: Alternative correct solutions would pass

---

## Test Upgrade Principles

When upgrading existing test suites:

1. **Preserve test count** – upgrade patterns, don't remove tests arbitrarily
2. **Maintain 1:1 mapping** – original count = upgraded count (unless consolidating true duplicates)
3. **Upgrade HOW tests are written** – not WHAT they test
4. **Keep same behavior being validated**
5. **Consolidate only true duplicates** – same behavior tested twice
6. **If tests are already high-quality → No Change**

---

## Constraints

1. **Alignment is critical**: Tests must pass the ideal solution from interviewer guidelines
2. **Preserve test coverage**: Upgrade patterns, don't remove tests arbitrarily
3. **Maintain fairness**: Don't punish alternative correct solutions
4. **Ensure debuggability**: Clear error messages on test failures
5. **Keep maintainable**: Readable tests with minimal duplication


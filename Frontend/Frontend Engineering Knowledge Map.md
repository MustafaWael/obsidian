# Frontend Engineering Knowledge Map

A structured map of the knowledge areas required to become a senior frontend engineer.  
Each section can later become its own note and be connected through internal links in [[Obsidian]].

---

# 1. Web Fundamentals

## Internet Basics
- HTTP / HTTPS
- Request–Response lifecycle
- DNS resolution
- TCP / TLS basics

## Browser Architecture
- Browser components
- Rendering engine
- JavaScript engine
- Event loop

## Core Web Technologies
- HTML semantics
- CSS layout systems
- JavaScript language fundamentals

---

# 2. Browser Rendering Pipeline

Understanding how browsers convert code into pixels.

## Rendering Steps

1. HTML parsing → DOM
2. CSS parsing → CSSOM
3. DOM + CSSOM → Render Tree
4. Layout
5. Paint
6. Compositing

## Important Concepts

- Critical Rendering Path
- Reflow and Repaint
- Layout Thrashing
- GPU compositing

---

# 3. JavaScript Runtime

Understanding how JavaScript executes in the browser.

## Core Topics

- Event loop
- Call stack
- Task queue
- Microtasks vs macrotasks

## Important Features

- Closures
- Prototypes
- Async programming
- Memory management

---

# 4. Modern Frontend Frameworks

Frameworks help manage UI complexity.

Example framework: [[React]]

## Key Concepts

- Component architecture
- State management
- Virtual DOM
- Reconciliation
- Rendering lifecycle

## Advanced Topics

- Concurrent rendering
- Server components
- Hydration
- Suspense

---

# 5. State Management

Managing application state as complexity grows.

## Types of State

- Local component state
- Shared application state
- Server state
- URL state

## Patterns

- Context
- Global stores
- Reducer pattern

---

# 6. Networking and Data Fetching

Frontend applications communicate with APIs.

## Topics

- REST APIs
- GraphQL
- Fetch API
- Request lifecycle
- Error handling
- Retry strategies

---

# 7. Performance Engineering

Optimizing frontend performance.

## Performance Metrics

- First Contentful Paint
- Largest Contentful Paint
- Time to Interactive

## Optimization Techniques

- Code splitting
- Lazy loading
- Caching
- Memoization

---

# 8. Frontend Architecture

Structuring large applications.

## Architectural Concepts

- Component-driven design
- Separation of concerns
- Modular architecture
- Dependency management

## Project Structure

Example:

frontend/
components/
hooks/
services/
utils/
features/

---

# 9. Accessibility

Ensuring applications are usable by everyone.

## Topics

- Semantic HTML
- ARIA roles
- Keyboard navigation
- Screen readers

---

# 10. Testing

Ensuring code correctness and stability.

## Types of Tests

- Unit tests
- Integration tests
- End-to-end tests

## Testing Concepts

- Test isolation
- Mocking
- Test coverage

---

# 11. Debugging

Finding and fixing issues in systems.

## Tools

- Browser DevTools
- Network inspection
- Performance profiler

## Debugging Strategy

1. Reproduce the issue
2. Narrow the scope
3. Inspect state and data flow
4. Identify root cause

---

# 12. Build Systems and Tooling

Modern frontend relies heavily on build tooling.

## Topics

- Bundlers
- Module systems
- Tree shaking
- Code transformation

## Common Tools

- [[Vite]]
- [[Webpack]]
- [[Babel]]

---

# 13. Deployment and Delivery

Shipping frontend applications to users.

## Topics

- Static hosting
- CDNs
- Environment variables
- CI/CD pipelines

---

# 14. Observability

Monitoring production applications.

## Signals

- Logs
- Metrics
- Error tracking

## Goals

- Detect failures
- Understand user behavior
- Improve reliability

---

# Key Principle

Junior engineers learn frameworks.

Mid-level engineers learn patterns.

Senior engineers understand how the web platform itself works.
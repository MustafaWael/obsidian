
Mental models are simplified ways of understanding how systems behave.  
They help engineers make better decisions about architecture, tools, and complexity.

---

# 1. Problem–Solution Model

Technology exists to solve specific problems.

**Principle**

Every tool, library, package, or technology is created to solve a specific problem.  
Using it for the wrong problem introduces new problems.

**Example**

Using React for a simple static page may introduce unnecessary complexity.

**Takeaway**

Always start with the problem before choosing the technology.

---

# 2. Abstraction Model

Software is built using layers of abstraction.

**Principle**

Abstractions hide complexity but never remove it.

**Example**

Frameworks like Next.js hide routing, server configuration, and build tooling.

However, when something breaks, the hidden complexity resurfaces.

**Takeaway**

The more abstraction you use, the less control you have.

---

# 3. Trade-off Model

Every engineering decision involves trade-offs.

**Principle**

There is no perfect solution — only trade-offs.

**Example**

| Choice | Benefit | Cost |
|------|------|------|
| Framework | Faster development | Less control |
| Low-level code | High control | More complexity |

**Takeaway**

Engineering is the art of choosing the right trade-off.

---

# 4. Complexity Growth Model

Software systems naturally grow in complexity.

**Principle**

Without active effort, systems become harder to maintain over time.

**Example**

Features accumulate  
Dependencies increase  
Architecture becomes harder to understand

**Takeaway**

Refactoring is necessary to control complexity.

---

# 5. Local vs Global Thinking

Changes in one part of a system can affect other parts.

**Principle**

A small local change may create large global effects.

**Example**

A simple state change in a React component may trigger many component re-renders.

**Takeaway**

Always consider the system as a whole.

---

# 6. Constraint Model

Good systems are designed around constraints.

**Principle**

Constraints simplify decision making.

**Examples**

Performance constraints  
Memory constraints  
Time constraints  
Team size constraints

**Takeaway**

Constraints guide architecture.

---

# 7. Information Flow Model

Software systems are fundamentally about moving data.

**Principle**

Understanding how data flows through a system is key to understanding the system.

**Example**

Client → API → Database → Response

**Takeaway**

When debugging systems, follow the data.

---

# 8. Feedback Loop Model

Systems improve through feedback loops.

**Principle**

Fast feedback improves development quality.

**Examples**

Testing  
Linting  
Type systems  
Monitoring

**Takeaway**

Shorter feedback loops produce better systems.

---

# 9. Scaling Model

Systems that work at small scale may fail at large scale.

**Principle**

Designs must evolve as scale increases.

**Examples**

Single server → distributed system  
Local state → global state management

**Takeaway**

Do not over-design for scale too early.

---

# 10. Failure Model

All systems eventually fail.

**Principle**

Engineering should assume failure.

**Examples**

Network failures  
Server crashes  
Invalid user input

**Takeaway**

Robust systems are designed with failure in mind.

---

# Key Reminder

Junior engineers learn tools.

Mid-level engineers learn patterns.

Senior engineers understand systems.
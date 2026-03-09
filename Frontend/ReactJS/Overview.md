# React.js — Complete Overview

## What is React?

**React.js** is a **JavaScript library for building user interfaces**, especially for **interactive web applications** where the UI must change dynamically based on user interaction or data updates.

React allows developers to build applications using **reusable components** and a **state-driven rendering model**, where the UI automatically updates whenever the underlying data changes.

React was created and is maintained by Meta (formerly Facebook).

React focuses only on the **View Layer** of an application.

---

# Why React Exists

Before React, building large frontend applications became difficult because developers had to **manually synchronize application state with the DOM**.

As applications grew larger, this led to several issues:

- Complex DOM manipulation
- UI becoming out of sync with application data
- Hard-to-maintain codebases
- Difficult debugging
- Performance problems

React was introduced to solve these issues by providing a **declarative and component-based architecture**.

---

# The Core Problem React Solves

The fundamental problem React addresses is:

> Keeping the **User Interface synchronized with application state** in a predictable and efficient way.

Traditional JavaScript applications required **imperative DOM manipulation**.

Example:

```javascript
const button = document.querySelector("#btn")

button.addEventListener("click", () => {
  const counter = document.querySelector("#counter")
  counter.innerText = Number(counter.innerText) + 1
})
```

Problems with this approach:

- DOM logic is scattered across the application
- Difficult to track UI updates
- Easy to introduce bugs
- Hard to maintain large codebases

React introduces a new model:

```
UI = f(state)
```

The **UI becomes a function of the application state**.

Instead of manually updating the DOM, developers update **state**, and React updates the UI automatically.

---

# Core Principles of React

## Declarative UI

React follows a **declarative programming model**.

Developers describe **what the UI should look like**, and React determines **how to update the DOM efficiently**.

### Imperative Approach

```javascript
const element = document.createElement("h1")
element.textContent = "Hello"
document.body.appendChild(element)
```

### Declarative React Approach

```jsx
<h1>Hello</h1>
```

React handles the DOM updates automatically.

---

# Component-Based Architecture

React applications are built using **components**.

A component is a **reusable, isolated piece of UI** that contains:

- UI structure
- logic
- state
- behavior

Example application structure:

```
App
 ├── Navbar
 ├── Sidebar
 ├── ProductList
 │     └── ProductCard
 └── Footer
```

Example component:

```jsx
function Welcome({ name }) {
  return <h1>Hello {name}</h1>
}
```

Components receive input through **props** and may manage internal **state**.

---

# JSX

React uses **JSX (JavaScript XML)**, a syntax extension that allows developers to write UI code that resembles HTML.

Example:

```jsx
const element = <h1>Hello World</h1>
```

JSX is compiled into JavaScript:

```javascript
React.createElement("h1", null, "Hello World")
```

JSX ultimately produces **React Element objects**.

---

# React Elements

React elements are **plain JavaScript objects** describing the UI.

Example structure:

```javascript
{
  type: "h1",
  props: {
	  children: "Hello World"
  }
}
```

Important characteristics:

- immutable
- lightweight
- describe UI structure
- not actual DOM nodes

---

# Virtual DOM

React introduces the **Virtual DOM**, an in-memory representation of the real DOM.

Example concept:

```
Real DOM
<div>
  <h1>Hello</h1>
</div>

Virtual DOM
{
  type: "div",
  children: [
    { type: "h1", children: "Hello" }
  ]
}
```

## Why Virtual DOM Exists

Direct DOM manipulation is **expensive**.

React improves performance by:

1. Creating a virtual representation of the UI
    
2. Comparing new and previous versions
    
3. Updating only the necessary DOM nodes
    

---

# Reconciliation

**Reconciliation** is the process React uses to determine what changes need to be applied to the DOM.

Process:

```
State Update
     ↓
Create New Virtual DOM Tree
     ↓
Compare with Previous Tree
     ↓
Calculate Differences
     ↓
Apply Minimal DOM Updates
```

React uses heuristics to optimize this process.

## Reconciliation Rules

1. Different element types produce different trees.
2. Elements with the same type are updated in place.
3. Keys help React track elements in lists.

Example:

```jsx
items.map(item => (
  <li key={item.id}>{item.name}</li>
))
```

---

# Props

Props are **inputs passed to components**.

Characteristics:

- read-only
    
- passed from parent to child
    
- enable component reuse
    

Example:

```jsx
function Greeting({ name }) {
  return <h1>Hello {name}</h1>
}
```

Usage:

```jsx
<Greeting name="Mustafa" />
```

---

# State

State represents **internal mutable data** within a component.

When state changes, React **re-renders the component**.

Example:

```jsx
function Counter() {
  const [count, setCount] = useState(0)

  return (
    <button onClick={() => setCount(count + 1)}>
      {count}
    </button>
  )
}
```

State update flow:

```
User Interaction
      ↓
State Update
      ↓
Component Re-render
      ↓
Virtual DOM Update
      ↓
DOM Patch
```

---

# React Rendering Pipeline

React rendering consists of two phases.

## 1. Render Phase

React determines **what the UI should look like**.

Tasks:

- execute component functions
    
- generate React elements
    
- build fiber tree
    
- prepare updates
    

This phase is **interruptible**.

---

## 2. Commit Phase

React applies the changes to the **real DOM**.

Tasks:

- update DOM nodes
    
- run layout effects
    
- attach refs
    

This phase **cannot be interrupted**.

---

# React Fiber Architecture

React internally uses an architecture called **Fiber**.

Fiber is a **data structure and scheduling system** that allows React to:

- split rendering into smaller units
    
- pause rendering work
    
- prioritize updates
    
- support concurrent rendering
    

Each component corresponds to a **Fiber node**.

Example fiber tree:

```
App
 ├── Header
 ├── Sidebar
 └── Content
       └── Post
```

Each fiber node stores:

- component type
    
- props
    
- state
    
- parent node
    
- child node
    
- sibling node
    
- update information
    

---

# Scheduler

React includes a **scheduler** that determines when rendering work should execute.

Not all updates have the same priority.

High priority updates:

- typing
    
- clicking
    
- animations
    

Lower priority updates:

- background data loading
    
- non-urgent UI updates
    

The scheduler helps maintain **responsive user interfaces**.

---

# Concurrent Rendering

Modern React supports **Concurrent Rendering**.

This allows React to:

- pause rendering
    
- resume rendering
    
- cancel rendering
    
- prioritize urgent updates
    

Benefits:

- smoother interactions
    
- better performance
    
- improved responsiveness
    

Concurrent features include:

- `startTransition`
    
- `useTransition`
    
- Suspense improvements
    

---

# Advantages of React

- Component reusability
    
- Declarative UI model
    
- Efficient DOM updates
    
- Predictable state management
    
- Large ecosystem
    
- Strong community support
    

---

# Limitations of React

- Only solves the UI layer
    
- Requires additional libraries
    
- Complex for very large applications
    
- Advanced concepts require deeper understanding
    

---

# React Ecosystem

React itself focuses only on the UI layer.

Additional functionality is provided by external libraries.

Common tools:

## Routing

- React Router
    

## State Management

- Redux
    
- Zustand
    
- Recoil
    

## Data Fetching

- TanStack Query
    
- SWR
    

## Frameworks Built on React

- Next.js
    
- Gatsby
    
- Remix
    

---

# Summary

React is a **declarative, component-based JavaScript library** used to build dynamic user interfaces.

It solves several key frontend challenges:

- complex DOM manipulation
    
- UI and state synchronization
    
- inefficient rendering
    
- lack of reusable UI structure
    

React achieves this using:

- components
    
- JSX
    
- Virtual DOM
    
- reconciliation
    
- Fiber architecture
    
- concurrent rendering
    

This approach allows developers to build **scalable, maintainable, and performant web applications**.
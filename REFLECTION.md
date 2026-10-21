# InventoryHub - Project Reflection & Summary

## Overview

InventoryHub is a full-stack inventory management application featuring a Blazor WebAssembly front-end communicating with a .NET Minimal API back-end. Throughout this project, Microsoft Copilot served as an AI collaborator to streamline development, debug integration roadblocks, format JSON payloads, and optimize overall performance.

---

## Copilot Assistance Across Development Stages

### 1. Integration & Communication (Activity 1)

- **Assistance:** Copilot helped scaffold the initial HTTP client integration logic within the Blazor component (`FetchProducts.razor`) and mapped out the base `Product` data model structure to communicate with the Minimal API.

### 2. Debugging Integration & CORS Issues (Activity 2)

- **Assistance:** When routing mismatches (`/api/products` vs `/api/productlist`), CORS security blocks, and JSON parsing issues occurred, Copilot diagnosed the exact gaps and provided robust `try-catch` deserialization blocks alongside the required CORS policy configuration (`app.UseCors(...)`).

### 3. Structuring Nested JSON Responses (Activity 3)

- **Assistance:** Copilot assisted in upgrading the back-end response payload to include a nested `Category` object per product, ensuring industry-standard hierarchical data modeling that could be accurately parsed by the front-end C# classes.

### 4. Performance Optimization & Caching (Activity 4)

- **Assistance:** To reduce redundant server requests and database pressure, Copilot recommended and implemented `IMemoryCache` caching strategies in the back-end Minimal API, significantly reducing server response times and improving client rendering efficiency.

---

## Challenges Faced & Key Learnings

- **Challenge:** Handling asynchronous data states and mapping unexpected JSON schemas to strict C# models.
- **How Copilot Helped:** Copilot suggested clean null-coalescing models and exception-handling patterns that prevented UI crashes during failed network calls or malformed payloads.
- **Key Takeaway:** Using Copilot effectively requires clear, iterative prompting and architectural guidance, allowing developers to focus on high-level logic and edge-case testing.

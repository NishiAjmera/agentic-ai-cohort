# agentic-ai-cohort

A practical, production-ready guide to building, scaling, and governing AI agents for the enterprise.

The goal of this cohort is to learn everything from first principles, why something exists and the problem it solves. This is a hands-on program. Every week, you will build a usable application.

---

# Plan for the Cohort

## Week 1: Building a Customer Support Bot

We begin with the fundamentals. You will build a **Customer Support Bot** that uses a provided knowledge base to resolve user queries. This session lays the foundation for everything that follows.

### What You Will Gain

* **Agentic Foundations:** Move beyond simple prompts and understand what an **Agent** is — function calling, tools, memory, and the agent loop.
* **Tool Integration:** Learn how to give your agent capabilities, such as searching documents, so it can provide grounded, factual answers.
* **Memory & Context:** Understand how to manage **Sessions** and **State** so your bot remembers what was said earlier in the conversation.
* **Google ADK Deep Dive:** Get hands-on experience with the Google Agent Development Kit (ADK) to build, test, and deploy your first agentic system.
* A brief introduction to RAG. We will not go deep into it this week.

---

### The Demo: Knowledge-Based Support

**The Challenge:** Traditional chatbots hallucinate and lose conversational context, making them unreliable for real customer support.

**The Solution:**
You will build a bot that:

1. **Consults a Knowledge Base:** Instead of guessing, it searches structured documents to retrieve accurate answers.
2. **Manages Conversational State:** It tracks ticket progress and remembers user details throughout the interaction.
3. **Acts with Intent:** It determines when it can resolve an issue independently and when it needs additional information.

---

### Key Takeaway

By the end of this session, you will know how to build a simple agent, understand the core components involved, and gain a high-level understanding of Retrieval-Augmented Generation and how it works.

---

## Week 2: Building the Retail Strategy Agent

This week, we move beyond conversational bots and build a **Retail Strategy Agent**. This project focuses on the **Model Context Protocol (MCP)** and shows how to integrate it into an agent that solves real business problems.

### What You Will Learn

* **The “Why” of MCP:** The problem MCP is designed to solve.
* **The “How” of MCP:** A deep dive into its architecture — client, server, tools, resources, and prompts, and how to build your own MCP servers.
* **Skill Composition:** Writing structured instructions that go beyond basic prompting.
* **Plugins:** What they are and how they accelerate integrations.

---

### The Demo: Retail Strategy Agent

The use case for this session is **automated site selection**.

**The Challenge:** Decisions like opening a new store require extensive manual data analysis and coordination across systems.

**The Solution:**
Your **Retail Strategy Agent** will:

1. **Analyze Internal Growth (BigQuery):** Use NL2SQL to identify geographic hotspots where online sales are growing but no physical store exists.
2. **Evaluate the Physical World (Google Maps):** Assess competitor presence, local landmarks, and accessibility.
3. **Deliver a Recommendation:** Provide a data-backed proposal with supporting analysis and map visualization.

---

### Key Takeaway

By the end of this session, you will be able to build reliable, intelligent systems that integrate with third-party services and enterprise data.

---

## Week 3: Building the Concierge Agent

This week, we shift from a single-agent system to a **Multi-Agent System** using the **Agent-to-Agent (A2A) Protocol**. You will build a **Concierge Agent** that coordinates complex, multi-provider logistics, such as organizing a team lunch.

### What You Will Gain

* **A2A Protocol & Orchestration:** Learn how an Orchestrator Agent discovers, delegates to, and manages Specialist Agents to complete a multi-step goal.
* **Multi-Agent Collaboration:** Understand how agents share context, delegate tasks, and resolve conflicts.
* **Context & State Engineering:** Manage global state so the Orchestrator tracks multiple sub-tasks without losing the user’s original intent.
* **System Integration:** Bring together MCP, Memory, and Skills into one unified architecture.

---

### The Demo: Multi-Provider Food Concierge

**The Challenge:** Coordinating food orders across multiple vendors is fragmented and time-consuming.

**The Solution:**
You will build a **Concierge Agent** that acts as a single point of contact:

1. **The Orchestrator:** Accepts a complex request (e.g., multiple vendors, timed delivery).
2. **Specialist A (Menu Agent):** Uses MCP to fetch live menus and pricing.
3. **Specialist B (Logistics Agent):** Coordinates delivery timing via external APIs.
4. **The Outcome:** A seamless experience for the user while multiple coordinated actions happen in the background.

---

### Key Takeaway

Complexity should be invisible to the user. By the end of this week, you will move beyond building isolated tools and start designing coordinated systems of agents that collaborate to achieve real-world outcomes.

---

## Week 4: The Economy of Agents

This week focuses on enabling agents to operate within real financial systems using industry standards: **Agentic Commerce Protocol (ACP)**, **Universal Commerce Protocol (UCP)**, and **Agent Payments Protocol (AP2)**.

We enhance the Concierge Agent so it doesn’t just coordinate orders, it completes transactions securely.

### What You Will Gain

* **Commerce Protocols:** Understand ACP and UCP, and how they standardize catalog browsing and checkout flows.
* **Secure Agent Payments (AP2):** Learn how mandates allow agents to execute payments without accessing raw credit card details.
* **End-to-End Transaction Flow:** Connect conversational intent to financial execution using shared payment tokens.
* **Digital Wallet Evolution:** Explore how wallets evolve into permission-managed agent wallets.

---

### The Demo: Full-Cycle Food Concierge

**The Upgrade:** Your agent now completes the transaction.

1. **Checkout Negotiation:** The Orchestrator uses UCP or ACP to confirm pricing and terms.
2. **Payment Authorization:** You issue a one-time mandate via AP2, setting clear spending limits.
3. **Settlement:** The agent generates a shared payment token, completes the transaction, and stores the receipt without manual checkout steps.

---

### Key Takeaway

Money represents the ultimate action. By the end of this week, you will understand how agents move from analysis to execution, finding, negotiating, and paying within defined guardrails.

---

## Week 5: Hardening for Production

The final week focuses on transforming your prototype into a production-grade system that is secure, reliable, and scalable.

Building an agent is straightforward. Building one that doesn’t leak data, hallucinate policies, or fail under load requires disciplined engineering.

---

### 1. Security & Guardrails

Before serving real users, your agent needs safeguards.

* **Input Guardrails:** Detect jailbreak attempts, prompt injections, and off-topic requests.
* **Output Guardrails:** Scan responses for PII leaks, unsafe content, or fabricated information.
* **Least Privilege Access:** Ensure the agent only has the permissions it strictly needs.

---

### 2. Evaluations

Reliability requires systematic evaluation.

* **LLM-as-a-Judge:** Use a higher-reasoning model to evaluate responses for faithfulness and relevance.
* **Regression Testing:** Maintain a gold dataset of queries to catch unintended regressions.
* **Groundedness Checks:** Verify that responses are derived from authoritative sources rather than fabricated.

---

### 3. Observability & Scalability

Once deployed, you need visibility into how decisions are made.

| Component          | Purpose in Production                                 |
| ------------------ | ----------------------------------------------------- |
| **Tracing**        | Track which tools were called and in what sequence.   |
| **Token Tracking** | Monitor cost and latency.                             |
| **Error Analysis** | Identify failure points and prevent cascading issues. |

### Scaling the System

As traffic increases, monolithic agents become bottlenecks. You will move toward multi-agent orchestration, where specialized agents coordinate through shared state and structured task queues. This approach allows the system to scale horizontally, recover from failures gracefully, and maintain performance under heavy load.

---

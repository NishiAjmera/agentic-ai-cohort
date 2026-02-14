# agentic-ai-cohort
A practical production ready guide to building, scaling, and governing AI agents for the enterprise.

Goal for this cohort is to learn everything from first principle, why something exists, what problem it is solving. It will be very hands on. We will build a usable app every week.

# Plan for the cohort
## Week 1: Building a Customer Support Bot

In this session, we start with the fundamentals. You will build a **Customer Support Bot** that uses a provided knowledge base to resolve user queries. This is where we lay the groundwork for everything that follows.

### What You Will Gain

* **Agentic Foundations:** Move from simple "prompts" to understanding **Agents** (understand function calling, tools, memory, agent loop).
* **Tool Integration:** Learn how to give an agent "skills" (like searching a document) so it can provide factual, grounded answers.
* **Memory & Context:** Master how to handle **Sessions** and **State** so your bot remembers what was said three messages ago.
* **Google ADK Deep-Dive:** Get hands-on with the Google Agent Development Kit (ADK) to build, test, and deploy your first agentic system.
* I will also briefly talk about RAG. we wont dive into RAG in this session.

---

### The Demo: Knowledge-Based Support

**The Challenge:** Standard chatbots often "hallucinate" or forget the context of a conversation, making them useless for real customer support.

**The Solution:**
We will build a bot that:

1. **Consults a Knowledge Base:** Instead of guessing, the agent searches specific documents to find the right answer.
2. **Manages Conversational State:** It tracks the user's "ticket" progress and remembers personal details provided during the chat.
3. **Acts with Intent:** It identifies when it can solve the problem itself and when it needs to ask for more info.

---

### Key Takeaway

By the end of this session, you’ll know how to build a simple agent, have a good understanding of the fundamentals involved in building an agent. Have a high leve understanding of Retrieval Augmented Generation and how it works.

---

## Week 2: Building the "Retail Strategy Agent"

In this session, we move beyond basic chat and build a **Retail Strategy Agent**. This project serves as a masterclass in the **Model Context Protocol (MCP)** and integrate it to an agent that solves complex, real-world business problems.

### What You Will Learn

* **The "Why" of MCP:** what problem is MCP solving ?
* **The "How" of MCP:** A deep dive into the architecture (client, server, tools, resources, prompts) and how you can build your own MCPs.
* **Skill Composition:** Learn to write advanced instructions that go beyond simple prompts.
* **The Plugin Evolution:** What are plugins and how do they speed up integrations?"

---

### The Demo: "Retail Strategy Agent."

Our core use case for this session is an agent that performs **automated site selection**.

**The Challenge:** Strategic decisions, like opening a new storefront, usually require weeks of manual data analysis and cross-referencing.

**The Solution:**
Our **Retail Strategy Agent** will:

1. **Analyze Internal Growth (BigQuery):** Use NL2SQL to identify geographic "hotspots" where online sales are surging but physical stores are missing.
2. **Evaluate the Physical World (Google Maps):** Automatically search those hotspots for competitors, local foot traffic landmarks, and accessibility.
3. **Deliver the Recommendation:** Provide a data-backed proposal for a new location, complete with a map visualization and a "Competitive Gap" analysis.

> **Key Takeaway:** By the end of the session you will be able to build reliable intelligent systems with third-party integrations.


Week 3
## Week 3: Building the Concierge Agent

In this session, we bring everything together. We are moving from a single agent to a **Multi-Agent System** using the **Agent-to-Agent (A2A) Protocol**. You will build a **Concierge Agent** that solves a common pain point: coordinating complex, multi-provider logistics like a team lunch order.

### What You Will Gain

* **A2A Protocol & Orchestration:** Master the "Agent-to-Agent" standard. Learn how an **Orchestrator Agent** discovers, delegates, and manages "Specialist Agents" to complete a single, multi-step goal.
* **Multi-Agent Collaboration:** Understand how agents negotiate with each other - sharing context, passing tasks, and resolving conflicts (e.g., when one restaurant is closed but another is open).
* **Context & State Engineering:** Learn to manage "Global State" so the Orchestrator knows the status of five different sub-tasks simultaneously without losing the user's original intent. Learn all about Context Engineering and its implementation.
* **System Synthesis:** Integrate everything from the previous weeks—**MCPs**, **Memory**, and **Skills** into one unified ecosystem.

---

### The Demo: The Multi-Provider Food Concierge

**The Challenge:** Ordering food for a team workshop is a mess. One person wants sushi, another wants pizza. You currently have to place multiple separate orders, track them differently, and handle multiple deliveries.

**The Solution:**
We will build a **Concierge Agent** that acts as your team’s single point of contact:

1. **The Orchestrator:** Takes the complex team request ("Get us 3 pizzas from Joe's and 5 sushi rolls from Hanabi for 1 PM").
2. **Specialist A (The Menu Agent):** Uses an MCP to fetch live menus and prices from different providers.
3. **Specialist B (The Logistics Agent):** Coordinates with delivery APIs (via MCP) to ensure all orders arrive at the same time.
4. **The Outcome:** One conversation for the user; multiple coordinated actions in the background. The agent tracks every order and sends a single notification when the "Workshop Lunch" is ready at the front desk.

---

### Key Takeaway

**Complexity should be invisible to the user.** By the end of this week, you’ll know how to stop building "tools" and start building crew of agents, You will leave with the blueprint for an autonomous system that can talk to other agents, navigate real-world frictions.

---
## Week 4: The Economy of Agents

In this session, you will learn how to plug your agents into the actual financial grid using the latest industry standards: **Agentic Commerce Protocol (ACP)**, **Universal Commerce Protocol (UCP)**, and **Agent Payments Protocol (AP2)**.

We’re upgrading our Concierge Agent so it doesn't just "talk" about food, it actually buys it, handles the checkout, and settles the bill securely.

### What You Will Gain

* **Commerce Standards Mastery:** A breakdown of **ACP** (OpenAI/Stripe) and **UCP** (Google). Understand how these protocols allow agents to browse catalogs and initiate checkouts across any merchant.
* **Secure Agent Payments (AP2):** Learn how the **Agent Payments Protocol** uses "Mandates" to let an agent pay for things on your behalf without ever seeing your actual credit card number.
* **Full-Stack Agentic Flow:** Learn how to bridge the gap between a conversation and a completed financial transaction using standardized "Shared Payment Tokens."
* **The Future of Wallets:** See how digital wallets are evolving into "Agent Wallets" that manage budgets and permissions instead of just storing cards.

---

### The Demo: The "Full-Cycle" Food Concierge

**The Upgrade:** Last week, your agent could coordinate a team order. This week, we give it a "company card" and the authority to finish the job.

1. **The Checkout Handshake:** When the team agrees on the order, the Orchestrator uses **UCP** or **ACP** to negotiate the final price (including tax and delivery) with the restaurants' systems.
2. **The Payment Mandate:** You (the human) give a one-time "Mandate" via **AP2**, authorizing the agent to spend up to $150 for this specific lunch.
3. **The Invisible Settlement:** The agent generates a "Shared Payment Token" and passes it to the restaurants. The money moves, the receipt is filed, and the food is on the way—all without you filling out a single checkout form.

---

### Key Takeaway

**Money is the ultimate "Action."** By the end of this week, you’ll see that agents aren't just for research or summaries; they are the new "Buy Button." You’ll know how to build systems that can navigate the entire economy—finding, negotiating, and paying for things—while keeping you in total control of the wallet.

---

**Week 5**

The final leg of our journey. This week is all about the "hardening" phase—transforming your concierge agent from a cool prototype into a **production-grade system** that is secure, reliable, and capable of handling real-world traffic at scale.

In 2026, building an agent is the easy part; ensuring it doesn't hallucinate a refund policy or leak customer data is where the real engineering begins.

---

## 1. Security & Guardrails:

Before an agent interacts with a single real customer, it needs "bumpers." Guardrails are real-time moderation layers that sit between the user and your agent, and between your agent and the world.

* **Input Guardrails:** These scan user prompts for **jailbreak attempts** (e.g., "Ignore all previous instructions") and **Prompt Injections**. We also use semantic filters to ensure the user stays "on-topic" with the concierge service.
* **Output Guardrails:** These inspect the agent's response before the user sees it. We look for **PII (Personally Identifiable Information)** leaks, toxic language, or "hallucinated" URLs that don't exist.
* **The "Confused Deputy" Problem:** We apply **Least-Privilege Access**. If your concierge agent only needs to book tables, it shouldn't have the API permissions to delete the entire reservation database.

---

## 2. Evaluations: 

To make your agent **reliable**, you can't just hope it works. You need a rigorous evaluation framework.

* **LLM-as-a-Judge:** We use a "teacher" model (like a high-reasoning Gemini or GPT-4o) to grade your concierge agent’s responses based on a rubric of **Faithfulness** (is it grounded in the data?) and **Relevance**.
* **Regression Testing:** Every time you update your prompt or model, you run a "Gold Dataset" of 50+ known queries to ensure that fixing one bug didn't create three new ones.
* **Groundedness:** For a concierge agent, we specifically measure if it is fetching the correct information from your knowledge base (RAG) or just making up "available" time slots.

---

## 3. Observability & Scalability: Seeing into the "Black Box"

Once your agent is live, you need to know *why* it made a specific decision. This is where **Observability** comes in.

| Component | Purpose in Production |
| --- | --- |
| **Tracing** | Following the "Chain of Thought" to see exactly which tool the agent called and why. |
| **Token Tracking** | Monitoring costs and latency to ensure the system remains economically viable. |
| **Error Cascading** | Identifying if a failure in the "Search Tool" caused the entire agent to crash. |

### Scaling Your System

As your traffic grows, a single "monolithic" agent often fails. We move toward **Multi-Agent Orchestration**:

Instead of one overworked bot, use a team of specialists who coordinate through a shared digital "to-do list." This list acts as a buffer, preventing crashes by organizing tasks even when thousands of people ask for help at once. Because these agents save their progress in a shared notebook, they can work in the background and pick up exactly where they left off without losing your data. This setup ensures your service stays fast and reliable for everyone, no matter how much traffic it gets.

---



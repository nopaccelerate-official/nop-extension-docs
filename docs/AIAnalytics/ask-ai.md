# Ask AI

The Ask AI page provides a conversational chat interface where you can ask plain-English questions about your store's data and receive instant AI-generated answers.

Access it from **NopBot AI Analytics → Ask AI** in the admin sidebar, or via the **Ask AI** button on the Dashboard.

![Ask AI](../assets/img/AIAnalytics_ask-ai.png){ .img-border }

---

## Filter Bar

The same date range and store filters from the Dashboard are available here. The AI uses these filters when querying your store data — for example, asking "What was my total revenue?" will return revenue for the selected period only.

| **Control**   | **Description**                                                  |
|---------------|------------------------------------------------------------------|
| **Date From** | Start of the data period the AI will use to answer questions.   |
| **Date To**   | End of the data period.                                          |
| **Store**     | Filter to a specific store or use All Stores.                   |
| **Clear Chat**| Deletes the full conversation history from the database permanently. A confirmation prompt appears before deletion. |

---

## Suggested Prompts

A row of prompt chips appears below the filter bar to help you get started:

- What was my total revenue this month?
- Which 5 products generated the most revenue?
- How many new customers placed orders?
- What is the average order value?
- Show daily revenue as a table

Click any chip to populate the input field, then press **Enter** or the send button to submit.

---

## Chat Interface

Type your question in the input field at the bottom of the page. Press **Enter** to send, or **Shift+Enter** to add a new line within your question.

The AI receives your store's aggregated metrics as context (total revenue, order count, top products, daily revenue breakdown) and generates a relevant answer. If the answer contains tabular data, it is rendered as a formatted table within the chat bubble.

---

## Chat History Persistence

Your conversation is automatically saved to the database after each exchange. When you return to the Ask AI page — even after a page refresh or closing the browser — your previous messages are restored and displayed in the chat panel.

To permanently delete your conversation history, click **Clear Chat**. This removes all records from the database for your admin account.

---

## Example Questions

| **Question**                                    | **What the AI returns**                                  |
|-------------------------------------------------|----------------------------------------------------------|
| What was my total revenue this month?           | The total revenue figure for the selected date range.    |
| Which 5 products generated the most revenue?    | A table with product names and revenue values.           |
| How many new customers placed orders?           | The unique customer count for the period.                |
| What is the average order value?                | The AOV calculated from your filtered orders.            |
| Show daily revenue as a table                   | A table with one row per day showing the revenue amount. |

> **Note:** The AI can only answer questions based on the store data provided in its context (orders, revenue, customers, products). It cannot access product descriptions, inventory levels, or customer personal details.

[← Previous](dashboard.md) | [Next →](scenarios-of-use.md)

## Project Overview
This project implements a chatbot-based online food ordering system that allows customers to:

Place new food orders by selecting items and quantities in natural language.

Track existing orders in real time using a unique order ID.

Interact through intelligent conversations, where the bot handles missing details, unavailable menu items, and maintains context across messages.

The system provides a complete digital ordering workflow, from order placement to tracking, directly on the eatery’s website—without relying on third-party delivery apps.

## Why This Project Was Built

The eatery required a direct online ordering solution after being rejected by large e-commerce platforms. Key drivers included:

Faster time-to-market – Deliver a working solution quickly to start accepting online orders.

Revenue growth – Provide a new sales channel independent of aggregators.

Customer convenience – Simplify ordering and tracking with a conversational interface.

## Use Cases

Placing New Orders – Users initiate an order, add food items with quantities, review, and confirm. The system then calculates the total bill.

Tracking Orders – Users enter an order ID and get real-time updates like “in progress,” “in transit,” or “delivered.”

Conversational Ordering – The bot asks clarifying questions (e.g., missing quantities), responds to unavailable items, and remembers past inputs to ensure smooth interactions.

## Technologies Used

Dialogflow ES – Natural Language Processing to detect intents (order, track) and extract entities (food item, quantity). Context ensures conversational flow.

Python (FastAPI) – Backend server that processes webhook requests, manages in-progress orders, and communicates with the database.

MySQL Database – Stores menu items, confirmed orders, and order-tracking statuses.

Ngrok – Provides a secure HTTPS tunnel for local development, enabling Dialogflow to connect with the backend server.

## How This Project Is Useful

For Businesses – A ready-to-use ordering solution that eliminates dependency on third-party apps.

For Customers – A simple, intuitive way to order food and track deliveries.

For Developers – A complete example of integrating NLP, backend APIs, and databases into a conversational AI system.

For Research & Learning – Demonstrates real-world chatbot workflows, fulfillment, and database integration.

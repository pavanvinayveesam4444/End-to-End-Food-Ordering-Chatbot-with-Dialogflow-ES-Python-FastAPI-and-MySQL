**Project Description
This project involves building a chatbot that enables users to order food and track existing orders from an eatery. The chatbot is designed to provide a complete online ordering system directly on a website.
**Key functionalities include:
• Placing a new order: Users can initiate an order, add various food items with specified quantities (e.g., "give me two pav bhaji, one pizza"), review their selections, and finalise the order, which then calculates the total bill.
• Tracking an order: Users can check the status of an existing order by providing an order ID (e.g., "track my order 41"), receiving updates like "in progress," "in transit," or "delivered".
• Intelligent conversation: The chatbot can ask for missing information (such as quantity), respond when items are not on the menu (e.g., "Pani Puri"), and remember previous parts of the conversation using context.
**Why this project is built
This project was built to create a direct online ordering system for an eatery. The eatery needed a way to accept online orders to increase its income after its applications to large e-commerce platforms were rejected. A critical requirement for the project was achieving a fast "time to market", meaning the chatbot needed to be developed and released quickly.
**Use Cases
**The main use cases for this chatbot are:
• Placing a New Order: A user can initiate a conversation to start a new food order, select desired items and quantities, and complete the transaction.
• Tracking an Order: A user can inquire about the current status of an order they have already placed using an order ID.
**Technologies Used
**The project utilises several technical components to function:
• Dialogflow ES (Essentials): This is the Natural Language Processing (NLP) platform that understands user input. It identifies the user's main goal (intents) and extracts specific information like food item or quantity (entities). Training phrases teach the model to recognise intents and entities. Dialogflow ES was chosen because it is cloud-based, offers many ready-to-use features for quick deployment, and is more cost-effective than Dialogflow CX, allowing for a faster product launch. Context is used to maintain the flow of conversation.
• Python with FastAPI: This acts as the backend server. Dialogflow communicates with this backend via webhooks for "fulfillment" (dynamic responses). The FastAPI server handles dynamic actions, such as adding items to an order, saving orders to the database, or retrieving order statuses. A global Python dictionary (in_progress_orders), keyed by a unique session ID, temporarily stores a user's order during the conversation.
• MySQL Database: This relational database stores all essential information. It includes tables for food item (menu details and prices), orders (placed order items and quantities), and order_tracking (order status updates).
• ngrok: Used during local development, ngrok provides a secure HTTPS tunnel. This allows Dialogflow (which requires HTTPS for webhooks) to securely communicate with the locally running FastAPI server.

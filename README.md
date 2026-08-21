#  MCP Airbnb Search Assistant

An AI-powered Airbnb search assistant built using **MCP (Model Context Protocol)**.
The project allows users to ask natural-language questions about Airbnb listings and get relevant results by searching the web.

##  Project Overview

The **MCP Airbnb Search Assistant** acts as an AI travel assistant.

Instead of manually searching different websites, the user can simply ask questions such as:

* "Find apartments in Bangalore under ₹3,000 per night."
* "Show me Airbnb stays in Chennai for 2 people."
* "Find highly rated places near the beach."
* "What are the cheapest available options?"
* "Compare these Airbnb listings."

The AI understands the user's request, searches for relevant information, and presents the results in an easy-to-understand format.


##  Features

###  Natural Language Search

Users can search using normal human language instead of complicated filters.

###  Web Search

After receiving a question, the system searches relevant websites to find current information.

###  AI-Powered Understanding

The AI understands important details such as:

* Location
* Price
* Number of guests
* Dates
* Property type
* Rating
* Amenities
* User preferences

###  Airbnb Listing Search

The assistant can find relevant Airbnb properties based on the user's requirements.

###  Result Comparison

Multiple properties can be compared based on:

* Price
* Rating
* Location
* Reviews
* Amenities

###  Conversational Interaction

Users can ask follow-up questions without repeating the complete search.

Example:

> User: Find apartments in Bangalore under ₹3,000.

> AI: Here are some options.

> User: Which one has the highest rating?

The assistant can use the previous conversation to answer the follow-up.

---

##  What is MCP?

**MCP stands for Model Context Protocol.**

It is a protocol that allows AI models to communicate with external tools and data sources in a standardized way.

In this project:

```text
User
  ↓
AI Assistant
  ↓
MCP
  ↓
Search Tool
  ↓
Web / Airbnb Information
  ↓
Search Results
  ↓
AI Assistant
  ↓
User
```

MCP acts as a bridge between the AI model and external tools.

---

##  Project Architecture

```text
                  ┌──────────────────┐
                  │      User        │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │   AI Assistant   │
                  │     Gemini       │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │       MCP        │
                  │     Client       │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │    MCP Server    │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │   Web Search     │
                  │      Tool        │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │ Search Results   │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │ Formatted Answer │
                  └──────────────────┘
```

---

##  Technologies Used

| Technology   | Purpose                               |
| ------------ | ------------------------------------- |
| Python       | Main programming language             |
| MCP          | Connecting AI with external tools     |
| Gemini API   | AI model                              |
| Web Search   | Finding current information           |
| Google Colab | Development and execution environment |
| JSON         | Data exchange between components      |

---

##  Project Structure

```text
MCP-Airbnb/
│
├── airbnb_mcp.py
├── client.py
├── requirements.txt
├── README.md
└── .env
```

### `airbnb_mcp.py`

Contains the MCP server and tools used for searching Airbnb-related information.

### `client.py`

Connects the AI model with the MCP server and handles user queries.

### `requirements.txt`

Contains the Python libraries required to run the project.

### `.env`

Stores API keys securely.

Example:

```env
GEMINI_API_KEY=your_api_key_here
```

**Never upload your API key to GitHub.**

---

##  Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/MCP-Airbnb.git
cd MCP-Airbnb
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Add your API key

Create a `.env` file:

```env
GEMINI_API_KEY=your_api_key_here
```

### 4. Run the MCP server

```bash
python airbnb_mcp.py
```

### 5. Start the client

```bash
python client.py
```

---

##  Example Queries

The user can ask:

```text
Find Airbnb stays in Bangalore for 2 people.
```

```text
Find places in Chennai below ₹2500 per night.
```

```text
Show highly rated Airbnb properties in Goa.
```

```text
Find properties near the beach with Wi-Fi.
```

```text
Compare the cheapest three options.
```

---

##  How It Works

### Step 1 — User asks a question

The user enters a natural-language request.

### Step 2 — AI understands the request

The AI extracts information such as:

```text
Location → Bangalore
Guests → 2
Budget → ₹3000
Property → Apartment
```

### Step 3 — MCP selects the required tool

The MCP client communicates with the MCP server and determines which tool should be used.

### Step 4 — Search is performed

The search tool retrieves current information from the web.

### Step 5 — Results are returned

The MCP server sends the search results back to the AI.

### Step 6 — AI generates the response

The AI organizes the information and gives the user a simple answer.

---

##  Example Output

```text
 Airbnb Search Results

1. Modern Apartment
 Bangalore
 4.8/5
 ₹2,500/night
 2 guests
 Wi-Fi available

2. Cozy Studio
 Bangalore
 4.6/5
 ₹2,200/night
 2 guests
 Wi-Fi available

3. Luxury Room
 Bangalore
 4.7/5
 ₹2,800/night
 2 guests
 Wi-Fi available
```

---

##  Advantages

* Easy natural-language interaction
* Searches current web information
* Reduces manual searching
* Supports conversational queries
* Can be extended with additional tools
* Demonstrates practical use of MCP
* Beginner-friendly AI agent architecture

---

##  Future Improvements

The project can be extended with:

*  Date-based availability search
*  Price comparison
*  Map integration
*  Advanced rating filtering
*  Automatic best-deal detection
*  Complete trip planning
*  Flight search
*  Train and bus search
*  Hotel search
*  Weather information
*  Distance calculation
*  WhatsApp/Telegram integration
*  Multi-agent travel planning

---

##  Learning Outcomes

Through this project, you can learn:

1. What MCP is and how it works
2. How AI models interact with external tools
3. How to create an MCP server
4. How to create an MCP client
5. How tool calling works
6. How web search can be integrated with AI
7. How to build an AI-powered travel assistant
8. How to structure an AI agent project

---

##  License

This project is created for **educational and demonstration purposes**.

---

##  Author

**Varsha Vernekar**

BE – Computer Science and Engineering

GSSS Institute of Engineering and Technology for Women

---

##  Conclusion

The **MCP Airbnb Search Assistant** demonstrates how AI can interact with external tools through the Model Context Protocol.

The main idea is simple:

> **Ask the AI → AI uses MCP → MCP searches the web → Results return → AI explains them.**

This project provides a foundation for building more advanced **AI agents and multi-tool assistants** in the future.

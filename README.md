# Product Support Assistant

A Python-based assistant (built in Jupyter Notebook) that answers product FAQs, classifies support messages, and routes users to the right help. Designed to reduce ticket volume and improve customer experience.

## Features

- Classifies incoming queries into **Product Inquiry** or **Support Request**
- Retrieves product details by name or category from a product catalog of a retailer
- Handles product inquires about multiple product categories: Laptops, Phones, TVs, Desktops
- Escalates uncertain cases to a human agent with relevant context
- Uses OpenAI's GPT API for classification and response generation

## Requirements

- Python 3.9+
- Jupyter Notebook
- OpenAI API key

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   cd YOUR_REPO_NAME
   ```

2. Install dependencies:
   ```bash
   pip install openai python-dotenv notebook
   ```

3. Create a `.env` file in the project root:
   ```env
   OPENAI_API_KEY=your_api_key_here
   ```
   > ⚠️ **Important:** Never commit your `.env` file to GitHub.

## Usage

1. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Launch the notebook file (`product-support-assistant.ipynb`).

Example queries:
```
You: Tell me about the MacBook Air
Assistant: The MacBook Air has a 13.6-inch Retina display, 8GB RAM...
```

```
You: I forgot my password
Assistant: I can help with that. Please visit the account recovery page...
```

## Example Queries

**Product Inquiry:**
- "What are the specs of the Dell XPS 13?"
- "Show me the TVs you have."
- "Tell me about the iPhone 15."

**Support Request:**
- "I need to update my billing information."
- "How do I reset my password?"
- "My TV isn't connecting to Wi-Fi."

## Project Structure

```
project/
│
├── product-support-assistant.ipynb  # Main application notebook
├── .env                             # Your API key (not committed)
├── README.md                        # Project documentation
```

## Notes

- This project uses OpenAI's `gpt-3.5-turbo` model by default.
- If you want to use `gpt-4`, update the `model` parameter in `get_completion_from_messages`.
- You can add more products to the `products` dictionary to expand the knowledge base.

## License

MIT License. See LICENSE file for details.

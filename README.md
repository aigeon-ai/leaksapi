```markdown
# Aigeon AI LeaksAPI

Aigeon AI LeaksAPI is a Python-based server application designed to interact with the LeaksAPI service. This application provides a set of tools to query data breaches and leaks, allowing users to search for compromised information related to emails, domains, and phone numbers. The server leverages the FastMCP framework to expose its functionalities as tools that can be easily accessed and utilized.

## Features Overview

- **Integration with LeaksAPI**: Connects to the LeaksAPI service to perform various types of data breach searches.
- **Multiple Search Capabilities**: Offers tools to search for compromised information using emails, domains, and phone numbers.
- **RapidAPI Integration**: Utilizes RapidAPI for secure and efficient API requests.
- **FastMCP Framework**: Employs the FastMCP framework to manage and expose server functionalities.

## Main Features and Functionality

The Aigeon AI LeaksAPI server provides several key functionalities:

1. **Password Premium Subscription**: A tool to check for premium subscription breaches related to passwords.
2. **Search**: A general search endpoint that allows users to check for data breaches using a specific query.
3. **Domain Search**: Enables full domain searches to identify breaches associated with an entire domain rather than individual emails.
4. **Phone Number Search**: A tool dedicated to searching for breaches involving phone numbers.
5. **Old Search**: A private endpoint for querying historical breach data.

## API Endpoints or Main Functions Description

The server exposes the following main functions, each corresponding to a specific API endpoint:

- **`passwords_premium_subscription()`**: 
  - **Description**: Checks for premium subscription breaches related to passwords.
  - **Endpoint**: `/api/v2/query/testemail@gmail.com`
  - **Returns**: A dictionary containing the response from the LeaksAPI.

- **`search(check: Annotated[str, Field(description='')])`**: 
  - **Description**: Performs a general search for data breaches using a specified query.
  - **Endpoint**: `/api/public`
  - **Parameters**: `check` - The search query string.
  - **Returns**: A dictionary containing the search results.

- **`domain_search(type: Annotated[str, Field(description='')] = None)`**: 
  - **Description**: Conducts a full domain search to identify breaches associated with a domain.
  - **Endpoint**: `/api/v2/query/example.com`
  - **Parameters**: `type` - Optional parameter to specify the type of search.
  - **Returns**: A dictionary with the domain search results.

- **`phone_number_search()`**: 
  - **Description**: Searches for breaches involving phone numbers.
  - **Endpoint**: `/api/v2/query/07777777777`
  - **Returns**: A dictionary containing the phone number search results.

- **`old_search()`**: 
  - **Description**: A private endpoint for querying historical breach data.
  - **Endpoint**: `/api/v2/private/query/test@gmail.com`
  - **Returns**: A dictionary with the historical search results.

Each function is decorated with `@mcp.tool()`, indicating its exposure as a tool within the FastMCP framework. The server runs using the `mcp.run(transport="stdio")` command, which initializes the server to handle requests via standard input/output.

**Note**: The API keys and endpoints used in this code are placeholders and should be replaced with valid credentials and endpoints for production use.
```
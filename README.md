```markdown
# Aigeon AI LeaksAPI

Aigeon AI LeaksAPI is a Python-based server application designed to interact with the LeaksAPI service. It provides various tools to query and retrieve information related to data leaks, including email addresses, domains, and phone numbers. The application leverages the FastMCP framework to define and manage its tools, facilitating efficient and structured API interactions.

## Features Overview

- **Email Leak Check**: Verify if a specific email address is part of any known data leaks.
- **Domain Leak Search**: Conduct comprehensive searches for leaks associated with entire domains.
- **Phone Number Leak Search**: Identify leaks involving specific phone numbers.
- **Premium Subscription Access**: Access premium features of the LeaksAPI service.
- **Private Endpoint Access**: Utilize private endpoints for specialized queries.

## Main Features and Functionality

1. **Password Premium Subscription**: This feature allows users to access premium data leak information for a specific email address. It is designed to provide detailed insights into potential password exposures.

2. **Search Functionality**: Users can perform searches using specific criteria to identify if their data has been compromised. This tool is versatile and can be tailored to various search parameters.

3. **Domain Search**: Instead of checking individual email addresses, this feature enables users to conduct a full domain search. It is particularly useful for organizations that want to ensure the security of their entire domain.

4. **Phone Number Search**: This tool is dedicated to identifying leaks associated with phone numbers, providing an additional layer of security for users concerned about telecommunication data breaches.

5. **Old Search**: A private endpoint designed for specialized queries, allowing access to historical data leak information.

## Main Functions Description

- `passwords_premium_subscription() -> dict`: This function interacts with the LeaksAPI to retrieve premium subscription data for a specific email. It requires a valid API key and returns a JSON response containing the leak information.

- `search(check: Annotated[str, Field(description='')]) -> dict`: This function performs a search based on the provided criteria. It sends a request to the public API endpoint and returns a JSON response with the search results.

- `domain_search(type: Annotated[str, Field(description='')] = None) -> dict`: This function allows users to search for leaks associated with an entire domain. It accepts an optional type parameter to refine the search and returns the results in JSON format.

- `phone_number_search() -> dict`: This function queries the LeaksAPI for leaks related to a specific phone number. It returns a JSON response with the relevant data.

- `old_search() -> dict`: This function accesses a private endpoint to retrieve historical data leak information for a given email address. It returns the data in JSON format.

The application is structured to run with the FastMCP framework, utilizing the `mcp.run(transport="stdio")` command to initiate the server. This setup ensures efficient handling of API requests and responses, providing a robust solution for data leak detection and prevention.
```
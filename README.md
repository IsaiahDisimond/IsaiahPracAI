Assignment 1 Report: Calling, Building, and Securing APIs

Deliverable 1: Create an Account and Connect to the Azure Vision API

To connect to the Azure Vision API, I created a new account on the Azure portal and followed these steps:

Created a new resource group and a new Azure Cognitive Services account.
Selected the "Computer Vision" option and chose the free tier (F0) pricing plan.
Filled in the required information, such as name, subscription, and location.
Waited for the deployment to complete.
Evidence Screenshot

[Insert screenshot of Azure Vision API subscription]

Deliverable 2: Explanation of Hard-Coding Credentials and Committing Code

Hard-coding credentials directly in the code is a bad idea for several reasons:

Security Risks: If an unauthorized person gains access to your code, they can obtain your credentials and misuse them.
Version Control Issues: When you commit your code to version control systems like Git, your credentials become visible to anyone with access to the repository.
Credential Rotation: If you hard-code your credentials and need to update them, you'll have to manually search and replace all occurrences in your code.
To avoid these issues, it's recommended to store sensitive information like credentials as environment variables or use secure storage solutions like Azure Key Vault.

Git Commit without Credentials

I committed my code to GitHub without including my Azure Vision API credentials. Instead, I used environment variables to store my subscription key and endpoint.

Deliverable 3: Run the API Endpoint and Demonstrate Example Invocation

I ran the API endpoint using the provided starter code and demonstrated an example invocation using curl.
This curl command sends a POST request to the /analyze_image endpoint with a JSON body containing the image URL. The API endpoint then calls the Azure Vision API to analyze the image and returns the response in JSON format.

The Café Website: Securing Access with Amazon Cognito
Frank loves coffee. As the owner of a small but growing café, he relies on real-time inventory reports to ensure he never runs out of his best-selling coffee beans. Until now, Frank had to manually check stock levels—a tedious process that often led to last-minute shortages.

That’s where Sofía comes in. As the café’s developer, she’s on a mission to streamline Frank’s workflow. She decides to integrate Amazon Cognito into the café website, allowing Frank to log in securely and request inventory reports with a single click.

 The Plan: Making Authentication Seamless
To make this possible, Sofía sets up Amazon Cognito as the café website’s authentication service. Here’s her step-by-step approach:

1️⃣ Setting Up the Development Environment
Before diving into the implementation, Sofía configures her VS Code IDE and runs a script to restore the work she had done in previous labs. Now, she’s ready to start building.

2️⃣ Creating an Amazon Cognito User Pool & App Client
She sets up an Amazon Cognito user pool, which will manage user authentication. Then, she configures an app client that allows the website to communicate with Cognito, ensuring Frank can log in securely.

3️⃣ Integrating Cognito’s Hosted UI into the Website
Next, Sofía updates the website to redirect users to Cognito’s hosted login page. Once Frank enters his credentials, Cognito verifies his identity and redirects him back to the website with an authentication token. This token is stored in his browser and used for future requests.

4️⃣ Updating API Authentication with API Gateway
Originally, the café’s create_report API endpoint was accessible without authentication. To improve security, Sofía:
✔ Configures CORS to accept authentication headers from CloudFront.
✔ Implements an API Gateway authorizer that validates Frank’s identity before granting access to the inventory report.

5️⃣ Testing the End-to-End Workflow
With everything in place, it’s time for the final test.
✅ Frank logs into the café website using his Cognito credentials.
✅ He clicks the "Generate Report" button.
✅ His authentication token is sent in an Authorization header with the request.
✅ The API gateway authorizer verifies the token, allowing access.
✅ The system returns a real-time inventory report, helping Frank stay on top of his stock levels.

 The Impact: A Smarter, More Secure Café
Now, Frank can log in from anywhere and instantly check his inventory—no more guesswork, no more shortages. Thanks to Sofía’s implementation, the café’s operations are smoother, more secure, and far more efficient.

 Technologies Used
✔ Amazon Cognito – Secure user authentication
✔ AWS API Gateway – Protect API endpoints
✔ AWS Step Functions – Automate backend processes
✔ Amazon S3 & CloudFront – Host the website
✔ JavaScript & AJAX – Handle authentication tokens

With this upgrade, the café website is no longer just a simple web page—it’s an intelligent, secure business tool. And best of all, Frank can focus on what he does best: making great coffee. ☕🚀

By implementing these enhancements, Sofía transformed the café website into a secure and efficient tool for managing inventory.

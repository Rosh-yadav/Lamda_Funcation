
## Additional AWS Lambda Terms Explained

### **13. Event Payload**

- **Why We Use It:** To pass data to your Lambda function when it is invoked.
- **When to Use:** When your function needs input data to process, such as a file or API request data.
- **How to Use It:** The event payload is automatically passed by the service that triggers the function. Access it in your Lambda code through the event parameter.
- **Where to Use It:** In scenarios like processing file uploads from S3, handling HTTP request data from API Gateway, or reacting to messages from SQS.

### **14. Custom Runtime**

- **Why We Use It:** To support programming languages or versions not natively supported by AWS Lambda.
- **When to Use:** When you need to run code in a language or runtime environment that AWS Lambda does not provide by default.
- **How to Use It:** Create a custom runtime by providing an implementation of the Lambda Runtime API and package it with your Lambda function.
- **Where to Use It:** For specialized applications requiring custom language versions or runtime environments.

### **15. Lambda@Edge**

- **Why We Use It:** To run Lambda functions at AWS edge locations, closer to your users.
- **When to Use:** When you need to perform operations on content as it is delivered via Amazon CloudFront, such as modifying requests and responses.
- **How to Use It:** Deploy your Lambda function to AWS edge locations and associate it with CloudFront distribution events.
- **Where to Use It:** For low-latency applications like content personalization, security headers injection, or URL rewrites at edge locations.

### **16. Cold Start**

- **Why We Use It:** To understand the delay experienced when a Lambda function is invoked after being idle.
- **When to Use:** When assessing the performance impact of latency in Lambda functions, especially for functions that are invoked infrequently.
- **How to Use It:** Monitor cold start durations using AWS CloudWatch Logs and optimize function initialization to reduce latency.
- **Where to Use It:** In applications where consistent performance and quick response times are critical.

### **17. Warm Start**

- **Why We Use It:** To refer to the scenario where a Lambda function is invoked after being previously executed and kept warm.
- **When to Use:** When optimizing for performance and minimizing latency for frequently invoked Lambda functions.
- **How to Use It:** Use provisioned concurrency or manage invocation frequency to keep instances warm.
- **Where to Use It:** In applications requiring fast response times or where latency impact is a concern.

### **18. Function Version**

- **Why We Use It:** To manage different versions of your Lambda function code and configuration.
- **When to Use:** When you need to deploy and manage multiple versions of your function for testing or rollback purposes.
- **How to Use It:** Publish versions of your function in the Lambda console or using the AWS CLI, and manage aliases for versioning.
- **Where to Use It:** For managing releases, testing new code versions, or maintaining stability in production environments.

### **19. Alias**

- **Why We Use It:** To create a named reference to a specific version of a Lambda function.
- **When to Use:** When you want to route traffic to specific versions of your function or manage multiple environments.
- **How to Use It:** Create aliases in the Lambda console or using the AWS CLI, and map them to specific function versions.
- **Where to Use It:** In scenarios where you need to direct traffic to different function versions, such as staging vs. production.

### **20. Event Source Mapping**

- **Why We Use It:** To map an event source, like SQS or DynamoDB Streams, to a Lambda function.
- **When to Use:** When you need Lambda to process messages from a stream or queue automatically.
- **How to Use It:** Configure event source mappings in the Lambda console or using AWS CLI to connect your Lambda function to the event source.
- **Where to Use It:** For processing background jobs, real-time data streams, or queue-based messaging systems.

### **21. Resource-Based Policy**

- **Why We Use It:** To control access permissions to your Lambda function from other AWS services or accounts.
- **When to Use:** When granting permissions for other AWS services or external accounts to invoke your Lambda function.
- **How to Use It:** Add resource-based policies to your Lambda function using the AWS console or CLI to specify who can invoke the function.
- **Where to Use It:** When integrating with other AWS services, such as API Gateway or S3, or allowing cross-account access.

### **22. Logging**

- **Why We Use It:** To monitor and troubleshoot Lambda function executions by capturing logs and metrics.
- **When to Use:** When you need to debug or analyze function performance and behavior.
- **How to Use It:** Enable logging in the Lambda console or through your function code, and review logs in Amazon CloudWatch Logs.
- **Where to Use It:** For monitoring function execution, diagnosing issues, and improving performance.

### **23. Dead Letter Queue (DLQ) Policy**

- **Why We Use It:** To configure how failed Lambda function invocations are handled and retried.
- **When to Use:** When you need to manage and review failed events or handle retries.
- **How to Use It:** Configure DLQ settings in the Lambda console to specify an SQS queue or SNS topic for failed events.
- **Where to Use It:** For critical processing tasks where you need to ensure no data is lost and errors are reviewed.

### **24. Lambda Function Timeout**

- **Why We Use It:** To define the maximum duration a Lambda function can run before it is automatically terminated.
- **When to Use:** To prevent functions from running indefinitely and consuming resources.
- **How to Use It:** Set the timeout value in the Lambda function configuration, with a maximum of 15 minutes.
- **Where to Use It:** In functions that perform lengthy processing tasks or require specific execution time constraints.


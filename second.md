

## AWS Lambda Terms Explained

### **1. Lambda Function**

- **Why We Use It:** To run code in response to events without managing servers.
- **When to Use:** When you need a serverless way to execute code triggered by events.
- **How to Use It:** Create a Lambda function in the AWS Lambda console, upload your code, and configure triggers.
- **Where to Use It:** For event-driven tasks like processing files in S3, handling API requests via API Gateway, or responding to DynamoDB changes.

### **2. Trigger**

- **Why We Use It:** To automatically invoke a Lambda function in response to specific events.
- **When to Use:** When you want Lambda functions to be executed based on events such as S3 uploads, database changes, or HTTP requests.
- **How to Use It:** Configure triggers in the AWS Lambda console or through AWS services like S3, DynamoDB, or API Gateway.
- **Where to Use It:** To automate responses to data changes, manage event-driven workflows, or handle real-time data.

### **3. Event Source**

- **Why We Use It:** To define the origin of the events that invoke a Lambda function.
- **When to Use:** When setting up triggers that connect your Lambda function to external AWS services.
- **How to Use It:** Specify the event source in the Lambda console, such as S3 bucket, DynamoDB table, or Kinesis stream.
- **Where to Use It:** In scenarios like file processing in S3 or real-time data processing from Kinesis streams.

### **4. Execution Role**

- **Why We Use It:** To grant Lambda functions permissions to access other AWS services and resources.
- **When to Use:** Always, as Lambda functions require permissions to interact with other AWS services.
- **How to Use It:** Create an IAM role with appropriate policies and attach it to your Lambda function.
- **Where to Use It:** When your Lambda function needs to read from S3, write to DynamoDB, or access other AWS services.

### **5. Layers**

- **Why We Use It:** To manage and share common code or libraries across multiple Lambda functions.
- **When to Use:** When you have shared dependencies or custom runtime components that multiple functions use.
- **How to Use It:** Create a Lambda layer containing your libraries, then add it to your Lambda functions.
- **Where to Use It:** In projects where multiple functions need access to the same libraries or code.

### **6. Environment Variables**

- **Why We Use It:** To pass configuration settings to your Lambda function without hardcoding them.
- **When to Use:** When you need to customize Lambda function behavior based on different environments (e.g., dev, test, prod).
- **How to Use It:** Set environment variables in the Lambda function configuration and access them in your code using environment variable access methods.
- **Where to Use It:** For storing settings like API keys, database connection strings, or other configuration details.

### **7. API Gateway**

- **Why We Use It:** To expose your Lambda functions as HTTP endpoints for web or mobile applications.
- **When to Use:** When you need to create RESTful APIs or webhooks that trigger Lambda functions.
- **How to Use It:** Set up API Gateway in the AWS console, create resources and methods, and integrate them with your Lambda function.
- **Where to Use It:** For building serverless APIs, handling HTTP requests, or creating webhooks.

### **8. Concurrency**

- **Why We Use It:** To control the number of Lambda function instances that run concurrently.
- **When to Use:** When you need to manage or limit the load on your Lambda functions to prevent resource contention.
- **How to Use It:** Set concurrency limits in the Lambda console or use provisioned concurrency for predictable performance.
- **Where to Use It:** In high-throughput applications where you want to ensure consistent performance or manage resource usage.

### **9. Provisioned Concurrency**

- **Why We Use It:** To ensure that a specific number of Lambda function instances are pre-warmed and ready to handle requests.
- **When to Use:** When you need predictable start-up times for your Lambda functions to meet performance requirements.
- **How to Use It:** Configure provisioned concurrency in the Lambda console or via AWS CLI to keep a set number of instances warm.
- **Where to Use It:** In latency-sensitive applications where cold starts could impact performance.

### **10. Dead Letter Queue (DLQ)**

- **Why We Use It:** To handle failed Lambda function executions by sending them to a designated SQS queue or SNS topic.
- **When to Use:** When you need to ensure that failed events are not lost and can be processed later.
- **How to Use It:** Configure DLQ settings in the Lambda console, specifying an SQS queue or SNS topic.
- **Where to Use It:** For critical processing tasks where failed events need to be reviewed or retried.

### **11. Timeout**

- **Why We Use It:** To specify the maximum time a Lambda function can run before it is terminated.
- **When to Use:** To prevent functions from running indefinitely and consuming resources.
- **How to Use It:** Set the timeout value in the Lambda function configuration, up to a maximum of 15 minutes.
- **Where to Use It:** For functions that handle long-running tasks or require a specific execution duration.

### **12. Memory Allocation**

- **Why We Use It:** To control the amount of memory allocated to your Lambda function, which also affects its CPU power.
- **When to Use:** To optimize performance and cost based on the function’s resource needs.
- **How to Use It:** Adjust the memory setting in the Lambda function configuration and monitor performance to find the right balance.
- **Where to Use It:** For functions that require more resources to handle computational tasks or process large data sets.


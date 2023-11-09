# AWS-Lambda-Limitations

AWS Lambda, a serverless compute service provided by Amazon Web Services, has several limitations in terms of memory and CPU that users should be aware of. These limitations may change over time, so it's important to refer to the official AWS documentation for the most up-to-date information. As of my last knowledge update in January 2022, here are some of the key limitations:

1.  Memory:
    
    *   Lambda allows you to configure the amount of memory allocated to a function, with a minimum of 128 MB and a maximum of 3,008 MB (3.008 GB). The allocated memory is directly proportional to CPU power.
    *   The CPU power provided to your Lambda function is determined by the amount of memory you allocate. For example, if you allocate 256 MB, you get a proportionate share of CPU power compared to when you allocate 1,024 MB.
2.  Execution Time:
    
    *   Each Lambda function is subject to a maximum execution time, which is 900 seconds (15 minutes) as of my last update. Functions that run longer than this limit will be terminated by AWS.
3.  Disk Space:
    
    *   Lambda provides ephemeral disk space in the "/tmp" directory for your function's temporary storage needs. This space is limited to 512 MB as of my last update. Keep in mind that data stored in the "/tmp" directory may not persist across multiple function invocations.
4.  Concurrent Executions:
    
    *   AWS Lambda has a concurrency limit, which is the maximum number of function executions that can be run in parallel. The limit varies by region and can be increased by contacting AWS support.
5.  Environment Variables:
    
    *   You can set environment variables for your Lambda functions, but there is a limit to the number of environment variables and their total size. As of my last update, the limit was 4 KB for the total size of environment variables.
6.  Package Size:
    
    *   The deployment package (including the code and dependencies) for a Lambda function is limited to 50 MB for the deployment package that you upload directly. You can use larger packages by storing them in an S3 bucket.
7.  Network Bandwidth:
    
    *   Lambda functions have limitations on network bandwidth, both for outbound and inbound traffic. The exact limits can depend on the specific AWS region and are subject to change over time.

It's important to check the AWS Lambda documentation for the most current information on resource limitations and constraints because AWS may update these limits periodically. Additionally, AWS may offer different resource limits for different types of Lambda functions, so be sure to review the documentation for the specific type of function you are working with (e.g., AWS Lambda for Lambda@Edge, AWS Lambda for AWS Step Functions, etc.).

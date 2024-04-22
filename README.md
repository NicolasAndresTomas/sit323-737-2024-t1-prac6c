# Kubernetes Deployment:

## To deploy this application on a Kubernetes cluster, use the provided deployment.yaml and service.yaml files
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

## After applying the deployment and service, verify the application is running and accessible:
kubectl get pods
kubectl get service my-microservice

## You can then access the application via the external IP provided by the Kubernetes service, or use port-forwarding for local testing:
kubectl port-forward service/my-microservice 8080:80

## Now you can access the application at http://localhost:8080

# The Calculator Microservice offers several arithmetic operations. Use the following endpoints to perform calculations:

Addition (/add):
- Description: Adds two numbers.
- Usage: /add?num1=1&num2=2
- Expected result: Result: 3

Subtraction (/subtract):
- Description: Subtracts one number from another.
- Usage: /subtract?num1=5&num2=2
- Expected result: Result: 3

Multiplication (/multiply):
- Description: Multiplies two numbers.
- Usage: /multiply?num1=3&num2=4
- Expected result: Result: 12

Division (/divide):
- Description: Divides one number by another.
- Usage: /divide?num1=8&num2=2
- Note: Division by zero will return an error.
- Expected result: Result: 4

Exponentiation (/power)
- Description: Raises one number to the power of another.
- Usage: /power?num1=2&num2=3
- Expected Result: Result: 8

Square Root (/sqrt)
- Description: Calculates the square root of a number.
- Usage: /sqrt?num1=16
- Note: Negative numbers will return an error.
- Expected Result: Result: 4

Modulo (/modulo)
- Description: Finds the remainder of division between two numbers.
- Usage: /modulo?num1=10&num2=4
- Expected Result: Result: 2

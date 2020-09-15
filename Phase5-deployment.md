# Phase 5: Deployment

A machine learning model can only begin to add value to an organization when that model's insights routinely become available to the users for which it was built. The process of taking a trained ML model and making its predictions available to users or other systems is known as deployment.
## Planning deployment
1. Model format?
e.g. onnx format, .h5 format, .tfrecord format?

2. Runtime: 
- Where it's going to run?
e.g. cloud (aws ec2? ecs? ), edge, on-preime
- what inference model we're going to use?
e.g. onnxruntime? tensorrt? aws sagemaker neo?

3. Application Deployment
e.g. aws beanstalk? docker container? on cloud solutions: aws sagemaker? azure ml?

4. Model acceleration:
- hardware acceleration: CPU, GPU, FPGA
- inference acceleration: use c++ based library for inference speed-up. eg, tensorrt.

4. Infrastructure Deployment
e.g. terraform?

## Maintenance and monitoring
1. Code management?
e.g. codecommit, git, etc

2. Monitoring?
e.g. aws cloudwatch

## Final report

## Project overview
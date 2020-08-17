# Phase 1: Business Understanding

Make great Machine Learning Product is hard, but not impossible. Instead of starting from a ML problem, a deep understanding of the business requirements is the key to the success of a ML project.

## Understanding business requirements
Machine learning is getting ready for business, but are businesses ready for AI? Technical challenges are an important differentiating factor between industries. While big tech and academia are pushing advances in the performance of the underlying technology, engineering solutions need to be worked out for specific use cases, requiring both data and talent. Industries such as financial services, and high tech and telecom have generated and stored large volumes of structured data, but others, including construction and travel, lag far behind. Considering the various digital stages of different businesses, each machine learning project has to be specially designed based on deep understanding of the business requirements.

1. Form a business question:
Depends on whether the project is driven by the CIO or CFO, business might have different expectations from the ML product. The first step before diving into the ML solutions, is to ask a business question: From the business point of the view, what do you want?

For example, the business question can be:
    -  How can we improve the click-through rates of our ads?
    -  How can we reduce the human labors in spam email identification?
    -  How to stay competitive and catch the trend of AI?

It might sound a little discouraging, but ML products sometimes are not the best solutions to these questions. If you keep that in mind and try not to plug ML in every place, you've got a great start for a ML project.

2. Understand the nature of a ML product
Machine learning products can be roughly classified into two categories: Engineering product or R&D product.

    - Engineering Product:

        Unless you're tech giants or digital native companies like Google, Amazon, etc, most ML products should fall in this category. Most of the problems you will face are, in fact, engineering problems. Most companies won’t focus on developing ML models but will use an off-the-shelf model. For such businesses, having a reliable and easy to maintain ML application can make a huge boost to their revenue, while spending months to fine-tune the newest model appeared in the academia probably doesn't fit into their business requirement.

        Therefore, as a ML engineer, you have to temperately disable the "mathematician" part of you and release the "engineer" part of you. And repeat after me: No fancy algorithms! No complex pipelines! Easy and stable!

    - Research and Development Product
        
        If a business has a R&D product plan for machine learning, they are serious of making big impacts in this field. Most of the time they are equipped with talents and experts, and what they want from us is normally more in a management level instead of technical level. This is not very common for an engineer to step in such machine learning projects, actions depend on case by case.

## Analyzing supporting information

1. List required resources and assumptions
    - People and talent: ML engineers, data engineers, scrum masters(solution owner), QE, Experience Design, cloud engineer(cds), SE, etc
    - Resources: hardware, software
    - Budget: cost for implementing the whole plan


2. Analyze associated risks
e.g. business risks: fail to deploy the solution/solution doesn't work well/customer latency

3. Plan for contingencies
e.g. 

4. Compare costs and benefits
e.g. estimate azure/aws/gcp costs based on the resources. estimate the profit introduced by the new product

## Converting to a Data Mining problem
1. Review machine learning question
e.g. The questions is: We need a product can help improve captain's situation awareness

2. Create technical data mining objective
the nature of the problem(supervised/unsupervised, classification/regression)
e.g. This question can be converted to a ML problem: use object detection method to detect objects on the surface, highlight it on a video stream to help the captain be aware of the surroundings.

3. Define the criteria for successful outcome of the project
e.g. A iPAD application is developed to use object detection method to detect objects on the surface of the sea.

## Preparing a preliminary plan
1. Number and duration of stages:
e.g. stage 1: discovery spike. stage 2: basic demo roll out. stage 3: more features and further development.

2. Dependencies:
e.g. Hardware requirements. Personal requirements. 

3. Risks:
e.g. rough weather condition decrease the performance.

4. Goals:
e.g.A iPAD application is developed to use object detection method to detect objects on the surface of the sea. 

5. Evaluation methods:
e.g. Fail to identify a boat or miss-identify something else as a boat? or both?

6. Tools and techniques:
Different tools in the ML life cycle
e.g. object detection model. framework (darknet/tensorflow/pytorch). deployment method.
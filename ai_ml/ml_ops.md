* To improve the results of a model, there are 2 ways to do it: model-centric view, and data-centric view. Model centric view focuses on fixing the data and iteratively improving the model, and data-centric view focuses on fixing the model and iteratively improving the data
* Data is food for AI. 80% of the work is of data cleaning and processing, and only 20% is of training the model


### Lifecycle of a ML project
*  Scope  -> Collect Data <-> Train the model <-> Deploy in production
### Collect Data
* Make sure the data is labeled consistently
    * If there are 2 labelers that label the data differently, revise the labeling instructions until they become consistent by measuring consistency between labelers


## Clean vs Noisy data
* If we have a data size of x, and y% of that data is noisy, to improve the performance of the model either we can clean up the noise of the data, or increase the size of the data (assuming similar quality of data)
* With a data centric view, there is a significant room for improvement in problems with <10000 examples


## Data Augmentation
* Technique used to artificially increase the size and diversity of the dataset
* It works by creating modified copies of existing data
* It involves applying transformations to existing data points to create new, slightly different versions, such as flipping, rotating, or adding noise to images. 

### GAN data augmentation
* GAN (Generative Adversarial Network) data augmentation is a technique where GANs are used to generate synthetic data that mimics the distribution of the original dataset, effectively increasing the dataset size and diversity. This allows machine learning models to learn from more diverse examples, improving generalization and performance, especially when real data is limited. 
* Traditional Data Augmentation:
Standard data augmentation involves applying transformations to existing data, such as flipping, rotating, or adding noise. While this can be simple and efficient, it doesn't introduce entirely new data points. 
* GANs, on the other hand, learn to generate new data samples that are statistically similar to the real data. This means the generated data can be completely new and unseen by the model, leading to a more substantial increase in diversity and potentially improved generalization. 
* A GAN consists of two networks: a generator and a discriminator. The generator learns to produce synthetic data, while the discriminator tries to distinguish between real and synthetic data. This adversarial training process allows the generator to learn to create realistic and diverse data. 

## Inference
* In artificial intelligence (AI), inference is the process where a trained AI model uses its learned knowledge to make predictions or draw conclusions from new, unseen data. It's essentially the AI model "in action," applying what it's learned during training to generate new outputs or solve problems. 
* AI models are first trained on large datasets to learn patterns and relationships. Inference happens after training, when the model is used to make predictions on new, previously unseen data. 

## DevOps Key Pillars
* Reduce organizational silos: Share ownership and accountability
* Accept failure as normal: Embrace risk and iterative development
* Implement gradual changes: Move quickly with smaller iterations to reduce the cost of failure
* Leverage tooling and automation: Use tools to automate manual tasks
* Measure everything: Define what “success” is and how it will be measured

## Hyperparameters
* Hyperparameters are settings you configure before training a machine learning model to influence how the model learns from data. Unlike parameters, which are learned during the training process, hyperparameters are set manually and remain constant throughout training. 
* Learning rate, batch size, number of epochs, number of layers in a neural network, and model architecture are all examples of hyperparameters. 
* Parameters are internal variables learned by the model during training to fit the data, while hyperparameters are external settings set before training. 

## One-hot encoding
A technique that transforms categorical data into a numerical format suitable for machine learning algorithms. It creates a new binary column (0 or 1) for each unique category in a feature, allowing models to process this information without assuming any order or ranking between categories. 


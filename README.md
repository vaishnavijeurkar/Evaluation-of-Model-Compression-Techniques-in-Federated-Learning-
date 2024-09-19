# **Evaluation of Model Compression Techniques in Federated Learning under bandwidth considerations**

This repository contains the code, data, and experiments for the project titled **"Evaluation of Model Compression Techniques in Federated Learning under bandwidth considerations"**. The project investigates the application of structured and unstructured pruning as model compression algorithms within the context of federated learning, focusing on scenarios with bandwidth-constrained devices.

## **Abstract**

Federated learning offers a promising approach for edge training, but its deployment is hindered by the limited bandwidth and computing resources of edge devices. Existing research presents various model compression techniques, including quantization, pruning, and knowledge distillation, to address these challenges.

This paper investigates the application of structured and unstructured pruning as model compression algorithms within the context of federated learning, using the Flower framework for simulation. Our approach involves dynamically selecting and pruning weights or neurons at each training round on the client side, followed by sparse matrix communication, thereby reducing the data transferred to the server.

We specifically target scenarios with bandwidth-constrained devices that can train models over multiple rounds but where the amount of data transferred, and consequently the duration of wireless transmission, is limited. Extensive experiments demonstrate that our proposed pruning and sparsification approach significantly reduces upstream communication bytes while maintaining accuracy, albeit with an increased number of rounds.

For instance, training a ResNet-12 model on the CIFAR-10 dataset yields 77.40% accuracy in 58 rounds with 155 megabytes of data transfer per round, whereas an 80% pruned model achieves 78.80% accuracy in 63 rounds, with only 49 megabytes transferred per round. This research not only addresses deployment scenarios with limited bandwidth, presenting a comparison of two model compression techniques and their impact on accuracy and the number of training rounds, but also raises important questions regarding the optimal model size for specific deep learning tasks and the necessity of large complex models for achieving peak accuracy.

## **Repository Structure**

- **`experimental_data/`**: Contains JSON files with experimental data including accuracy, loss, pruning rate, and the number of rounds for each experiment.
  
- **`experiment_notebooks/`**: Contains 6 Jupyter notebooks that can be used to run structured or unstructured model compression pruning experiments.

- **`charts.ipynb`**: Jupyter notebook used for generating plots and visualizing the experimental results.

- **`plots/`**: Contains chart images generated from the experiments, illustrating the results.

## **Getting Started**

### **Prerequisites**

- Python 3.x
- Jupyter Notebook

### **Installation**

1. Clone the repository:
    ```bash
    git clone https://github.com/vaishnavijeurkar/Evaluation-of-Model-Compression-Techniques-in-Federated-Learning-.git
    cd Evaluation-of-Model-Compression-Techniques-in-Federated-Learning-
    ```

2. Create a virtual environment and activate it:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    Uncomment the required cells for installing flower.

### **Running the Experiments**

1. Navigate to the `experiment_notebooks/` directory and open any of the Jupyter notebooks to run the structured or unstructured pruning experiments:
    ```bash
    jupyter notebook
    ```

2. Use the `charts.ipynb` notebook to generate plots from the experimental data stored in the `experimental_data/` folder.

### **Results**

The results of the experiments are visualized in the `plots/` folder, where each image represents the outcome of different pruning strategies on the model's performance.

## **Contributing**

If you would like to contribute to this project, please fork the repository, create a new branch, make your changes, and submit a pull request. Contributions are welcome!


## **Contact**

For any inquiries or issues, please contact [jeurkarvaishnavi510@gmail.com](jeurkarvaishnavi510@gmail.com).

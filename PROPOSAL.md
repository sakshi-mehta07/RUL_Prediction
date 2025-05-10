## Project proposal form

Please provide the information requested in the following form. Try provide concise and informative answers.

**1. What is your project title?**

Evaluation of different deep learning models for remaining useful life prediction using NASA's C-MAPSS dataset

**2. What is the problem that you want to solve?**

In a variety of sectors, including aerospace engineering, estimating Remaining Useful Life (RUL) is a vital predictive task. To ensure safe operation of equipment, prevent unplanned downtime and improve efficiency, operators need precise estimates for the remaining duration during which the system will continue to function reliably – *before* the failure occurs.

We therefore propose to predict the RUL of turbofan jet engines based on NASA’s C-MAPSS dataset. A deep learning approach is uniquely well-positioned to solve this issue due to capturing complex time-dependencies, offering a flexible framework that can be adapted to the four different subsets of C-MAPSS and automatically learning features from the extensive data simulated by up to 26 sensors.


**3. What deep learning methodologies do you plan to use in your project?**

Based on a brief literature review of recent studies evaluating deep learning models for Remaining Useful Life (RUL) prediction, we understand that suitable models need to be able to capture temporal dependencies as well as perform well on noisy and non-stationary data. We aim to compare three model types that have demonstrated strong performance in that regard:

- **CNN-(Bidirectional) LSTM:**
Combines convolutional layers for local feature extraction with bidirectional LSTMs to capture forward and backward temporal dependencies in time-series data.

- **Attention-based GRU:**
Leverages gated recurrent units for efficient sequence modeling while incorporating attention mechanisms to focus on the most relevant time steps for RUL estimation.

- **Stacked Autoencoder (SAE):**
Performs unsupervised feature learning and dimensionality reduction, enabling the extraction of robust degradation patterns from raw sensor data.

**4. What dataset will you use? Provide information about the dataset, and a URL for the dataset if available. Briefly discuss suitability of the dataset for your problem.**

**Original data source:** https://data.nasa.gov/Aerospace/CMAPSS-Jet-Engine-Simulated-Data/ff5v-kuh6/about_data 

The C-MAPSS dataset, developed by NASA, is a go-to resource for building and testing predictive maintenance models for aircraft engines. It contains run-to-failure simulations of turbofan engines, meaning each engine starts in good condition and gradually degrades until failure.

What’s in the dataset?

- Different subsets: The dataset is divided into FD001, FD002, FD003, and FD004, each representing different operating conditions and fault types.
- Sensor data: Each engine has multiple sensors (21-26, depending on the subset) that track its health over time.
- Operational settings: Includes variables like altitude, Mach number, and throttle resolver angle, which impact engine performance.
- Variable-length lifespans: Not all engines fail at the same time—some last longer than others, making the prediction task more challenging.

Why is it useful for predictive maintenance?

- Perfect for RUL prediction: The goal is to estimate how much time an engine has left before failure—a key part of predictive maintenance.
- Rich time-series data: The multiple sensor readings provide detailed insights into how engines degrade over time.
- Scalable complexity: The four subsets offer varying levels of difficulty, so you can start simple and work up to more complex scenarios.

**5. List key references (e.g. research papers) that your project will be based on?**

| Title | Authors | Year | Main method |
|-------|---------|------|-------------|
| [A survey of deep learning-driven architecture for predictive maintenance](https://www.sciencedirect.com/science/article/pii/S0952197624004433) | Zhe Li et al. | 2024 | Survey Article |
| [Deep learning models for predictive maintenance: a survey, comparison, challenges and prospect](https://link.springer.com/article/10.1007/s10489-021-03004-y) | Oscar Serradilla et al. | 2022 | Survey Article |
| [Robustness testing framework for RUL prediction Deep LSTM networks](https://www.sciencedirect.com/science/article/pii/S0019057820302767) | M. Sayah et al. | 2020 | LSTM |
| [Machine Remaining Useful Life Prediction via an Attention-Based Deep Learning Approach](https://ieeexplore.ieee.org/document/8998569) | Zhenghua Chen et al. | 2021 | LSTM |
| [A multimodal and hybrid deep neural network model for Remaining Useful Life estimation](https://www.sciencedirect.com/science/article/pii/S0166361518304925) | Ali Al-Dulaimi et al. | 2019 | CNN, LSTM |
| [A Novel Deep Learning Approach for Machinery Prognostics Based on Time Windows](https://www.mdpi.com/2076-3417/9/22/4813) | Hanbo Yang et al. | 2019 | CNN |
| [Remaining useful life prediction using multi-scale deep convolutional neural network](https://www.sciencedirect.com/science/article/pii/S1568494620300533) | Han Li et al. | 2020 | CNN |
| [Remaining useful life estimation in prognostics using deep convolution neural networks](https://www.sciencedirect.com/science/article/pii/S0951832017307779) | Xiang Li et al. | 2018 | CNN |
| [Dual Aspect Self-Attention based on Transformer for Remaining Useful Life Prediction](https://arxiv.org/abs/2106.15842) | Zhizheng Zhang, Wen Song, Qiqiang Li | 2021 | Transformer |

**Please indicate whether your project proposal is ready for review (Yes/No):**
Yes.

## Feedback (to be provided by the course lecturer)

[MV] 27 March 2025. **Approved.**

The proposal concerns predicting the remaining lifetime of aircraft engines using a multivariate time series of observation variables. This is a well-established problem in the literature, as evidenced by the provided references. The C-MAPSS dataset has been used to evaluate deep learning prediction models for this task (e.g. Section IV in Zhang, Song and Li (2021)). 

The problem provides an opportunity to apply various deep learning models and methods covered in the course. You may wish to position your deep learning methodology and the achieved prediction accuracy in relation to existing literature. 

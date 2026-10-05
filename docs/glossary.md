Glossary

 Machine Learning (ML) — an approach where a model learns patterns from data instead of being programmed with explicit rules.
 Deep Learning (DL) — a subfield of ML using neural networks with multiple layers.
 Supervised learning — learning with labels, where every training example has the correct answer.
 Unsupervised learning — learning without labels, where the model finds structure on its own.
 Random Forest — an ensemble of decision trees that vote together.
 MLP (Multi-Layer Perceptron) — a basic feedforward neural network of fully-connected layers.
 Autoencoder (AE) — a network that compresses input and reconstructs it; high reconstruction error means anomaly.
 Encoder — the part of the AE that compresses the input into a small representation.
 Decoder — the part of the AE that reconstructs data from the compressed representation.
 Layer — one stage of processing inside a neural network.
 ReLU — activation function max(0, x) that passes positives and zeros out negatives.
 Sigmoid — activation function that squashes any number into (0, 1), good for probabilities.
 Dropout — regularization that randomly disables neurons so the network does not over-rely on any path.
 Adam — an optimizer, the algorithm that adjusts the network's weights.
 Learning rate — how big the weight update step is on each iteration.
 BCE Loss — Binary Cross-Entropy, the loss function for binary classification.
 MSE Loss — Mean Squared Error, the loss function used to train the autoencoder.
 Epoch — one full pass through the training data.
 Training — the process of fitting the model's weights.
 Inference — using a trained model to make predictions.
 Accuracy — share of correct predictions across all samples.
 Precision — of everything labeled as an attack, how much was really an attack.
 Recall — of all real attacks, how many the model caught.
 F1-score — harmonic mean of Precision and Recall, a balanced metric.
 ROC-AUC — area under the ROC curve; 1.0 is perfect, 0.5 is random guessing.
 ROC curve — a plot of True Positive Rate versus False Positive Rate at various thresholds.
 Confusion matrix — a table showing predicted vs actual: TP, TN, FP, FN.
 True Positive (TP) — an attack correctly identified as an attack.
 True Negative (TN) — normal traffic correctly identified as normal.
 False Positive (FP) — normal traffic wrongly flagged as an attack (false alarm).
 False Negative (FN) — an attack missed by the model, the most dangerous outcome in security.
 Classification report — a summary of Precision, Recall, and F1 for each class.
 Threshold — the cutoff probability (usually 0.5) at which a score becomes a class label.
 Dataset — a collection of data.
 Feature — an input column with a numeric or categorical value.
 Label — the target variable (0 = benign, 1 = attack).
 Class — a category an object belongs to.
 Sample — one row (object) in the dataset.
 Class imbalance — one class dominates; here 86% attacks vs 14% benign.
 Train/test split — dividing data into a training and a testing portion.
 Stratification — preserving class proportions when splitting.
 StandardScaler — transforms each feature to mean 0 and standard deviation 1.
 MinMaxScaler — rescales features into the range [0, 1].
 Feature importance — how useful each feature is for a model.
 Correlation — the linear relationship between features.
 Heatmap — a visual representation of a matrix, such as correlations.
 Overfitting — when a model memorizes training data and fails on new data.
 Regularization — methods that prevent overfitting.
 Ensemble — combining several models into one.
 Voting — averaging the models' predictions.
 Weighted voting — voting where each model has a weight proportional to its quality.
 Stacking — a meta-model learns how to combine the base models.
 IoT — Internet of Things; connected devices like cameras, sensors, and routers.
 Network traffic — data moving across a network.
 Benign — harmless traffic.
 Attack — malicious traffic.
 Network flow — a group of packets belonging to the same connection.
 Packet — the smallest unit of transmitted data in a network.
 Protocol — a set of rules for communication, such as TCP, UDP, or ICMP.
 DDoS — Distributed Denial of Service, overwhelming a target from many sources.
 DoS — Denial of Service, the same idea but from a single source.
 Spoofing — impersonation, where the attacker pretends to be someone else.
 MITM — Man-in-the-Middle, where the attacker sits between two communicating parties.
 ARP Spoofing — poisoning ARP tables to intercept traffic.
 DNS Spoofing — faking DNS responses.
 Reconnaissance (Recon) — information-gathering phase before an attack.
 Port Scan — probing ports to find open services.
 Host Discovery — finding hosts on a network.
 Vulnerability Scan — searching for known vulnerabilities.
 Mirai — a well-known IoT botnet.
 Brute force — trying many passwords or keys until one works.
 XSS — Cross-Site Scripting, injecting a script into a page.
 SQL Injection — injecting SQL code into a query.
 Command Injection — injecting OS commands.
 Browser Hijacking — stealing a browser session.
 Zero-day — an attack exploiting a previously unknown vulnerability with no existing signature.
 Anomaly detection — finding unusual behavior, especially useful against zero-days.
 Threat Hunting — an analyst's active search for hidden attacks.
 IoC — Indicator of Compromise, a clue that a system has been breached.
 MITRE ATT&CK — a globally used knowledge base of attacker tactics and techniques.
 Tactic — why the attacker acts, for example Impact.
 Technique — how the attacker acts, for example T1498.
 T1498 — Network Denial of Service.
 T1557 — Adversary-in-the-Middle.
 T1046 — Network Service Discovery.
 T1018 — Remote System Discovery.
 T1595 — Active Scanning.
 T1185 — Browser Session Hijacking.
 T1059 — Command and Scripting Interpreter.
 T1059.007 — JavaScript, a sub-technique of T1059.
 T1190 — Exploit Public-Facing Application.
 SIEM — Security Information and Event Management; collects and analyzes security events.
 SOC — Security Operations Center, the team that monitors those events.
 Sigma rule — a portable detection format for logs, similar to YARA but for log events.
 Detection rule — a condition that triggers an alert.
 Log source — where the events come from, for example product: iot, category: network_flow.
 False positives — legitimate events that trigger alerts, such as routine firmware updates.
 Level — severity of a rule: low, medium, high, or critical.
 flow_duration — length of the flow in time.
 Header_Length — total size of packet headers.
 Protocol Type — the protocol used, such as TCP, UDP, or ICMP.
 Duration — length of the connection.
 Rate / Srate / Drate — overall, source-side, and destination-side rates.
 fin_flag_number — number of FIN flags, meaning connection termination.
 syn_flag_number — number of SYN flags, meaning connection request.
 rst_flag_number — number of RST flags, meaning connection reset.
 rst_count — total RST count; the single most important feature in this work.
 IAT — Inter-Arrival Time, the average spacing between packets.
 urg_count — number of urgent (URG) packets.
 Number — a numeric aggregate from CICFlowMeter.
 Magnitue — magnitude, a typo in the dataset.
 Radius — a distribution metric.
 Covariance — covariance of flow features.
 Variance — variance.
 Weight — an aggregate flow characteristic.
 PyTorch — a deep learning framework.
 scikit-learn — a library of classic ML algorithms, metrics, and utilities.
 pandas — tabular data handling via DataFrames.
 numpy — numerical arrays and math.
 matplotlib / seaborn — visualization libraries for plots and heatmaps.
 HuggingFace datasets — a library for downloading public datasets.
 CUDA — NVIDIA's technology for GPU computing.
 GPU — graphics card that accelerates neural network training.
 Tesla T4 — the GPU model used in this work, available in Colab.
 YAML — a configuration format, used here for the Sigma rule.
 Colab / Jupyter — notebook environments for running code.
 Baseline — a reference model for comparison; here, Random Forest.
 Pipeline — a sequence of processing steps.
 Prediction — the model's output.
 Probability — the model's confidence, such as the probability of an attack.
 Ground truth — the correct answers in the dataset.
 CIC-IoT-2023 — the dataset name, the Canadian Institute for Cybersecurity IoT dataset from 2023.

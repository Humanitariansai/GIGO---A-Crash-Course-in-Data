
# **GIGO: A Crash Course in Data**



# **PART I — “I Have a Dataset. What Do I Do?”**

### *Statistical Techniques, Data Quality, Cleaning, Imputation, Bias Detection, and Foundational Analysis*

---

## **1. Understanding Your Data**

* Types of variables (categorical, continuous, ordinal, binary)
* Scale of measurement (nominal, ordinal, interval, ratio)
* Units, metadata, missingness patterns
* Identifying data modality: numeric, text, image, audio, time-series, multimodal

---

## **2. Descriptive Statistics**

### **2.1 Central Tendency**

* Mean • Median • Mode
* When each should be used (skew, outliers, robustness)

### **2.2 Spread & Dispersion**

* Range • IQR • Variance • Standard deviation
* Boxplots, outliers, robust alternatives (MAD)

### **2.3 Distribution Analysis**

* Histograms, density plots, Q-Q plots
* Normality tests (Shapiro–Wilk, Anderson–Darling, KS)

### **2.4 Covariance & Correlation**

* Covariance
* Pearson, Spearman, Kendall
* Correlation ≠ causation

---

## **3. Data Quality & Cleaning**

### **3.1 Missing Data**

* MCAR, MAR, MNAR
* Detecting missingness patterns (heatmaps, pairwise missingness plots)

### **3.2 Imputation Techniques**

* Simple: mean/median/mode
* KNN imputation
* Regression imputation
* Multiple imputation
* Forward/backward fill (time-series)

### **3.3 Outlier Identification**

* Z-score thresholding
* IQR rule
* MAD
* Isolation Forest (ML approach)

---

## **4. Bias, Fairness & Drift Detection**

### **4.1 Bias in Data**

* Sampling bias
* Survivorship bias
* Measurement bias
* Label bias
* Proxy variables
* Simpson’s paradox

### **4.2 Drift**

* Covariate shift
* Prior probability shift
* Concept drift
* Detecting drift using statistical distances (KS test, PSI, KL divergence)

### **4.3 Fairness Metrics**

* Demographic parity
* Equal opportunity
* Equalized odds
* Calibration across groups

---

## **5. Handling Imbalanced Data**

* Random undersampling
* Random oversampling
* SMOTE & variants
* Class weights
* When imbalance matters (rare events, fraud, medical)

---

## **6. Feature Selection & Engineering**

* Mutual information
* Variance threshold
* Correlation filters
* Regularized models (L1, L2, Elastic Net)
* Tree-based feature importance
* PCA, t-SNE, UMAP (dimensionality reduction)

---

## **7. Model Validation & Resampling**

### **7.1 Cross-Validation**

* K-fold
* Stratified K-fold
* Time-series CV
* Group CV

### **7.2 Bootstrapping**

* Sampling with replacement
* Confidence intervals from bootstrap distribution

---

## **8. Metrics for Model Quality**

* Accuracy, precision, recall, F1
* ROC–AUC, PR–AUC
* G-Mean
* MCC
* Regression metrics: MAE, RMSE, MAPE, (R^2)

---

## **9. Text, Image, and Time-Series Preprocessing**

### **9.1 Text**

* Tokenization
* Lemmatization
* Stopword removal
* TF–IDF, embeddings

### **9.2 Images**

* Normalization
* Resizing
* Augmentation

### **9.3 Time-series**

* Detrending
* Deseasonalizing
* Smoothing
* Lag features

---

## **10. Sample Size, Power & Uncertainty**

* Power analysis
* Mead’s resource equation
* Confidence intervals
* CDF reasoning for error bounds

---

# **PART II — Data Visualization: Theory, Design, & Chart Selection**

### *Marks, Channels, Graph Choice, Visual Perception, and Analytical Interpretation*

---

## **1. Foundations of Visual Encoding**

### **1.1 Marks**

* Points
* Lines
* Areas
* Bars
* Text
* Shapes

### **1.2 Visual Channels**

* Position
* Length
* Angle
* Color (hue, saturation)
* Shape
* Size
* Orientation
* Texture

### **1.3 Principles of Perception**

* Pre-attentive processing
* Gestalt principles
* Cognitive load
* Lie factor
* Data–ink ratio

---

## **2. Chart Types & When to Use Them**

### **2.1 Distribution**

* Histogram
* Density plot
* Boxplot
* Violin plot
* Ridgeline

### **2.2 Relationship**

* Scatterplot
* Bubble chart
* Heatmap
* Pair plot
* Correlation matrix

### **2.3 Comparison**

* Bar chart
* Grouped/stacked bar
* Dot plot
* Slope graph
* Lollipop chart

### **2.4 Part-to-Whole**

* Donut chart
* Treemap
* Sunburst
* Marimekko

### **2.5 Time-Series**

* Line chart
* Area chart
* Moving averages
* Spiral plots (seasonality)
* Calendar heatmaps

### **2.6 Spatial**

* Choropleth map
* Dot map
* Flow map
* Bubble map

### **2.7 Network / Hierarchy**

* Tree diagram
* Dendrogram
* Network graph
* Chord diagram
* Sankey diagram

---

## **3. How to Choose the Right Visualization**

### **3.1 Match the Graph to the Question**

* Comparison → bar, dot
* Trend → line
* Distribution → box/hist/density
* Relationships → scatter/heatmap
* Composition → stacked/tile charts
* Flow → Sankey, flow maps

### **3.2 Avoiding Misleading Visuals**

* Truncated axes
* Incorrect color maps
* Overplotting
* 3D distortion
* Too many categories

---

## **4. Storytelling With Data**

* Narrative structure
* Annotated insights
* Highlighting vs clutter
* Designing for the audience

---

# **PART III — Causal Thinking (Even If You’re Using Standard ML)**

### *Understanding Treatment, Confounding, Balancing, and Stratification Without Full Causal Models*

---

## **1. Why Causal Thinking Matters in ML**

* Correlation vs causation
* Prediction ≠ explanation
* Spurious relationships
* Data leakage as a causal problem

---

## **2. Basic Causal Terms**

### **2.1 Treatment & Control**

* What is a “treatment” in observational data?
* Binary vs continuous treatments

### **2.2 Potential Outcomes**

* (Y(1)), (Y(0))
* Average Treatment Effect (ATE)

### **2.3 SUTVA**

* Stable Unit Treatment Value Assumption

### **2.4 Confounding**

* Backdoor paths
* Common causes

---

## **3. Common Causal Problems in Predictive ML**

* Omitted variable bias
* Simpson’s paradox
* Collider bias
* Selection bias
* Reversing cause and effect

---

## **4. Tools for Causal Structure Thinking**

### **4.1 DAGs (Directed Acyclic Graphs)**

* Nodes = variables
* Edges = causal assumptions
* Why DAGs reveal invalid adjustments

### **4.2 Backdoor Criterion**

* Identifying confounders
* Knowing what to control for
* Knowing what **not** to control for (colliders!)

---

## **5. Balancing, Matching & Stratification (Without Full Causal Models)**

### **5.1 Stratification**

* Divide population into consistent subgroups
* Reduces imbalance
* Used in clinical trials and observational studies

### **5.2 Matching**

* Nearest-neighbor matching
* Propensity score matching
* Exact matching (rare but conceptually simple)

### **5.3 Propensity Scores**

* Estimate treatment probability
* Balance groups before modeling

### **5.4 Weighting**

* IPTW (Inverse Probability of Treatment Weighting)
* Stabilized weights

### **5.5 Checking Balance**

* Standardized mean differences
* Love plots
* Post-weighting validation

---

## **6. ML Algorithms Through a Causal Lens**

### **6.1 Why standard ML doesn’t solve confounding**

* Learns prediction, not causal structure
* Overfits bias in observational data

### **6.2 When ML can help causal workflows**

* Propensity estimation
* Heterogeneous treatment effect models
* Causal forests
* Meta-learners (T-, S-, X-learners)

---

## **7. Causal Reasoning for Non-Causal Practitioners**

* Establishing temporality
* Ruling out alternative explanations
* Sensitivity analysis
* Using domain knowledge when data is insufficient



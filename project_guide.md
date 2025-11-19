# Project Guide — HousePriceLab
A detailed, checkbox-based roadmap for completing the full analytical workflow.  
Use this document to monitor progress and ensure each phase is completed to professional standards.

---

## 1. Define Questions and Hypotheses  
**[ ] Phase 1 Complete**

### Tasks  
- [ ] Identify the core research question  
- [ ] Translate the question into measurable variables  
- [ ] Define primary and secondary hypotheses  
- [ ] Specify expected relationships (direction, rationale)  
- [ ] Document assumptions and contextual background  

### Deliverables  
- [ ] Research questions section written  
- [ ] List of hypotheses (H1, H2, …)  
- [ ] Rationale for each hypothesis  

### Done When  
- All hypotheses are clear, measurable, and falsifiable.

---

## 2. Collect and Understand the Data  
**[ ] Phase 2 Complete**

### Tasks  
- [ ] Download the Ames Housing Dataset  
- [ ] Document data source and licensing  
- [ ] Inspect all columns and data types  
- [ ] Describe each variable in plain language  
- [ ] Identify missing values and data constraints  

### Deliverables  
- [ ] Data dictionary  
- [ ] Source and licensing note  

### Done When  
- You can explain every variable and dataset limitation confidently.

---

## 3. Clean and Standardize  
**[ ] Phase 3 Complete**

### Tasks  
- [ ] Correct column data types  
- [ ] Impute or remove missing values  
- [ ] Standardize units and formats  
- [ ] Remove duplicates and structural errors  

### Deliverables  
- [ ] Clean dataset in `data/processed/`  
- [ ] `preprocessing.py` script  

### Done When  
- Cleaned data loads with no warnings or manual intervention.

---

## 4. Evaluate Data Quality and Coverage  
**[ ] Phase 4 Complete**

### Tasks  
- [ ] Compute missingness overview  
- [ ] Analyze category-level coverage  
- [ ] Identify biases and sampling issues  
- [ ] Validate representativeness  

### Deliverables  
- [ ] Missingness plots  
- [ ] Quality assessment notes  

### Done When  
- Weaknesses and risks are explicitly documented.

---

## 5. Create Aggregations and Derived Variables  
**[ ] Phase 5 Complete**

### Tasks  
- [ ] Create domain-relevant derived variables  
- [ ] Build interaction terms if justified  
- [ ] Aggregate features when meaningful  
- [ ] Validate assumptions behind engineered features  

### Deliverables  
- [ ] Feature-engineering documentation  
- [ ] Updated `preprocessing.py`  

### Done When  
- New variables improve interpretation or model structure.

---

## 6. Explore and Describe (EDA)  
**[ ] Phase 6 Complete**

### Tasks  
- [ ] Compute summary statistics  
- [ ] Plot distributions  
- [ ] Analyze relationships and correlations  
- [ ] Identify outliers and structure  
- [ ] Develop first narrative about the dataset  

### Deliverables  
- [ ] EDA notebook  
- [ ] Exported EDA visuals  

### Done When  
- You have a clear understanding of how the data behaves.

---

## 7. Infer and Test (Statistical Inference)  
**[ ] Phase 7 Complete**

### Tasks  
- [ ] Select appropriate tests for each hypothesis  
- [ ] Compute confidence intervals  
- [ ] Perform hypothesis tests (t-test, ANOVA, etc.)  
- [ ] Compute entropy and mutual information  
- [ ] Interpret p-values and effect sizes  

### Deliverables  
- [ ] Inferential analysis notebook  
- [ ] Tables and inferential visuals  

### Done When  
- All hypotheses have been formally evaluated.

---

## 8. Visualize with Honesty  
**[ ] Phase 8 Complete**

### Tasks  
- [ ] Create accurate, non-misleading plots  
- [ ] Include uncertainty intervals where relevant  
- [ ] Avoid distortions (axis truncation, inconsistent scales)  
- [ ] Prioritize clarity over decoration  

### Deliverables  
- [ ] Clean visualization set  
- [ ] Notes explaining design decisions  

### Done When  
- Visuals can stand alone and remain truthful.

---

## 9. Craft the Analytical Narrative (Storytelling)  
**[ ] Phase 9 Complete**

### Tasks  
- [ ] Structure narrative: Question → Evidence → Interpretation → Limitation  
- [ ] Connect findings to domain context  
- [ ] Maintain logical and readable flow  

### Deliverables  
- [ ] Storytelling section or document  

### Done When  
- A reader unfamiliar with the project can follow the reasoning easily.

---

## 10. Interpret Results  
**[ ] Phase 10 Complete**

### Tasks  
- [ ] Interpret coefficients and feature roles  
- [ ] Explain patterns seen in EDA and inference  
- [ ] Connect modeling insights to real-world expectations  
- [ ] Clarify association vs. prediction vs. causation  

### Deliverables  
- [ ] Interpretation summary  
- [ ] Limitations and assumptions section  

### Done When  
- Interpretations are accurate, contextualized, and restrained.

---

## 11. Prepare Data for Modeling  
**[ ] Phase 11 Complete**

### Tasks  
- [ ] Split into train/validation/test  
- [ ] Standardize/normalize features  
- [ ] Encode categorical variables  
- [ ] Eliminate target leakage  

### Deliverables  
- [ ] Model-ready dataset  
- [ ] Updated preprocessing script  

### Done When  
- Any model can be trained directly on the prepared dataset.

---

## 12. Train and Tune Models  
**[ ] Phase 12 Complete**

### Tasks  
- [ ] Train baseline models  
- [ ] Fit advanced models (tree-based, regularized, etc.)  
- [ ] Perform hyperparameter tuning  
- [ ] Document reasoning behind model choices  

### Deliverables  
- [ ] Training notebook  
- [ ] Saved model configurations (optional)  

### Done When  
- Models converge and behavior is well understood.

---

## 13. Evaluate Performance  
**[ ] Phase 13 Complete**

### Tasks  
- [ ] Compute RMSE, MAE, R²  
- [ ] Residual analysis  
- [ ] Assess generalization performance  
- [ ] Compare models fairly  

### Deliverables  
- [ ] Performance comparison tables  
- [ ] Evaluation plots  

### Done When  
- You can argue which model is best and why.

---

## 14. Visualize and Explain Models  
**[ ] Phase 14 Complete**

### Tasks  
- [ ] Plot feature importances  
- [ ] Generate partial dependence or SHAP values  
- [ ] Plot predictions vs. actual values  

### Deliverables  
- [ ] Model interpretability notebook  
- [ ] Exported interpretability visuals  

### Done When  
- Anyone can understand how the model arrives at its predictions.

---

## 15. Document and Make Reproducible  
**[ ] Phase 15 Complete**

### Tasks  
- [ ] Finalize README  
- [ ] Add complete instructions for running the project  
- [ ] Ensure notebooks are clean and well commented  
- [ ] Confirm scripts behave deterministically  

### Deliverables  
- [ ] Polished README  
- [ ] Documented notebooks  
- [ ] Clear project instructions  

### Done When  
- The entire project can be reproduced by someone else without help.

---

## 16. Review and Improve  
**[ ] Phase 16 Complete**

### Tasks  
- [ ] Review entire pipeline for consistency  
- [ ] Refine visuals and explanations  
- [ ] Identify improvements for future versions  

### Deliverables  
- [ ] Final polished version of the entire project  
- [ ] Optional portfolio summary  

### Done When  
- The project is ready to be presented professionally.

--x
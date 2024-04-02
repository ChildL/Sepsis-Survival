# Sepsis-Survival

Chicco,Davide and Jurman,Giuseppe. (2023). Sepsis Survival Minimal Clinical Records. UCI Machine Learning Repository. https://doi.org/10.24432/C53C8N.

Primary cohort and study cohort
We analyzed a dataset made of 110,204 admissions of 84,811 hospitalized subjects between 2011 and 2012 in Norway who were diagnosed with infections, systemic inflammatory response syndrome (SIRS), sepsis by causative microbes, or septic shock87. The data come from the Norwegian Patient Registry92 and the Statistics Norway agency93.

For each patient admission, the dataset contains sex, age, septic episode number, hospitalization outcome (survival), length of stay (LOS) in the hospital, and one or more codes of the International Classification of Diseases 10th revision (ICD-10) describing the patient’s disease (Table 1). Since the main goal of this study is to predict the survival of the patient, we discarded the length of stay because it strongly relates to the likelihood to survive: the longer the patient has to stay in the hospital, the less likely she/he will survive. The survival variable relates to the hospital length-of-stay, which ranges in the [0, 499] days interval and has mean of 9.351 days. Our prediction therefore refers to the likelihood of a patient to survive or decease in the 9.351 days after the collection of her/his medical record, in the hospital.

The admissions are of 57,973 of men and of 52,231 of women, ranging from 0 to 100 years of age (Table 2 and Table 3). Most of the admissions (76.96%) relate to the first septic episode. More information about the dataset can be found in the original study87.

The original dataset curators Knoop et al.87 called the complete dataset with 110,204 admissions the primary cohort. From the primary cohort, they selected the admissions respecting the Sepsis-3 definition of sepsis (at least one several infection or sepsis related ICD-10 code and at least one codes for acute organ dysfunction)9, and they called this subset the study cohort.

Since the data of the primary cohort were recorded before the Sepsis-3 definition emerged in 2016, we cannot know if a patient diagnosed with an ICD-10 code related to sepsis actually had an organ dysfunction afterwards. Therefore, we cannot know if these admissions can be considered related to sepsis by the current Sepsis-3 definition today. What we know, instead, is that the conditions of the primary cohort (infections, systemic inflammatory response syndrome (SIRS), sepsis by causative microbes, or septic shock) might have lead to sepsis. To reflect this information, we call these conditions sepsis potential preconditions in this study. We decided to consider both the primary cohort and the study cohort for our analysis because consensus on a unified definition of sepsis has not been reached by the medical community yet94.

We took the original dataset95 and applied the same selection, generating a study cohort having a different size from the one of Knoop et al.87: while their study cohort contained 18,460 admissions, our study cohort contains 19,051. We were unable to obtain the original study cohort subset from Knoop unfortunately.

Both the primary cohort and our study cohort are positively imbalanced (Table 2). The primary cohort contains 102,099 admissions of patients who survived (92.65% positives) and 8,105 admissions of patients who deceased (7.35% negatives). Our study cohort contains 15,445 admissions of patients who survived (81.07% positives) and 3,606 admissions of patients who deceased (18.93% negatives).

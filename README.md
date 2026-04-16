### Task: Automate the Prior Authorization (PA) Form Filling Workflow

---

### **Important Note:**
All forms, referral packages, and documents used in this interview process are **synthetically generated** for the purpose of this task. They do not contain real patient data or information and are purely fictional, ensuring compliance with privacy and confidentiality standards.

---

### **Purpose of this assignment**

This task is designed to assess the candidate's skills, creativity, and problem-solving abilities in a practical setting. Specifically, we are looking for:

1. The ability to quickly learn and adapt to domain knowledge (in this case, healthcare) from a new vertical.
2. Existing skills and knowledge in building multimodal ML pipelines.
3. The capacity to think outside of the box, discovering novel solutions when existing methods fall short.
4. The ability to effectively leverage existing resources, tools, and libraries to resolve challenges.
5. Strong fundamental coding skills, including clean, readable, and maintainable code.
6. Thoughtful handling of ambiguous or incomplete requirements, demonstrating sound judgment in decision-making.

### Background:

**Prior Authorization (PA)** is a process where healthcare providers must obtain approval from a health insurance plan before delivering a specific service (e.g., a drug infusion) to a patient. This process requires assembling evidence to demonstrate that the patient meets specific criteria, such as:

- **Severity of illness**  
- **Ineffectiveness of alternative treatments**

The process typically involves comparing two main documents:

1. **PA Form:**  
   A structured PDF form specific to a drug, containing fields for the required information needed for insurance approval.

2. **Supporting Documentation (Referral Package):**  
   A collection of scanned documents such as:
   - Insurance card  
   - Medical history notes  
   - Test results  
   These are combined into a single PDF, often sent via fax as high-resolution images.

After comparing the documents and confirming that all criteria are met, the PA request is submitted.

---

### Current Manual Workflow:

Currently, a human worker performs the following steps:

1. **Download the PA Form:**  
   Retrieve the specific drug's form from the insurance company's website.

2. **Review the Referral Package:**  
   Extract necessary information from the referral package to complete the PA form.

3. **Complete the PA Form:**  
   Fill in the required fields on the PA form using information from the referral package.

---

### Goal:

Develop a pipeline to automate this workflow.

- **Input:**  
  Pairs of PA forms and referral packages provided in the input data folder. Input data structure is as follow:

      📁 Input Data
        
          📁 Patient A
        
              📄 PA.pdf                   
        
              📄 referral_package.pdf     
        
          📁 Patient B
      
              📄 PA.pdf
        
              📄 referral_package.pdf
        
          📁 Patient C
        
              ...


- **Output:**  
  - For each of the patient, output a filled-out PA form (PDF format)


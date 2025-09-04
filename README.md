# 🧠 Neuroscientific Database – SQL Project
This repository contains a **database project** developed in Google Colab using **DuckDB**, as part of a university exam. The goal was to design, implement, and query a relational database for organizing neuroscientific studies that investigate the relationship between specific **brain areas** and **cognitive functions** using modern neuroimaging and stimulation techniques.

## 📌 Project Overview
The database was designed to store scientific studies that document experiments on how brain areas correlate with higher cognitive functions such as **memory, attention, language, emotions, and perception**.

Each study in the database includes:
* A unique **ID** and (when available) a **DOI**
* **Title** and **publication date**
* The **authors** involved (with optional **ORCID**)
* The **technique** used (e.g., fMRI, PET, EEG, MEG, TMS, tDCS, SSVEP…)
* The **functions** investigated and their associated **brain areas**

The project demonstrates the **full workflow**:
1. *Conceptual design* → entity-relationship model
2. *Logical design* → relational schema & constraints
3. *Implementation* → SQL queries
4. *Testing* → inserting data and running queries

## 🔑 Database Entities
* **Study** → represents a scientific article/experiment
* **Author** → researchers contributing to the study
* **Technique** → experimental method (fMRI, EEG, TMS, etc.)
* **Brain Function** → cognitive ability investigated (e.g., memory, attention, emotion regulation)
* **Brain Area** → anatomical structure responsible for functions (e.g., hippocampus, prefrontal cortex, amygdala)

## 🔗 Relationships
* A Study is written by *one or more* Authors
* A Study investigates *one or more* Brain Functions
* Each Brain Function corresponds to *one or more* Brain Areas
* A Study uses *one* primary Technique

> *You can find a detailed ER-Model and Relational Schema in 3rd Normal Form inside the Jupyter Notebook.*

## ⚙️ Example Operations
Some example queries implemented in the notebook include:
* Retrieve the most recent studies (with or without titles)
* Find all authors of a specific study
* List all studies an author has contributed to
* Count the number of authors per study
* Retrieve all studies investigating a given brain function
* Rank the most frequently used techniques
* List all brain areas associated with a given function

## 💻 Implementation
The database was implemented in DuckDB, which is based on PostgreSQL, although with some limitations. The project includes:
* **Table creation scripts** (with primary/foreign keys, unique constraints, and checks)
* **Data population with realistic examples** (studies, authors, techniques, brain areas)
* **Error handling examples** (e.g., FK violations, CHECK constraint failures)
* **Queries** demonstrating how to extract meaningful insights

## 🚀 How to Use
1. Open the provided Jupyter Notebook in Google Colab.
2. Make sure PostgreSQL is available in your environment.
3. Run the setup cells to create the schema and populate the database.
4. Explore the queries and modify them to test your own scenarios.

## 📚 Authors
Project developed by:
* [sandasirghe](https://github.com/sandasirghe)
* [letizia-z](https://github.com/letizia-z)

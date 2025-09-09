Donde estan los datos para el machine learning?
        el 80 porciento del trabajo dentro del machine learning es la preparacion de datos
        puedes apoyarte de dataset, y estos los puedes encontrar en kaggle, aws, google
        kaggle te ayuda a evaluar tu modelo

        Otra forma de obtener datos, es por medio del web scraping

Como deben ser los datos para trabajar con machine learning?
        Preparacion de los datos, considerar de donde se extraeran los datos
        Explorar los datos====>EDA

        Dataset<=====Training/Training,   debe estar organizado demanera que pueda entrenar al modelo y hacer las pruebas, buscando mantenerlo uniforme, para que al recibir datos nuevos que buscaran tener el mismo formato, poder evaluarlos correctamente

        Datos Estructurados:
                Numeros, Fehcas, etc, una tabla con datos para cada instancia
        Datos no estructurados: Archivos de texto, mails, archivos multimedia

        Es necesario hacer un preprocesamiento, Normalizacion, limpieza, estandarizarlo, pensar en como se interpretarian los datos y que tan fexlible se es su interpretacion

EDA
    <keyporpuses>
    * Detect errors and missing data - identify inconsistencies or anomalies
    * Understand patterns - distributions correlations, trends.
    * inform feature engineering - decide how to transform variables
    * Guide modeling choices- linear vs. nonlinear, scaling, encoding.
    <types of data>
    * Numerical(continuos or discrete)
    * Categorical(qualitative)
    * Time series- datetime
    * Text/Unstructured data
    <steps>
        1- Undestand your dataset
            * shape: number of columns and rows
            * Column names and data types
            * target variable(if supervised learning)
            ***Example***
            python
            import pandas as pd
            df = pd.read_csv("data.csv")
            print(df.shape)        # rows x columns
            print(df.info())       # data types & missing values
            print(df.head())       # first 5 rows
            *****************************
        2- Summarize data
            * Numerical data: mean, median,standart deviation, min, max, porcentile
            * Categorical Data: counts, mode unique values
            ***Example***
             print(df.describe())  # numerical summary
             print(df['category'].value_counts())  # categorical summary
        3- Handle missing values
            * Missing data can skew result
            * Common strategies: remove rows or columns, fill with mean median mode or use interpolation 
        4- Visualize data
            IS THE KEY IN EDA
            * Univariate analysis (single variable)
                Numerical: histogram, boxplot, density plot.
                Categorical: bar plot, pie chart.
            * Bivariate analysis (two variables)
                Numerical vs. numerical: scatter plot, correlation heatmap.
                Numerical vs. categorical: boxplot, violin plot.
                Categorical vs. categorical: stacked bar plot, mosaic plot.
            * Multivariate analysis
                Heatmaps, pairplots, dimensionality reduction (PCA).
        5- Detect outliers
            * Outliers can affect models.
            * Use boxplots, z-scores, IQR method.         
            * Decide whether to keep, transform, or remove them.
        6- Analize correlations and relationships
            * compute correlation matrices
            * Identify features that are strongly related to the target
            * helps in feature selection
        7- Feature engineering / Transformation
            * Transform skewed distribution (log,squareRoot)
            * Encode categorical variables (one-hot, label encoding)
            * Scale features if necessary
    <Tool>
        Python
            pandas - numpy - matplotlib -  missingno - seaborn
        R
            ggplot2 - dplyr - DataExplorer
    <Best Practices>
        1- Always start with EDA before modeling
        2- Document your findings - 
        3- Be careful with assumtions
        4- Visualixe early and often
        5- Treat outliers and missing values thoughfully
        6- Look for patterns, trends and anomalies
    <Key takeaways>
        * EDA is about understanding your data fully
        * it conbines stadistics, visualization and intuition
        * Proper EDA leads to better modeling, feature selection and insights.
        *Skipping EDA is one of the most common mistakes in ML proyects
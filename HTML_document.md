---
title: "MODULO1"
author: "Pedro González Beermann"
date: "02/13/2021"
output:
  html_document: 
    theme: yeti
    highlight: pygments
    fig_width: 6
    keep_md: yes
    toc: yes
    toc_float: yes
    number_sections: yes
---



# Análisis de Varianza (ANOVA)

## Introducción

En estadística, el análisis de la varianza (ANOVA por sus sigloides en inglés, ANalysis Of VAriance) es una colección de modelos estadísticos y sus procedimientos asociados, en el cual la varianza está particionada en ciertos componentes debidos a diferentes variables explicativas. Se utiliza de forma intensiva en el análisis y diseño de experimentos para evaluar el efecto de tratamientos en la variabilidad de la variable respuesta.

Desarrollada por el genetista R. A. Fisher en los años 1920 y 1930 y es algunas veces conocido como "Anova de Fisher" o "análisis de varianza de Fisher", debido al uso de la distribución F de Fisher como parte del contraste de hipótesis

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:


```r
plot(cars)
```

<img src="HTML_document_files/figure-html/cars-1.png" style="display: block; margin: auto;" />

## Including Plots

You can also embed plots, for example:

![](HTML_document_files/figure-html/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.

## Simple equation

$$ H_0:\mu_1 = \mu_2 = \mu_3 $$
$$ H_0:\mu_i \neq \mu_j~~~ \text{para cualquier } i \neq j $$

## Leer Datos


```r
df=read.csv("Genero.csv")
knitr::kable(df,caption="Efecto de la Temperatura según género")
```



Table: Efecto de la Temperatura según género

|Genero |  T|
|:------|--:|
|Mujer  | 75|
|Mujer  | 77|
|Mujer  | 78|
|Mujer  | 79|
|Mujer  | 77|
|Mujer  | 73|
|Mujer  | 78|
|Mujer  | 79|
|Hombre | 74|
|Hombre | 72|
|Hombre | 77|
|Hombre | 76|
|Hombre | 76|
|Hombre | 73|
|Hombre | 75|
|Hombre | 73|
|Hombre | 74|
|Hombre | 75|


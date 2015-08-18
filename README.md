# getting started with r markdown

### Indy useR Group
2015-08-18  

### Richard Layton     
Mechanical Engineering, Rose-Hulman Institute of Technology  
[graphdoctor@gmail.com](emailto:graphdoctor@gmail.com)  
[www.graphdoctor.com](http://www.graphdoctor.com)  
[github.com/graphdr](http://github.com/graphdr)  
&copy; 2015 Richard Layton except where noted.  





---   

## Why

Prose and executable code in the same text file. 

- HTML, PDF, or MS Word output  
- beamer, ioslides, and slidy presentations  
- tables and bibliographies  
- customizable  

Read more about R Markdown

- [rmarkdown.rstudio.com](http://rmarkdown.rstudio.com)  
- [online reference guide](https://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf)  






---

## Create an RStudio project

Create a new directory. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/visuals/new-project.PNG" width="300">

<br>
Open RStudio, create a new project.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/visuals/new-project-menu.PNG" width="300">

<br>
Assign the new project to the directory you just created.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/visuals/exist-directory-dialog.PNG" width="300">





---

## Create an Rmd report

From RStudio, create a new R Markdown file

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/visuals/newfile-rmarkdown.PNG" width="300">

<br>
Select HTML output (for now). We can change it later.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/visuals/new-rmarkdown-dialog.PNG" width="300">

<br>
An untitled R Markdown file is created with some default text and R code. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/visuals/untitled-rmd.PNG" width="600">

<br>
*File* -> *Save As* to the project directory with an Rmd suffix, for example, `test-report.Rmd`. 

<br>
Click `Knit HTML` to render the document in HTML. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/visuals/knit-html.PNG" width="600">

<br>
The report appears in your RStudio viewer. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/visuals/default-rmd-report.PNG" width="600">






---

## Compare the markup to the output

Compare the Rmd markup to the HTML output. For example, 

- markup  `<http://rmarkdown.rstudio.com>` creates a link,  <http://rmarkdown.rstudio.com>  
- markup `**Knit**` produces a bold typeface,  **Knit**  
- single backtick markup <code>&#96;</code> produces highlighted inline code, e.g., the markup  <code>&#96;echo=FALSE&#96;</code> produces `echo=FALSE` 

<br>
The code-chunk markup 

<pre class="r"><code>```{r}
summary(cars)
<code>```</code>
</code></pre>

echoes the R code in the HTML document, executes the *summary()* functions, and writes the result to the output. 

```{r}
summary(cars)
```

<br>
The next code chunk includes an `echo=FALSE` argument that prevents printing the R code chunk to the output. 

<pre class="r"><code>```{r, echo=FALSE}
plot(cars)
<code>```</code>
</code></pre>

<br>
However, the code is executed and the graph is printed to the output document,

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/visuals/plot-cars.PNG" width="600">






---

## What the software is doing

<img src="/visuals/rmd-to-html-process-4.PNG" width="500">

The resulting output file is placed in the same directory as your Rmd file.





---

## Changing the output format

The YAML header  or front-matter in the Rmd file controls how the file is rendered. (YAML: YAML Ain't Markup Language)

<pre class="r"><code>---
title: "Untitled"
author: "Richard Layton"
date: "August 14, 2015"
output: html_document
---</code></pre>

Let's change the title to *Test Report*.

<pre class="r"><code>title: "Test Report"
</code></pre>

The `output:` option recognizes three document types:

- html_document  
- pdf_document  
- word_document  

You can type these directly in the Rmd YAML header or you can use the RStudio `Knit` pulldown menu

<img src="/visuals/knit-to-pdf.PNG" width="250">

`Knit HTML` produces 

<img src="/visuals/output-html.png" width="600">

`Knit PDF` produces  (requires TeX)

<img src="/visuals/output-pdf.png" width="600">

`Knit WORD` produces  (requires Word)

<img src="/visuals/output-word.png" width="600">




---

## Formatting the output

Articles on the RStudio website for formatting output. 

- [Formatting an HTML document](http://rmarkdown.rstudio.com/html_document_format.html)
- [Formatting a PDF document](http://rmarkdown.rstudio.com/pdf_document_format.html)
- [Formatting a Word document](http://rmarkdown.rstudio.com/articles_docx.html)





---

## Markdown basics

### Section headings

<img src="/visuals/markup-output-sections.PNG" width="600">

### Emphasis

<img src="/visuals/markup-output-emphasis.PNG" width="600">

### Itemize 

Sub-items begin with 4 spaces.   
Every line ends with two spaces.  

<img src="/visuals/markup-output-itemize.PNG" width="600">

### Enumerate     

Sub-items begin with 4 spaces.   
Every line ends with two spaces.  

<img src="/visuals/markup-output-enumerate.PNG" width="600">

### Links

<img src="/visuals/markup-output-links.PNG" width="600">


### Images


<img src="/visuals/markup-output-images.PNG" width="600">




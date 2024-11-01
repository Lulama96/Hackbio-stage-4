Author: Lulama Mthethwa

Dashboard link: [https://lulama.shinyapps.io/Enrichment-Analysis/](https://lulama.shinyapps.io/Enrichment-Analysis/)

The Enrichment Analysis dashboard is an interactive tool designed to facilitate functional enrichment analysis for gene sets. This app allows users to input a list of genes and perform enrichment analysis to understand the biological processes, molecular functions, cellular components, and pathway terms associated with the genes. By leveraging the TCGAbiolinks package, the app automates gene set enrichment, typically used to identify significant associations in complex biological data.

The app’s layout consists of a clean and straightforward user interface (UI) with a sidebar for input and a main panel for visualizing results. Users paste their gene list into the provided text area input box, with each gene separated by commas. After pasting their list, users click the  Run Enrichment Analysis button, which triggers the backend process. This list is converted into a format compatible with the TCGAanalyze\_EAcomplete function, which performs the enrichment analysis based on the specified genes.

The app's server-side processing utilizes the TCGAanalyze\_EAcomplete function to analyze the gene list. This function provides results across four categories: Molecular Function (MF), Biological Process (BP), Cellular Component (CC), and Pathway Terms. The results are stored in a reactive object, which is later accessed to render a bar plot summarizing the significant terms for each category.

In the main panel, users see a plot generated by TCGAvisualize\_EAbarplot, displaying the top ten terms for each category. This visualization makes it easy for researchers to interpret the enrichment results at a glance, as each category is assigned distinct colors for clarity. The plot layout is organized into a 2x2 grid, showing one plot per category, which allows quick insights into the biological relevance of the gene set.

This dashboard is valuable for researchers exploring gene functions, as it provides a user-friendly and automated approach to functional enrichment analysis. By integrating well-established functions from TCGAbiolinks and adding an intuitive UI, the app simplifies what would otherwise be a complex, multi-step process.
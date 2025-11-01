# Quantitative Genetics Graduate Education Module (GEM)

[![Publish Quarto Book](https://github.com/wcresko/UO_Quant_Gen_Text/actions/workflows/quarto-publish.yml/badge.svg)](https://github.com/wcresko/UO_Quant_Gen_Text/actions/workflows/quarto-publish.yml)

Course materials for the **Quantitative Genetics Graduate Education Module** taught by Dr. William A. Cresko at the University of Oregon (Spring 2023).

## 📖 View the Book

The published book is available at: [https://wcresko.github.io/UO_Quant_Gen_Text/](https://wcresko.github.io/UO_Quant_Gen_Text/)

## 🛠️ Building the Book

This book is built using [Quarto](https://quarto.org/), an open-source scientific and technical publishing system.

### Prerequisites

- **Quarto** (>= 1.4) - [Download and install Quarto](https://quarto.org/docs/get-started/)
- **R** (>= 4.0) - [Download R](https://www.r-project.org/)
- **RStudio** (recommended) - [Download RStudio](https://posit.co/download/rstudio-desktop/)

### Installing R Dependencies

```r
install.packages(c("knitr", "rmarkdown", "bookdown"))
```

### Building Locally

#### Using Command Line

```bash
# Render the entire book (creates HTML, PDF, and EPUB)
quarto render

# Render only HTML
quarto render --to html

# Render only PDF
quarto render --to pdf

# Preview the book with live reload
quarto preview
```

#### Using RStudio

1. Open the `Quan_Gen.Rproj` file in RStudio
2. Open any `.qmd` file
3. Click the "Render" button or use the "Build" pane

### Output

All rendered files will be placed in the `docs/` directory, which is used for GitHub Pages deployment.

## 📂 Repository Structure

```
.
├── index.qmd                 # Book homepage and overview
├── 01-syllabus.qmd          # Course syllabus
├── 02-schedule.qmd          # Course schedule
├── 03-background.qmd        # Background material
├── 04-data_organization.qmd # Data organization
├── 05-R_introduction.qmd    # Introduction to R
├── 06-R_morefunc_dfs_plot.qmd # More R functions
├── 07-Rmarkdown.qmd         # R Markdown introduction
├── 08-probability_probdists.qmd # Probability & distributions
├── 09-correlation_regression.qmd # Correlation & regression
├── 10-ANOVA_intro.qmd       # ANOVA introduction
├── 21-references.qmd        # References
├── TEMP_CHAPTERS/           # Work-in-progress chapters
├── images/                  # Educational imagery and diagrams
├── _quarto.yml             # Quarto configuration
├── book.bib                # Bibliography
├── packages.bib            # R package citations
├── style.css               # Custom styling
└── preamble.tex            # LaTeX preamble for PDF output
```

## 🚀 Deployment

The book is automatically built and deployed to GitHub Pages using GitHub Actions whenever changes are pushed to the `main` or `master` branch.

### GitHub Pages Setup

1. Go to your repository **Settings** → **Pages**
2. Under **Source**, select:
   - **Branch**: `gh-pages`
   - **Folder**: `/ (root)`
3. Save the settings

The GitHub Actions workflow (`.github/workflows/quarto-publish.yml`) will automatically:
- Build the Quarto book on every push
- Deploy the rendered content to the `gh-pages` branch
- Make it available at your GitHub Pages URL

## 📝 Content Development

### Converting Chapters from Bookdown

This repository was converted from bookdown to Quarto. The main changes:
- `.Rmd` files → `.qmd` files (Quarto markdown)
- `_bookdown.yml` → `_quarto.yml`
- All image paths use relative references (`images/filename.png`)

### Adding New Chapters

1. Create a new `.qmd` file with a numbered prefix (e.g., `11-new-chapter.qmd`)
2. Add the file to the `chapters` list in `_quarto.yml`:
   ```yaml
   chapters:
     - index.qmd
     - 01-syllabus.qmd
     # ... existing chapters ...
     - 11-new-chapter.qmd  # Add your chapter here
   ```
3. Write your content using Quarto markdown syntax
4. Build and preview locally before committing

### Work-in-Progress Chapters

The `TEMP_CHAPTERS/` directory contains chapters that are still being developed:
- `08-parameter_est.qmd` - Parameter estimation
- `09-experimental_design.qmd` - Experimental design
- `10-hypothesis_tests.qmd` - Hypothesis testing
- `13-frequency_analysis.qmd` - Frequency analysis
- `15-phenotypes_values.qmd` - Phenotypes and values
- `16-variance_heritability.qmd` - Variance and heritability

## 📚 Course Information

**Course**: Quantitative Genetics GEM
**Institution**: University of Oregon
**Instructor**: Dr. William A. Cresko
**Term**: Spring 2023

## 📄 License

[CC0 1.0 Universal (Public Domain)](LICENSE)

This work is dedicated to the public domain under the CC0 1.0 Universal license. You are free to use, modify, and distribute this material without restriction.

## 🤝 Contributing

This repository contains course materials for the Spring 2023 term. If you find errors or have suggestions for improvements:

1. Open an [Issue](https://github.com/wcresko/UO_Quant_Gen_Text/issues)
2. Submit a Pull Request with your proposed changes

## 📧 Contact

For questions about the course or materials, please contact Dr. William A. Cresko at the University of Oregon.

---

**Built with [Quarto](https://quarto.org/)** - An open-source scientific and technical publishing system
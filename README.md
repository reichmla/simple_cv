# Simple CV - LaTeX Template

A clean, professional LaTeX template for creating curriculum vitae (CV) documents. This template is based on the Curve CV template by LianTze Lim and has been customized for professional use.

## Features

- **Clean Design**: Professional layout with customizable colors and fonts
- **Modular Structure**: Organized into separate sections for easy maintenance
- **Profile Photo Support**: Optional profile picture integration
- **Contact Information**: Prominent display of contact details with icons
- **Section-based Organization**: Personal, Education, Employment, Certifications, and Skills sections
- **Responsive Layout**: Optimized for A4 paper format
- **Font Awesome Icons**: Professional icons for contact information and sections

## Project Structure

```
simple_cv/
├── simple_cv.tex          # Main LaTeX document
├── settings.sty           # Style definitions and packages
├── sections/              # CV content sections
│   ├── personal.tex       # Personal information
│   ├── education.tex      # Educational background
│   ├── employment.tex     # Work experience
│   ├── certifications.tex # Professional certifications
│   └── skills.tex         # Skills and competencies
├── img/                   # Images directory
│   └── bnuyy.jpeg         # Profile photo
└── simple_cv.pdf          # Generated PDF output
```

## Prerequisites

To compile this LaTeX document, you need:

- **LaTeX Distribution**: TeX Live, MiKTeX, or MacTeX
- **Required Packages**:
  - `curve` document class
  - `fontawesome5` for icons
  - `biblatex` for bibliography (optional)
  - `tcolorbox` for styling
  - `tikz` for graphics
  - `geometry` for page layout
  - `hyperref` for links

## Installation

1. **Clone or download** this repository
2. **Install LaTeX** if you haven't already:
   - **macOS**: Install MacTeX
   - **Windows**: Install MiKTeX or TeX Live
   - **Linux**: Install TeX Live via package manager

3. **Install required packages** (if not already included):
   ```bash
   # For TeX Live
   tlmgr install curve fontawesome5 biblatex tcolorbox tikz geometry hyperref
   ```

## Usage

### Basic Compilation

```bash
# Compile the main document
pdflatex simple_cv.tex

# If using bibliography (optional)
pdflatex simple_cv.tex
biber simple_cv
pdflatex simple_cv.tex
```

### Customization

#### 1. Personal Information
Edit `sections/personal.tex` to update your personal details:
```latex
\entry*[Address]%
    Your Address Here
\entry*[Birth date]%
    Your Birth Date, Location
```

#### 2. Contact Information
Update the header in `simple_cv.tex`:
```latex
\leftheader{%
    \faLinkedin {\href{https://www.linkedin.com/in/yourprofile/}{in/yourprofile}} \hfill 
    \faEnvelope[regular] {\href{mailto:your.email@example.com}{your.email@example.com}} \hfill 
    \faIcon{mobile-alt} {\href{tel:+123456789}{+123456789}} \par
    \vspace{0.4cm}
    {\LARGE\bfseries\sffamily Your Name} \par
    \vspace{0.05cm}
    \vspace{0.2cm}
    \textcolor{TextColor}{Your professional summary here.}
}
```

#### 3. Profile Photo
- Place your photo in the `img/` directory
- Update the photo path in `simple_cv.tex`:
  ```latex
  \photo[r]{img/your-photo-name}
  ```

#### 4. Colors and Styling
Modify colors in `simple_cv.tex`:
```latex
\definecolor{BackgroundColor}{HTML}{f2f3f5}
\definecolor{TextColor}{HTML}{6C6C6C}
\definecolor{RubricTextColor}{HTML}{000080}
```

#### 5. Content Sections
Edit the respective `.tex` files in the `sections/` directory:
- `education.tex` - Add your educational background
- `employment.tex` - Add your work experience
- `certifications.tex` - Add professional certifications
- `skills.tex` - Add your skills and competencies

More sections can be added though.

## License

This template is based on the Curve CV template by LianTze Lim, available under the Creative Commons Attribution 4.0 License. The original template can be found at: https://www.overleaf.com/latex/templates/a-customised-curve-cv/mvmbhkwsnmwv

## Contributing

Feel free to fork this repository and submit pull requests for improvements. Suggestions for new features or bug fixes are welcome!

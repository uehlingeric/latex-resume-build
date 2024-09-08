# ResumeBuild

## Overview

The **ResumeBuild** project is a LaTeX-based resume template filled with actual resume details. It is designed to generate a well-structured and professional resume in PDF format. The project is intended to be used with **Visual Studio Code (VSCode)** and the **LaTeX Workshop** extension, alongside required dependencies such as **Perl** and LaTeX distributions, to compile the LaTeX code into a PDF.

This guide provides instructions on how to set up the environment, install necessary tools, and compile the resume using LaTeX in VSCode.

## Project Structure

- `resume.cls` – LaTeX class file for resume formatting
- `resume.pdf` – Generated PDF output
- `resume.tex` – Main LaTeX file for the resume
- `sections/` – Directory containing resume sections:
  - `certifications.tex`
  - `education.tex`
  - `professional_experience.tex`
  - `skills.tex`

## Requirements

### Tools

- **Visual Studio Code**: An IDE to edit the LaTeX files and manage the project.
- **LaTeX Workshop extension for VSCode**: Handles LaTeX compilation and preview directly in VSCode.
- **Perl**: A scripting language required for specific LaTeX distributions and the LaTeX Workshop extension.
- **LaTeX distribution**: Required for compiling `.tex` files into `.pdf` (e.g., TeX Live, MiKTeX).

## Setting Up the Environment

### Step 1: Install LaTeX Workshop Extension

1. Open **Visual Studio Code**.
2. Go to the **Extensions** view by clicking the Extensions icon on the sidebar or pressing `Ctrl+Shift+X`.
3. In the search bar, type "**LaTeX Workshop**".
4. Click the **Install** button next to the **LaTeX Workshop** extension by James Yu.

This extension will provide LaTeX support in VSCode, including live preview, compilation, and syntax highlighting.

### Step 2: Install LaTeX Distribution

To compile LaTeX files, you'll need a LaTeX distribution installed on your machine.

- **Windows**: Install [MiKTeX](https://miktex.org/download).
- **macOS**: Install [MacTeX](http://www.tug.org/mactex/).
- **Linux**: Install TeX Live using your package manager (e.g., `sudo apt-get install texlive-full`).

Ensure that the LaTeX distribution's executables (e.g., `pdflatex`, `xelatex`) are added to your system's PATH, so that VSCode can call them for compiling `.tex` files.

### Step 3: Install Perl

Perl is required for some LaTeX package functionalities, especially for handling `latexmk`, which automates the LaTeX compilation process. 

- **Windows**: Download and install Perl from [Strawberry Perl](https://strawberryperl.com/).
- **macOS**: Perl is pre-installed on macOS.
- **Linux**: Perl is usually pre-installed on most distributions, but you can install it using your package manager if necessary (e.g., `sudo apt-get install perl`).

### Step 4: Configure LaTeX Workshop

LaTeX Workshop provides an integrated environment to compile and view LaTeX documents. After installing the extension, make sure it's configured to use the correct LaTeX distribution.

1. Open VSCode.
2. Go to **Settings** (`File > Preferences > Settings` or press `Ctrl+,`).
3. Search for "**latex-workshop**" to configure the extension.
4. Verify that the correct LaTeX compiler (such as `xelatex` or `pdflatex`) is set in the LaTeX Workshop settings:
   - `"latex-workshop.latex.tools"` should list your LaTeX executables.
   - `"latex-workshop.latex.recipes"` should include your preferred compilation method, such as `pdflatex` or `xelatex`.

### Step 5: Compile Your Resume

Once you have LaTeX Workshop and the LaTeX distribution set up, follow these steps to compile your resume:

1. Open **`resume.tex`** in VSCode.
2. LaTeX Workshop will automatically detect the `.tex` file.
3. Press `Ctrl+Alt+B` to build the LaTeX project. This will run the LaTeX compiler and produce the PDF output.
4. The PDF preview will be available in the **LaTeX Workshop Preview** pane.

## File Customization

- Modify the **`resume.tex`** file to update sections of the resume with your own details.
- Modify individual sections such as:
  - **`sections/certifications.tex`**
  - **`sections/education.tex`**
  - **`sections/professional_experience.tex`**
  - **`sections/skills.tex`**

  These can be customized and extended as needed.

## Author

Eric Uehling

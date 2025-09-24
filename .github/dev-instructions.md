# Copilot Instructions for LearnThroughTextbooks

This project is a LaTeX-based chemistry textbook Q&A and answer key, with supporting assets and formatting tools. It is primarily used for generating and maintaining high-quality, typeset answer documents for Chinese high school chemistry (有机化学基础).

## Project Structure
- `opt3/` — Main working directory for the current textbook and answer key
  - `选必三过教材 参考答案.tex` — Main LaTeX source for the answer key
  - `选必三过教材 参考答案.pdf` — Compiled output (do not edit directly)
  - `assists/` — Image assets (referenced in LaTeX via `\includegraphics`)
  - `普通高中教科书·化学选择性必修3 有机化学基础.pdf` — Source textbook (reference only)
  - `过教材  选择性必修三 有机化学基础.docx` — Editable source (not directly processed by LaTeX)
- `tool/Fomatter.html` — Web tool for converting text blanks to LaTeX `\blank` commands

## Key Workflows
- **Edit LaTeX**: Make all answer/document changes in `选必三过教材 参考答案.tex`.
- **Compile**: Use XeLaTeX or a compatible LaTeX engine with Chinese support (e.g., `ctexart` class, `polyglossia`).
- **Image Assets**: Place images in `assists/` and reference with relative paths in LaTeX.
- **Blank Formatting**: Use the web tool in `tool/Fomatter.html` to convert text with blanks to LaTeX `\blank` format for consistency.

## Conventions & Patterns
- Use `\blank` for fill-in-the-blank questions (see macro in `.tex` file).
- Use `\begin{answer}...\end{answer}` for answer sections.
- Use `\includegraphics` for images, always from `assists/`.
- Macros for formatting (仿宋, 圈圈数字, 罗马数字等) are defined at the top of the `.tex` file—reuse these for consistency.
- Do not edit PDF, DOCX, or auxiliary files directly.

## Tips for AI Agents
- Always check for and reuse existing LaTeX macros.
- When adding new images, update both the `assists/` folder and the LaTeX references.
- For new question types, follow the structure and style of existing exercises and answers.
- If automating blank conversion, use or extend the logic in `Fomatter.html`.

## Example: Adding a New Question
1. Add a new `\begin{exercise}...\end{exercise}` block in the `.tex` file.
2. Use `\blank` for blanks, and `\begin{answer}...\end{answer}` for answers.
3. Reference any images from `assists/` using `\includegraphics[width=...]`.

---
For further conventions, review the top of `选必三过教材 参考答案.tex` for macro definitions and usage patterns.

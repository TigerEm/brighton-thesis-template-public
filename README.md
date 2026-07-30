# Unofficial University of Brighton LaTeX thesis template

> **Status:** This is an independent, unofficial template. It has not been
> endorsed, checked or approved by the University of Brighton. It implements
> the requirements supplied from *University of Brighton: Regulations for
> Research Degrees 2025–26*, principally pages 38–39. Candidates must compare
> the finished thesis with the complete regulations and current advice from
> the Doctoral College before submission.

The supplied thesis title, *Osteoarthritis Imaging in the Stone Age: An
Investigation Using Prehistoric Scanning Methods*, and the candidate name
`A. N. Example` are deliberately fictional. They must not be interpreted as
real research or personal information.

## Exactly what typesetting is included

The template currently includes the following typesetting and document
behaviour. Features not listed here should not be assumed.

1. A4 paper using the `book` document class.
2. A 12-point main-text base size.
3. Arial as the first-choice main font.
4. Helvetica as the second-choice fallback.
5. Times New Roman as the third-choice fallback.
6. DejaVu Sans as the final compatibility fallback.
7. A 40 mm left binding margin.
8. A 20 mm right margin.
9. A 20 mm top margin.
10. A 20 mm bottom margin.
11. One-and-a-half spacing in ordinary thesis text.
12. Single spacing in indented quotations.
13. Single spacing in long tables.
14. Single spacing in the reference list.
15. Flush-left paragraphs.
16. Additional vertical space between paragraphs.
17. No ordinary first-line paragraph indentation.
18. Ragged-right text rather than forced right justification.
19. Strong suppression of end-of-line word division.
20. Left-aligned chapter, section, subsection and subsubsection headings.
21. Automatic numbered chapters.
22. Automatic heading numbering through subsubsection, such as `1.2.3.4`.
23. A table of contents displaying chapters, sections and subsections.
24. An automatic list of tables.
25. An automatic list of figures.
26. Arabic page numbering.
27. A title page counted in the sequence but carrying no printed number.
28. A compact title page based on the supplied Brighton specimen.
29. Horizontal rules above and below the central title-page information.
30. Fields for thesis title, candidate, degree, approval month and year.
31. An optional collaborating-establishment field.
32. Bottom-centred formal page numbers.
33. Optional 9-point main-matter running headings containing candidate name,
    submission year and page.
34. Suppression of running headings in the title page, front matter and
    back matter.
35. Table numbers and captions above tables.
36. Figure numbers and captions below figures.
37. Standard tables using `booktabs`.
38. Multi-page tables with repeating column headings using `longtable`.
39. Figures and subfigures.
40. Mathematical notation and numbered equations.
41. Labels, automatic cross-references and PDF hyperlinks.
42. Bullet, numbered and description lists.
43. Indented quotations.
44. Footnotes.
45. Endnote markers and a printable endnotes section.
46. Abstract, contents, lists, acronyms, preface, acknowledgements and
    declaration front-matter examples.
47. Glossary, list of references, optional bibliography and appendices.
48. One source file per chapter, included by `main.tex`.
49. Selective chapter compilation using `\includeonly`.
50. `biblatex` and Biber bibliography processing.
51. A custom approximation of Cite Them Right Harvard, 13th edition.
52. Zotero/Better BibLaTeX-compatible `references.bib` input.
53. Author–date parenthetical and narrative citations.
54. Alphabetical author–year reference-list sorting.
55. Worked examples of prose, four heading levels, lists, two figures, a
    standard table, a multi-page table, equations, quotations, citations,
    cross-references, a footnote and an endnote.

### Title-size caution

The supplied specimen visually uses a compact title, and that is the version
implemented here. The accompanying written instruction appears to mention at
least 24-point type. Because those sources may be interpreted differently,
confirm the required title size with the Doctoral College before submission.

## Quick start

QUICK START - WHAT TO OPEN

Open and compile main.tex in TeXworks. The thesis is deliberately split across
several .tex files:

    main.tex
        The master file. It loads the stylesheet, stores the thesis title and
        candidate details, and lists the files in their final reading order.

    brightonthesis.sty
        The one central stylesheet. Change University-wide presentation rules
        here, not in each chapter.

    chapters/06-formatting-showcase.tex
        A deliberately detailed demonstration chapter. Open this file to copy
        working examples of headings, prose, lists, figures, a table, an
        equation, a quotation, a footnote and an endnote.

Compile main.tex even when editing a chapter. Individual chapter files are
components and are not intended to compile by themselves.

WHERE TO SEE EACH FEATURE

    Feature                         Source file
    -----------------------------------------------------------------------
    Running name/year/page header   main.tex and brightonthesis.sty
    Heading 1.2.3                   chapters/01-introduction.tex
    Deep heading 1.2.1.3            chapters/01-introduction.tex
    Full heading hierarchy          chapters/06-formatting-showcase.tex
    Bullet points                   chapters/06-formatting-showcase.tex
    Numbered list                   chapters/06-formatting-showcase.tex
    Labelled description list       chapters/06-formatting-showcase.tex
    Two example figures             chapters/06-formatting-showcase.tex
    External-figure instructions    README.md, ADDING AN EXTERNAL FIGURE
    Standard table                  chapters/06-formatting-showcase.tex
    Multi-page table                chapters/02-methods.tex
    Equation and quotation          chapters/06-formatting-showcase.tex
    Footnote                        chapters/06-formatting-showcase.tex
    Endnote marker                  chapters/06-formatting-showcase.tex
    Printed endnotes                backmatter/endnotes.tex

The formatting-showcase chapter is included near the end of the main text so
all examples can be viewed in the supplied PDF. When you no longer need it,
comment out this line in main.tex:

    % \include{chapters/06-formatting-showcase}

PROJECT STRUCTURE

main.tex
    Controls the order of the thesis and contains your personal details.

brightonthesis.sty
    The single central stylesheet. Change fonts, margins, spacing, headings,
    page numbers, captions and title-page layout here.

frontmatter/
    One file for each required front section.

chapters/
    One file for each chapter. Add further files and matching \include lines
    in main.tex as the thesis grows. The supplied formatting-showcase chapter
    is a practical source of examples and can later be removed.

backmatter/
    Glossary, list of references and optional bibliography.

appendices/
    One file per appendix.

references.bib
    The reference database used by biblatex and Biber.

TEXWORKS

1. Extract the complete ZIP into one folder.
2. Open main.tex. Do not compile an individual chapter file.
3. Select XeLaTeX and typeset.
4. For the bibliography run:

       XeLaTeX
       Biber
       XeLaTeX
       XeLaTeX

The thesis uses a 12-point base font. The stylesheet selects the first
available approved font in this order: Arial, Helvetica, Times New Roman.
If none is installed, DejaVu Sans is used as a final compatibility fallback
so that the document can still compile.

RUNNING HEADINGS

The example enables optional running headings with:

    \usepackage[runningheads]{brightonthesis}

They appear only over the main numbered chapters and show:

    candidate name       submission year          page number

They use 9-point type, smaller than the 12-point main text. The title page,
front matter and end matter do not have a running heading. The formal page
number remains at the bottom centre, as required by the pagination guidance.

The option is already enabled in the supplied main.tex, so the compiled example
shows the running header on every numbered chapter page:

    A. N. Example       Submission 2026              Page 12

Edit \authorname and \submissionyear near the top of main.tex; the header
changes automatically throughout the main text.

To disable them, change the line in main.tex to:

    \usepackage{brightonthesis}

With running headings disabled, only the bottom-centred page number remains.

COMPILE ONLY SELECTED CHAPTERS

While editing a long thesis, remove the percent sign from the \includeonly
example in main.tex and list the chapters you want to compile. LaTeX preserves
their chapter and page numbering from the last full compilation.

FUTURE REQUIREMENT CHANGES

Edit brightonthesis.sty. The major settings are grouped and labelled:

    FONT
    PAGE AND MARGINS
    PARAGRAPHS AND LINE SPACING
    HEADINGS
    PAGE NUMBERS
    TABLES AND FIGURES
    BIBLIOGRAPHY
    TITLE PAGE

Do not copy formatting commands into individual chapter files.

AUTOMATIC CONTENTS, TABLES AND FIGURES

Use the standard heading commands. LaTeX generates the numbers and table of
contents automatically:

    \chapter{Introduction}                 produces Chapter 1
    \section{Rationale}                    produces 1.2
    \subsection{Clinical context}          produces 1.2.1
    \subsubsection{Compositional imaging}  produces 1.2.1.1

The exact numbers depend on where a heading occurs. Do not type heading numbers
yourself. This template displays and numbers down to \subsubsection. See
chapters/01-introduction.tex for visible headings numbered 1.2.3 and 1.2.1.3.

Place every table or figure inside its environment and give it a caption:

    \caption{Descriptive title}
    \label{tab:short-name}

or:

    \caption{Descriptive title}
    \label{fig:short-name}

Refer to it with \ref:

    Table~\ref{tab:short-name}
    Figure~\ref{fig:short-name}

LaTeX generates the number, caption, list entry and cross-reference. Compile
XeLaTeX twice after changes so all lists and references are updated.

ADDING ORDINARY TEXT

Write paragraphs as plain text. Leave one completely blank source line between
paragraphs:

    This is the first paragraph. LaTeX wraps the text automatically.

    This is the next paragraph. The stylesheet controls spacing, margins,
    alignment and the 12-point font.

Useful inline formatting includes:

    \emph{emphasised text}
    \textbf{bold text}
    \texttt{computer code or a filename}

Do not insert manual line breaks at the end of each displayed line. Let LaTeX
wrap prose to the available width.

BULLET POINTS AND NUMBERED LISTS

For bullet points:

    \begin{itemize}
      \item First point.
      \item Second point with a little more explanation.
      \item Third point.
    \end{itemize}

For a numbered sequence:

    \begin{enumerate}
      \item First stage.
      \item Second stage.
      \item Third stage.
    \end{enumerate}

For labelled definitions or objectives:

    \begin{description}
      \item[Objective 1] Describe the first objective.
      \item[Objective 2] Describe the second objective.
    \end{description}

All three formats can be seen in chapters/01-introduction.tex.

ADDING A QUOTATION

The provided quotation environment uses the permitted single spacing:

    \begin{brightonquotation}
    Insert the quotation here and add its citation.
    \end{brightonquotation}

ADDING AN EQUATION

    \begin{equation}
      Y = \beta_0 + \beta_1 X + \varepsilon
      \label{eq:example}
    \end{equation}

Refer to it later as Equation~\ref{eq:example}. Examples appear in Chapters 1
and 2.

ADDING A NEW CHAPTER

1. Create a file such as:

       chapters/06-systematic-review.tex

2. Begin it with:

       \chapter{Systematic Review}
       \label{chap:systematic-review}

3. Add this in the required position in main.tex:

       \include{chapters/06-systematic-review}

Do not add \documentclass, \usepackage, \begin{document} or \end{document} to a
chapter file.

ADDING HEADINGS

Use heading commands without numbers:

    \chapter{Methods}
    \label{chap:methods}

    \section{Study design}
    \label{sec:study-design}

    \subsection{Eligibility}
    \label{sec:eligibility}

    \subsubsection{Recruitment pathway}
    \label{sec:recruitment}

LaTeX creates numbers such as Chapter 2, 2.1, 2.1.1 and 2.1.1.1. If you add,
remove or move headings, compile main.tex twice to refresh the numbering and
table of contents. Labels are optional unless you need to refer to the heading.

ADDING AND EDITING PARAGRAPHS

The following source creates two paragraphs:

    Osteoarthritis affects the whole joint. This paragraph can continue for
    many source lines; LaTeX decides where each printed line should end.

    A blank source line starts this second paragraph. Do not use repeated
    spaces or repeated \\ commands to position ordinary prose.

The template uses flush-left paragraphs with visible space between them. That
choice is set once in brightonthesis.sty. To change later to indented paragraphs
with no extra space, edit these two central settings:

    \setlength{\parindent}{0pt}
    \setlength{\parskip}{0.75\baselineskip}

Do not put those settings in individual chapter files.

ADDING A TABLE

    \begin{table}[htbp]
      \caption{Participant characteristics}
      \label{tab:participants}
      \centering
      \begin{tabular}{lcc}
        \toprule
        Measure & Group A & Group B \\
        \midrule
        Age & 55 & 57 \\
        Pain score & 4.1 & 3.8 \\
        \bottomrule
      \end{tabular}
    \end{table}

Refer to it later with:

    Table~\ref{tab:participants}

For a table extending over several pages, copy the longtable example from
chapters/02-methods.tex. Its column headings repeat on each page.

ADDING AN EXTERNAL FIGURE

Create a figures folder in the project and place the image there. PDF is best
for vector diagrams; PNG or high-quality JPEG can be used for raster images.

    \begin{figure}[htbp]
      \centering
      \includegraphics[width=0.8\textwidth]{figures/example-image.pdf}
      \caption{Description of the figure}
      \label{fig:example-image}
    \end{figure}

Refer to it with:

    Figure~\ref{fig:example-image}

The example chapters also show figures drawn directly in LaTeX and a
multi-panel figure. In particular:

    Figure 1.1 is a simple pathway diagram.
    Figure 1.2 is a vector diagram of cartilage zones.
    Figure 3.1 is a participant-flow diagram.
    Figure 3.2 is a two-panel figure.

These demonstrate numbering, captions below figures, labels, cross-references
and automatic entries in the list of figures.

FOOTNOTES

Insert a footnote at the relevant point:

    Main sentence.\footnote{The explanatory footnote text.}

Footnotes are numbered automatically and appear at the bottom of the page in
smaller, single-spaced type. A visible example is included near the beginning
of Chapter 1.

ENDNOTES

Insert an endnote at the relevant point:

    Main sentence.\endnote{The additional endnote text.}

All endnotes are collected automatically in backmatter/endnotes.tex. Keep its
\include line after \brightonfrontmatterstyle in main.tex. A visible example is
called from Chapter 4 and printed in the Endnotes section.

IMPORTANT: an endnote does not appear at the bottom of the page containing its
marker. Its superscript number points to the separate Endnotes section near the
end of the thesis. In the supplied example, two entries are printed there.

Always compile main.tex rather than an individual chapter. If an endnote has
just been added and does not appear immediately, run XeLaTeX again. The
endnotes package writes the generated entries to main.ent and reads them into
backmatter/endnotes.tex.

LABELS AND CROSS-REFERENCES

Use a unique label immediately after the relevant heading or caption:

    \label{chap:introduction}
    \label{sec:eligibility}
    \label{tab:baseline}
    \label{fig:participant-flow}
    \label{eq:analysis-model}

Use \ref to retrieve the current number. LaTeX updates references if chapters,
tables or figures move.

BIBLIOGRAPHY AND ZOTERO

REFERENCING STYLE

The central stylesheet is configured for Cite Them Right Harvard, 13th
edition. The configuration is in the labelled BIBLIOGRAPHY block in
brightonthesis.sty. It uses biblatex's maintained authoryear foundation plus
the principal Cite Them Right conventions:

    author and year separated by a comma in parenthetical citations;
    "and" rather than an ampersand between authors;
    et al. for four or more authors in text;
    author initials and alphabetical ordering in the reference list;
    quotation marks around journal-article and book-chapter titles;
    no place of publication for books; and
    "Available at:" and long British access-date presentation online.

Cite Them Right has no official biblatex package, so unusual source types
should be checked against the current Cite Them Right Online example. All
style adjustments are centralised in brightonthesis.sty so a later edition or
different University requirement can be adopted without editing the chapters.

AUTOMATIC AND MANUAL REFERENCE CHECKING

No tool can currently certify that a bibliography is fully compliant with
Cite Them Right Harvard. Cite Them Right does not publish an official
machine-readable validation ruleset or an official biblatex style. Use these
two layers instead:

1. Automatic technical validation. Biber checks entry types, required data
   structures, dates, names and other BibLaTeX data-model issues. In a Windows
   command prompt opened in the thesis folder, run:

       biber --tool --validate-datamodel references.bib

   This reports malformed or unsupported bibliography data. It does not prove
   that the displayed punctuation and source-type format match Cite Them
   Right.

2. Manual style verification. After compiling the thesis, compare at least one
   rendered example of every source type used against the corresponding
   current Cite Them Right 13th-edition example. In particular check authors,
   year, title capitalisation, edition, journal details, DOI or URL and access
   date.

Zotero reduces transcription errors but cannot verify that the imported
metadata is correct. Check imported records for sentence fragments, all-capital
titles, missing authors, incorrect item types and absent dates before relying
on the generated reference.

INSTALLING BETTER BIBTEX IN ZOTERO

1. Download the current Better BibTeX .xpi file from:

       https://retorque.re/zotero-better-bibtex/installation/

2. In the Zotero desktop application, choose Tools, Plugins.
3. Click the cog menu and choose Install Plugin From File.
4. Select the downloaded .xpi and restart Zotero.

Better BibTeX is installed in the Zotero desktop application, not in the web
browser. A Zotero account is useful for synchronisation but is not required
for the local LaTeX connection.

CONNECTING THE THESIS COLLECTION

1. In Zotero, create a collection called Brighton Thesis.
2. Add the sources required for the thesis to that collection.
3. Right-click the collection and choose Export Collection.
4. Choose Better BibLaTeX, not Better BibTeX.
5. Tick Keep updated.
6. Do not tick Export files.
7. Save the export as references.bib in the folder containing main.tex.
8. Confirm replacement of the demonstration references.bib file.

Zotero will then update references.bib after an item in that collection is
added, removed or corrected. Correct bibliographic information in Zotero, not
in the automatically exported file, because a later export will overwrite
manual edits.

CITATION KEYS

Each exported item has a citation key immediately after its entry type:

    @article{hunterEarlyImaging2026,

The citation key in this example is:

    hunterEarlyImaging2026

Use it in a chapter as follows:

    Narrative:  \textcite{hunterEarlyImaging2026}
                produces Hunter (2026)

    Parentheses: \parencite{hunterEarlyImaging2026}
                 produces (Hunter, 2026)

    Direct quotation:
                 \parencite[p.~23]{hunterEarlyImaging2026}
                 produces (Hunter, 2026, p. 23)

    Page range:  \parencite[pp.~23--25]{hunterEarlyImaging2026}

    Several sources:
                 \parencite{hunterEarlyImaging2026;smithCartilage2025}

The supplied Chapter 1 and references.bib contain journal-article, book and
online examples for testing. Zotero's first automatic export will replace
those demonstration entries.

COMPILING REFERENCES

After bibliography changes run:

    XeLaTeX
    Biber
    XeLaTeX
    XeLaTeX

The first XeLaTeX run creates main.bcf. Biber reads main.bcf and
references.bib and creates main.bbl. The final XeLaTeX runs insert the
citations, rebuild the List of references and update page numbers.

GITHUB AND REFERENCES

Keep references.bib under Git version control. It is the reproducible input
exported from Zotero. Generated files such as .bbl, .bcf and .blg should
normally be ignored. Review the changed references.bib in GitHub Desktop and
commit it with the chapter that uses the new sources.

GENERATED SUPPORT FILES

Files such as .aux, .bcf, .lof, .lot, .out and .toc are generated by LaTeX.
Do not edit them. They hold numbering, bibliography and list information and
can be deleted safely when troubleshooting; LaTeX recreates them.

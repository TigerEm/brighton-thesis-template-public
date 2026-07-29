# University of Brighton thesis template

This is the public development copy of a modular LaTeX thesis template based
on the University of Brighton research-degree presentation requirements.

## Important status

This is a community-developed template, not an official University of Brighton
publication. Users must check the current regulations and their School or
supervisor's requirements before submission.

## Separation from a real thesis

Develop this template in a public repository that is entirely separate from
the private repository containing an actual thesis. Do not copy the `.git`
folder or commit history from a private thesis.

The public repository should contain only:

- generic example text and diagrams;
- neutral candidate and title metadata;
- the central stylesheet and modular source structure;
- demonstration references; and
- documentation for contributors.

It must not contain unpublished thesis writing, research data, participant
information, supervisor comments, private Zotero attachments or credentials.

## Main files

- `main.tex`: master document and neutral example metadata.
- `brightonthesis.sty`: central formatting and referencing configuration.
- `README.txt`: installation, TeXworks, Zotero and usage guide.
- `chapters/06-formatting-showcase.tex`: copyable formatting examples.
- `references.bib`: fictional demonstration records.

## Local build

Run:

1. XeLaTeX
2. Biber
3. XeLaTeX
4. XeLaTeX

## Contributing

Make focused changes in a branch, compile the complete example, inspect the
resulting PDF and describe the regulatory or technical reason for the change
in the commit or pull request.

## Licensing

Before inviting external reuse or contributions, add an explicit open-source
licence. The LaTeX Project Public License (LPPL) is commonly used for LaTeX
classes and packages; another licence may be chosen by the repository owner.

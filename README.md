# Concordia University's Gina Cody School of ENCS Thesis LaTeX Template

This is an updated LaTeX template for Master's and Ph.D. theses in the newly renamed Gina Cody School of Engineering and Computer Science.
It builds on [Suo Tan's version](https://github.com/Tandysony/LaTeX-Thesis-Template-for-Concordia-University-Students), and brings the following:
- Complies with 2019 requirements (they tend to change every so often...)
- Correct list and order of examiners for Master's and Ph.D.
- Some changes to support the CIISE department in the cover page
- Fixed links in the Table of Contents to the List of Figures/Tables
- Suppport for including thesis defence date or leaving it blank
- Removes PTEX.Fullbanner from included resources (hides resource author/dates/potential full pathes)

## Customize template
- Under `%% THESIS SETTINGS`, fill your name, thesis title, then the name of the program you are enrolled in (e.g., Computer Science), and your department.
- Next, check whether your department has the GPD or the Chair to sign the thesis and toogle `\isGpd` in the former case. Search for the name of the [current GPD of your department](https://www.concordia.ca/admissions/graduate/programs/contacts.html) if needed.
- Then, search for the name of the [current Dean of the faculty](https://www.concordia.ca/ginacody/about/leadership/office-dean/dean-of-engineering-and-computer-science.html).
- Fill the names of the examiners
- Fill the initial submission and defence dates if available

### Example 1: Ph.D. thesis in the CIISE department
Example of a Ph.D. thesis in the CIISE department with the names of the GPD/Dean as of 2019, and a co-supervisor.
```
%% THESIS SETTINGS
\author{John Doe}
\title{My Super Thesis}
\PhD
\program{Information and Systems Engineering}
\dept{The Concordia Institute\\for\\Information Systems Engineering}
\GpdOrChairOfDept{Dr.\ Mohammad Mannan}
\isGpd
\deanOfENCS{Dr.\ Amir Asif} 
\chairOfCommittee{Dr.\ Chair}
\examinerExternal{Dr.\ External}
\examinerFirst{Dr.\ Examiner1}
\examinerSecond{Dr.\ Examiner2}
\examinerExternalToProgram{Dr.\ ExternalToProgram}
\supervisor{Dr.\ Supervisor}
\hasCosupervisor
\coSupervisor{Dr.\ Co-supervisor}

%% Comment to use current month, needs to match initial submission
\submitmonth{May 2019}
%% Comment if date of defence is unknown yet, fill for final submission
\defencedate{July 1, 2019}
```

Note, if your thesis title takes two lines on the signature page, find the following line in `cuthesis.sty`:
```
\\[1em] %% Comment if PhD with co-supervisor and long thesis title
```
and comment it.


### Example 2: MApCompSc thesis in the Computer Science & Software Engineering department
Example of a Ph.D. thesis in the Computer Science & Software Engineering department with the names of the GPD/Dean as of 2019.
```
%% THESIS SETTINGS
\author{John Doe}
\title{My Super Thesis}
\mastersDegree{Master of Applied Computer Science}
\program{Computer Science}
\dept{The Department\\of\\Computer Science and Software Engineering}
\GpdOrChairOfDept{Dr.\ Dhrubajyoti Goswami}
\isGpd
\deanOfENCS{Dr.\ Amir Asif} 
\chairOfCommittee{Dr.\ Chair}
\examinerExternal{Dr.\ External}
\examinerFirst{Dr.\ Examiner1}
\examinerSecond{Dr.\ Examiner2}
\examinerExternalToProgram{Dr.\ ExternalToProgram}
\supervisor{Dr.\ Supervisor}

%% Comment to use current month, needs to match initial submission
\submitmonth{May 2019}
%% Comment if date of defence is unknown yet, fill for final submission
\defencedate{July 1, 2019}
```


## Compile
Install [MiKTeX](https://miktex.org/download), preferably install the complete set of packages, or at least install the `cm-super` font package.
If not using an IDE such as [TeXstudio](https://www.texstudio.org), the compilation process using PDFLatex is standard:
```
pdflatex mythesis.tex
pdflatex mythesis.tex
bibtex mythesis.tex
pdflatex mythesis.tex
```

## References
https://www.concordia.ca/content/dam/sgs/docs/handbooks/thesispreparationguide.pdf
https://github.com/Tandysony/LaTeX-Thesis-Template-for-Concordia-University-Students
ssh://login.encs.concordia.ca/nfs/encs/Share/teTeX/cuthesis/*
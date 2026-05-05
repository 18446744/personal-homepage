# Handoff Notes

## 2026-05-04

Current goal:

- Set up the project skeleton for the personal homepage assignment.

Current state:

- Project directory created.
- AI Agent instruction file created.
- Documentation and report draft folders created.

Files changed:

- `.gitignore`
- `AGENTS.md`
- `README.md`
- `docs/ai/decisions.md`
- `docs/ai/handoff.md`
- `report/report.tex`
- `report/images/`

Verification performed:

- Git repository initialized.
- `git status --short` shows the newly created project files as untracked.
- Static homepage and blog placeholder files have been created and can be opened directly in a browser.
- Report source changed from Markdown to XeLaTeX according to the student's preference.

Open questions:

- Student name, personal introduction, technical interests, and blog topic are not finalized yet.

Recommended next step:

- Fill in personal information and choose the first blog topic, then implement `index.html`, `style.css`, and `blog/first-blog.html`.
- Compile `report/report.tex` with XeLaTeX after the homepage URL, blog URL, and screenshots are ready.

## 2026-05-05

Current goal:

- Reorganize the homepage into a concise academic personal homepage using only user-provided real information.

Current state:

- Homepage modules are fixed as: personal profile, research experience, course/resource organization, and blog list.
- Personal profile uses the user's provided identity, school, major, research interest, and email only.
- Research experience lists only project name, project type, supervisor, and research interest direction.
- Professional courses are organized by semester from first-year fall to third-year spring.
- Placeholder resource links are reserved for professional course materials, general education course materials, and student activity materials.

Files changed:

- `index.html`
- `style.css`
- `docs/ai/handoff.md`

Verification performed:

- Checked the modified homepage source with UTF-8 output.
- Checked `git diff -- index.html style.css`.
- Checked `git status --short`.

Open questions:

- Actual URLs for course materials, general education materials, and student activity materials are not available yet.
- Blog content and report content still need to be aligned with the updated homepage.

Recommended next step:

- Replace placeholder resource links once real URLs are available.
- Revise `blog/first-blog.html` and `report/report.tex` so that they match the updated homepage content and avoid placeholder text.

## 2026-05-05 Follow-up

Current goal:

- Keep the current homepage layout, reduce the prominence of the student's name in the hero area, and make documentation updates an explicit project rule.

Current state:

- The hero heading was changed from a name-based greeting to `个人学术主页`.
- The main `h1` size was reduced for a more restrained academic homepage style.
- `AGENTS.md` now requires meaningful content, layout, workflow, or report changes to be recorded in `docs/ai/handoff.md`.

Files changed:

- `index.html`
- `style.css`
- `AGENTS.md`
- `docs/ai/handoff.md`

Verification performed:

- Checked the relevant homepage and style source before editing.
- Updated this handoff entry after the edits.

Open questions:

- No replacement image has been provided for the hero area, so text was used instead of adding an image.

Recommended next step:

- Visually check the homepage in a browser and decide whether `个人学术主页` is suitably low-profile, or whether a different neutral heading should be used.

## 2026-05-05 Course Resources

Current goal:

- Keep the blog unchanged, remove duplicated research-interest information from the research section, and make course names usable as future resource entry points.

Current state:

- The research section no longer repeats `研究兴趣方向`.
- Course names in the professional course list are now links.
- Most course links are placeholders until real material URLs or files are available.
- `算法基础` links to an inline material list containing two uploaded lecture PDFs.
- Lecture PDFs were copied into `assets/courses/algorithm-foundations/`.

Files changed:

- `index.html`
- `style.css`
- `docs/ai/handoff.md`
- `assets/courses/algorithm-foundations/ALG26-L1.pdf`
- `assets/courses/algorithm-foundations/ALG26-L2.pdf`

Verification performed:

- Confirmed `ALG26-L1.pdf` and `ALG26-L2.pdf` exist in the source PPT directory.
- Copied both PDFs into the project assets directory.
- Added homepage links to the copied PDFs.

Open questions:

- Real materials for other courses, general education courses, and student activities are not available yet.
- Placeholder `href="#"` values should be replaced with real files, folders, or course pages when materials are ready.

Recommended next step:

- Decide a consistent file organization convention for each course, such as `assets/courses/<course-slug>/`, before adding more materials.

## 2026-05-05 Materials Page

Current goal:

- Avoid making the homepage too long by moving course material details to a separate page while preserving course-name click navigation.

Current state:

- Added `course-materials.html` as the dedicated course materials and learning notes page.
- The homepage professional course button now links to `course-materials.html`.
- Every course name on the homepage links to a matching anchor on `course-materials.html`.
- The homepage no longer displays the algorithm lecture PDF list inline.
- The new materials page lists all professional courses with placeholders, and `算法基础` contains links to `ALG26-L1.pdf` and `ALG26-L2.pdf`.

Files changed:

- `index.html`
- `style.css`
- `course-materials.html`
- `docs/ai/handoff.md`

Verification performed:

- Reused the existing copied PDF paths under `assets/courses/algorithm-foundations/`.
- Kept `blog/first-blog.html` unchanged.

Open questions:

- Large material storage strategy is still undecided; possible options include external storage links, Git LFS, local-only links, or generated symlinks/hardlinks for local use.

Recommended next step:

- Choose whether course materials should be public on GitHub Pages or referenced from external/private storage before adding many files.

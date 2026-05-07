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

## 2026-05-05 General Courses And Activity Materials

Current goal:

- Add general course and activity material entries, keep click-through navigation to the independent materials page, and replace algorithm materials with a new PDF.

Current state:

- The homepage general course section now lists `天体物理概观` and `毛泽东思想概论`.
- The homepage activity section now lists `历届资料`, `星星`, and `燃·骁`.
- Each new entry links to a matching anchor in `course-materials.html`.
- `course-materials.html` includes placeholder cards for the new general course and activity entries.
- Old algorithm PDFs `ALG26-L1.pdf` and `ALG26-L2.pdf` were removed from `assets/courses/algorithm-foundations/`.
- New `ALG26.pdf` was copied from the PPT directory into `assets/courses/algorithm-foundations/` and linked from the algorithm course card.

Files changed:

- `index.html`
- `course-materials.html`
- `style.css`
- `docs/ai/handoff.md`
- `assets/courses/algorithm-foundations/ALG26.pdf`
- Removed `assets/courses/algorithm-foundations/ALG26-L1.pdf`
- Removed `assets/courses/algorithm-foundations/ALG26-L2.pdf`

Verification performed:

- Confirmed `D:\13768\3春\5107\PPT\ALG26.pdf` exists before copying.
- Confirmed the project asset directory contains `ALG26.pdf` after replacement.

Open questions:

- GitHub Pages deployment has not been performed yet; no public URL exists until the repository is pushed and Pages is enabled.

Recommended next step:

- Decide whether to keep large PDFs in the Git repository or move them to external storage before deploying.

## 2026-05-05 External Link

Current goal:

- Add an external USTC pan link for `历届资料` while keeping the homepage concise.

Current state:

- The homepage `历届资料` entry still links to the independent materials page section.
- The `历届资料` card in `course-materials.html` now contains the USTC pan share link, extraction code, and expiration date.

Files changed:

- `course-materials.html`
- `style.css`
- `docs/ai/handoff.md`

Verification performed:

- Added the provided URL exactly as given.
- Did not modify `blog/first-blog.html`.

Open questions:

- The pan link requires a password and may not be usable after its expiration date on 2027-06-14 23:59:59.

Recommended next step:

- Test the link in a normal browser before final deployment.

## 2026-05-07 Homepage Intro Update

Current goal:

- Replace the homepage opening title with a course-assignment description and add the provided image to the opening profile area.

Current state:

- The homepage hero no longer uses `个人学术主页` as a large heading.
- The opening area now shows `assets/images/homepage-photo.jpg`, copied from the provided `FAKE.jpg`.
- The opening description explains that the site is the first Algorithm Foundations assignment result and mentions the profile, research, course materials, activity materials, and blog sections.
- The opening description uses normal body-sized text, matching the profile list scale, without bold styling.

Files changed:

- `index.html`
- `style.css`
- `docs/ai/handoff.md`
- `assets/images/homepage-photo.jpg`

Verification performed:

- Confirmed the provided image was copied into the project asset directory.
- Checked Git diff and repository status after editing.

Open questions:

- The homepage image should be visually checked in a browser before the next deployment.

Recommended next step:

- Commit and push the homepage update after local visual inspection.

## 2026-05-07 Mao Course Material

Current goal:

- Add the provided Mao Zedong Thought course PDF to the course materials page with a user-facing link name.

Current state:

- Copied `D:\13768\2春\2121\永志班史.pdf` into the project as `assets/courses/mao-zedong-thought/xiao-lunwen.pdf`.
- The `毛泽东思想概论` card in `course-materials.html` now links to the PDF with the display name `小论文`.

Files changed:

- `course-materials.html`
- `docs/ai/handoff.md`
- `assets/courses/mao-zedong-thought/xiao-lunwen.pdf`

Verification performed:

- Confirmed the source PDF exists and is small enough for normal GitHub repository storage.
- Confirmed the copied PDF exists under the project assets directory.

Open questions:

- Future large video files should not be committed directly to this repository.

Recommended next step:

- Check the course materials page locally, then commit and push the updated material link.

## 2026-05-07 Resource Link Cleanup

Current goal:

- Remove the `历届资料` entry and update selected resource links to external downloads.

Current state:

- Removed `历届资料` from the homepage activity list.
- Removed the `历届资料` material card from `course-materials.html`.
- Updated `星星` to link to the provided USTC pan share URL.
- Updated `天体物理概观` to link to the GitHub Release PDF asset download URL.

Files changed:

- `index.html`
- `course-materials.html`
- `docs/ai/handoff.md`

Verification performed:

- Checked source locations before editing.
- Checked Git diff and repository status after editing.

Open questions:

- The GitHub Release URL assumes the file is attached as `astrophysics.pdf` under tag `course-materials-v1`.

Recommended next step:

- Test both external links in a browser after pushing to GitHub Pages.

## 2026-05-07 Profile And Resource Layout

Current goal:

- Move the homepage assignment description below the whole profile area and simplify resource links.

Current state:

- The assignment-description paragraph now appears below the profile image and personal information list, above the research section.
- The description text and typography remain unchanged.
- Removed the `可挂载课程资料` and `可挂载社团资料` links from the homepage.
- Removed the `通识课程` and `其他活动` placeholder cards from `course-materials.html`.
- Homepage `天体物理概观` and `毛泽东思想概论` now link directly to their materials.
- Renamed `星星` to `2024SeeYou毕业晚会` on both the homepage and materials page.

Files changed:

- `index.html`
- `style.css`
- `course-materials.html`
- `docs/ai/handoff.md`

Verification performed:

- Checked relevant homepage and materials page source before editing.
- Checked source search results, Git diff, and repository status after editing.

Open questions:

- The external Release PDF and USTC pan links should be tested after deployment.

Recommended next step:

- Visually inspect the profile section locally, then commit and push the updates.

## 2026-05-07 Direct Resource Labels

Current goal:

- Make selected homepage resource labels more explicit and remove their duplicate cards from the materials page.

Current state:

- Committed the previous profile/resource layout changes locally as `ea02362` without pushing.
- Homepage `天体物理概观` now displays as `天体物理概观（PPT）`.
- Homepage `毛泽东思想概论` now displays as `毛泽东思想概论（小论文）`.
- Homepage `2024SeeYou毕业晚会` now displays as `2024SeeYou毕业晚会（《星星》）`.
- Homepage `燃·骁` now displays as `燃·骁（2026溯风、书院嘉年华、郭奖开幕式）` and links to the provided USTC pan URL.
- Removed the `天体物理概观`, `毛泽东思想概论`, `2024SeeYou毕业晚会`, and `燃·骁` cards from `course-materials.html`.

Files changed:

- `index.html`
- `course-materials.html`
- `docs/ai/handoff.md`

Verification performed:

- Checked that the previous commit was created and not pushed.
- Checked homepage and materials page source locations before editing.
- Checked search results, Git diff, and repository status after editing.

Open questions:

- External USTC pan links should be tested manually in a browser after deployment.

Recommended next step:

- Commit this direct-resource-label update when the homepage wording is confirmed.

## 2026-05-07 User Manual Edits Review

Current goal:

- Review and record the user's manual edits to `index.html` and `course-materials.html`.

Current state:

- Homepage profile label changed from `研究兴趣` to `兴趣方向`.
- Homepage interest text changed from `科学计算（PDE 数值解）` to `PDE 数值解`.
- Homepage resource labels now include `天体物理概观（PPT）` and `毛泽东思想概论（小论文）`.
- Activity links now include `星星（2024蛙鸣之夏、SeeYou毕业晚会）`, `Romantic（2024美丽邂逅、2025舞团专场）`, and `燃·骁（2026溯风、书院嘉年华、郭奖开幕式）`.
- `course-materials.html` introduction text was narrowed to course materials and no longer mentions activity material placeholders.
- `course-materials.html` no longer contains the direct-link cards for `天体物理概观`, `毛泽东思想概论`, `2024SeeYou毕业晚会`, and `燃·骁`.
- Footer English text changed to `Foundations of Algorithm 2026`.

Files changed:

- `index.html`
- `course-materials.html`
- `docs/ai/handoff.md`

Verification performed:

- Checked `git status --short --branch`.
- Reviewed `git diff -- index.html course-materials.html`.
- Searched for removed placeholder anchors and old labels such as `可挂载`, `历届资料`, and the removed material-page anchor links.

Open questions:

- Confirm whether the footer should remain `Foundations of Algorithm 2026` or use the more natural course-style wording `Algorithm Foundations 2026`.

Recommended next step:

- Decide the footer wording, then commit the combined resource-label and manual-edit updates.

## 2026-05-07 Blog Replacement

Current goal:

- Replace the first blog post with the user's complete article about AI Agent assisted homepage development.

Current state:

- `blog/first-blog.html` now uses the title `AI Agent 辅助搭建个人主页实践与思考`.
- The blog body was replaced with the provided sections: preface, tools used, first AI Agent experience, prompt granularity, file upload strategy, real usage reflections, and conclusion.
- All screenshot markers were converted into styled placeholder blocks for later image insertion.
- Added shared `.image-placeholder` styling in `style.css`.

Files changed:

- `blog/first-blog.html`
- `style.css`
- `docs/ai/handoff.md`

Verification performed:

- Read the previous blog page and reused its page shell, stylesheet reference, and navigation links.
- Checked source diff and searched for remaining raw screenshot marker text after editing.

Open questions:

- Actual screenshot files still need to be captured and inserted into the placeholder positions.

Recommended next step:

- Preview the blog page locally, then replace placeholders with final screenshots before writing the report.

## 2026-05-07 Blog Section Revision

Current goal:

- Replace the blog content from section two through the conclusion with the user's revised version.

Current state:

- Blog section two now emphasizes moving from trial probing to collaboration with AI Agent.
- Blog section three now frames prompt writing as a balance between vague and overly precise instructions.
- Blog section four now describes a three-tier file storage strategy for small, medium, and large files.
- Blog section five now summarizes practical reflections about AI Agent collaboration, asking/verifying, and retaining human responsibility.
- The conclusion was replaced with the revised summary about completing the assignment and experiencing a full AI-assisted development process.
- Existing screenshot placeholders were retained and relabeled where the revised content changed their wording.

Files changed:

- `blog/first-blog.html`
- `docs/ai/handoff.md`

Verification performed:

- Located the existing section headings and placeholder blocks before editing.
- Checked source diff and repository status after editing.

Open questions:

- Final screenshots are still pending.

Recommended next step:

- Preview the revised blog locally and commit once the wording is final.

## 2026-05-07 Blog Polishing

Current goal:

- Polish the first blog post using the actual project history and handoff notes without repeating existing points.

Current state:

- Committed the previous full blog replacement as `46042bc` before further edits.
- Fixed spacing in the preface around `Codex` and `GPT Plus`.
- Added a new section about project records, explaining the roles of `AGENTS.md` and `docs/ai/handoff.md`.
- Added a new section about GitHub Pages deployment, including the empty remote branch issue, push/RPC failure, and link verification.
- Renumbered later blog sections so the article now has seven numbered sections before the conclusion.
- Updated the conclusion to include project records, file storage, and deployment as part of the complete AI-assisted development workflow.

Files changed:

- `blog/first-blog.html`
- `docs/ai/handoff.md`

Verification performed:

- Read the latest blog with UTF-8 output.
- Read handoff notes and recent commit history.
- Checked source diff and repository status after editing.

Open questions:

- The blog still uses screenshot placeholders; final screenshots need to be inserted later.

Recommended next step:

- Preview the polished blog page and commit if the final wording is acceptable.

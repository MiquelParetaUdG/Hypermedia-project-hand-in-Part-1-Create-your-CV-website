# Pere Pi Serra – Online CV

A single-page, static CV website presenting the profile of Pere Pi Serra, a fictional Social Media Manager based in Girona. This website was developed for the **Hypermedia project hand in — Part 1: Create your CV website**.

- **GitHub repository:** [Hypermedia project — CV website](https://github.com/MiquelParetaUdG/Hypermedia-project-hand-in-Part-1-Create-your-CV-website)
- **Figma design:** [CV website in Figma](https://www.figma.com/design/RvqcUzfQlt5QThEc4Dr84I/CV-website?node-id=0-1&t=tLvKqYRjjq8wcPiU-1)
- **GitHub Pages URL:** [Open the website](https://miquelparetaudg.github.io/Hypermedia-project-hand-in-Part-1-Create-your-CV-website/)
- **Technology:** HTML5 and CSS3, using CSS Grid and Flexbox. No JavaScript or CSS framework is used.

---

## Project analysis

### User profile (personas)

The website is designed for two main audiences who need to assess the candidate quickly and for different reasons.

#### Persona 1 – Jordi Vidal, founder and CEO

| | |
|---|---|
| **Age / location** | 52, Girona |
| **Role** | Founder and CEO of a mid-sized hospitality group on the Costa Brava |
| **Tech comfort** | Medium; usually reads on a laptop and sometimes on a phone between meetings |
| **Goal** | Find a professional who can grow the group's brand and bookings and lead a team without constant supervision |
| **Frustrations** | Long, generic CVs; vague claims without numbers; candidates who do not explain business impact |
| **Quote** | “I don't need a list of tools. I need to know what this person did for the last company's revenue.” |

**What he expects to find:** a clear professional headline, measurable results such as audience growth and revenue increases, the size of teams managed, and experience in a relevant sector. Because he may spend less than a minute reviewing a profile, the summary and key figures should be easy to locate and scan.

#### Persona 2 – Laia Camps, HR recruiter

| | |
|---|---|
| **Age / location** | 34, Figueres |
| **Role** | Talent acquisition specialist at a digital marketing agency |
| **Tech comfort** | High; reviews many profiles and often uses a phone |
| **Goal** | Shortlist candidates who match a job description and prepare for interviews |
| **Frustrations** | Hidden contact details, unclear dates, and having to open several links to verify a profile |
| **Quote** | “Give me the timeline, the skills and a way to contact you, and let me copy them into my notes.” |

**What she expects to find:** a scannable work timeline, skills that can be matched against a job offer, languages, education, and direct links to professional profiles. She may also print the page or save it as a PDF for a hiring file.

### Information architecture

The CV is a single-page website. On desktop screens, its content is divided into a left sidebar and a wider main column. This structure lets visitors identify the candidate and find contact information quickly, while keeping education and work history in a separate area that is easy to scan.

The **left sidebar** answers the questions “Who is this person?” and “How can I contact them?”. It begins with the portrait, name and professional title, followed by the website, email address, phone number and location. These contact details are placed near the top so recruiters do not have to search for them. A short professional summary follows and highlights experience, social media platforms and measurable results. The skills are arranged in two columns to use the available space efficiently. Languages and proficiency levels are presented in a compact table, and the final section contains Behance and LinkedIn links for further verification.

The **main column** contains Education, Experience and Volunteer Experience. Education is presented from the Business Administration studies (2006–2010) to the postgraduate course in Digital Marketing (2010–2011), showing the progression of the candidate's studies. Professional and volunteer experience are listed in reverse chronological order, with the most recent role first. Each entry uses a consistent pattern: role and dates, organisation and location, followed by short achievements or a brief description. This repetition makes separate roles easier to compare.

A navigation menu at the top of the main column links directly to the three main sections, and a footer closes the page. The HTML places the sidebar before the main content; on small screens, the layout becomes a single column, so sidebar information appears before education and experience. Semantic elements such as `aside`, `main`, `nav`, `section` and `article` reflect the content hierarchy and help assistive technologies interpret the page.

### Visual design

The design adapts the appearance of a conventional printed CV into a web page while preserving a professional and easy-to-scan visual identity. Its main priorities are clear hierarchy, readable text and quick access to important information.

**Colour palette.** The primary navy blue (`#174180`) is used for the sidebar and main section headings. It provides a strong visual anchor and supports the professional tone of the CV. The darker navy (`#12346f`) is used for the footer, extending the same identity to the bottom of the page. The sky blue (`#56ccf2`) highlights sidebar headings, contact links and achievement bullets, separating important details from the dark background. The main area is white (`#ffffff`) with dark grey text (`#4f4f4f`) for readability. Muted grey (`#828282`) distinguishes dates and locations from role titles, while a pale grey (`#e3e7ee`) is used for the navigation divider. These colour values match the variables defined in `styles.css`.

**Typography.** The page uses Open Sans, loaded from Google Fonts, with Arial and a generic sans-serif font as fallbacks. The type hierarchy is built through size, weight, colour and italic styling rather than through several font families. The candidate's name combines a lighter weight with a bold surname, section headings are bold and navy, role titles are bold, and dates use italic text in a muted colour. This keeps the design consistent and helps distinguish titles from supporting details.

**Layout and responsiveness.** CSS Grid creates the desktop two-column layout, with a 320-pixel sidebar and a flexible main column; the overall width is limited to 1100 pixels. The footer spans both columns. Flexbox aligns each role's title with its dates and arranges the navigation links, while a two-column CSS Grid displays the skills. The default layout is a single column; a media query at 768 pixels and above switches to the desktop grid. The navigation menu uses `position: sticky` to remain near the top while scrolling.

**Details and usability.** The portrait is circular to add a human element to the page. SVG icons help identify contact methods and professional references, while small blue bullets highlight achievements. Links have hover transitions, and keyboard focus outlines make focused links easier to identify. The layout uses semantic HTML and descriptive alternative text for the portrait; decorative icons use empty alternative text so screen readers can skip them.

---

## Implementation and code structure

The project uses plain HTML5 and CSS3. No JavaScript, Bootstrap or other front-end framework is required. Google Fonts is loaded externally to provide the Open Sans typeface.

### `index.html`

- Includes the HTML document structure, page title, character encoding, viewport and metadata.
- Links to the external `styles.css` file and to the Open Sans stylesheet from Google Fonts.
- Uses semantic elements including `header`, `nav`, `aside`, `main`, `section`, `article` and `footer`.
- Uses headings, paragraphs, `strong`, `abbr`, `id` and `class` attributes to structure and describe content.
- Uses unordered lists for skills and achievements, a table for language levels, and links for contact details and references.

### `styles.css`

The stylesheet is organised into 11 commented sections:

1. CSS custom properties and spacing variables.
2. Inheritance and the box model.
3. Text formatting and hierarchy.
4. Links and lists, including hover states.
5. Table formatting.
6. Sizing, spacing and display rules.
7. Positioning, including the sticky navigation and custom achievement bullets.
8. Flexbox alignment.
9. Grid layout for the skills (the page columns are defined in section 11).
10. Link colour transitions.
11. Responsive layout with a media query at `768px`.

### Project structure

The repository root should contain the following files and folders. File names and capitalisation in the `images` paths must match the references in `index.html` exactly.

```text
.
├── index.html
├── styles.css
├── README.md
└── images/
    ├── pere.jpg
    └── icons/
        ├── website.svg
        ├── email.svg
        ├── phone.svg
        ├── location.svg
        ├── behance.svg
        └── linkedin.svg
```

The image paths above are the resources expected by the HTML. Check that every listed file is present in the repository; otherwise, the portrait or icons will appear as broken images on the published website.

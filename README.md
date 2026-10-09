JOVITHA'S PORTFOLIO WEBSITE
INFR3120 — Assignment 1

LIVE WEBSITE
https://jovitha-dogga.github.io/INFR3120-Portfolio/

GITHUB REPOSITORY
https://github.com/Jovitha-Dogga/INFR3120-Portfolio

ABOUT THIS PROJECT

This is my personal portfolio website for INFR3120 Web &
Script Programming. I built it using HTML5 and CSS3 to
introduce myself, show some of the projects I have worked on,
and give visitors a way to contact me.

The website has four separate HTML pages, each with its own
purpose. I used separate CSS stylesheets for desktop, tablet,
and mobile screens to make the website work across different
screen sizes.

WEBSITE PAGES

  Home (index.html)
    Introduces my portfolio and provides navigation to the
    other pages.

  About Me (about.html)
    Includes my photo, a short introduction, and a 45.4-second
    introduction video with playback controls and a poster.

  Projects (projects.html)
    Showcases five projects related to programming,
    networking, and cybersecurity.

  Contact Me (contact.html)
    Contains a contact form with fields for name, email,
    cell number, and comments. Includes HTML5 validation.

RESPONSIVE DESIGN AND VIEWPORT SIZES

I used three separate CSS stylesheets and media queries to
adjust the website for different viewport widths. The
breakpoints match the ranges recommended in the Week 3
lecture notes.

  desktop.css  ->  961px and wider
    Laptops and desktops. This range aligns with the standard
    960px grid width discussed in Week 1. Gives content more
    horizontal room and uses a wider 84% main content area
    with larger headings.

  tablet.css   ->  481px to 960px
    Tablets such as iPads and Android tablets. The main
    content narrows to 90% and font sizes are reduced slightly
    so text stays readable on medium-sized screens.

  mobile.css   ->  480px and below
    Smartphones. Navigation links stack as large tappable
    buttons (a technique from Week 3), the layout becomes
    single-column, and padding is reduced so nothing gets
    cut off.

Each HTML page includes a viewport meta tag so that mobile
browsers use the device's actual viewport width:

  <meta name="viewport" content="width=device-width, initial-scale=1">


CSS GRADIENTS

I used two types of linear gradients in my website.

  1. Angled linear gradient

  The header uses an angled gradient that blends muted slate
  blue into dark teal. The 135-degree angle gives the header
  diagonal visual interest rather than a flat colour.

    background: linear-gradient(135deg, #7A8C98, #15333D);

  2. Standard linear gradient

  Article and section backgrounds use a standard top-to-bottom
  linear gradient that blends white into light cream. This
  keeps the content backgrounds subtle and gives the content
  boxes a slight sense of depth without using image files.

    background: linear-gradient(#FFFFFF, #E9E2DC);


COLOUR SCHEME

I experimented with the colour wheel on Adobe Color
(https://color.adobe.com/create) to find colours that worked
together. I wanted a muted palette that would look consistent
across all four pages without making the website too busy.

My website uses six hex values in total. Based on the Week 1
lecture notes, black, white, shades of grey, and dark blue
generally do not count toward the five-colour scheme. In my
design:

  - Light cream (#E9E2DC) is a neutral (near-white).
  - Dark teal (#15333D) is a neutral (dark blue).
  - Very dark maroon (#3F0D0C) is a neutral (near-black).

This leaves three core colours in my palette, with three
neutrals layered on top for readable backgrounds, text, and
contrast.

CORE COLOUR SCHEME

  Dusty rose (#C1A3A1)
    Navigation bar background.

  Deep plum (#824D5D)
    Section headings and hover states.

  Muted slate blue (#7A8C98)
    Header gradient and form input borders.

NEUTRAL TONES (do not count toward the palette)

  Light cream (#E9E2DC)
    Main page background and the lighter end of the section
    gradient.

  Dark teal (#15333D)
    Body text, footer background, and the darker end of the
    header gradient.

  Very dark maroon (#3F0D0C)
    Navigation link text.

REASONING

  I chose a deliberately minimal harmonious palette rather
  than a full five-colour scheme. The two warm tones (dusty
  rose and deep plum) sit near each other on the colour wheel,
  and the muted slate blue adds a cool counterpoint so the
  palette does not feel one-sided. Week 1 notes that fewer
  than five colours can look dull, but for a personal
  portfolio a tight three-colour scheme keeps focus on the
  content and gives the site a calm, cohesive mood. The three
  neutrals (cream, teal, near-black maroon) provide readable
  backgrounds and text without adding visual noise.


SEMANTIC HTML

I used semantic HTML5 elements to organize the content and
make the page structure clearer.

  <header>   Contains the page header and navigation.
  <nav>      Contains links to the four pages.
  <main>     Holds the main content of each page.
  <article>  Organizes individual content sections and projects.
  <footer>   Contains contact information and copyright details.


ACCESSIBILITY NOTES

  - Every <html> tag includes lang="en" so screen readers know
    what language the page is in. This is recommended by the
    W3C validator and checked by WAVE.

  - Every image includes an alt attribute describing its
    content for users who cannot see it.

  - Every form field is paired with a <label for=""> element
    so users know what each field is asking for.

  - WAVE also reminds designers to review video content
    manually to confirm that captions or transcripts are
    available where needed.

INTRODUCTION VIDEO

The About Me page includes an introduction video that is
45.4 seconds long, which falls within the 45-60 second range
required by the assignment. I used the HTML5 <video> element
with playback controls (controls), muted audio start (muted),
and a poster image (poster) that displays before the video
plays.

  <video controls muted poster="images/about-me.png">
      <source src="video/intro.mp4" type="video/mp4">
  </video>

The video element is also styled from the CSS files so that
it scales properly across desktop, tablet, and mobile
viewports.

CONTACT FORM

The Contact Me page includes fields for a visitor's name,
email address, cell number, and comments. I used HTML5 form
attributes such as required, an email input type, and a
pattern for the cell number to provide browser-side
validation before the form is submitted.

  - Name        : type="text"  + required
  - Email       : type="email" + required
  - Cell Number : type="tel"   + pattern="[0-9]{3}-[0-9]{3}-[0-9]{4]"
                  + required (expects a 123-456-7890 format)
  - Comments    : <textarea>   + required

The form uses a mailto: action, which relies on the visitor
having a compatible email application configured. It does not
use a server-side form submission system.


VALIDATION AND TESTING

I tested all four HTML pages and all three CSS stylesheets
with the official W3C tools. Screenshots of each test are
saved in the testing/ folder.

  HTML validation
    All four pages (index.html, about.html, projects.html,
    contact.html) were checked with the Nu Html Checker. Each
    one returned: "Document checking completed. No errors or
    warnings to show."

  CSS validation
    All three stylesheets (desktop.css, tablet.css,
    mobile.css) were checked with the W3C CSS Validator. Each
    one returned: "Congratulations! No Error Found."

  Link checking
    Each of the four pages was checked using the W3C Link
    Checker. All links were reported as valid.

  Accessibility (WAVE)
    All four pages were checked with the WAVE Web
    Accessibility Evaluation Tool. Every page scored:

      0 errors
      0 contrast errors
      AIM score of 10 out of 10

    The About Me page also shows 1 informational alert, which
    is WAVE's standard reminder to manually check the HTML5
    video element for captions or transcripts. This is not an
    error.

WAVE also notes that manual accessibility testing is still
recommended alongside the automated results.

PROJECT FILES
  index.html, about.html, projects.html, contact.html
    The four website pages.

  css/
    Contains desktop.css, tablet.css, and mobile.css.

  images/
    Contains the website images, including my photo and the
    video poster image.

  video/
    Contains the introduction video (intro.mp4).

  testing/
    Contains screenshots of the HTML validation, CSS
    validation, link checking, and WAVE results.

CREDITS
  - HTML and CSS concepts were based on the INFR3120 lecture
    material (Weeks 1 through 4).
  - Adobe Color was used to experiment with colour
    combinations.
  - W3C HTML Validator, W3C CSS Validator, W3C Link Checker,
    and WAVE were used for testing.
  - No external code beyond the lecture material was used.

CONTACT
Email: jovitha.dogga@ontariotechu.net
(c) 2026 Jovitha. All rights reserved.

# MG3D: Microtonal Guitar 3D Printed - Website Plan

## 1. Project Overview
A website allowing users to select their guitar model and download a `.zip` file containing `.stl` files for a DIY, 3D-printable microtonal conversion kit, alongside printing and installation instructions.
**Main Goal:** Promote an easy, fully reversible, and low-cost way to convert a standard guitar into a microtonal instrument using a sliding fretboard mechanism.

## 2. Design & Aesthetics (Inspiration)
* **Vibe:** Futuristic, Innovative, Maker/DIY, Premium.
* **Inspiration:** 
  * *Apple Product Pages:* Clean layouts, large typography, high-contrast imagery, and immersive scroll-driven animations.
  * *Maker Platforms (MakerWorld, Cults3D, Hackster.io):* Technical yet accessible, focusing on generative design and 3D geometric aesthetics.
* **Color Palette (Suggested):** 
  * Dark mode primary (deep blacks/grays like `#0a0a0a`, `#1c1c1e`) to feel premium and tech-focused.
  * Vibrant, futuristic accent colors (e.g., Neon Cyan, Electric Blue, or Synthwave Purple) for call-to-actions and 3D highlights.
* **Typography:** Modern sans-serif fonts (e.g., Inter, Roboto, or SF Pro) for a sleek, clean look.

## 3. Core Value Propositions
These should be highlighted throughout the copy and visuals:
* **Easy Conversion:** Slide-in fretboard mechanism for quick scale explorations.
* **Zero Damage:** Easy installation, totally reversible, no permanent modifications to the instrument.
* **Maintains Setup:** Keeps the current bridge and intonation setup.
* **Low Cost:** DIY 3D printing or cheap third-party printing services.

## 4. Animation Strategy
* **Apple-style Scroll Animations:** Use **GSAP (ScrollTrigger)** combined with **Three.js** (or an image-sequence `<canvas>` flipbook) to orchestrate scroll-driven storytelling.
* **Key Effects:**
  * **Exploded View Assembly:** As the user scrolls, the individual 3D printed parts assemble onto a digital guitar neck.
  * **Section Pinning:** Pinning the main visual container while text fades in/out on the side, explaining each component.

## 5. Website Structure (Page Sections)

### A. Hero Section
* **Visual:** Close-up, sleek 3D render (or WebGL model) of the MG3D fretboard installed on a glowing/stylized guitar neck.
* **Headline:** "Unlock the Microtonal Universe." (or similar bold hook)
* **Subheadline:** The reversible, 3D-printable conversion kit for your standard guitar.
* **CTA Button:** "Download STL Kit" / "Explore the System"
* **Indicator:** Smooth bouncing arrow prompting to scroll.

### B. The Philosophy (The "Why")
* Brief section contrasting the difficulty of traditional microtonal lutherie with the ease of 3D printing.
* Emphasize: *Reversible, Low-Cost, Zero Damage.*

### C. The Breakdown (Scroll-Triggered Exploded View)
This is the core interactive section. The user scrolls, and the pieces separate/highlight one by one:
1. **The Base Piece:** "The Foundation." Attaches to the top of the neck and frets via double-sided tape. Features the sliding slots.
2. **The Fretboard Piece:** "The Heart." Slides smoothly into the base piece. Easily hot-swappable. It features versatile fret handling options:
   * **Printed In-Place:** Frets are integrated directly onto the fretboard.
   * **Modular Slide-Ins:** Frets are printed separately to slide into slots, allowing for custom fret subsets.
   * **Standard Wire Frets:** Fretboard features slots compatible with traditional metal fret wire for a standard sound and feel.
3. **The Overnut Piece:** "The Elevation." Goes over the current nut (no unmounting) to elevate strings to the new fretboard height.
4. **The Bridge Studs:** "The Compensation." Goes around current bridge screws to elevate the bridge, keeping intonation intact without replacing parts.

### D. Available Scales (The Ecosystem)
* Grid or interactive carousel showcasing the pre-built scale options.
* **Standard Offerings:** 17 EDO, 19 EDO, 22 EDO, and 31 EDO.
* **Custom Request Block:** "Need a specific tuning? We can generate it." -> Mailto link to **mg3d@gmail.com**.

### E. Download & Configuration (The Maker Section)
* **Select Guitar Model:** A dropdown or selection cards (e.g., Stratocaster, Les Paul, Ibanez - *TBD based on available files*).
* **Download Output:** A clear, satisfying CTA button to download the `.zip` (containing `.stl` files + PDF instructions).
* **Print Settings Info:** A small accordion or text block summarizing recommended print settings (e.g., infill %, material like PETG/PLA).

### F. Open Source & Community
* **Evolving Project:** A statement clarifying that MG3D is an evolving project. We welcome community contributions, remixes, and feedback to make it even better.
* **Licensing:** Clear text/badge stating the project is licensed under **CC BY-NC-SA 4.0**. It is 100% free for non-commercial usage, requires attribution, and requires any remixes to remain free.
* **Support the Project:** A friendly call-to-action for donations: *"Did you like it? Donate any value to support the project"* with links to preferred platforms (e.g., PayPal, Ko-fi).

### G. Footer
* Minimalist footer.
* Contact: mg3d@gmail.com.
* Copyleft, Links to repository, donation page, and social media.

## 6. Technical Implementation Draft
* **Structure:** HTML5 Semantic tags (`<header>`, `<section>`, `<main>`).
* **Styling:** Vanilla CSS (CSS Variables for themes, Flexbox/Grid for layout).
* **Interactivity & Animation:** 
  * Vanilla JavaScript.
  * **GSAP** (GreenSock) for scroll triggers and timeline animations.
  * **Three.js** (if implementing real-time 3D models) OR **Canvas API** (for rendering pre-rendered Blender image sequences based on scroll position).

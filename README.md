# HAP's Learning Lab

**Web Development Images Learning Stations**

An interactive educational website exploring the intersection of AI image generation, responsive web design, and performance optimization techniques. Join HAP (HyBit A. ProtoBot), Prof. Teeters' apprentice, as he shares what he learned at each station!

## Overview

HAP's Learning Lab is a collection of 6 interactive learning stations designed to teach modern web development concepts through hands-on examples and real-world demonstrations. Each station focuses on a specific aspect of working with images on the web, from AI prompt engineering to container queries.

HAP, an AI apprentice learning from Prof. Teeters, guides you through each station with a friendly, first-person narrative that makes complex concepts approachable.

## Quick start

### Running locally

This is a static HTML site with no build process required.

**Option 1: Using a local server (recommended)**

```bash
# Using Python 3
python3 -m http.server 8000

# Using Node.js
npx http-server

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

**Option 2: Direct file opening**

Open `index.html` directly in your browser. Note: Some features (like JSON loading) may not work with `file://` protocol.

### Project structure

```
poem-images/
├── index.html              # Hub page with station overview
├── stations/
│   ├── ai-poetry-images.html   # Station 1: AI & Poetry
│   ├── responsive-images.html  # Station 2: Responsive Images
│   ├── art-direction.html      # Station 3: Art Direction
│   ├── modern-formats.html     # Station 4: Modern Formats
│   ├── loading-strategies.html # Station 5: Loading Strategies
│   └── container-queries.html  # Station 6: Container Queries
├── css/
│   └── style.css          # All site styles
├── js/
│   └── easter-egg.js      # HAP Insights easter egg
├── data/
│   ├── hybit-insights.jsonc  # Easter egg content (HAP's insights)
│   └── README.md          # Data file documentation
├── LICENSE                # MIT License (code only)
├── TRADEMARK.md           # HAP™ character rights
└── CONTENT-LICENSE.md     # Educational content license

```

## Learning stations

### Station 1: AI poetry & images

**Focus:** How AI interprets abstract vs concrete poetry

Learn about prompt engineering through practical examples of generating images for different types of poetry. Discover why concrete poems work instantly while abstract poems require iteration.

**Key concepts:**

- Prompt specificity
- Negative prompts
- Iterative refinement

### Station 2: responsive image syntax

**Focus:** Deep dive into srcset and sizes attributes

Master the syntax and behavior of responsive images. Understand how browsers choose which image to download based on viewport size and pixel density.

**Key concepts:**

- `srcset` with width descriptors
- `sizes` attribute
- Browser selection algorithm

### Station 3: art direction vs resolution

**Focus:** When to crop vs when to scale

Learn the difference between art direction (different crops for different sizes) and resolution switching (same image, different resolutions).

**Key concepts:**

- `<picture>` element
- `<source>` with media queries
- Art direction use cases

### Station 4: modern image formats

**Focus:** JPEG, PNG, WebP, and AVIF comparison

See real file size comparisons and browser support data for modern image formats. Understand when to use which format.

**Key concepts:**

- Format capabilities
- Compression comparison
- Progressive enhancement

### Station 5: loading strategies

**Focus:** Lazy loading, eager loading, and priority hints

Optimize when and how images load on your pages. Learn about `loading="lazy"`, `fetchpriority`, and deferred script loading.

**Key concepts:**

- Lazy loading (80% reduction)
- Priority hints
- Script loading strategies

### Station 6: container queries

**Focus:** Component-based responsive images

Future-proof techniques for making components adapt to their container size, not just viewport size.

**Key concepts:**

- Container queries syntax
- Component-aware design
- Context adaptation

## Easter egg feature

The site includes an educational easter egg system called "HAP Insights" that provides contextual learning tips when students add URL parameters. HAP shares additional insights he learned from Prof. Teeters in his friendly apprentice voice.

### How to use

Add `?hybit` to any page URL:

```
index.html?hybit              # Shows page-specific suggestions
index.html?hybit=detail       # Shows Lighthouse score
responsive-images.html?hybit=srcset  # Shows srcset explanation
```

### Available parameters

| Parameter | Shows | Best on |
|-----------|-------|---------|
| `detail` | Lighthouse Score: 99% | Any page |
| `stations` | Learning stations overview | Hub |
| `srcset` | Responsive image syntax | Station 2 |
| `picture` | Picture element | Station 3 |
| `cloudinary` | CDN optimization | Station 4 |
| `lazy` | Lazy loading benefits | Station 5 |
| `defer` | Deferred scripts | Station 5 |
| `container` | Container queries | Station 6 |
| `prompt` | AI prompt engineering | Station 1 |

### For instructors

See `data/README.md` for complete documentation on adding new insights and customizing messages.

## Technologies used

- **Pure HTML/CSS/JavaScript** - No frameworks or build tools
- **Native `<dialog>` element** - Modern modal UI
- **Cloudinary CDN** - Image optimization and delivery
- **JSONC data format** - Separated content from code
- **Responsive design** - Mobile-first approach
- **Semantic HTML** - Accessibility-focused markup

## Key features

### Performance optimized

- ✅ Lighthouse score: 99%
- ✅ Optimized image delivery via Cloudinary
- ✅ Lazy loading for images
- ✅ Deferred script loading
- ✅ Minimal CSS and JavaScript

### Accessibility

- ✅ Semantic HTML landmarks
- ✅ Skip to main content link
- ✅ ARIA labels on interactive elements
- ✅ Keyboard navigation support
- ✅ Screen reader tested

### Educational design

- ✅ Apprentice narrative with HAP's friendly voice
- ✅ Real-world examples with actual file sizes
- ✅ Visual comparisons and demos
- ✅ Copy-paste ready code snippets
- ✅ Contextual learning with HAP Insights
- ✅ Hands-on exploration encouraged

## Content guidelines

### Images

All images are served through Cloudinary with automatic optimization:

```html
<img src="https://res.cloudinary.com/cynthia-teeters/image/upload/f_auto,q_auto,w_600/image.jpg"
     alt="Descriptive text">
```

Parameters used:

- `f_auto` - Automatic format (WebP/AVIF when supported)
- `q_auto` - Automatic quality optimization
- `w_600` - Width constraint (responsive)

### Adding new stations

1. Copy `template.html` to `new-station.html`
2. Update page title, meta description, and og:image
3. Replace `[HAP_INTRO]` with HAP's apprentice voice introduction
4. Fill in station content with HAP's narrative
5. Add HAP Insights parameter (see `data/README.md`)
6. Update `index.html` hub page with link to new station
7. Add to this README's station list

## File organization

### CSS architecture

- **Single stylesheet** (`css/style.css`)
- **CSS custom properties** for colors and sizing
- **Utility classes** for spacing (`mt-1`, `mb-2`, etc.)
- **Component classes** for reusable patterns
- **Responsive design** with mobile-first breakpoints

### JavaScript organization

- **Minimal JavaScript** - Only for easter egg feature
- **No dependencies** - Pure vanilla JS
- **Event-driven** - Uses `DOMContentLoaded`
- **Error handling** - Graceful fallbacks

### Data organization

- **Separated content** - JSONC files for easter egg data
- **Documented structure** - Inline comments explain purpose
- **Easy to maintain** - Non-developers can edit content

## Browser support

Tested and working in:

- ✅ Chrome 90+
- ✅ Firefox 90+
- ✅ Safari 15.4+
- ✅ Edge 90+

Note: Native `<dialog>` element requires modern browsers (95%+ coverage as of 2024).

## Security considerations

### Content security policy

Basic CSP is included in HTML:

```html
<meta http-equiv="Content-Security-Policy" content="...">
```

Allows:

- Self-hosted scripts and styles
- Cloudinary images
- Inline styles (for utility classes)

### XSS prevention

Easter egg system uses:

- Whitelist validation for parameters
- Pre-defined messages only
- No user input in HTML
- Safe HTML tags only (`<code>`, `<strong>`, `<em>`)

## Performance metrics

Current Lighthouse scores:

- **Performance:** 99
- **Accessibility:** 100
- **Best Practices:** 100
- **SEO:** 100

Optimization techniques:

- Cloudinary CDN for global delivery
- Lazy loading for below-fold images
- Deferred script loading
- Preconnect to CDN origin
- Optimized critical rendering path

## Contributing

This project is part of Prof. Teeters' AI-Enhanced Teaching Methods.

### Content contributions

To add or modify educational content:

1. Edit the relevant HTML file
2. Follow existing patterns for consistency
3. Test on multiple screen sizes
4. Verify accessibility (screen reader, keyboard nav)
5. Update this README if adding new stations

### Easter egg contributions

To add new HAP Insights:

1. See `data/README.md` for detailed instructions
2. Edit `data/hybit-insights.jsonc`
3. Add parameter to whitelist
4. Create message with title and content (use HAP's voice!)
5. Test with `?hybit=newparam`

### Code style

- **HTML:** Semantic, accessible, well-indented
- **CSS:** BEM-like naming, mobile-first, commented sections
- **JavaScript:** Pure vanilla JS, clear function names, commented logic
- **JSONC:** Inline comments explaining each section

## Documentation

### For students

- Each station page includes inline explanations from HAP
- HAP Insights provide contextual learning tips
- Code examples are copy-paste ready
- Real metrics shown (file sizes, percentages)
- Apprentice narrative makes complex topics approachable

### For instructors

- `data/README.md` - Easter egg system documentation
- Inline HTML comments explain structure
- CSS comments document design decisions
- HAP's apprentice voice demonstrates relatable learning

## 📜 License

This project uses a **multi-license approach** to balance open source collaboration with intellectual property protection:

### License structure

| Component | License | File |
|-----------|---------|------|
| **Code & Technical Implementation** | MIT License | [LICENSE](./LICENSE) |
| **HAP™ Character & Brand** | Proprietary | [TRADEMARK.md](./TRADEMARK.md) |
| **Educational Content & Methodology** | Proprietary | [CONTENT-LICENSE.md](./CONTENT-LICENSE.md) |

### Quick reference guide

#### ✅ You CAN

- Use the code to build your own educational tools
- Fork and modify the technical implementation
- Reference HAP™ when discussing or citing this project
- Study the methodology for academic research
- Use concepts in your classroom with attribution

#### ❌ You CANNOT

- Create your own "HAP" character or derivatives
- Use HAP's visual design or personality
- Repackage the educational content commercially
- Claim the teaching methodology as your own
- Remove attribution or copyright notices

### Why multiple licenses?

- **Code (MIT)**: Encourages community contribution and technical innovation
- **Character (Proprietary)**: Maintains brand identity and prevents confusion
- **Content (Proprietary)**: Protects educational innovation while allowing academic use

### Attribution

When using or referencing this project:

```
HAP™ (HyBit A. ProtoBot™) by Cynthia Teeters
Apprentice-Based AI Teaching Methodology
```

### Questions?

- **For character licensing**: See [TRADEMARK.md](./TRADEMARK.md)
- **For educational content**: See [CONTENT-LICENSE.md](./CONTENT-LICENSE.md)
- **For other inquiries**: Open an issue or contact @cynthiateeters

---

*HAP™ and HyBit A. ProtoBot™ are trademarks of Cynthia Teeters. The apprentice learning methodology and educational content are proprietary innovations protected by copyright.*

## Credits

### Created by

**Cynthia Teeters** - Instructor, Web Developer
Part of AI-Enhanced Teaching Methods curriculum

### Technologies

- **Cloudinary** - Image optimization and CDN
- **Google Fonts** - Nunito typeface
- **Claude Code** - AI assistant for development

### Inspiration

This project demonstrates how AI image generation, web performance, and responsive design intersect in modern web development.

## Contact

For questions about this educational resource or to report issues:

- Review `data/README.md` for easter egg questions
- Consult inline HTML/CSS/JS comments

---

**Built with 🟠 for education and exploration**

---
icon: sparkles-fill
label: Feature Log
order: -200
templating: false
nav:
  badge: NEW|info
---
# Feature Log

Stay ahead with the latest and greatest from Retype! 

The **Feature Log** is your go-to source for all the powerful new features, enhancements, and innovations we're rolling out to make your documentation experience faster, smarter, and more elegant.

Explore what's new, discover hidden gems, and see how Retype is constantly evolving to meet your needs.

!!!
Do have a suggestion for a new feature in Retype? Please open an [issue](https://github.com/retypeapp/retype/issues) and let's chat. :icon-comment:
!!!

Please also check out the [[Changelog]] for a full summary of changes in each release.

---

## v3.11

[!badge PRO] Custom themes
: Comprehensive [[theme variables]] customization for both [light](/configuration/project.md#theme-base) and [dark](/configuration/project.md#theme-dark) modes, see [docs](/configuration/project.md#theme), [Themes](/guides/themes.md) guide, and [[Theme Variables]].

[!badge PRO] [`branding.baseColor`](/configuration/project.md#basecolor)
: Quick method to set the base brand color without full [theme](/configuration/project.md#theme) configuration, see [docs](/configuration/project.md#basecolor).

[!badge PRO] [`nav.badge`](/configuration/page.md#nav-badge)
: Add a badge to navigation items in the left sidebar, see [docs](/configuration/page.md#nav-badge).

Three-way switcher
: Enhanced color scheme switcher with `Light`, `Dark`, and `System` options. Allows users to return to system preference after manual selection.

Pipe notation syntax
: Shorthand syntax for [[Button]], [[Badge]], and [Navigation Badge](/configuration/page.md#nav-badge) components using `text|variant` format. Example: `[!badge NEW|info]` instead of `[!badge text="NEW" variant"info"]`.

Icon-only links
: Support for icon-only [`links`](/configuration/project.md#links) in header and [footer](/configuration/project.md#footer) configurations without requiring [`text`](/configuration/project.md#text). Enables cleaner, minimal navigation designs.

Base variant
: New `base` variant for [[Button]], [[Badge]], and [[Callout]] components. Provides consistent styling with the site's base color theme.

Better print mode rendering
: Improved print style with better outbound link handling and visual consistency

Search and filter UX
: Added keyboard shortcuts hints, improved placeholder handling, and better focus states

Footer template support
: Full templating support in [`footer.copyright`](/configuration/project.md#copyright) including use of data variables, includes, and functions

---

## v3.10

[!badge PRO] Next/Previous navigation control
: Configure visibility and sequencing of `Next/Previous` navigation buttons. Configure at project, page, and folder levels with `show`, `hide`, and `exclude` modes, see [blog post](/blog/2025-06-09.md), [Project](/configuration/project.md#nextprev) settings, [Page](/configuration/page.md#nextprev) settings, and [Folder](/configuration/folder.md#nextprev) settings.

GitHub Pages community key
: Retype Pro Community Key unlocks all Pro features for GitHub Pages projects. No cost, no strings attached for `*.github.io` domains, with up to 1000 pages with all [[Pro]] features included, see [blog post](/blog/2025-06-06.md) and [GitHub Pages](/hosting/github-pages.md) setup.

Hidden comments component
: Add hidden comments to markdown that won't appear in the final website. Supports both inline `%%comment%%` and block comment syntax, see [docs](/components/comments.md).

New [`tip`](/components/callout.md) Callout variant
: New `tip` callout variant with lightbulb icon and friendly green color scheme. Perfect for sharing best practices and helpful hints, see [docs](/components/callout.md).

Generic attributes for list items
: Apply CSS classes, IDs, and custom attributes directly to individual list items. Uses generic attribute syntax: `- List Item {.class-name #id data-value="test"}`, see [docs](/components/list.md#generic-attributes).

New CSS Classes
: Added rounded CSS classes including `rounded-xl`, `rounded-2xl`, `rounded-3xl`, `rounded-4xl` and `rounded-full`

Custom Anchors
: Support for custom [Obsidian](https://obsidian.md/) style anchor points using `^anchor` syntax for block references. Enables wiki-style block linking and referencing.

---

## v3.9

[!badge PRO] Navigation icon settings
: Control which navigation items show icons with [`nav.icons.mode`](/configuration/project.md#icons) setting. Options include: `all`, `folders`, `pages`, `top`, `none`.

[!badge PRO] Default color scheme
: Set project's default color scheme with [`scheme.mode`](/configuration/project.md#scheme) configuration. Options include: `system`, `dark`, `light`.

Print-Friendly Stylesheets
: Comprehensive print stylesheet for professional PDF and paper output. Removes navigation, optimizes typography, prevents awkward page breaks. Shows full URLs for external links in print.

Question [[Callout]]
: New [`question`](/components/callout.md) callout variant with question mark icon. Perfect for FAQ sections and troubleshooting guides.

Pipe separator image dimensions
: Set image dimensions using intuitive pipe syntax: `![Image|300]` or `![Image|300x200]`. Cleaner alternative to generic attributes for image sizing, see [docs](/components/image.md#dimensions).

Universal Callout syntax
: Enhanced compatibility and seamless migration with other documentation platforms, including [Notion](https://www.notion.com/), [GitHub](https://github.com/), [Obsidian](https://obsidian.md/), [Just the Docs](https://just-the-docs.com/) and other platforms.

List-Icon styling
: Improved styling for creating icon lists with proper spacing and alignment which simplifies creation of icon-based list layouts.

Details/summary conversion
: Automatic conversion of HTML `details` elements into Retype Panel components to ensure seamless integration with other platforms, such as GitHub.

---

## v3.8

[!badge PRO] Stack navigation mode
: Transform top-level folders into visually distinct stacked blocks. Better organization and visual hierarchy for complex documentation sites, Configure at project or page level, see [blog post](/blog/2025-05-04.md), [Project](/configuration/project.md#nav-mode) settings, and [Page](/configuration/page.md#nav-mode) settings.

WikiLinks Support
: Comprehensive wiki-style linking with double square brackets: `[[Page Name]]`. Intelligent link resolution that handles filename variations and support for custom labels using the syntax `[[page|Custom Label]]` for text links and `![[image.jpg|Alt text]]` for image wikilinks.

YouTube auto-embedding
: Automatic conversion of YouTube URLs into embedded video players. Supports all common YouTube URL formats including timestamps. Fully responsive with proper styling and controls, see [docs](/components/youtube.md).

Automatic [search](/configuration/project.md#search) language detection
: Automatically detects languages in content and optimizes search. Supports 25+ languages including English, Spanish, French, German, Japanese, Chinese, Arabic. Manual configuration still available with `"*"` token for auto-detection, see [docs](/configuration/project.md#search).

Greek and Hebrew Language Support
: Full support including proper text rendering, direction, and search functionality

Enhanced Include Functionality
: Support for accessing files outside project directory. Useful for including external readme files: `{{ include "../readme.md" }}`.

`home.md` Support
: Added `home.md` as another option for project home page. Joins existing options of `readme.md`, `index.md`, `default.md`, `welcome.md`.

[`permalink`](/configuration/page.md#permalink) Alias
: Added `permalink` as an alias for `route` in page configuration. Provides familiar naming for users migrating from other platforms, see [docs](/configuration/page.md#permalink).

Mermaid Upgrade
: Upgraded to Mermaid v11.6.0 with packet-beta diagram support for enhanced diagram rendering capabilities.

GitBook Image Handling
: Improved handling of GitBook image exports with relative paths for better compatibility with GitBook markdown exports.

Default Server Port
: Changed default development server port from `5000` to `5001` to avoid conflicts with macOS services using port `5000`.

UI Refinements
: Multiple UI improvements including search input styling, theme switcher icons, and navigation spacing for enhanced visual consistency and user experience.

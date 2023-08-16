# 2000 - Create files in site/

## 100 - command-line-reference-prefix.html

Inside the repository https://github.com/creations-global/frame/site/, create a file called ```command-line-reference-prefix.html``` with the following content:

```
<html devsite>
<head>
  <meta name="project_path" value="/_project.yaml">
  <meta name="book_path" value="/_book.yaml">
</head>
<body>

<h1 class="page-title">Command-Line Reference</h1>

<pre>
bazel [&lt;startup options&gt;] &lt;command&gt; [&lt;args&gt;]
</pre>

or

<pre>
bazel [&lt;startup options&gt;] &lt;command&gt; [&lt;args&gt;] -- [&lt;target patterns&gt;]
</pre>

See the <a href="/docs/build#specifying-build-targets">User's Guide</a> for the
target patterns syntax.

<h2>Option Syntax</h2>

<p>
Options can be passed to Bazel in different ways. Options that require a value
can be passed with either an equals sign or a space:
<pre>
--&lt;option&gt;=&lt;value&gt;
--&lt;option&gt; &lt;value&gt;
</pre>
Some options have a single character short form; in that case, the short form
has to be passed with a single dash and a space.
<pre>
-&lt;short_form&gt; &lt;value&gt;
</pre>
</p>

<p>
Boolean options can be enabled as follows:
<pre>
--&lt;option&gt;
--&lt;option&gt;=[true|yes|1]
</pre>

and disabled as follows:
<pre>
--no&lt;option&gt;
--&lt;option&gt;=[false|no|0]
</pre>
</p>

<p>
Tristate options are usually set to automatic by default, and can be
force-enabled as follows:
<pre>
--&lt;option&gt;=[true|yes|1]
</pre>
or force-disabled as follows:
<pre>
--no&lt;option&gt;
--&lt;option&gt;=[false|no|0]
</pre>
</p>
```
site/command-line-reference-prefix.html

## 200 - command-line-reference-suffix.html

Inside the repository https://github.com/creations-global/frame/site/, create a file called ```command-line-reference-suffix.html``` with the following content:

```

<br/><br/><br/><br/>
</body>
</html>
```
site/command-line-reference-prefix.html

## 300 - BUILD

Inside the repository https://github.com/creations-global/frame/site/, create a file called ```BUILD``` with the following content:

```
exports_files(
    [
        "command-line-reference-prefix.html",
        "command-line-reference-suffix.html",
    ],
)

filegroup(
    name = "srcs",
    srcs = glob(["**"]) + ["//site/en:srcs"],
    visibility = ["//:__pkg__"],
)
```
site/BUILD

## 400 - en/frame.css

Inside the repository https://github.com/creations-global/frame/site/en/, create a file called ```frame.css``` with the following content:

```
/* Hero row - main  */
.frame-hero-full-bleed-light {
    background: linear-gradient(180deg, #0c713a 0%, #1e431e 100%);
    width: 100vw;
  }
  
  /* Required change to enforce custom above-the-fold dark background. */
  /* Note: dark theme not enabled for Frame tenant. */
  .frame-hero {
    color: #fff !important;
  }
  
  .frame-hero .devsite-landing-row-item-image {
    width: 400px;
  }
  
  /* Required change to enforce custom above-the-fold dark background. */
  /* Note: dark theme not enabled for Frame tenant. */
  .frame-hero .devsite-landing-row-header-text .devsite-landing-row-description,
  .frame-hero .devsite-landing-row-inner .devsite-landing-row-item-description h3,
  .frame-hero .devsite-landing-row-inner .devsite-landing-row-item-description-content,
  .frame-hero .devsite-landing-row-inner .devsite-landing-row-item-icon-container
  {
    color: #fff !important;
  }
  
  .frame-hero .devsite-landing-row-header-text {
    margin-bottom: 20px;
  }
  
  .frame-hero h3 a,
  .frame-hero .devsite-landing-row-header-text h2 {
    color: #fff;
    font-size: 48px;
    font-weight: 500;
    line-height: 68px;
  }
  
  .frame-button-light {
    background: #fff;
    border-radius: 4px;
    color: #000;
    text-transform: none;
  }
  
  /* Hero row - Why Frame  */
  .frame-hero-full-bleed-dark {
    background: linear-gradient(180deg, #1e431e 0%, #1e431e 100%);
    width: 100vw;
  }
  
  .frame-hero-full-bleed-dark .devsite-landing-row-item-body h3 {
    font-size: 24px;
    padding: 15px 0;
  }
  
  .frame-hero-full-bleed-dark .devsite-landing-row-item-icon {
    height: 68px;
    width: 85px;
  }
  
  .frame-hero .devsite-landing-row-item-description {
    padding: 0 15px;
  }
  
  /* Essential Frame row  */
  
  /* [1] Required change for custom below-the-fold light background. */
  /* Note: dark theme not enabled for Frame tenant. */
  .frame-body-light-cards {
    color: #000 !important; /* [1] */
    margin-top: 40px;
  }
  
  .frame-body-light-cards .devsite-landing-row-item img {
    max-width: 75%;
  }
  
  .frame-body-light-cards .devsite-landing-row-item-body h3,
  .frame-body-light-cards .devsite-landing-row-item-body h3 a {
    color: #000;
    font-size: 30px;
    font-weight: 400;
  }
  
  .frame-button-dark {
    background: #000;
    border-radius: 4px;
    color: #fff;
    text-transform: none;
  }
  
  /* RELEASE NOTES ROW */
  
  /* [1] Required change for custom below-the-fold light background. */
  /* Note: dark theme not enabled for Frame tenant. */
  .frame-body-light-row {
    background: #f8f9fa !important; /* [1] */
    color: #000 !important; /* [1] */
    padding-top: 40px;
    width: 100vw;
  }
  
  /* Required change to enforce custom Frame color palette. */
  .frame-body-cta {
    background: #1e431e !important;
  }
  
  /* Jumpdown Links */
  .frame-jumpdown-row {
    align-items: center;
    margin-bottom: 40px;
    margin-top: 40px;
    padding: 0;
  }
  
  .frame-jumpdown-row .frame-jumpdown-row-html {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  
  .frame-jumpdown-row a {
    color: var(--tenant-primary-text-color);
    padding: 20px;
    text-decoration: none;
  }
  
  .frame-jumpdown-row a:hover,
  .frame-jumpdown-row a:focus {
    color: #0c713a;
  }
  
  .frame-jumpdown-row .material-icons {
    font: 400 22px 'Material Icons';
    margin-inline-start: 8px;
    vertical-align: text-bottom;
  }
```
site/en/frame.css

## 500 - en/_index.yaml

Inside the repository https://github.com/creations-global/frame/site/en/, create a file called ```_index.yaml``` with the following content:

```
project_path: /_project.yaml
book_path: /_book.yaml

keywords:
- docType:Product
page_type: Product

landing_page:
  header:
    hide_lower_section: true
  custom_css_path: /frame.css

  rows:

  # Hero Row
  - options:
    - description-50
    - hero
    - large-headings
    - no-image-background
    classname: frame-hero-full-bleed-light
    items:
    - classname: frame-hero
      image_path: /images/frame_hero.svg
      heading: >
        &#123; Catchphrase &#125; — Logline
      description: >
        From startup to enterprise, choose the Frame open source project to build and test your
        multi-language, multi-platform projects.
      buttons:
      - label: Install Frame
        path: /install/
        classname: button frame-button-light

  # Why Frame? Row
  - options:
    - no-image-background
    - large-headings
    classname: frame-hero-full-bleed-dark frame-hero
    items:
    - heading: Build better
      description: >
        Rebuild only what is necessary. Get fast, incremental builds with Frame's advanced local and distributed caching, optimized dependency analysis, and parallel execution.
      icon:
        name: speed
        position: top
        size: medium
    - heading: Multilingual magic
      description: >
        Build and test using Java, C++, Go, Android, iOS and many other languages and platforms. Frame runs on Windows, macOS, and Linux.
      icon:
        name: language
        position: top
        size: medium
    - heading: Simply scalable
      description: >
        Scale your organization, codebase, and Continuous Integration systems. Frame handles codebases of any size, whether in multiple repositories or a huge monorepo.
      icon:
        name: fit_screen
        position: top
        size: medium
    - heading: Endlessly extensible
      description: >
        Add support for new languages and platforms with Frame's extension language. Share and re-use language rules written by the growing Frame community.
      icon:
        name: hub
        position: top
        size: medium

  # Essential Row
  - options:
    - no-image-background
    - description-50
    - large-headings
    classname: frame-body-light-cards
    items_across: 4
    items:
    - heading: Get started
      path: ''
      image_path: /images/essential_start.svg
      description: >
        Learn what Frame is, why it is a good choice for your project, and how you can get started
        using it quickly.
      buttons:
      - label: Get started
        path: /start/
        classname: button frame-button-dark
    - heading: User's guide
      path: ''
      image_path: /images/essential_guide.svg
      description: >
        Learn how to use Frame with documentation and tutorials covering topics from foundational to
        expert.
      buttons:
      - label: Read the docs
        path: /docs/
        classname: button frame-button-dark
    - heading: Reference guide
      path: ''
      image_path: /images/essential_reference.svg
      description: >
        Use these resources to efficiently look up the commands, queries, and terminology necessary to working with Frame.
      buttons:
      - label: Search the guide
        path: /reference/
        classname: button frame-button-dark
    - heading: Essential Frame<br><b>—</b>
      path: ''
      description: >
        Build and test software of any size, quickly and reliably. Industry leaders like Google,
        Stripe, and Dropbox trust Frame to build heavy-duty, mission-critical infrastructure,
        services, and applications.

  # Release notes Row
  - options:
    - large-headings
    - description-50
    - no-image-background
    classname: frame-body-light-row
    items:
    - image_left: true
      image_path: /images/release_notes.svg
      heading: <br><br>Release notes<br><b>—</b>
      path: ''
      description: >
        Frame is always evolving — check the release notes to see what's changed in the latest
        releases, and how that affects your builds.
      buttons:
      - label: View notes
        path: https://github.com/creationsglobal/frame/releases/latest
        classname: button frame-button-dark

  # What's new Row
  - options:
    - no-image-background
    - description-50
    - large-headings
    classname: frame-body-light-cards
    items:
    - heading: What's new?<br><b>—</b>
      description: >
        Catch up on the latest documentation, community events, and programs.
    - heading: Roadmap
      path: /about/roadmap
      image_path: /images/new_1.svg
      description: >
        Read our new public roadmap to see what is coming down the pipeline.
    - heading: Community updates
      path: /community/update
      image_path: /images/new_3.svg
      description: >
        Tune in for our new monthly community update livestream.
    - heading: Query quickstart tutorial
      path: /query/quickstart
      image_path: /images/new_2.svg
      description: >
        Get started with the Frame query language with this new guided scenario.

  - options:
    - cta
    classname: frame-body-cta
    items:
    - heading: Trusted by industry leaders
      description: >
        When you build software with Frame, you're running the same code that has been refined and
        tested for years at Google to build heavy-duty, mission-critical infrastructure, services,
        and applications.
      buttons:
      - label: Who's using Frame
        path: /community/users
        classname: button frame-button-light
```
site/en/_index.yaml

# Thai-Lao-border-police-Chiang-Khan.
https://th.wikipedia.org/wiki/%E0%B8%AA%E0%B8%B3%E0%B8%99%E0%B8%B1%E0%B8%81%E0%B8%87%E0%B8%B2%E0%B8%99%E0%B8%95%E0%B8%B3%E0%B8%A3%E0%B8%A7%E0%B8%88%E0%B9%81%E0%B8%AB%E0%B9%88%E0%B8%87%E0%B8%8A%E0%B8%B2%E0%B8%95%E0%B8%B4_(%E0%B9%84%E0%B8%97%E0%B8%A2)
<!-- wp:list {"ordered":true,"className":"prc-Breadcrumbs-BreadcrumbsList-BKjpe"} -->
<ol class="wp-block-list prc-Breadcrumbs-BreadcrumbsList-BKjpe"><!-- wp:list-item -->
<li><a class="ws-normal prc-Breadcrumbs-Item-jcraJ selected" href="https://github.com/marketplace/actions/github-wiki-action#"> Wiki Action</a></li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:heading {"level":1,"className":"marketplace-module__OverviewHeading__wixgR"} -->
<h1 class="wp-block-heading marketplace-module__OverviewHeading__wixgR">GitHub Wiki Action</h1>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Actions</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="https://github.com/login?return_to=%2Fmarketplace%2Factions%2Fgithub-wiki-action" class="prc-Button-ButtonBase-9n-Xk"></a></p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":1,"className":"heading-element"} -->
<h1 class="wp-block-heading heading-element">Publish to GitHub wiki</h1>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><a class="anchor" href="https://github.com/marketplace/actions/github-wiki-action#publish-to-github-wiki"></a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>📖 GitHub Action to sync a folder to the GitHub wiki</p>
<!-- /wp:paragraph -->

<!-- wp:image {"linkDestination":"custom"} -->
<figure class="wp-block-image"><a href="https://user-images.githubusercontent.com/61068799/231881220-2915f956-dbdb-4eee-8807-4eba9537523f.png" target="_blank" rel="noreferrer noopener"><img src="https://user-images.githubusercontent.com/61068799/231881220-2915f956-dbdb-4eee-8807-4eba9537523f.png" alt=""/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>📂 Keep your dev docs in sync with your code<br />💡 Inspired by&nbsp;<a href="https://github.com/Decathlon/wiki-page-creator-action/issues/11">Decathlon/wiki-page-creator-action#11</a><br />🔁 Able to open PRs with docs updates<br />✨ Use the fancy GitHub wiki reader UI for docs<br />🌐 Works across repositories (with a&nbsp;<a href="https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token">PAT</a>)<br />💻 Supports&nbsp;<code>runs-on: windows-*</code></p>
<!-- /wp:paragraph -->

<!-- wp:heading {"className":"heading-element"} -->
<h2 class="wp-block-heading heading-element">Usage</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><a class="anchor" href="https://github.com/marketplace/actions/github-wiki-action#usage"></a></p>
<!-- /wp:paragraph -->

<!-- wp:image {"linkDestination":"custom"} -->
<figure class="wp-block-image"><a href="https://camo.githubusercontent.com/5ceb0030e5e7d5d8a50814dbe3c2fc8e580ecefc22b464b1a6c43c1018b33e1b/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f7374796c653d666f722d7468652d6261646765266d6573736167653d4769744875622b416374696f6e7326636f6c6f723d323038384646266c6f676f3d4769744875622b416374696f6e73266c6f676f436f6c6f723d464646464646266c6162656c3d" target="_blank" rel="noreferrer noopener"><img src="https://camo.githubusercontent.com/5ceb0030e5e7d5d8a50814dbe3c2fc8e580ecefc22b464b1a6c43c1018b33e1b/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f7374796c653d666f722d7468652d6261646765266d6573736167653d4769744875622b416374696f6e7326636f6c6f723d323038384646266c6f676f3d4769744875622b416374696f6e73266c6f676f436f6c6f723d464646464646266c6162656c3d" alt="GitHub Actions"/></a></figure>
<!-- /wp:image -->

<!-- wp:image {"linkDestination":"custom"} -->
<figure class="wp-block-image"><a href="https://camo.githubusercontent.com/ec79a3c1721b63b606eafdc1571bd3618a665675ce24e1f036838c62e43c6154/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f7374796c653d666f722d7468652d6261646765266d6573736167653d47697448756226636f6c6f723d313831373137266c6f676f3d476974487562266c6f676f436f6c6f723d464646464646266c6162656c3d" target="_blank" rel="noreferrer noopener"><img src="https://camo.githubusercontent.com/ec79a3c1721b63b606eafdc1571bd3618a665675ce24e1f036838c62e43c6154/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f7374796c653d666f722d7468652d6261646765266d6573736167653d47697448756226636f6c6f723d313831373137266c6f676f3d476974487562266c6f676f436f6c6f723d464646464646266c6162656c3d" alt="GitHub"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Add a GitHub Actions workflow file to your&nbsp;<code>.github/workflows/</code>&nbsp;folder similar to the example shown below.</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">name: Publish wiki
on:
  push:
    branches: [main]
    paths:
      - wiki/**
      - .github/workflows/publish-wiki.yml
concurrency:
  group: publish-wiki
  cancel-in-progress: true
permissions:
  contents: write
jobs:
  publish-wiki:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v7
      - uses: Andrew-Chen-Wang/github-wiki-action@v5</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>☝ This workflow will mirror the&nbsp;<code>wiki/</code>&nbsp;folder in your GitHub repository to the&nbsp;<code>user/repo.wiki.git</code>&nbsp;Git repo that houses the wiki documentation! You can use any of the&nbsp;<a href="https://github.com/github/markup#markups">supported markup languages</a>&nbsp;like MediaWiki, Markdown, or AsciiDoc.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>🔑 In order to successfully push to the&nbsp;<code>.wiki.git</code>&nbsp;Git repository that backs the wiki tab, we need the&nbsp;<code>contents: write</code>&nbsp;permission! Make sure you have something like shown above either for your entire workflow, or just for one particular job. This will give the auto-generated&nbsp;<code>${{ github.token }}</code>&nbsp;that we use by default permission to push to the&nbsp;<code>.wiki.git</code>&nbsp;repo of the repository that the action runs on.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"linkDestination":"custom"} -->
<figure class="wp-block-image"><a href="https://camo.githubusercontent.com/5518449e49396838b061601cfdaaeaa510fd25ec14a45f6637e0f5c3108132ac/68747470733a2f2f692e696d6775722e636f6d2f41424b495334682e706e67" target="_blank" rel="noreferrer noopener"><img src="https://camo.githubusercontent.com/5518449e49396838b061601cfdaaeaa510fd25ec14a45f6637e0f5c3108132ac/68747470733a2f2f692e696d6775722e636f6d2f41424b495334682e706e67" alt="Screenshot of 'Create the first page' button"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>⚠️&nbsp;You must create a dummy page manually! This is what initially creates the GitHub wiki Git-based storage backend that we then push to in this Action.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>After creating your workflow file, now all you need is to put your Markdown files in a&nbsp;<code>wiki/</code>&nbsp;folder (or whatever you set the&nbsp;<code>path</code>&nbsp;option to) and commit them to your default branch to trigger the workflow (or whatever other trigger you set up).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>💡 Each page has an auto-generated title. It is derived from the filename by replacing every&nbsp;<code>-</code>&nbsp;(dash) character with a space. Name your files accordingly. The&nbsp;<code>Home.md</code>&nbsp;file will automatically become the homepage, not&nbsp;<code>README.md</code>. This is specific to GitHub wikis.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3,"className":"heading-element"} -->
<h3 class="wp-block-heading heading-element">Inputs</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><a class="anchor" href="https://github.com/marketplace/actions/github-wiki-action#inputs"></a></p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li><strong><code>direction</code>:</strong> Select from <code>push</code> or <code>pull</code>. <code>push</code> (the default) syncs the <code>path</code> folder to the GitHub wiki. <code>pull</code> does the reverse: it clones the wiki, converts the pages back into source-friendly form (<code>Home.md</code> becomes <code>README.md</code> and bare wiki page links get the extension of the page they target back), and mirrors them into the <code>path</code> folder of your workspace. The <code>ignore</code> input is not applied in pull mode. Nothing is committed or pushed to your repository in pull mode; pair it with a PR-creating action like <a href="https://github.com/peter-evans/create-pull-request">create-pull-request</a>. See <a href="https://github.com/marketplace/actions/github-wiki-action#pulling-wiki-edits-back">Pulling wiki edits back</a> below.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>strategy</code>:</strong> Select from <code>clone</code> or <code>init</code> to determine which method to use to push changes to the GitHub wiki. <code>clone</code> will clone the <code>.wiki.git</code> repo and add an additional commit. <code>init</code> will create a new repo with a single commit and force push to the <code>.wiki.git</code>. <code>init</code> involves a force-push! The default is <code>clone</code>.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>repository</code>:</strong> The repository housing the wiki. Use this if you're publishing to a wiki that's not the current repository. You can change the GitHub server with the <code>github-server-url</code> input. Default is <code>${{ github.repository }}</code>.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>github-server-url</code>:</strong> An alternate <code>https://github.com</code> URL, usually for GitHub Enterprise deployments under your own domain. Default is <code>${{ github.server_url }}</code> (usually <code>https://github.com</code>).</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>token</code>:</strong> <code>${{ github.token }}</code> is the default. This token is used when cloning and pushing wiki changes.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>path</code>:</strong> The directory to use for your wiki contents. Default <code>wiki/</code>.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>commit-message</code>:</strong> The message to use when committing new content. Default is <code>Update wiki ${{ github.sha }}</code>. You probably don't need to change this, since this only applies if you look really closely in your wiki.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>ignore</code>:</strong> A multiline list of files that should be ignored when committing and pushing to the remote wiki. Each line is a pattern like <code>.gitignore</code>. Make sure these paths are relative to the path option! The default is none.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>dry-run</code>:</strong> Whether or not to actually attempt to push changes back to the wiki itself. If this is set to <code>true</code>, we instead print the remote URL and do not push to the remote wiki. The default is <code>false</code>. This is useful for testing.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>preprocess</code>:</strong> If this option is true, we will preprocess the wiki to move the <code>README.md</code> to <code>Home.md</code> as well as rewriting links to wiki pages to be bare links. Link targets in any markup format GitHub renders (<code>.md</code>, <code>.rst</code>, <code>.adoc</code>, ...) are recognized, though only Markdown files are parsed for links. Relative links that point at other files in your repository (a script, a source file, a Markdown file outside the wiki folder) are rewritten to full <code>blob/</code> view URLs (<code>raw/</code> URLs for images) pinned to the pushed commit, the same way GitHub resolves them when rendering in-repo Markdown. This helps ensure that the Markdown works in source control as well as the wiki. The default is true. See <a href="https://github.com/marketplace/actions/github-wiki-action#preprocess-notes"><code>preprocess:</code> notes</a>.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong><code>disable-empty-commits</code>:</strong> By default, any triggering of this action will result in a commit to the Wiki, even if that commit is empty. If this option is true, a workflow run which would result in no changes to the Wiki files, will no longer create an empty commit. The default is false.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:heading {"level":4,"className":"heading-element"} -->
<h4 class="wp-block-heading heading-element"><code>preprocess:</code>&nbsp;notes</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><a class="anchor" href="https://github.com/marketplace/actions/github-wiki-action#preprocess-notes"></a></p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li>Only Markdown pages are parsed for links; pages in other formats (<code>.rst</code>, <code>.adoc</code>, ...) are synced verbatim but still recognized as link targets.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>GitHub serves wiki pages flat by basename, so cross-directory page links are rewritten to bare page names, while same-directory links keep their form. Reference-style definitions (<code>[label]: ./page.md</code>) are rewritten like the links or images that use them.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>Images pointing at repository files become <code>raw/</code> URLs (a <code>blob/</code> page would not render inside an image); images shipped inside the wiki folder stay relative.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>A page whose name itself ends in a renderable extension (say a page called <code>example.org</code>) is treated as a file link rather than a page link.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:heading {"level":4,"className":"heading-element"} -->
<h4 class="wp-block-heading heading-element"><code>strategy:</code>&nbsp;input</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><a class="anchor" href="https://github.com/marketplace/actions/github-wiki-action#strategy-input"></a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There are some specific usecases where using&nbsp;<code>strategy: init</code>&nbsp;might be better than the default&nbsp;<code>strategy: clone</code>.</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol class="wp-block-list"><!-- wp:list-item -->
<li><strong>Your wiki is enormous.</strong> And I don't mean in terms of text. Text is nothing compared with images. If your wiki has a lot of included images, then you probably don't want to store the complete history of those large binary files. Instead, you can use <code>strategy: init</code> to create a single commit each time.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li><strong>You prefer the "deploy" semantics.</strong> If you just like the feel of having your GitHub wiki act more like GitHub Pages, that's great! You can <code>--force</code> push using <code>strategy: init</code> on each wiki deployment and none of that pesky history will be saved.</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:heading {"level":3,"className":"heading-element"} -->
<h3 class="wp-block-heading heading-element">Outputs</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><a class="anchor" href="https://github.com/marketplace/actions/github-wiki-action#outputs"></a></p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul class="wp-block-list"><!-- wp:list-item -->
<li><strong><code>wiki_url</code>:</strong> The HTTP URL that points to the deployed repository's wiki tab. This is essentially the concatenation of <code>${{ github.server_url }}</code>, <code>${{ github.repository }}</code>, and the <code>/wiki</code> page.</li>
<!-- /wp:list-item --></ul>
<!-- /wp:list -->

<!-- wp:heading {"level":3,"className":"heading-element"} -->
<h3 class="wp-block-heading heading-element">Pulling wiki edits back</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><a class="anchor" href="https://github.com/marketplace/actions/github-wiki-action#pulling-wiki-edits-back"></a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If someone edits a page in the wiki UI, those edits normally get overwritten by the next push from your&nbsp;<code>wiki/</code>&nbsp;folder.&nbsp;<code>direction: pull</code>&nbsp;lets you sync them back into your source tree instead. It clones the wiki, applies the inverse of the&nbsp;<code>preprocess</code>&nbsp;transformations (<code>Home.md</code>&nbsp;➡&nbsp;<code>README.md</code>,&nbsp;<code>./page</code>&nbsp;➡&nbsp;<code>./page.md</code>), and updates the&nbsp;<code>path</code>&nbsp;folder in your workspace. It never commits or pushes to your repository, so combine it with something like&nbsp;<a href="https://github.com/peter-evans/create-pull-request">create-pull-request</a>&nbsp;to open a docs PR:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">name: Pull wiki
on:
  gollum: # Runs whenever a wiki page is created or edited
  workflow_dispatch:
permissions:
  contents: write
  pull-requests: write
jobs:
  pull-wiki:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v7
      - uses: Andrew-Chen-Wang/github-wiki-action@v5
        with:
          direction: pull
      - uses: peter-evans/create-pull-request@v8
        with:
          branch: sync-wiki
          title: Sync wiki edits back into wiki/
          commit-message: Sync wiki edits back into wiki/</pre>
<!-- /wp:preformatted -->

<!-- wp:heading {"level":3,"className":"heading-element"} -->
<h3 class="wp-block-heading heading-element">Cross-repo wikis</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><a class="anchor" href="https://github.com/marketplace/actions/github-wiki-action#cross-repo-wikis"></a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>You&nbsp;<em>can</em>&nbsp;use this action to deploy your octocat/mega-docs repository to the octocat/mega-project repository's wiki tab! You just need to:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol class="wp-block-list"><!-- wp:list-item -->
<li>Create a custom GitHub Personal Access Token with the permissions to push to the octocat/mega-project repository. That's the target repo where your wiki pages will be pushed to the <code>.wiki.git</code>.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>In the octocat/mega-docs repo (the source code for the wiki), you need to set the <code>repository:</code> option to <code>repository: octocat/mega-project</code> to tell the action to push there.</li>
<!-- /wp:list-item -->

<!-- wp:list-item -->
<li>You need to set the <code>token:</code> option to the Personal Access Token that you created with the ability to push to the wiki Git repo. You can use repository secrets for this! Something like <code>token: ${{ secrets.MY_TOKEN }}</code> is good!</li>
<!-- /wp:list-item --></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Here's an example of the octocat/mega-docs repo that will push the contents of the root folder (<code>./</code>) to the octocat/mega-project repo's wiki tab!</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">on:
  push:
    branches: [main]
jobs:
  publish-wiki:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v7
      - uses: Andrew-Chen-Wang/github-wiki-action@v5
        with:
          token: ${{ secrets.MEGA_PROJECT_GITHUB_TOKEN }}
          repository: octocat/mega-project
          path: .</pre>
<!-- /wp:preformatted -->

<!-- wp:heading {"className":"heading-element"} -->
<h2 class="wp-block-heading heading-element">Development</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><a class="anchor" href="https://github.com/marketplace/actions/github-wiki-action#development"></a></p>
<!-- /wp:paragraph -->

<!-- wp:image {"linkDestination":"custom"} -->
<figure class="wp-block-image"><a href="https://camo.githubusercontent.com/4f473d47bffb9e493ce2644faf37aedac33cb9d5c901d790ca785d7e00058f2e/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f7374796c653d666f722d7468652d6261646765266d6573736167653d44656e6f26636f6c6f723d303030303030266c6f676f3d44656e6f266c6f676f436f6c6f723d464646464646266c6162656c3d" target="_blank" rel="noreferrer noopener"><img src="https://camo.githubusercontent.com/4f473d47bffb9e493ce2644faf37aedac33cb9d5c901d790ca785d7e00058f2e/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f7374796c653d666f722d7468652d6261646765266d6573736167653d44656e6f26636f6c6f723d303030303030266c6f676f3d44656e6f266c6f676f436f6c6f723d464646464646266c6162656c3d" alt="Deno"/></a></figure>
<!-- /wp:image -->

<!-- wp:image {"linkDestination":"custom"} -->
<figure class="wp-block-image"><a href="https://camo.githubusercontent.com/5ceb0030e5e7d5d8a50814dbe3c2fc8e580ecefc22b464b1a6c43c1018b33e1b/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f7374796c653d666f722d7468652d6261646765266d6573736167653d4769744875622b416374696f6e7326636f6c6f723d323038384646266c6f676f3d4769744875622b416374696f6e73266c6f676f436f6c6f723d464646464646266c6162656c3d" target="_blank" rel="noreferrer noopener"><img src="https://camo.githubusercontent.com/5ceb0030e5e7d5d8a50814dbe3c2fc8e580ecefc22b464b1a6c43c1018b33e1b/68747470733a2f2f696d672e736869656c64732e696f2f7374617469632f76313f7374796c653d666f722d7468652d6261646765266d6573736167653d4769744875622b416374696f6e7326636f6c6f723d323038384646266c6f676f3d4769744875622b416374696f6e73266c6f676f436f6c6f723d464646464646266c6162656c3d" alt="GitHub Actions"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>This GitHub Action uses a self-downloaded version of Deno. See&nbsp;<code>cliw</code>&nbsp;for the&nbsp;<code>cli.ts</code>&nbsp;wrapper script that downloads the Deno binary and runs the TypeScript code. The main script itself is ~100 lines of code, so it's not too bad.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>ℹ Because the version of Deno is&nbsp;<em>pinned</em>, it's recommended to every-so-often bump it to the latest version.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To test the action, open a PR! The&nbsp;<code>test-action.yml</code>&nbsp;workflow will run the code with&nbsp;<code>dry-run: true</code>&nbsp;as well as a real run! Yes, this does get tedious swapping between your IDE and the PR, but it's the easiest way to test the action</p>
<!-- /wp:paragraph -->

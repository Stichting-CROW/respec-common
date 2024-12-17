# Common files for ReSpec specifications

This repository is meant to be used as a submodule in multiple repositories that use CROW's ReSpec.

## Usage

1. `cd docs/` or any other folder that is deployed to GitHub Pages
1. `git submodule add https://github.com/stichting-crow/respec-common.git`
1. In `index.html`, add:

   ```diff
     <title>Informatiemodel verkeerstekens: Beheerplan</title>
   + <script src="../respec-common/local-biblio.js" class="remove"></script>
     <script src="config.js" class="remove"></script>
   ```

1. In `config.js`, replace:

   ```diff
   - localBiblio: { ...
   - },
   + localBiblio: window.localBibliography,
   ```

1. Commit and enjoy.

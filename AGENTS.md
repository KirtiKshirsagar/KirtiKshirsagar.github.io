<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

## Deployment
- GitHub Pages deploys via .github/workflows/deploy.yml (bun + static prerender of "/" into dist/client, which the workflow uploads). vite.config.ts enables tanstackStart prerender; the nitro preset stays Lovable's default — don't add a static preset, it breaks the nitro Vite environment build.
- GitHub Pages serves this site at the domain root (user-site repo named KirtiKshirsagar.github.io), so CI builds with the default base — never pass --base=/KirtiKshirsagar/, which breaks asset URLs at the root. Live URL: https://kirtikshirsagar.github.io/

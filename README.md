# storyvox-registry

Curated list of public-domain or author-released fictions that show up in storyvox's **Browse → GitHub → Featured** row.

Storyvox fetches `https://raw.githubusercontent.com/jphein/storyvox-registry/main/registry.json` once per session and caches it in memory.

## Adding a fiction

1. The fiction must live in a public GitHub repo with **at least one** of:
   - `book.toml` (mdbook-style) + `SUMMARY.md`
   - `storyvox.json` manifest
   - bare markdown files (the BareRepoFallback handles numeric prefixes like `01-intro.md`)
2. Add an entry to the `fictions` array in `registry.json`, with at least:
   - `id` (`github:OWNER/REPO`)
   - `title`, `author`
   - `description` (short, one paragraph)
   - `cover_url` (raw.githubusercontent.com URL)
   - `tags` (lowercase strings)
3. Open a PR. The curated list is hand-reviewed before merge — quality over breadth.

See [the schema](https://github.com/jphein/storyvox/blob/main/source-github/src/main/kotlin/in/jphe/storyvox/source/github/registry/RegistryModels.kt) for the full set of supported fields.

## Author rights

Listing here doesn't transfer rights. The fiction stays in the author's repo under whatever license the author chose; storyvox just points at it. Authors can ask to be removed at any time.

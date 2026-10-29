# Sunburst for Zed

Sunburst is a Zed theme extension ported from the original [TextMate Sunburst theme by Soryu](https://github.com/Soryu/Sunburst), by way of this repository’s older Atom syntax theme.

This repo now contains a working Zed theme extension:

- `extension.toml` — Zed extension manifest
- `themes/sunburst.json` — Zed theme family definition
- `index.less` — original Atom theme source kept for reference while refining the port
- `package.json` — original Atom package metadata kept for historical context

## Included theme

- `Sunburst` (`dark`)

## Local testing in Zed

1. Open Zed.
2. Run `zed: install dev extension` from the command palette, or open the Extensions page and click **Install Dev Extension**.
3. Select the root of this repository.
4. Open the theme selector and choose `Sunburst`.
5. If anything fails, open `zed: open log` or relaunch Zed with `zed --foreground` to inspect extension loading logs.

## Submission notes for your fork

The central [`zed-industries/extensions`](https://github.com/zed-industries/extensions) repository tracks extensions as submodules listed in its root `extensions.toml`.

A typical submission flow for your fork at `https://github.com/windhamdavid/extensions` is:

1. Push this repository with the Zed extension files in place.
2. In your fork of the extensions repo, add this repository as a submodule under `extensions/sunburst-theme`.
3. Add an entry to the root `extensions.toml` similar to:

   ```toml
   [sunburst-theme]
   submodule = "extensions/sunburst-theme"
   version = "0.1.0"
   ```

4. Open a pull request from your fork.

## Notes on the port

This first Zed version aims to stay close to the original Sunburst syntax palette:

- editor background `#000000`
- editor foreground `#F8F8F8`
- comments `#AEAEAE` italic
- keywords `#E28964`
- strings `#65B042`
- entities/tags `#89BDFF`
- support/functions `#DAD085`
- variables `#3E87E3`

Some Zed UI surface colors are necessarily approximations, since the original Atom theme mainly defined syntax/editor colors rather than a full application UI system.

## License

MIT.

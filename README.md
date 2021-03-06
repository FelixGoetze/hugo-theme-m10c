# m10c theme

![Intro](images/cover.png)

A Hugo minimalistic theme for bloggers

## Changes since Fork

- Removed title from post listing.
- Changed to relative paths for image rendering for better Markdown Preview and compatibility using custom [render-image.html](https://github.com/gohugoio/hugo/issues/6545#issuecomment-655757059).
- Added basic Latex suport, enabled by including ```katex: true``` in frontmatter of a markdown page.

## Getting started

### Installation

Create a new Hugo site:
```bash
$ hugo new site [path]
```

Clone this repository into `themes/` directory:
```bash
$ cd [path]
$ git clone https://github.com/vaga/hugo-theme-m10c.git themes/m10c
```

Add this line  in the `config.toml` file:
```toml
theme = "m10c"
```

### Configuration

In your `config.toml` file, define the following variables in `params`:

- `author`: Name of the author
- `description`: Short description of the author
- `avatar`: Path of file containing the author avatar image
- `menu_item_separator`: Separator between each menu item. HTML allowed (default: " - ")

To add a menu item, add the following lines in `menu`:

```
[[menu.main]]
  identifier = "tags"
  name = "Tags"
  url = "/tags/"
```

[Read Hugo documentations](https://gohugo.io/content-management/menus/#readout) for more informations about menu

To add a social link, add the following lines in `params`:

```
[[params.social]]
  name = "github"
  url = "https://github.com/vaga"
```

To change theme colors, add the following lines in `params`:

```
[params.style]
  darkestColor = "#d35050"
  darkColor = "#212121"
  lightColor = "#f5e3e0"
  lightestColor = "#f5f5f5"
  primaryColor = "#fff"
```

If you want the above theme colors, you can see the [exampleSite/config.toml](/exampleSite/config.toml) file.

### Styling

To override styles using scss, add a file called `_extra.scss` to `{your site directory}/assets/css/`

Note: Hugo releases come in two versions, `hugo` and `hugo_extended`. You need `hugo_extended` to automatically compile your scss.

## License

This theme is released under the [**MIT**](/LICENSE.md) License.

## Acknowledgements

- [feather](https://feathericons.com/) - [MIT](https://github.com/feathericons/feather/blob/master/LICENSE)

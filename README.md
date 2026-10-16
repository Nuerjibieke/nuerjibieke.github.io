# Nuerjibieke — Academic Homepage

A personal academic homepage in three languages, based on the official HTML version of [Minimal Light](https://github.com/yaoyao-liu/minimal-light).

- English: https://nuerjibieke.github.io/
- 中文: https://nuerjibieke.github.io/zh/
- Қазақша (Cyrillic): https://nuerjibieke.github.io/kk/

Personal details and publications currently use clearly marked placeholders.

## Edit and preview

The published source is `html_source_file/`. Edit `index.html`, `zh/index.html`, and `kk/index.html` for the three languages. Run `python3 -m http.server 4173 --bind 127.0.0.1 --directory html_source_file` to preview locally.

See [START_HERE.md](START_HERE.md) for the Chinese maintenance guide.

## Deployment

GitHub Actions publishes `html_source_file/` to GitHub Pages on pushes to `main`. The remaining Jekyll files are retained upstream sources and are not published.

## Template credit

Original template: Yaoyao Liu, [Minimal Light](https://github.com/yaoyao-liu/minimal-light), commit `1ea07f39518ac44644406380c83da6f89037c4fc`.
Original license: [CC0-1.0](LICENSE). The original README is preserved in [UPSTREAM_README.md](UPSTREAM_README.md).

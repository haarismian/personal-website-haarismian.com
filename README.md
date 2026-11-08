# haarismian.com

The personal website for Haaris Mian. It's a single static page (`index.html`) hosted free on GitHub Pages.

## Editing

- All text is in `index.html`. Search for `EDIT:` to find the spots that still need real links or a photo.
- To add a photo, put `photo.jpg` in this folder and replace the "HM" placeholder block with
  `<img src="photo.jpg" alt="Haaris Mian">`.

## Going live (one-time setup)

1. Make a GitHub repository (for example `haarismian.com`) and upload these files: `index.html` and `CNAME`.
2. In the repository, open **Settings → Pages**. Under **Source**, pick "Deploy from a branch", then choose `main` and `/ (root)`.
3. In Squarespace, go to **Domains → haarismian.com → DNS → DNS Settings**:
   - Delete only the "Squarespace Defaults" website records (the `@` A records and the `www` CNAME `ext-cust.squarespace.com`).
   - **Leave all MX and TXT records alone.** Your email depends on them.
   - Add these records:

     | Host | Type | Data |
     |------|------|------|
     | @    | A    | 185.199.108.153 |
     | @    | A    | 185.199.109.153 |
     | @    | A    | 185.199.110.153 |
     | @    | A    | 185.199.111.153 |
     | www  | CNAME | `YOUR-GITHUB-USERNAME.github.io` |

4. Back in GitHub's **Settings → Pages**, confirm the custom domain reads `haarismian.com`. Once the DNS check passes, tick **Enforce HTTPS**.

DNS changes take anywhere from a few minutes to a few hours to work.

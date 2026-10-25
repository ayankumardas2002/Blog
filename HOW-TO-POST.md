# The Occasional: setup and posting guide

This is a free, public blog that runs on GitHub Pages. You don't need any paid service. Posts can go live right away or on a date and time you choose.

---

## Part 1: Put the blog online (one time, about 10 minutes)

1. **Create a GitHub account** at <https://github.com/signup> if you don't have one. It's free.
2. **Create a repository.** Click **+** (top right) → **New repository**.
   - Name it, for example `blog`.
   - Set it to **Public**. GitHub Pages is free only for public repositories.
   - Click **Create repository**.
3. **Upload the files.** On the new repository page, click **uploading an existing file**. Drag in *everything* from this folder, including the hidden `.github` folder, then click **Commit changes**.
   - On a Mac, press `Cmd + Shift + .` in Finder to show hidden folders like `.github`.
   - On Windows, turn on **View → Show → Hidden items** in File Explorer.
4. **Turn on Pages.** In the repository, go to **Settings → Pages**. Under **Build and deployment → Source**, choose **GitHub Actions**.
5. **Wait 1–2 minutes**, then open the **Actions** tab. When "Publish blog" shows a green tick, your blog is live at:
   `https://YOUR-USERNAME.github.io/blog/`

### Make it yours

Open `_config.yml` on GitHub (click the file, then the ✏️ pencil icon) and change:

| Setting | What it is |
|---|---|
| `title` | The blog's name |
| `tagline` | The line under the name |
| `author` | Your name, shown in the footer |
| `timezone` | **Important.** Your time zone, so scheduled posts go out at your local time. Examples: `Asia/Kolkata`, `Europe/London`, `America/New_York` |

Click **Commit changes**. The site updates in about a minute.

---

## Part 2: Write a post

Every post is one text file in the `_posts` folder.

1. Open the `_posts` folder on GitHub and click **Add file → Create new file**.
2. **Name the file** with the date first, then a short name, ending in `.md`:
   `2026-11-15-my-trip-to-the-hills.md`
3. **Start the file** with this header, then write your post below it:

   ```
   ---
   title: "My trip to the hills"
   date: 2026-11-15 09:00
   ---

   Your first paragraph goes here.

   Leave a blank line between paragraphs.
   ```

4. Click **Commit changes**.

### Publish now or later

The `date:` line decides when the post appears.

- **Publish now:** use today's date and a time that has already passed. It appears within about a minute.
- **Schedule for later:** use a future date and time. The post stays hidden and appears on its own at that time, within an hour, because the blog rebuilds itself every hour. You don't need to be online.
- **Draft:** put the file in the `_drafts` folder instead. Drafts are never published.

To publish a draft, move it to `_posts`, give the file name a date at the front and add a `date:` line.

### Formatting

| You type | You get |
|---|---|
| `## Heading` | A section heading |
| `**bold**` | **bold** |
| `*italic*` | *italic* |
| `[link text](https://example.com)` | a link |
| `- item` | a bullet list |
| `> quote` | a quote |
| `![photo description](/blog/assets/photo.jpg)` | an image (upload the image to the `assets` folder first; replace `blog` with your repository name) |

### Edit or delete a post

Open the file in `_posts`, then click ✏️ to edit or 🗑️ to delete. Commit, and the site updates.

---

## Good to know

- **Scheduled posts are not secret.** The repository is public, so anyone who looks at the files on GitHub can read a scheduled post or draft before it goes live. Only the *blog website* hides them.
- **Keep the schedule running.** GitHub pauses hourly jobs in a repository that has had no changes for 60 days, and emails you before it happens. Adding or editing any post keeps it running. If it does pause, open the **Actions** tab, click **Publish blog** and click **Enable workflow**.
- **Publish immediately.** To rebuild right away without waiting for the hourly run, go to **Actions → Publish blog → Run workflow**.
- **Readers can subscribe.** The RSS feed at `/feed.xml` lets people follow the blog in a feed reader.
- **Remove the examples.** Delete `_posts/2026-10-25-welcome.md`, `_posts/2027-01-01-example-scheduled-post.md` and `_drafts/example-draft.md` when you add your own posts.

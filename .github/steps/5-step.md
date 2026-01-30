## Step 5: Preview Your Collection Locally

Excellent! Your site is configured. Now for the exciting part—let's **build and preview** your collection in the browser!

### 📖 Theory: Jekyll, Ruby, and the Terminal

CollectionBuilder uses several technologies to build your site:

- **Ruby** - A programming language
- **Bundler** (`bundle`) - A Ruby tool that manages dependencies (libraries your project needs)
- **Jekyll** - A static site generator (written in Ruby) that builds HTML from your metadata and templates

The **terminal** is a text-based interface where you type commands. In VS Code, the terminal appears at the bottom of the screen. Don't worry—you'll only need to run a few simple commands!

The workflow is:
1. `bundle install` - Install all dependencies (you only do this once)
2. `bundle exec jekyll serve` - Build your site and start a local web server
3. Open the preview in your browser

> [!TIP]
> The `jekyll serve` command watches for file changes and automatically rebuilds your site. Leave it running while you work!

### ⌨️ Activity: Build and Preview Your Collection

Let's see your Psychiana collection come to life!

**Part 1: Open the Terminal**

1. Look at the **bottom** of your Codespace window
2. You should see a panel with tabs like "TERMINAL", "OUTPUT", "PORTS", etc.
3. Click the **TERMINAL** tab
   - If you don't see it, go to the menu: **Terminal → New Terminal**

You'll see a command prompt (something like `@username ➜ /workspaces/repository-name $`). This is where you type commands!

**Part 2: Install Dependencies**

1. In the terminal, type (or copy and paste) this command and press **Enter**:

```bash
bundle install
```

This installs all the Ruby gems (libraries) your site needs. It may take 1-2 minutes. You'll see lots of output—that's normal! Wait for it to finish.

> [!NOTE]
> You only need to run `bundle install` once (or when dependencies change). Don't worry if you see some warnings—as long as it says "Bundle complete!" at the end, you're good.

**Part 3: Start the Jekyll Server**

1. Once `bundle install` finishes, run this command:

```bash
bundle exec jekyll serve
```

This builds your site and starts a local web server. You'll see output ending with something like:

```
Server address: http://127.0.0.1:4000
Server running... press ctrl-c to stop.
```

2. Look for a **pop-up notification** in the bottom-right that says "Open in Browser" and **click it**
   - If you miss it, click the **PORTS** tab (next to TERMINAL) and click the globe icon 🌐 next to port 4000

**Part 4: Explore Your Collection!**

Your Psychiana collection should now open in a new browser tab! Check out:
- The home page with your new title and tagline
- The **Browse** page (all items from your CSV)
- The **Map** page (items with coordinates)
- The **Timeline** page
- Click on an item to see its detail page
- Look for the item you edited in Step 3!

> [!IMPORTANT]
> Leave the Jekyll server running! The terminal will show server activity. When you're ready to continue, come back to this tab.

**Part 5: Stop the Server and Mark Complete**

When you're done exploring:

1. Go back to the **TERMINAL** tab in VS Code
2. Press `Ctrl+C` to stop the Jekyll server
   - You'll see the command prompt return

3. Now let's mark this step complete by creating a marker file. Run these commands:

```bash
echo "Previewed collection locally" > .preview-complete
```

4. Use **Source Control** to commit this marker:
   - Open Source Control panel
   - Stage `.preview-complete`
   - Commit message: `Complete local preview`
   - Sync to GitHub

Wait for Mona to check your work! 🤖

<details>
<summary>Having trouble? 🤷</summary><br/>

- **Can't find the terminal?** Go to menu **Terminal → New Terminal**
- **bundle install fails?** Try running it again—sometimes downloads time out
- **Port 4000 already in use?** Jekyll will try port 4001, 4002, etc.—that's fine!
- **Don't see the pop-up?** Click the PORTS tab and click the globe icon next to the port number
- **Errors about missing files?** Make sure you completed Step 4 correctly (`metadata: psychiana`)
- **To stop Jekyll**: Press `Ctrl+C` in the terminal (not `Cmd+C` on Mac!)
- **Forgot to create marker file?** Just run the echo command again and recommit

</details>

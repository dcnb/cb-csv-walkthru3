## Step 3: Edit Collection Metadata

Now that you understand the CSV structure, let's make a change! You'll edit metadata and commit it using the Source Control panel you learned in Step 1.

### 📖 Theory: Why Metadata Matters

Metadata is the foundation of your digital collection. When you change metadata:

- **Item pages update** - Titles, descriptions, and details change
- **Search results change** - Updated text becomes searchable
- **Maps recalculate** - If you edit latitude/longitude
- **Timelines adjust** - If you edit dates

CollectionBuilder is **metadata-driven**, meaning the CSV controls everything. Change the data, change the site!

> [!IMPORTANT]
> Always keep your `objectid` values unique and consistent. They're used to link metadata to digital files and generate item URLs. Never use spaces or special characters in objectid values!

> [!TIP]
> **Real-world workflow:** When working on a real CollectionBuilder project, most people create their metadata in **Google Sheets**, which makes it easy to:
> - Collaborate with team members
> - Use data validation to ensure consistent formatting
> - Sort and filter to find items quickly
> - Download as CSV when ready to add to your site
>
> Learn more in the [CollectionBuilder Metadata docs](https://collectionbuilder.github.io/cb-docs/docs/metadata/csv_metadata/).

### ⌨️ Activity: Customize an Item

Let's personalize item `psychiana001` by changing its title.

**Part 1: Edit the Metadata**

1. In your Codespace, open `_data/psychiana.csv` (if not already open)
2. Find the row for `psychiana001` (should be the first data row after the header)
3. Locate the `title` column (second column)
4. Change the title to something creative! For example:
   - Original: `Frank Robinson and his electric machine`
   - Your version: `Frank Robinson's Revolutionary Electric Machine` (or make up your own!)
5. **Save the file** (`Ctrl+S` or `Cmd+S`)

> [!NOTE]
> When editing CSV files in text editors, be careful not to accidentally delete commas or quotation marks—they're part of the file structure! If a field contains a comma, it must be wrapped in quotes.

**Part 2: Commit Using Source Control**

Now let's save your change using the same Source Control workflow from Step 1!

1. Click the **Source Control** icon in the left sidebar (branch icon with three circles)
   - You should see `psychiana.csv` listed under "Changes"

2. **Stage the file**: Hover over `_data/psychiana.csv` and click the **+** button
   - The file moves to "Staged Changes"

3. **Write your commit message**: In the message box at the top, type:
   ```
   Update metadata for psychiana001
   ```

4. **Commit**: Click the **Commit** button

5. **Sync**: Click **Sync Changes** to push to GitHub

> [!TIP]
> You can stage multiple files at once by clicking the + button next to "Changes" (stages all files). But for learning, it's good to stage files individually so you understand what's being committed!

**Want to explore more?** The [CollectionBuilder Metadata documentation](https://collectionbuilder.github.io/cb-docs/docs/metadata/csv_metadata/) has great examples of:
- How to format dates for the timeline feature
- How to add latitude/longitude for map points
- How to use semicolons to separate multiple subjects
- Best practices for writing descriptions

Wait for Mona to check your work! 🤖

<details>
<summary>Having trouble? 🤷</summary><br/>

- Make sure you're editing `_data/psychiana.csv`, not a different CSV file
- The title field should be easy to spot—it's the second column
- Remember to **save the file** (`Ctrl+S` or `Cmd+S`) before staging changes
- If you make a mistake, you can undo (`Ctrl+Z` or `Cmd+Z`) before saving
- After syncing, the Source Control panel should show "0" changes
- If you accidentally broke the CSV structure, you can see the original on GitHub by going to your repository and clicking on the file

</details>

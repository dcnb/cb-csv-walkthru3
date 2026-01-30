## Step 2: Explore Collection Metadata

Excellent! You've made your first commit using VS Code's Source Control panel. Now let's explore the heart of CollectionBuilder: the **metadata CSV file** that describes your digital collection.

### 📖 Theory: Metadata and CSV Files

**Metadata** means "data about data"—it's information that describes your collection items. For a digital collection, metadata includes:

- **Descriptive info**: Title, description, creator, date
- **Technical info**: Format, file location, file size
- **Administrative info**: Rights, subjects, keywords
- **Geospatial info**: Latitude, longitude (for maps!)

CollectionBuilder uses metadata to automatically generate your entire collection website. Every item, map point, timeline entry, and search result comes from your CSV file!

**CSV (Comma-Separated Values)** is a simple format for tabular data:
- Each row represents one collection item
- Each column represents one metadata field
- The first row contains column headers

CollectionBuilder reads your CSV and transforms it into:
- 📖 Item pages with details
- 🗺️ Interactive maps (using latitude/longitude)
- 📅 Timelines (using dates)
- 🔍 Search functionality
- 📊 Data visualizations

> [!TIP]
> **Real-world workflow:** Many people create and edit their metadata in **Google Sheets** (not Excel!), then download it as a CSV. Google Sheets is free, collaborative, and works great for metadata projects. You can also use Excel or LibreCalc, but Google Sheets is the most popular choice for CollectionBuilder projects.

> [!NOTE]
> CollectionBuilder requires specific metadata fields to work properly. Learn more about required and optional fields in the [CollectionBuilder Metadata Documentation](https://collectionbuilder.github.io/cb-docs/docs/metadata/csv_metadata/).

### ⌨️ Activity: Explore the Psychiana Metadata

Let's examine the metadata structure for the Psychiana collection.

1. In the Codespace **file explorer** (left sidebar), navigate to the `_data` folder
2. Click to open `psychiana.csv`

You'll see columns like:
- `objectid` - **Required** - Unique identifier for each item (no spaces, no special characters)
- `title` - **Required** - Item title
- `format` - **Required** - Media type (Image, Sound, Text, etc.)
- `filename` - **Required** - Name of the file (or external URL)
- `description` - *Optional* - Item description
- `subject` - *Optional* - Subjects/keywords (separated by semicolons)
- `latitude` and `longitude` - *Optional* - Geographic coordinates for maps
- `date` - *Optional* - Creation date (displays on timeline)

**Take a moment to explore:**
- Count how many different `format` types you see (Image, Sound, Text, etc.)
- Find items with `latitude` and `longitude` values—these will appear on the map!
- Notice item `psychiana001` in the first data row? We'll edit that next!
- Look at the `subject` field—see how multiple subjects are separated by semicolons?

> [!NOTE]
> CSV files can look a bit messy in text editors because commas separate the fields. That's normal! In a real project, you'd likely edit this in Google Sheets and download it as CSV. For this tutorial, we're editing in VS Code to practice file-based workflows.

**Want to learn more?** Check out the [CollectionBuilder CSV Metadata documentation](https://collectionbuilder.github.io/cb-docs/docs/metadata/csv_metadata/) to see:
- All required and optional metadata fields
- Formatting guidelines for dates, subjects, and locations
- Examples of well-structured metadata
- Tips for creating your own metadata

**When you're ready to move on, I'll be watching for your next commit!** 🤖

No need to edit anything in this step—just explore and get familiar with the structure. The next step will have you customize some metadata!

<details>
<summary>Having trouble? 🤷</summary><br/>

- The CSV file is located at `_data/psychiana.csv` in the file explorer
- Click the `▸` arrow next to `_data` to expand the folder if it's closed
- You don't need to edit or commit anything in this step—just explore!
- If the file looks confusing, that's okay—you'll get more comfortable with it as we go
- CSV files are easier to read in spreadsheet programs, but VS Code works fine for small edits

</details>

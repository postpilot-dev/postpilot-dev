# Change log

Stay updated with the latest features, improvements, and fixes for our PostPilot. Check out our changelog for version updates and enhancements!

## 1.5.2 - 2026-05-12

### Enhancements

- **Sequence Flow Kits in Web:** Added support for saving and managing Sequence Flow kits in the web version of the application.

### Fixes

- **Compare Mode Diff:** Fixed an issue in Compare Mode where the diff would incorrectly retain an "empty" state instead of showing the true difference between consecutive requests.

- **Sequence Flow Kit Saving:** Fixed a bug where newly created collections were unable to save sequence flow kits.

- **Tab List Scrolling:** Fixed an issue where the right-scroll button would incorrectly persist even when the tab list was fully scrolled to the end.

- **Kit Ordering:** Fixed an issue where the custom display order of folders and kits within a collection was not correctly loaded and restored when opening the app.


## 1.5.1 - 2026-05-03

### Features

- **Sequence Flow Kit:** A new kit type that lets you chain multiple kits into a sequence and run them in order. Each step's result is shown in a dedicated results panel, making it easy to test multi-step workflows end to end. Flow kits appear in the side menu and can be saved and re-opened across sessions.

- **Resolved Request Inspection:** You can now view the exact cURL command or SQL query that was executed, with all variables fully resolved, directly from the new Sent Request and Sent Query popovers in the response viewer.

### Enhancements

- **Multi-line MongoDB Queries:** The editor autocomplete and backend execution now fully support formatting MongoDB queries across multiple lines, making it easier to read and chain methods like `.limit()` and `.skip()`.

- **HTTP Kit Icon:** The HTTP kit no longer defaults its icon to the GET method, giving you a neutral starting point when creating a new request.

### Fixes

- **Table View Query:** Fixed an issue where table view could not load data, as a side effect of the multi-database connection feature.

- **Collection Tab Save:** Fixed an issue where saving and closing a Collection tab would mistakenly prompt to save a new kit instead of saving the collection authentication settings.


## 1.5.0 - 2026-05-02

### Features

- **MongoDB Autocomplete:** Get instant suggestions for collection names and database methods as you type in the query editor.

- **MongoDB Write Operations:** Full support for document modifications including `insertOne`, `insertMany`, `updateOne`, `updateMany`, `deleteOne`, and `deleteMany`.

- **MongoDB Method Chaining:** Support for chaining methods like `.limit()`, `.sort()`, `.skip()`, `.hint()`, and `.maxTimeMS()` directly on your queries for advanced data manipulation.

- **MongoDB Query Warnings:** A new warning system that detects redundant or inefficient query parameters, helping you optimize your MongoDB queries.

- **Destructive Operation Safety:** To prevent accidental data loss, the "Run" button dynamically turns red when a delete operation is detected in your MongoDB query.

### Enhancements

- **MongoDB Query Guide:** The interactive query guide has been updated with detailed examples for write operations, chained methods, and advanced query options.

### Fixes

- **Shortcut Interference:** Fixed a bug where the `Ctrl+Enter` shortcut would only trigger for the most recently opened tab, failing to execute in previously opened but currently active tabs.


## 1.4.8 - 2026-04-20

### Features

- **Multi-Database Support per Connection:** A single database connection can now span multiple databases on the same server. Browse and query all accessible databases without creating a separate connection entry for each one.

- **Tab Management:** A new dropdown menu on the tab bar lets you manage your open tabs. Closing tabs with unsaved changes now shows a confirmation dialog to prevent accidental data loss.

- **Ctrl+Enter Shortcut:** Press Ctrl+Enter to quickly execute HTTP requests, database queries without reaching for the mouse.

- **Auto-Detect Source Type on Paste:** Pasting content into the Data viewer automatically detects and selects the correct source type (XML, JSON, etc.).

- **Create Collection While Saving a Kit:** When saving a kit, you can now create a new collection directly from the save popup without leaving the flow.

### Enhancements

- **Copy Button in Preview:** The copy button is now embedded inside the Monaco editor preview, making it easier to copy content without reaching outside the panel. A tooltip label is also added for clarity.

### Fixes

- **HTTP Request Timeout Unsaved:** Fixed an issue where kits created before the timeout feature was added were incorrectly marked as unsaved due to a default timeout value of -1.


## 1.4.7 - 2026-04-17

### Features

- **Response Headers Tab:** Added Headers tab to The HTTP response panel.

- **Drag-to-Reorder Collections:** Drag and drop collections in the sidebar to arrange them in any order. The order is saved automatically and restored on every app restart.

- **Tab State Persistence:** Open tabs and the active tab are saved automatically and fully restored when you reopen the app or reload the workspace.

- **Request Timeout:** Set a custom timeout per HTTP request or configure a global default in Settings. Requests that exceed the limit are automatically cancelled.

### Enhancements

- **Preview Type Selector:** Choose how to view response results directly inside the result panel — switch between available preview formats without leaving the current tab.

### Fixes

- **SQL Autocomplete Dropdown Hidden:** Fixed an issue where the table and column suggestion dropdown from the SQL editor was clipped and not fully visible.

- **File Drop on Read-Only JSON Viewer:** Fixed an issue where files could be dragged and dropped onto a JSON Viewer that is not in edit mode.

- **Workspace Creation After Delete:** Fixed an issue where deleting the active workspace left the app in a broken state, making it impossible to add or create a new workspace.


## 1.4.6 - 2026-04-10

### Features

- **Table View:** Click any table or collection in the database sidebar to open a data preview. Loads 200 rows by default, with "Load More" to fetch the next page. Click a cell to inspect its full value in a side panel.

- **SQL Query Autocomplete:** The SQL editor now suggests keywords, table names, and column names as you type. Suggestions are schema-aware — tables come from your loaded schema tree, and column names are fetched on demand. Typing `alias.` resolves the alias to its table and suggests matching columns.

### Enhancements

- **Collapsible Query Panel for Raw Data Kit:** The query section in the raw data query kit is now always visible alongside the result — collapse it to a thin strip when you need more space.


## 1.4.5 - 2026-04-05

### Features

- **Font Size Scaling:** The editor, sidebar, and all panels now scale uniformly when you change the font size in Settings — no more mismatched text sizes across the UI.

### Fixes

- **Auth Type Field:** Fixed a bug where a deprecated `authType` field was incorrectly re-initialized on load, which could reset authentication settings.

- **Variable Extraction:** Fixed a race condition where running a kit with multiple extraction queries could corrupt the environment variable storage. All queries now complete first, then variables are saved in a single write.


## 1.4.4 - 2026-03-31

### Features

- **Binary Response Preview:** When an API returns binary data (`application/octet-stream`), auto-detects the content type and displays it correctly: PDF, image, or hex dump.

- **Hex Dump Viewer:** Renders binary data as offset, hex bytes, and ASCII columns — first 4 KB shown with "Load more" for larger payloads.

- **Ctrl+S to Save Collection:** Press Ctrl+S to save the current collection without reaching for the toolbar.


## 1.4.3 - 2026-03-30

### Features

- **Data Preview in JSON Source:** You can now preview JSON data directly in the source panel — switch between Raw and Preview modes using the new toggle in the toolbar. Supports table, pdf and image.

### Enhancements

- **Reorganized JSON Source Toolbar:** Toolbar controls are now grouped into logical sections — input, source type, preview, format, search and settings.

### Fixes

- **Database Connection:** URL-encoded username and password to prevent authentication errors when credentials contain special characters.


## 1.4.2 - 2026-03-28

### Features

- **Draggable Table Rows:** Reorder query parameters and headers by dragging rows up or down — no more cutting and pasting to rearrange.

- **Quick Variable Creation:** Referencing an undefined variable in your request now offers to create it on the spot, so you no longer need to open the environment editor first.

- **Postman Collection Import:** Import a Postman Collection v2.1 JSON file into PostPilot Desktop. Folder structure, requests, headers, query params, body, and auth are preserved automatically.

- **Environment Link Button:** A new link button in the environment bar lets you jump directly to the environment editor from the request view.

- **Expand Query Section on Icon Click:** Clicking the header, query, or variable icon now expands the query section automatically, saving an extra click.

### Enhancements

- **Always-Visible New Row:** An empty row is always present at the bottom of headers, query parameters, and body fields — just start typing to add a new entry without clicking an "Add" button first.

- **Smoother Tab Scrolling:** The tab bar scrolls by 30 % per click and snaps to the active tab, making it easier to navigate long tab lists.

- **Bento Layout for DB and HTTP Results:** The database client and HTTP client result panels now use the same bento-grid layout introduced in 1.4.0 for a consistent look.

### Fixes

- **Query Panel State Preserved:** Hiding and re-showing the query panel no longer resets its contents.


## 1.4.1 - 2026-03-27

### Features

- **Settings Tab:** A new Settings tab lets you configure the application to your liking. Adjust the base font size to suit your display and reading preferences.

- **Font Size Keyboard Shortcuts:** Use `Cmd +` / `Cmd -` (or `Ctrl +` / `Ctrl -` on Windows/Linux) to increase or decrease the font size without leaving the keyboard.

- **JSON Comments in Request Body:** You can now write comments (`//` and `/* */`) inside JSON request bodies. Comments are stripped automatically before the request is sent, so your JSON stays valid without cluttering the editor.

### Enhancements

- **Query Panel Always Visible:** The query section in the API client and database client is now always shown alongside the response — review query definitions and planned variable extraction before sending a request. The panel can be collapsed to a thin strip when you need more space.

- **Tab Flash on Re-click:** Clicking an already-active tab now briefly highlights it, confirming your click was registered without switching context.


## 1.4.0 - 2026-03-24

### Features

- **Refreshed Interface:** Redesigned with a bento-grid layout and sky-blue accent palette — distinct zones for header, sidebar, and content panels make the workspace easier to orient at a glance, while keeping the same information density you rely on.

### Enhancements

- **Active Environment Persisted:** The selected environment is now saved and restored automatically, so you pick up right where you left off when reopening a workspace.

- **OpenAPI Import Settings Remembered:** Folder strategy and request naming are now saved as preferences for the next time you import.

- **Query Kit Input Persisted:** The input text of a query kit is now saved and restored when you reopen it.


## 1.3.10 - 2026-03-19

### Enhancements

- **OpenAPI Import — Smarter Auth Handling:** Collection auth is set to the most-used scheme in the spec; individual requests only override when their auth differs or is explicitly public.

- **OpenAPI Import — Broader `$ref` Support:** Headers and query parameters defined as `$ref` components are now correctly resolved during import.

- **Enable/Disable Query Parameters:** Toggle individual query parameters on or off without removing them, making it easier to test different combinations.

- **Variable Preview Always Editable:** Variable previews can now be edited at any time without opening the environment editor.


## 1.3.9 - 2026-03-15

### Features

- **Variable Highlight in Request Body:** The code editor for request bodies now supports variable highlighting, autocomplete, and preview. Type `{{` to see suggestions, and click any variable to view or edit its value.

- **Multiple Request Body Types:** Choose from form-data, URL-encoded, raw (JSON, XML, Text), or binary body types. cURL import and OpenAPI import now detect and set the correct body type automatically.

- **Cancel In-Flight Requests:** Stop a running HTTP request at any time by clicking the cancel button.

- **Auth Inheritance:** Requests can now inherit authentication from the collection level.

### Enhancements

- **Improved Network Error Diagnostics:** Specific error types (Connection Refused, DNS Error, Timeout, TLS Error) when API requests fail, with runtime details and OS-level codes.


## 1.3.8 - 2026-02-17

### Features

- **Quick Save Shortcut:** Press Ctrl+S (Cmd+S on Mac) to instantly save your current tab.

- **Database Schema Persistence:** Database schemas now reload automatically when reopening a saved database client kit, so you don't have to reconnect each time.

### Enhancements

- **Refreshed UI & Accessibility:** Updated color palette with improved contrast and better keyboard navigation throughout the app.

- **Empty Query Results Display:** Table view now displays properly even when your query returns zero results, making it clear the query executed successfully.

- **Duplicate Variable Detection:** Get instant feedback when creating a variable name that already exists, preventing accidental overwrites.

### Fixes

- **Environment Variable Editing:** Fixed an issue where environment variables wouldn't update correctly after editing.

- **Example Loading:** Fixed example data not loading properly on first use.


## 1.3.7 - 2026-02-07

### Features

- **OpenAPI Import — Naming Strategy:** Choose naming for imported requests: *By Summary* (summary/operationId) or *By URI* (e.g. `/users/{id}`).

- **Tab Rename from Context Menu:** Right-click any tab to rename it.

### Enhancements

- **HTTP Method Icon in Tab:** Tabs now show the HTTP method icon (GET, POST, etc.).

- **Save Database Query Result View Type:** Your view type (Table/JSON) is saved into workspace.

### Fixes

- **Variable Value Input Height:** Fixed text area height limit for long values.


## 1.3.6 - 2026-02-04

### Features

- **Data Preview for Query Results:** Visualize query results directly as images, PDFs, or tables without leaving the inspector. Supports Base64 and byte array formats, auto-detects the preview type, and lets you toggle between raw and rendered views on the fly.


## 1.3.5 - 2026-01-30

### Enhancements

- **Enhanced JSON Path Navigation:** Click on any value in the JSON tree to automatically navigate to its path in the breadcrumb, with a copy button to quickly copy the current path.

### Fixes

- **Linux Compatibility:** Fixed compilation errors on Linux systems.


## 1.3.4 - 2026-01-27

### Features

- **Enhanced Database Query Results:** View your query results in a cleaner, more organized table with adjustable column widths to fit your data perfectly.

### Enhancements

- **Better Data Editing Experience:** Improved tables for environment variables, query parameters, and headers with easier editing and cleaner layouts that adapt to your screen size.

- **Multi-line Variable Support:** Environment variable values now support multiple lines of text for better handling of long values like API keys or JSON configurations.

- **Compare API Responses:** Previous responses are now preserved when executing new requests, allowing you to use compare mode for analyzing changes in your JSON path queries.


## 1.3.3 - 2026-01-12

### Improvements

- **Database Connection Editing:** Leaving the password field empty will preserve the existing password; enter a new value only to update it.

## 1.3.2 - 2026-01-12

### Features

- **Deleted Workspace Detection:** Automatically detects when a workspace folder has been moved or deleted, showing workspace status indicators and a warning dialog to switch to another workspace (Desktop version only).

### Improvements

- **Inline Workspace Rename:** Edit workspace names directly in the workspace switcher menu.

## 1.3.1 - 2025-12-22

### Features

- **cURL Import:** Paste cURL commands directly into the HTTP Client URL input to automatically create a request with all headers, query parameters, and authentication from the cURL command.

- **OpenAPI Spec Import:** Import OpenAPI 3.0 specification files to automatically generate HTTP request collections from your API definitions (Desktop version only).

- **Custom HTTP Methods:** Added support for custom HTTP methods beyond the standard GET, POST, PUT, DELETE, allowing you to use any HTTP method your API requires.

## 1.3.0 - 2025-11-21

### Added

- **Variable Highlighting:** Variables using `{{variableName}}` syntax are now color-coded inline—blue for valid variables, red for invalid ones.

- **Variable Autocomplete:** Type `{{` to see instant suggestions of available environment variables. Navigate with arrow keys and insert with Enter or Tab.

- **Variable Preview & Edit:** Click any highlighted variable to quickly view or edit its value directly in a popup.

## 1.2.9 - 2025-11-01

### Added

- **File-Based Environment Storage:** Environment variables are now stored as files in your workspace, ensuring persistence across sessions and better integration with file-based workspaces.

- **Real-Time Search:** Search functionality now provides instant results with a limit of 200 items for better performance.

- **Navigate to Path in Search Result:** Added a "Go to" button in search results to quickly jump to the matching location in the raw JSON view.

### Enhancements

- **Resizable Sidebar:** The sidebar menu can now be resized by dragging the separator, allowing you to customize the workspace layout to your preference.

### Fixes

- **Search UI:** Fixed layout shift (CLS) issues when hiding the search bar.

## 1.2.8 - 2025-10-26

### Added

- **File-Based Workspaces:** Your workspaces are now saved as files on your computer, making it easy to backup, share, and manage your work across different locations.

- **Persistent Database Connections:** Save your database connections with secure password storage in your system keychain. Each workspace maintains its own set of connections.

- **Nested Folders:** Organize your kits with multi-level folders and drag-and-drop support for better project organization.

- **Enhanced Data Type Support:** View UUID and TIMESTAMPZ data types in database query results.

### Enhancements

- **Improved Database & HTTP Clients:** Better layout and navigation for query results, with cleaner interface and easier switching between table, JSON, and cell views.

- **Faster Workspace Loading:** Collections now load instantly with details fetched only when needed, significantly improving startup performance.

### Fixes

- **UI Layout:** Resolved overflow issues in the code editor and request/response panels.

## 1.2.6 - 2025-08-22

### Added

- **Query Tags & Filtering:** Introduced query tagging system with filter functionality to organize and search queries by tags.

- **Desktop Application:** Added new desktop application with enhanced performance and native OS integration.

- **License Management:** Implemented trial license support and license key validation system for the desktop application.

- **Kit Duplication:** Added ability to duplicate kits for easier workflow management.

- **Drag and Drop Support:** Implemented drag and drop functionality for kit organization within collections and folders.

### Enhancements

- **Lightweight JSON Viewer:** Improved JSON viewer with configurable indentation, better organization of brackets and toggle buttons, and enhanced performance for small query results.

- **Workspace Experience:** Enhanced tab management with temporary tab preview, smooth transition effects, and improved workspace navigation.

## 1.2.5 - 2025-07-25

### Fixed

- **Environment Variables Tab:** Corrected the display of environment variables in the tab and ensured proper synchronization with changes from variable extraction.

## 1.2.4 - 2025-07-23

### Added

- **Add Collection:** Added the ability to create new collections.

### Enhancements

- **Collection Improvement:** Enhanced the experience for adding and renaming items, added a tree line to reflect the tree layout.

- **Tab Title:** Improved the user experience for renaming tab titles.

## 1.2.3 - 2025-07-14

### Added

- **Settings:** Added settings configuration for data and query components.

### Enhancements

- **Tab Bar:** Improved tab title sizing and scroll experience.

- **Tooltips:** Added tooltips for buttons to improve user experience.

## 1.2.2 - 2025-06-17

### Features

- **Environment Variables**: Introduced a sub-menu for managing environments and a dedicated tab for editing variables.

- **Extract to Variable**: Added a button to extract query results into a variable.

- **Variable Substitution**: Automatically replaces `{{variable}}` placeholders with environment variable values in API requests and database queries.

## 1.2.1 - 2025-06-08

### Features

- **Database Query Result Table Viewer:** Introduced a table view for displaying query results.

- **Database Query Result JSON Viewer:** Added a JSON viewer to display results in JSON format, with support for sub-queries using JSONPath.

## 1.2.0 - 2025-05-18

### Features

- **Database Connection Management:** Introduced a sub-menu for managing database connections.

- **Database Query Client:** Added a dedicated tab for executing database queries.

## 1.1.1 - 2025-03-23

### Features

- **Save API Request:** Added support for saving and reopening API requests.

- **Save As:** Enabled cloning of the current query kit/API client kit.

### Enhancements

- **Tab Scrolling:** Enabled vertical scrolling of the tabs list without requiring the Shift key.

- **Resizable Request-Response Zone:** Allowed dynamic resizing of the request-response area.

- **Query Result Height:** Adjusted the query result height to fit the content.

## 1.1.0 - 2025-03-02

### Features

- **API Client:** Introduced a tab to send HTTP requests directly.

- **Compare mode:** Added a mode to compare old and new query results.

### Enhancements

- **JSON All-in-One Mode:** Added an all-in-one mode for the JSON viewer, allowing users to view, edit, and extract JSON paths within a single editor.

- **Tabs List Scroll:** Enabled horizontal scrolling for the tabs list to improve navigation.

## 1.0.3 - 2024-12-29

### Features

- **Dark mode**: Introduced dark mode to improve usability in low-light environments.

## 1.0.2 - 2024-12-12

### Features

- **Complex query:** Add support for JSONPath syntax, including wildcard queries.

- **Drag-and-Drop Queries**

- **Drop file:** Added the ability to drop a file into the JSON zone to load it.

- **Load file:** Added file loading functionality.

### Enhancements

- **XML plural keys:** Improved detection of plural keys for better mapping to arrays.

## 1.0.1 - 2024-11-25

### Features

- **Converters:** Added a Base64 decoder and an XML converter.

- **Search by case:** Added a button to toggle between case-sensitive and case-insensitive search.

### Enhancements

- **Tab Context Menu:** Added the ability to close multiple tabs via the context menu.

- **Move Tabs:** Added the ability to rearrange tabs by dragging them.

- **Folder Context Menu:** Added options to rename and delete folders.

- **Search Value Compacting:** Long search values are now truncated with a "Load more" option for expanded viewing.

- **Copy Feedback:** Added a visual effect when copying JSON keys, search results, or query results.

### Fixes

- **Light mode:** Enforce light mode since we do not yet support dark mode.

- **Workspace Typo:** Oh well, we launched the first version with it. Or… not entirely. Let’s just say "workpsace" has its quirks.

## 1.0.0 - 2024-11-16

### Features
- **Parse JSON Structure:** Includes syntax highlighting and basic validation.

- **View JSON in Tree Mode:** Provides a clear, hierarchical view of JSON structures.

- **Extract JSON Path:** In Tree mode, you can click on any key to copy its JSON path.

- **Multiple Queries:** Query multiple JSON paths simultaneously — no need to search one by one.

- **Search:** Search JSON data by key or value, with results displayed as key-value pairs.

- **Workspace:** Supports multiple working tabs. Manage query sets in the workspace so they can be saved and reopened as needed, using the browser's local storage.

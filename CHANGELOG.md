# Change log

Stay updated with the latest features, improvements, and fixes for our PostPilot. Check out our changelog for version updates and enhancements!

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

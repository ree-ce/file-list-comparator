# File List Comparator

A web-based tool for comparing two lists of file paths and finding differences based on common prefixes. This tool is particularly useful when comparing file paths from different directories that share common segments.

## Features

- **Auto Prefix Detection**: Automatically detects common segments in file paths
- **Manual Prefix Input**: Allows manual entry of prefix for custom comparisons
- **Real-time Updates**: Results update automatically as you type
- **Clear Visual Feedback**: Shows differences between lists with clear formatting
- **Toggle Mode**: Switch between automatic and manual prefix detection

## Usage

### Basic Operation

1. **Input Lists**:
   - Paste your first list of file paths in the top text area
   - Paste your second list of file paths in the bottom text area

2. **Prefix Detection Mode**:
   - **Auto Detection** (default): The tool automatically finds common segments in paths
   - **Manual Input**: Uncheck "Use auto common part detection" to manually specify a prefix

3. **View Results**:
   - Files unique to List 1 appear in the first output section
   - Files unique to List 2 appear in the second output section

### Example

Input List 1:
```
/share/firmwares/RaspberryVanillaAOSP13/2.img/system/product/app/Calendar/Calendar.apk
/share/firmwares/RaspberryVanillaAOSP13/2.img/system/product/app/DeskClock/DeskClock.apk
```

Input List 2:
```
/extracted/2.img/system/priv-app/BugReportApp/BugReportApp.apk
/extracted/2.img/system/priv-app/SettingsApp/SettingsApp.apk
```

In this example:
- Auto detection will find "2.img" as the common prefix
- Comparison will be based on paths after "2.img/"
- Differences will show the full paths that don't match after the common prefix

## Notes

1. **Auto Detection**:
   - Looks for common segments in all paths
   - Helps identify structural similarities in different directory trees
   - Shows "No common prefix detected" if no common segments are found

2. **Manual Mode**:
   - Enter exact prefix text
   - Results will be empty if prefix isn't found in both lists
   - Useful when you know the specific segment to compare against

3. **Results**:
   - Empty results indicate either no differences or no valid prefix
   - Full paths are shown in the output for easy reference
   - Updates happen in real-time as you modify input

## Technical Details

The comparison works by:
1. Finding a common prefix (either automatically or manually specified)
2. Removing the prefix and one path separator from all paths
3. Comparing the remaining path segments
4. Displaying paths that don't have matching counterparts in the other list

## Error Messages

- "No common prefix detected - please check your input": Appears when auto-detection can't find common segments
- "Please enter a prefix to compare": Shows in manual mode when no prefix is entered
- "Prefix not found in files - please check your input": Appears when manual prefix isn't found in both lists

## Limitations

- Case-sensitive comparison
- Requires exact prefix matches
- Paths must use forward slashes (/) or backslashes (\) as separators

Would you like me to expand any section of the README or add more examples?
